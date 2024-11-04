    mv docker-compose-linux-x86_64 /usr/local/bin/docker-compose  
    sudo chmod +x /usr/local/bin/docker-compose  
    sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose  
    docker-compose -v


set http_proxy=http://192.168.0.104:7890 & set https_proxy=http://192.168.0.104:7890


echo 'export http_proxy=http://192.168.0.104:7890' >> ~/.bashrc
echo 'export https_proxy=http://192.168.0.104:7890' >> ~/.bashrc


[Service]
Environment="HTTP_PROXY=http://192.168.0.104:7890/"
Environment="HTTPS_PROXY=http://192.168.0.104:7890/"
Environment="NO_PROXY=localhost,127.0.0.1"