## 因為是內網，所以用 frp 架 socket
## nmap scanning
- <img width="1920" height="784" alt="image" src="https://github.com/user-attachments/assets/d9c6477d-eb3e-4f18-8bb1-467f6b2a957a" />

## 445 port
- 用前幾台靶機發現到的 user 和密碼去炸
  - <img width="963" height="571" alt="image" src="https://github.com/user-attachments/assets/4bdd8599-f60e-4b5e-821d-688d35c81d4c" />
  - <img width="960" height="535" alt="image" src="https://github.com/user-attachments/assets/38120a5d-8871-4ac9-9e0e-7a9c7d27dc78" />
- 使用 crackmapexec 炸 smb 登入，成功發現 yoshi:Mushroom! 可以登入 smb，並且此帳號可以登入 3389 port
  - <img width="1919" height="393" alt="image" src="https://github.com/user-attachments/assets/32a2d558-a0a2-4f84-ace6-930aaec10650" />

## 3389 port
- 成功登入 RDP
  - <img width="1920" height="712" alt="image" src="https://github.com/user-attachments/assets/85d5ceee-7173-4419-999d-c064c5021e8b" />

## 提權
- msfconsole
  - <img width="1920" height="693" alt="image" src="https://github.com/user-attachments/assets/bac3ab7b-ca91-437d-8c7a-b319496839cc" />
- 取得 proof.txt
  - <img width="1062" height="113" alt="image" src="https://github.com/user-attachments/assets/18ddd809-5c95-4d4c-adb0-217924c1e38c" />








































































