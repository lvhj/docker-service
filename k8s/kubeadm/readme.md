

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
