## nmap scanning
- <img width="1919" height="726" alt="image" src="https://github.com/user-attachments/assets/87ac4e62-e013-4b3b-8c48-6c9f99f9116e" />

## 2222 port
- 成功用 anita 的 id_rsa 登入
  - <img width="1920" height="742" alt="image" src="https://github.com/user-attachments/assets/612d5bbc-ea17-49b6-bdde-a51222b0daa2" />
- 取得 local.txt
  - <img width="835" height="62" alt="image" src="https://github.com/user-attachments/assets/f65134bb-a827-41cd-bf40-5ee15b5f18ce" />

## 提權
- linpeas.sh
  - 發現本地有開 8000 port
    - <img width="1440" height="247" alt="image" src="https://github.com/user-attachments/assets/f63bf2ea-0c4d-425c-9254-1518f2ca52cc" />
    - <img width="1918" height="670" alt="image" src="https://github.com/user-attachments/assets/bf226bcd-74aa-47e2-b1b1-dceca7551fab" />
  - http://localhost:8000/backend/?view=user.inc 存在 LFI
    - <img width="1918" height="762" alt="image" src="https://github.com/user-attachments/assets/b25e9fcf-f062-47a2-9c9d-73ad4911367d" />
- 先上傳 php reverse shell 到靶機上，再 curl -v "http://localhost:8000/backend/?view=../../../../../dev/shm/shell.php"
- 成功取得 shell (www-data)
  - <img width="1918" height="302" alt="image" src="https://github.com/user-attachments/assets/e563f2e0-0b3f-480a-952d-eda0f9a0db20" />
- sudo -l 發現 www-data 可以 sudo 接任何指令
  - <img width="1398" height="220" alt="image" src="https://github.com/user-attachments/assets/a99cad1e-e938-4927-9b50-57d6a94e397d" />
- sudo su 成功提權
  - <img width="707" height="152" alt="image" src="https://github.com/user-attachments/assets/f083ef57-7360-4a23-bcbc-7b35fee1eb47" />
- 取得 proof.txt
  - <img width="1023" height="56" alt="image" src="https://github.com/user-attachments/assets/cb4eba00-c85f-443f-a088-52dab78e71d0" />




















































