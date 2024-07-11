启动 elk 命令  
docker composer up -d 


kibana启动报错，kibana_system用户认证  
[ERROR][elasticsearch-service] Unable to retrieve version information from Elasticsearch nodes. security_exception: [security_exception] Reason: unable to authenticate user [kibana_system] for REST request [/_nodes?filter_path=nodes.*.version%2Cnodes.*.http.publish_address%2Cnodes.*.ip]

解决办法:
进入到es容器,执行以下命令，新密码和kibana.yml 文件中的es password 保持一致  
elasticsearch-reset-password -u kibana_system -i