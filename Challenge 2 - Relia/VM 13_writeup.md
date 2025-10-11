## nmap scanning
- <img width="1918" height="726" alt="image" src="https://github.com/user-attachments/assets/8a38dd12-4074-42a6-92be-5e3bb592542d" />
- <img width="1920" height="716" alt="image" src="https://github.com/user-attachments/assets/0c34e48e-bd80-47e5-b53e-6e0c575b5bc0" />

## 80 port 
- DNN
  - <img width="1919" height="857" alt="image" src="https://github.com/user-attachments/assets/cdb5a6db-7566-4d41-b5ec-3108ead16c34" />

## 445 port
- smbclient 允許匿名登入
  - <img width="1459" height="345" alt="image" src="https://github.com/user-attachments/assets/3021991c-cd5c-4d15-85fa-a3afa8c42ccd" />
- 在 transfer 裡面發現 Emma 應該是 user
  - <img width="1179" height="468" alt="image" src="https://github.com/user-attachments/assets/69a417b3-d7af-4dc0-8f8d-9b0760ef30be" />
  - <img width="1076" height="192" alt="image" src="https://github.com/user-attachments/assets/da1256e5-0a1e-47b8-aed3-842bfa4a58a0" />
- 在 transfer 裡面發現 Database.kdbx
  - <img width="1920" height="289" alt="image" src="https://github.com/user-attachments/assets/d65ea4ef-4c41-4dba-b3ac-7e18748b8bc9" />

## kdb
- 用 keepass2john 將 Database.kdbx 轉成 Database.kdbx.hash
  - <img width="1045" height="88" alt="image" src="https://github.com/user-attachments/assets/89024f44-149f-480c-ae63-13f0c0bdc86b" />
- 用 john 解 Database.kdbx.hash
  - <img width="1426" height="337" alt="image" src="https://github.com/user-attachments/assets/3616c898-5272-4da1-a988-6ea03e45084d" />
- 用 kpcli 輸入密碼查看資料庫
  - <img width="1084" height="240" alt="image" src="https://github.com/user-attachments/assets/8d26bddc-60e8-4b52-a0d7-15e72a6c30dc" />
- 發現 Emma 的密碼
  - <img width="1920" height="800" alt="image" src="https://github.com/user-attachments/assets/9077562f-6081-4018-aeaf-31080c3d5f44" />

## 3389
- xfreerdp3 成功登入 Emma
  ```
  xfreerdp3 /v:192.168.224.248 /u:emma /p:SomersetVinyl1!
  ```
  - <img width="1920" height="854" alt="image" src="https://github.com/user-attachments/assets/73a5c774-53e3-41f1-831d-e0df50e2a4e2" />
- 取得 local.txt
  - <img width="1060" height="805" alt="image" src="https://github.com/user-attachments/assets/349924e3-5fbb-4c40-a5c6-bed70bd325fe" />

## 提權
- CVE-2023-28252 
  - https://github.com/duck-sec/CVE-2023-28252-Compiled-exe
  - 成功提權
    - <img width="1918" height="832" alt="image" src="https://github.com/user-attachments/assets/13d70742-5781-4d0a-9d23-5763ed7542e5" />
- 取得 proof.txt
  - <img width="804" height="100" alt="image" src="https://github.com/user-attachments/assets/932532d5-8633-4a59-ba0d-21b33d2a3b19" />
















































