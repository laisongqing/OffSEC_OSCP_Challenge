## nmap scanning
- tcp
  - <img width="1918" height="755" alt="image" src="https://github.com/user-attachments/assets/2d644f53-9a4e-47eb-b143-829a7fb1c091" />
  - <img width="1918" height="697" alt="image" src="https://github.com/user-attachments/assets/a0843bb9-67ba-4218-b23a-0d3dca6f1aba" />
  - <img width="1918" height="717" alt="image" src="https://github.com/user-attachments/assets/fd0f20a5-add4-4ebd-ad39-22bd9bd3785a" />
  - <img width="1918" height="737" alt="image" src="https://github.com/user-attachments/assets/eb4e8480-816a-4562-b7d1-a0bcbe733cef" />
- udp
  - <img width="1175" height="435" alt="image" src="https://github.com/user-attachments/assets/07a84977-c5ff-43b3-ac84-683388f7ebb6" />

## 161 port
- snmpbrute.py 找到 community string 是 public
  - <img width="1918" height="725" alt="image" src="https://github.com/user-attachments/assets/2b28bfa8-8cc1-491a-8300-c074f7dc21b8" />
- snmpwalk 找到有帳號密碼
  ```
  snmpwalk -c public -v2c 192.168.169.156 NET-SNMP-EXTEND-MIB::nsExtendObjects
  ```
  - <img width="1918" height="710" alt="image" src="https://github.com/user-attachments/assets/d4798571-b943-4b59-b566-6c36134260f6" />

## 8083 port
- 是 vesta 的登入頁面
  - <img width="1918" height="785" alt="image" src="https://github.com/user-attachments/assets/ee50c03b-4c86-4e14-a367-b9ad92f48ac4" />
- 成功登入
  ```
  jack:3PUKsX98BMupBiCf
  ```
  - <img width="1918" height="817" alt="image" src="https://github.com/user-attachments/assets/1bb08e6b-88f4-4566-a11e-49af70c5a528" />
- VestaCP RCE Exploit 成功取得 shell
  - https://github.com/CSpanias/vesta-rce-exploit
  - <img width="1918" height="472" alt="image" src="https://github.com/user-attachments/assets/561fed3f-4ee0-48a3-8206-963c2fca10f8" />
- 取得 local.txt
  - <img width="463" height="52" alt="image" src="https://github.com/user-attachments/assets/4eb669c2-9ac6-41b6-8136-c8295a547868" />
- 取得 proof.txt
  - <img width="572" height="75" alt="image" src="https://github.com/user-attachments/assets/4c065dd3-91ec-4ee7-8613-c747ad5ee687" />

















































