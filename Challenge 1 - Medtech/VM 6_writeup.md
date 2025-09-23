## 因為是內網，所以用 frp 架 socket
## nmap scanning
- <img width="1920" height="764" alt="image" src="https://github.com/user-attachments/assets/30b8cdd1-dd1c-449a-8d6e-274ffbacf2a9" />

## 445 port
- - 用前幾台靶機發現到的 user 和密碼去炸
  - <img width="963" height="571" alt="image" src="https://github.com/user-attachments/assets/4bdd8599-f60e-4b5e-821d-688d35c81d4c" />
  - <img width="960" height="535" alt="image" src="https://github.com/user-attachments/assets/38120a5d-8871-4ac9-9e0e-7a9c7d27dc78" />
- 發現 wario、joe 和 yoshi 可以登入 smb
  - <img width="1920" height="336" alt="image" src="https://github.com/user-attachments/assets/10893880-52b4-4bed-abec-930d5aee9095" />
  - <img width="1920" height="389" alt="image" src="https://github.com/user-attachments/assets/a5f13869-b362-46b4-8f4e-c975168d13b0" />
  - <img width="1920" height="367" alt="image" src="https://github.com/user-attachments/assets/474ad3a4-782d-4ace-82a8-7041d9018d14" />
  - <img width="1920" height="455" alt="image" src="https://github.com/user-attachments/assets/1792ab4e-6a69-47d0-ad18-d0dc72366552" />
  - <img width="1920" height="470" alt="image" src="https://github.com/user-attachments/assets/d21c8c1a-9a94-4e26-aaa7-9924bb8366d2" />
  - <img width="1920" height="465" alt="image" src="https://github.com/user-attachments/assets/93211eef-099e-48e9-9165-6d6df2f90cd0" />
- 但 smb 裡沒什麼重要的資訊

## 5985 port
- crackmapexec 炸 evil-winrm 登入，結果都沒辦法登入
  - <img width="1920" height="773" alt="image" src="https://github.com/user-attachments/assets/75046933-60d6-44f1-9837-3e0594e3b2d8" />

## 3389 port
- 嘗試登入 joe、wario、yoshi，結果只有 yoshi 成功 RDP 登入
  - <img width="1916" height="672" alt="image" src="https://github.com/user-attachments/assets/33939475-c672-455c-b7b4-ad4700f384c9" />
  - <img width="1920" height="671" alt="image" src="https://github.com/user-attachments/assets/9f8e2856-e559-4f34-9d07-26cb60463154" />
  - <img width="1920" height="747" alt="image" src="https://github.com/user-attachments/assets/f9298c00-3277-443b-b0b3-d5017e2cc1c8" />
- 取得 local.txt
  - <img width="1920" height="870" alt="image" src="https://github.com/user-attachments/assets/ef647ea6-ed83-4799-b66f-bdec78c1e2df" />

## 提權
- msfconsole
  - <img width="1749" height="690" alt="image" src="https://github.com/user-attachments/assets/3a9b234c-1413-4729-b02a-4a80020d24a2" />
- 取得 proof.txt
  - <img width="819" height="107" alt="image" src="https://github.com/user-attachments/assets/54f367dd-5334-4990-acaa-0b32c6a17266" />








































