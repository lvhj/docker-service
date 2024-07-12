
启动报错
Error from server (NotFound): storageclasses.storage.k8s.io "standard" not found

kubectl apply -f standard-storageclass.yaml

#查看是否创建storageclass  
kubectl get storageclasses
