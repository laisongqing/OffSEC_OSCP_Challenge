## nmap scanning
- <img width="1918" height="740" alt="image" src="https://github.com/user-attachments/assets/6904d338-db49-48cf-8fc6-49503534f244" />

## 80、81、443 port
- 沒什麼資訊

## 3003 port
- 發現可以 nc 反連到靶機，並發現 version 是 Aerospike Community Edition build 5.1.0.1
  - <img width="732" height="137" alt="image" src="https://github.com/user-attachments/assets/c99d93bd-18b8-4b64-9979-6ab3fdedcf9d" />
- Aerospike Community Edition build 5.1.0.1 存在漏洞
  - https://www.exploit-db.com/exploits/49067
  - <img width="1918" height="857" alt="image" src="https://github.com/user-attachments/assets/9ea104cc-ad77-4986-955b-c779a3ed7cec" />
- 用 github 上的 poc 成功取得 shell
  - https://github.com/b4ny4n/CVE-2020-13151
  - <img width="1918" height="287" alt="image" src="https://github.com/user-attachments/assets/a3d59489-e42a-4e17-b2ef-80d71cfef7dc" />
  - <img width="1918" height="187" alt="image" src="https://github.com/user-attachments/assets/61f77980-719d-4d0b-94a9-95c4a29262c2" />
- 取得 local.txt
  - <img width="703" height="72" alt="image" src="https://github.com/user-attachments/assets/f5d155b5-a445-485c-9b13-de1579ceaaf2" />

## 提權
- pspy64 發現 /opt/aerospike/bin/asadm 是用 root 去執行的
  - <img width="1918" height="757" alt="image" src="https://github.com/user-attachments/assets/145a3dd0-4263-4d62-8c06-ed7cbcdd46e8" />
- /opt/aerospike/bin/asadm 可以修改程式碼
  - <img width="1037" height="82" alt="image" src="https://github.com/user-attachments/assets/2f56b220-856a-4537-9664-9f9cac9d1118" />
- 寫 reverse shell 到 /opt/aerospike/bin/asadm
  - <img width="1918" height="78" alt="image" src="https://github.com/user-attachments/assets/e628c06e-deea-467b-bada-9689715f1e1e" />
- 成功提權成 root
  - <img width="1918" height="182" alt="image" src="https://github.com/user-attachments/assets/97c30bd8-0939-41e5-b86f-bdafbde214b2" />
- 取得 proof.txt
  - <img width="587" height="87" alt="image" src="https://github.com/user-attachments/assets/ba3034e0-ca08-4fc3-aa35-4d4cef44ae83" />












































