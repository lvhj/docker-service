## master节点和work保持一致的文件

从master复制  

    /etc/cni/net.d/10-flannel.conflist
    /var/lib/kubelet/kubeadm-flags.env 
    /etc/kubernetes/kubelet.conf
    /etc/containerd/config.toml

    scp root@120.55.62.240:/etc/cni/net.d/10-flannel.conflist /etc/cni/net.d/10-flannel.conflist
    scp root@120.55.62.240:/var/lib/kubelet/kubeadm-flags.env  /var/lib/kubelet/kubeadm-flags.env 
    scp root@120.55.62.240:/etc/kubernetes/kubelet.conf /etc/kubernetes/kubelet.conf
    scp root@120.55.62.240:/etc/containerd/config.toml /etc/containerd/config.toml


master节点和worker节点 config.toml保持一致

    scp root@120.55.62.240:/etc/containerd/config.toml /etc/containerd/config.toml


kubeadm reset之后会删除掉/etc/kubernetes/admin.conf 文件

    scp root@120.55.62.240:/etc/kubernetes/admin.conf  /etc/kubernetes/admin.conf   
    echo "export KUBECONFIG=/etc/kubernetes/admin.conf" > /etc/profile.d/kubeconfig.sh  
    source /etc/profile.d/kubeconfig.sh  

安装网络插件flannel，配置文件保持一致 

    scp root@120.55.62.240:/etc/cni/net.d/10-flannel.conflist /etc/cni/net.d/10-flannel.conflist


若master节点未配置10-kubeadm.conf work节点也无须配置

    rm -rf /etc/systemd/system/kubelet.service.d/10-kubeadm.conf

### 开放端口
    30880(kube-sphere)
    10250(worker节点)
    10255(worker节点)
    6444(etcd)
    6443(etcd)
