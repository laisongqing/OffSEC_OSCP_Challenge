## nmap scanning
- <img width="1920" height="678" alt="image" src="https://github.com/user-attachments/assets/1df7d6fb-4dd9-44e5-b2d3-38b619c4ece9" />

## 80 port
- dirsearch 發現存在 /.git/
  - <img width="1920" height="793" alt="image" src="https://github.com/user-attachments/assets/2ebf2e0b-a1e2-4f8a-80fe-179216c74560" />
- 用 gitdumper.py 挖 http://192.168.224.144/.git/ 裡面的資料
  - <img width="1920" height="787" alt="image" src="https://github.com/user-attachments/assets/8fa64231-22f5-4930-ae2a-42be248ea037" />
- 在 /.git/configuration 發現 database.php，但無法將明文憑證新增至公共儲存庫！(Cleartext creds cannot be added to public repos!)
  - <img width="1920" height="560" alt="image" src="https://github.com/user-attachments/assets/599af009-04e1-4411-9b19-759df48c2aaa" />
- 用 ```git show``` 將明文憑證顯示出來
  - <img width="1920" height="90" alt="image" src="https://github.com/user-attachments/assets/47889f77-b1d7-452c-aabf-c1e2a38cb6ad" />

## 22 port
- 成功用憑證登入
  - <img width="1920" height="772" alt="image" src="https://github.com/user-attachments/assets/bb3a0abd-8ee1-4836-8591-113f58ba19df" />
- 取得 local.txt
  - <img width="793" height="59" alt="image" src="https://github.com/user-attachments/assets/52b72157-5eb8-45e2-a7a4-24d3d30b346a" />

## 提權
- metasploit
  - <img width="1920" height="532" alt="image" src="https://github.com/user-attachments/assets/8b0887af-49e2-4603-a57a-ffa022ec78a7" />
- 取得 proof.txt
  - <img width="1348" height="81" alt="image" src="https://github.com/user-attachments/assets/c809fbef-c8d6-457e-b282-1386e9b39e7b" />



















































