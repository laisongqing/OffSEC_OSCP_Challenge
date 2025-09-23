## nmap scanning
- <img width="1920" height="478" alt="image" src="https://github.com/user-attachments/assets/8cf1a3a4-61fb-4f1c-ace4-78b92881fe95" />

## 80 port
- dirsearch 掃不出重要的子目錄
  - 

## 22 port
- 在 .10 發現 C:\Users\Administrator\Desktop 底下有個 credentials.txt
  - <img width="970" height="343" alt="image" src="https://github.com/user-attachments/assets/458c63a9-4f2f-48c2-9db8-2767289f819e" />
- credentials.txt 有帳號密碼
  - <img width="822" height="121" alt="image" src="https://github.com/user-attachments/assets/743d38a3-b293-427a-b041-937222deca75" />
- 用此帳號密碼成功登入
  - <img width="1318" height="472" alt="image" src="https://github.com/user-attachments/assets/55594cfb-054d-4877-aafc-dcbf8f440391" />

## 提權
- sudo -l 發現可以無密碼 sudo 接所有指令
  - <img width="1812" height="179" alt="image" src="https://github.com/user-attachments/assets/7ea08468-ca55-4291-9ccc-6c786b5abb64" />
- sudo su 成功提權，並取得 proof.txt
  - <img width="763" height="104" alt="image" src="https://github.com/user-attachments/assets/a85d9544-b26a-4124-9650-78da9867bb8a" />








































