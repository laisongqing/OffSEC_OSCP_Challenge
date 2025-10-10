## nmap scanning
- <img width="1918" height="690" alt="image" src="https://github.com/user-attachments/assets/37fc5a51-cf0b-45cc-9a52-ac8123c0e45f" />

## 21 port
- ftp 可以匿名登入，發現 backup 有 5 個 pdf
  - <img width="1347" height="627" alt="image" src="https://github.com/user-attachments/assets/7c5dbdb5-62ad-4487-b17e-0171bfc4956c" />
- 用 exiftool 查看檔案詳細資訊，發現有 Cassie、Mark、Robert 這 3 個 Author
  - <img width="1212" height="572" alt="image" src="https://github.com/user-attachments/assets/7c75b574-1607-453a-bcf0-85b0e765ff3f" />
  - <img width="1332" height="575" alt="image" src="https://github.com/user-attachments/assets/50342e82-0ed0-4833-b77a-d3a6d5be334f" />
  - <img width="1323" height="573" alt="image" src="https://github.com/user-attachments/assets/21aec283-796a-45e0-a95c-38b3125194dd" />
## 20000 port
- Usermin
  - <img width="1918" height="837" alt="image" src="https://github.com/user-attachments/assets/11aa674d-f0c6-49d2-88dc-df543221f780" />
- 用 

- 用 cassie:cassie 成功登入
  - 
- Usermin 存在 Usermin 1.820 - Remote Code Execution (RCE) (Authenticated)
  - https://www.exploit-db.com/exploits/50234
  - https://github.com/tunahantekeoglu/userminrce
- 成功取得 shell
  - <img width="1918" height="572" alt="image" src="https://github.com/user-attachments/assets/f8e64022-dc46-4e3f-a5c4-91a63ea70e17" />
  - <img width="1270" height="232" alt="image" src="https://github.com/user-attachments/assets/038263e7-a517-49dd-9818-f488ce359f66" />
- 取得 local.txt
  - <img width="712" height="77" alt="image" src="https://github.com/user-attachments/assets/484d6ef3-c57d-4eca-8273-87770dc54a7d" />

## 提權
- msfconsole
  - <img width="1790" height="533" alt="image" src="https://github.com/user-attachments/assets/2c1d11cc-6353-4e62-8e1e-62e4471527fe" />
- 取得 proof.txt
  - <img width="588" height="77" alt="image" src="https://github.com/user-attachments/assets/935c27f3-6129-455f-af34-c1d7a911b45e" />






































