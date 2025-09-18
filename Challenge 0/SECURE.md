<img width="1920" height="806" alt="image" src="https://github.com/user-attachments/assets/368abac7-8d4a-441e-8573-b39ecdc3d658" />## namp scanning
- <img width="1920" height="782" alt="image" src="https://github.com/user-attachments/assets/d02ec2f2-983b-406f-a603-6a13d38640bf" />
- <img width="1920" height="795" alt="image" src="https://github.com/user-attachments/assets/2ef59404-14dd-4e92-ba22-1f4017f45f8e" />

## 5001 port
- <img width="1920" height="819" alt="image" src="https://github.com/user-attachments/assets/95d9cbd8-5157-4a91-bb5b-49a2adef8071" />

## 8443 port
- 是 ManageEngine 1470 登入頁面
  - <img width="1920" height="795" alt="image" src="https://github.com/user-attachments/assets/8c57b7b2-e94d-4d81-8550-39b111c3a57f" />
- 點選 First Time User 發現登入帳號及密碼
  - <img width="1920" height="746" alt="image" src="https://github.com/user-attachments/assets/be3d531a-8c4c-4e9c-9fe8-8d8170c9dfbc" />
- 成功登入
  - <img width="1920" height="829" alt="image" src="https://github.com/user-attachments/assets/ac3d10cf-c870-44da-bdb8-3d1b4c4672c0" />
- ExploitDB 發現 ManageEngine Applications Manager 14700 - Remote Code Execution (Authenticated) 
  - https://www.exploit-db.com/exploits/48793
- ExploitDB 的 payload 無法使用
- 到 admin -> Upload Files / Binaries -> Upload Script to <Product_Home>/working/ -> 'Execute Program' 創一個 cmd1.bat
  - <img width="1920" height="806" alt="image" src="https://github.com/user-attachments/assets/206d7e83-838f-4d19-9764-8de7df51a5cd" />
- kali 寫個 cmd1.bat
  - <img width="1920" height="802" alt="image" src="https://github.com/user-attachments/assets/4dd9e05f-c1d8-4bf3-b350-6d00eb709b30" />
- 將 cmd1.bat 上傳
  - <img width="1920" height="821" alt="image" src="https://github.com/user-attachments/assets/26decc70-a723-41e4-b724-f2d38ebe953e" />
- 執行 cmd1.bat，並取得 reverse shell
  - <img width="1920" height="853" alt="image" src="https://github.com/user-attachments/assets/ebb040f2-4da4-40c5-8ae2-f8f034bc2495" />
- 取得 proof.txt
  - <img width="866" height="113" alt="image" src="https://github.com/user-attachments/assets/4b9acfbd-04a3-47e8-88e7-75b908552072" />














































