## Linux kubeadm安装文档
https://kubernetes.io/zh-cn/docs/setup/production-environment/tools/kubeadm/install-kubeadm/

在低于 Debian 12 和 Ubuntu 22.04 的发行版本中，/etc/apt/keyrings 默认不存在。 应在 curl 命令之前创建它。

    mkdir /etc/apt/keyrings/
    curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.30/deb/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg

## kubeadm init
    kubeadm init --apiserver-advertise-address=172.28.107.113 --image-repository=registry.aliyuncs.com/google_containers --pod-network-cidr=10.244.0.0/16
    
    注意事项
    --apiserver-advertise-address=172.28.107.113 替换为master节点内网ip
    新版本中 k8s已经不支持 初始化设置docker
    --container-runtime=docker


