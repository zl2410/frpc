# frpc

配置

user = "fc"

# frps的地址和通信端口

serverAddr = "107.151.249.220"  

serverPort = 5100

# 与frps通信的认证方式和token值

auth.method = "token"

auth.token = "12345dfFDFERDFDF678"

[[proxies]]

name = "ssh_local_linux01"

type = "tcp"

localIP = "127.0.0.1"

localPort = 22

remotePort = 5600


[[proxies]]

name = "web01"

type = "http"

localIP = "127.0.0.1"

localPort = 8080

#subdomain = "web01"

customDomains = ["107.151.249.220"]  # 替换为您的自定义域名

locations = ["/", "/pic"]

httpUser = "admin"

httpPassword = "admin"

