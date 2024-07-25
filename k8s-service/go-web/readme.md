## 创建 TLS 证书 Secret
你需要将 TLS 证书和密钥创建为 Kubernetes Secret。假设你有 tls.crt 和 tls.key 文件，运行以下命令创建 Secret：

        kubectl create secret tls go-web-tls --cert=./cert/tls.crt --key=./cert/lvhj.publicvm.com.key -n go-web