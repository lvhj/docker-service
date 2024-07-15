## Linux 安装kubeadm文档
https://kubernetes.io/zh-cn/docs/setup/production-environment/tools/kubeadm/install-kubeadm/


## 注意事项
mkdir /etc/apt/keyrings/
curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.30/deb/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg

### master节点和work保持一致的文件

从master复制
/etc/cni/net.d/10-flannel.conflist
/var/lib/kubelet/kubeadm-flags.env 
/etc/kubernetes/kubelet.conf
/etc/containerd/config.toml

若master节点未配置10-kubeadm.conf work节点也无须配置
rm -rf /etc/systemd/system/kubelet.service.d/10-kubeadm.conf

### 端口
30880(kube-sphere)
10250(worker节点)
10255(worker节点)
6444(etcd)
6443(etcd)
