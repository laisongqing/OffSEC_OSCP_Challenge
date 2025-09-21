## nmap
- <img width="1918" height="408" alt="image" src="https://github.com/user-attachments/assets/8e0cbf56-baf1-4695-b6ec-32d466cfa687" />

## .121
- 在 .121 發現有以下 user
  - <img width="1067" height="617" alt="image" src="https://github.com/user-attachments/assets/2d887c07-2798-4baf-969b-3bb5e5942c35" />
- 用 hydra 成功爆出 offsec:passeord 可以 ssh 登入 .122
  - <img width="1918" height="778" alt="image" src="https://github.com/user-attachments/assets/82b3608b-62f0-4669-a8b8-b3e85be7a84c" />

## 22 port
- 成功登入
  - <img width="1918" height="677" alt="image" src="https://github.com/user-attachments/assets/93bf2929-e555-46bb-ad86-accb5df7d05b" />
- 取得 local.txt
  - <img width="1125" height="57" alt="image" src="https://github.com/user-attachments/assets/a3f3fabd-4c49-4e83-8d84-c82a6c7767b4" />

## 提權
- sudo -l 發現可以用 openvpn 提權
  - <img width="1292" height="250" alt="image" src="https://github.com/user-attachments/assets/a787b85e-f67a-4d02-b817-170d9fa47867" />
- GTFOBins 
  - <img width="1332" height="392" alt="image" src="https://github.com/user-attachments/assets/63f8d1ac-d363-4ca0-86f8-8a669be6923c" />
- 成功提權
  ```
  sudo openvpn --dev null --script-security 2 --up '/bin/sh -c sh'
  ```
  - <img width="1187" height="367" alt="image" src="https://github.com/user-attachments/assets/376a5e10-1ce6-47ac-9e42-44b66188ee41" />
- 取得 proof.txt
  - <img width="677" height="55" alt="image" src="https://github.com/user-attachments/assets/4658b436-b3df-49bb-9496-92da0e318f24" />





















































