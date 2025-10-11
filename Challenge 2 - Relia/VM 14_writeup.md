## nmap scanning
```
nmap -sC -sV -sS -Pn -p- -T4 192.168.126.249 --min-rate 1000
```
- <img width="1920" height="791" alt="image" src="https://github.com/user-attachments/assets/0cf6447a-19a7-44aa-ad9e-e2c297e952c3" />
- <img width="1920" height="750" alt="image" src="https://github.com/user-attachments/assets/b6a07fbf-8102-4346-af0b-3165b56b2c9e" />

## 80 port
- 是 IIS 10.0
  - <img width="1920" height="835" alt="image" src="https://github.com/user-attachments/assets/4bfd94b4-e334-4e97-a1ed-af20b854140e" />
- dirsearch 掃子目錄
  ```
  dirsearch -u http://192.168.126.249/
  ```
  - <img width="1920" height="798" alt="image" src="https://github.com/user-attachments/assets/4aef7c26-a685-4c8b-bc78-5335f0286acf" />
  - <img width="1920" height="782" alt="image" src="https://github.com/user-attachments/assets/0103fec1-25b6-402d-a432-2605096ddcdc" />
- 發現沒什麼重要的東西

## 8000 port
- 在網站發現 Apache Friends、XAMPP 7.4.30、RiteCMS 3.0
  - <img width="1920" height="853" alt="image" src="https://github.com/user-attachments/assets/1ec33fe6-ce36-4386-8d50-bfc76d49e66c" />
- feroxbuster 掃子目錄發現爆太快不行， /cms 底下很可疑，所以在用 dirsearch 爆 /cms/ 底下的目錄
  - <img width="1920" height="794" alt="image" src="https://github.com/user-attachments/assets/60efa080-6549-4692-8928-8fa9dc03e30f" />
- dirsearch 爆 /cms
  - <img width="1920" height="793" alt="image" src="https://github.com/user-attachments/assets/dbab905b-023a-43bb-9f34-99c321aca0a4" />
  - <img width="1920" height="800" alt="image" src="https://github.com/user-attachments/assets/236cb590-0fa6-499e-8e52-54ed571946a3" />
  - <img width="1920" height="453" alt="image" src="https://github.com/user-attachments/assets/851e748b-9ccc-4eac-9019-6c71728837d2" />
- 發現 /cms/admin.php 是個登入頁面
  - <img width="1920" height="858" alt="image" src="https://github.com/user-attachments/assets/703283ef-dc0d-4a2d-ad95-91758ea3b92f" />
- admin:admin 成功登入
  - <img width="1920" height="883" alt="image" src="https://github.com/user-attachments/assets/2df72fe0-d028-471e-ae27-4fced78d74d6" />
- ExploitDB 發現 RiteCMS v3 存在 RiteCMS 3.1.0 - Remote Code Execution (RCE) (Authenticated)
  - https://www.exploit-db.com/exploits/50616
  - <img width="1920" height="848" alt="image" src="https://github.com/user-attachments/assets/429ea46f-1808-4665-8432-eea8a1db608d" />
- 漏洞原理說明：
  - 先在 Files Manager 選擇 Media 將 shell.pHp 上傳
    - <img width="1920" height="860" alt="image" src="https://github.com/user-attachments/assets/6b1ae268-af18-4703-809b-0aec3c950a5e" />
  - 再到 /cms/media/ 點選剛剛上傳的 shell.pHp
    - <img width="1920" height="745" alt="image" src="https://github.com/user-attachments/assets/3d75097d-25d5-45b5-8bc3-8c233d6fd66a" />
  - 成功取得 reverse shell
    - <img width="1920" height="853" alt="image" src="https://github.com/user-attachments/assets/5cbd3435-0faf-439b-a175-aab587a36eba" />
  - 取得 local.txt
    - <img width="753" height="87" alt="image" src="https://github.com/user-attachments/assets/815c7615-8326-46ad-af34-b6b3c3311599" />

## 提權
- metasploit
  - 先拿到 meterpreter 後，在 meterpreter 下指令掃有哪些可以提權的 exploit
    ```
    run post/multi/recon/local_exploit_suggester
    ```
    - <img width="1918" height="532" alt="image" src="https://github.com/user-attachments/assets/16c53ab3-7942-4618-8c8f-cf4319406902" />
  - 發現以下 exploit 可以拿來提權
    ```
    exploit/windows/local/cve_2024_30088_authz_basep
    ```
    - <img width="1919" height="768" alt="image" src="https://github.com/user-attachments/assets/8c3a8b35-1cbc-4bc7-9e97-57f2f7f12009" />
- 取得 proof.txt
  - <img width="909" height="109" alt="image" src="https://github.com/user-attachments/assets/71fb2727-56fb-4f0a-95c1-18542628c83e" />

## git
- 在 C:\staging 底下發現有 .git
  - <img width="898" height="365" alt="image" src="https://github.com/user-attachments/assets/677e2346-0389-455b-8465-dd19290c6b00" />
- 輸入 git show 將資料 git 出來
  - <img width="1918" height="507" alt="image" src="https://github.com/user-attachments/assets/fa3a942a-bceb-4117-addc-b3a992a20bf5" />
- 發現 maildmz:DPuBT9tGCBrTbR
  - <img width="1918" height="537" alt="image" src="https://github.com/user-attachments/assets/2aed556f-bb8a-4dc2-8371-15cb8d1e5031" />
















































