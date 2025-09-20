## nmap scanning
- <img width="1918" height="777" alt="image" src="https://github.com/user-attachments/assets/465d3908-ef3b-47c3-8fc5-e8767685ae17" />

## 80 port
- dirsearch 沒掃到什麼重要的東西
  - <img width="1918" height="833" alt="image" src="https://github.com/user-attachments/assets/c79c03e4-b07d-45ab-bd8d-fde5f5a132b8" />

## 81 port
- dirsearch 掃到 /admin 是個登入頁面
  - <img width="1918" height="787" alt="image" src="https://github.com/user-attachments/assets/00162c4e-e63f-4e45-80b6-80fcff8f3c22" />
  - <img width="1918" height="817" alt="image" src="https://github.com/user-attachments/assets/30d3de54-0225-4ba4-9bb8-8c766ebc08ec" />
- 從 title 發現網頁是 Attendance and Payroll System
  - <img width="1918" height="840" alt="image" src="https://github.com/user-attachments/assets/05cc4a88-1383-49a4-9743-1821c9e82567" />
- Attendance and Payroll System v1.0 - Remote Code Execution (RCE)
  - https://www.exploit-db.com/exploits/50801
- 修改腳本程式碼後，成功 RCE
  - <img width="1475" height="337" alt="image" src="https://github.com/user-attachments/assets/f9907890-682d-4eaf-9cf8-3a73404596be" />

## 提權
- 下 whoami /priv 發現 SeImpersonatePrivilege 可以提權
  - <img width="1522" height="385" alt="image" src="https://github.com/user-attachments/assets/8b75a305-b705-46da-a3d6-c67ccf7ba50a" />
- 成功提權成 system
  - <img width="1250" height="297" alt="image" src="https://github.com/user-attachments/assets/7c3c719a-8a29-4b9d-8fb4-604169d3301a" />



















































