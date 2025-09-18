## namp scanning
- <img width="1920" height="778" alt="image" src="https://github.com/user-attachments/assets/a98f9ecc-f55d-47c8-bd54-43d376e476b9" />

## 80 port
- dirsearch 發現有個登入頁面
  - /login.aspx
  - <img width="1920" height="828" alt="image" src="https://github.com/user-attachments/assets/8c30b9b3-0318-4160-b59a-8564a654cfbf" />
- burp suite 攔截登入資訊，並存成 test
  - <img width="1599" height="844" alt="image" src="https://github.com/user-attachments/assets/975e6cdd-0079-4590-80cb-e48e7f70289f" />
- sqlmap 成功爆破取得 os-shell
  ```
  sqlmap -r test --dbms=mssql --os-shell
  ```
  - <img width="1920" height="833" alt="image" src="https://github.com/user-attachments/assets/e5062188-1635-45dc-ad08-4f9e54bd66f9" />
- 利用 os-shell 上傳 nc.exe 並取得 reverse shell
  - <img width="1920" height="830" alt="image" src="https://github.com/user-attachments/assets/624e72fe-de63-4aac-90b1-66355a10206e" />
  - <img width="1920" height="837" alt="image" src="https://github.com/user-attachments/assets/624233db-7d42-423c-88d5-ef3f4d7591a9" />

## 提權
- whoami /priv 發現可以利用 SeImpersonatePrivilege 提權
  - <img width="1213" height="381" alt="image" src="https://github.com/user-attachments/assets/37ef8d94-aa5c-4214-9f33-0a17c363afb8" />
- 成功提權成 system
  - <img width="1122" height="299" alt="image" src="https://github.com/user-attachments/assets/7453880d-fd56-47f3-b212-1d4964445266" />
- 取得 proof.txt  
  - <img width="906" height="107" alt="image" src="https://github.com/user-attachments/assets/918554c0-240c-4fb8-9566-405e255a877f" />
















































