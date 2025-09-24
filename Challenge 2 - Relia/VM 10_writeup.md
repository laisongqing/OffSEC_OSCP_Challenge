## namp scanning
- <img width="1920" height="731" alt="image" src="https://github.com/user-attachments/assets/942dae22-9677-4d5d-a2a1-10062cf1bc42" />
- <img width="1920" height="550" alt="image" src="https://github.com/user-attachments/assets/27a3fc46-1891-4725-ba1b-dde95467f40c" />

## 21 port
- ftp 要輸入 passive 才能 ls -la 檔案，但無法上傳 shell
  - <img width="1919" height="762" alt="image" src="https://github.com/user-attachments/assets/1d6cbf01-986f-4cbf-ad1e-c4e7a9f4abb6" />

## 80、443、8000 port
- Apache httpd 2.4.49 存在 CVE-2021-41773
- 利用 github 上的 exploit
  - https://github.com/twseptian/cve-2021-41773
- 成功讀到 /etc/passwd
  - <img width="1920" height="770" alt="image" src="https://github.com/user-attachments/assets/7fb9150f-f7b9-4dff-8092-3a544b46f2be" />
- 成功在 /home/anita 底下讀到 local.txt
  - <img width="1572" height="104" alt="image" src="https://github.com/user-attachments/assets/2e66a188-2dc8-4ad0-8850-60959b1ad608" />
- 成功嘗試讀取 /home/anita/.ssh/id_ecdsa (id_rsa)
  - <img width="1920" height="317" alt="image" src="https://github.com/user-attachments/assets/b098c651-869d-4e64-90c1-2116fb594985" />

## 2222 port
- 成功破解 id_rsa 的密碼
  - <img width="1920" height="384" alt="image" src="https://github.com/user-attachments/assets/a0b6376a-5675-4445-9bae-92d975ada5a4" />
- 成功 ssh 登入
  - <img width="1920" height="743" alt="image" src="https://github.com/user-attachments/assets/9086a0b8-a298-458b-a254-77b420d7a2a0" />

## 提權
- msfconsole
  - <img width="1920" height="634" alt="image" src="https://github.com/user-attachments/assets/955e8c31-473d-4762-ada4-2595522b7c84" />
- 取得 proof.txt
  - <img width="1156" height="58" alt="image" src="https://github.com/user-attachments/assets/ea3be5b9-95f7-4b9e-879f-910f4f778194" />
















































