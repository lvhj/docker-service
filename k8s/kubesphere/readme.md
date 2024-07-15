# 常见问题
## 未创建storageclass
Error from server (NotFound): storageclasses.storage.k8s.io "standard" not found

解决办法
kubectl apply -f standard-storageclass.yaml
#查看是否创建storageclass  
kubectl get storageclasses
