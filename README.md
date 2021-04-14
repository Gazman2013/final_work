# final_work
1. Устанока 2-х инстанцев в GCP. instance ansible-ctrl для использования blaybook-ов, zabbix-сервера. docker. Jenkins для сервера jenkins, docker.  
2. Сбока приложения выполняется в docker-compose. https://github.com/Gazman2013/docker-compose-final-work исходное приложение. Там же находится Jenkinsfile
3. 
4. Установка плагина Docker Compose Build Step
5. visudo ansible ALL=(ALL:ALL) NOPASSWD:ALL
6. Установка на ansible-ctrl docker 
7. Установка Zabbix 
docker run --name zabbix-appliance -t \
      -p 10051:10051 \
      -p 80:80 \
      -d zabbix/zabbix-appliance:latest
