## 因為是內網，所以用 frp 架 socket

## nmap scanning
- <img width="1503" height="316" alt="image" src="https://github.com/user-attachments/assets/b855b6f7-cc74-48bb-8637-5b2a522ec753" />

## 445 port
- smbclient 沒辦法匿名登入
  - <img width="1290" height="203" alt="image" src="https://github.com/user-attachments/assets/68ad835b-0ad6-4c4d-959a-cd8eb5ff229c" />

## 5985 port
- 在 .121 發現 joe 和 joe 的密碼
  - <img width="1920" height="253" alt="image" src="https://github.com/user-attachments/assets/95a4e6f7-f537-4bac-9af2-5725f3e444db" />
 - 成功用 evil-winrm 登入 joe
   - <img width="1920" height="469" alt="image" src="https://github.com/user-attachments/assets/25166c40-7824-4e9e-a868-be3cdb81f1cc" />
- 取得 local.txt
  - <img width="1266" height="346" alt="image" src="https://github.com/user-attachments/assets/3ee0de3f-14cb-466c-8909-4c7a9cdaa34d" />

## 提權
- msfconsole
  - <img width="1920" height="694" alt="image" src="https://github.com/user-attachments/assets/e4ce3f56-6856-433d-bd9f-e841e530a0aa" />
- 取得 proof.txt
  - <img width="1058" height="102" alt="image" src="https://github.com/user-attachments/assets/4aadd6a2-ee40-4960-9ab2-2ce246a1d6e0" />
















































