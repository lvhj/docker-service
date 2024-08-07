## 创建 TLS 证书 Secret
你需要将 TLS 证书和密钥创建为 Kubernetes Secret。假设你有 tls.crt 和 tls.key 文件，运行以下命令创建 Secret：

    kubectl create secret tls go-web-tls --cert=./cert/tls.pem --key=./cert/private.key -n go-web

## 查看秘钥
kubectl get secrets -n ingress-nginx
kubectl get secrets -n go-web

curl -v https://lvhj.publicvm.com/lvhj-go/lvhj -k

    kubectl delete -A ValidatingWebhookConfiguration ingress-nginx-admission

