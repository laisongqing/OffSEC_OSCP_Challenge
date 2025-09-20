## nmap scanning
- <img width="1918" height="662" alt="image" src="https://github.com/user-attachments/assets/a3dc9ff7-d787-4a67-82ce-8b5856271c41" />

## 445 port 
- smbclient 沒辦法匿名登入
  - <img width="942" height="160" alt="image" src="https://github.com/user-attachments/assets/ea94b21a-179a-4ab2-9650-daa1487a9a25" />

## .95
- 用 mimikatz dump 出使用者 ntlm
  ```
  privilege::debug
  sekurlsa::logonpasswords
  ```
- 發現 Administrator 的 ntlm 和 apache 的 password
  - <img width="1918" height="750" alt="image" src="https://github.com/user-attachments/assets/d7665a1d-1f80-4ba1-b29c-f802a73999f9" />

## 5985
- 嘗試用 evil-winrm 登入 apache，結果成功了
  - <img width="1918" height="377" alt="image" src="https://github.com/user-attachments/assets/a99515fd-55fd-4d80-829a-3da0e594e724" />

## 提權
- metasploit 成功提權成 system
  - <img width="1918" height="695" alt="image" src="https://github.com/user-attachments/assets/a12207b6-3eca-4e66-99e5-fb2d4fb9e8f2" />
- 取得 local.txt
  - <img width="985" height="107" alt="image" src="https://github.com/user-attachments/assets/b34a021c-0eda-4bbb-9b72-294c9146de01" />
- 取得 proof.txt
  - <img width="1033" height="112" alt="image" src="https://github.com/user-attachments/assets/026d1544-ae8d-4c13-a7a3-3f5065b11fed" />



















































