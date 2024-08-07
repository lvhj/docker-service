## master节点和work保持一致的文件

contained镜像代理
master节点和worker节点 config.toml保持一致

    scp root@120.55.62.240:/etc/containerd/config.toml /etc/containerd/config.toml

### 开放端口
    30880(kube-sphere)
    10250(worker节点)
    10255(worker节点)
    6444(etcd)
    6443(etcd)
