# final_work
1. instance ansible-ctrl для использования blaybook-ов
2. https://github.com/Gazman2013/docker-compose-final-work исходное приложение
3. Zabbix https://blog.zabbix.com/installing-the-zabbix-server-with-ansible/13317/
4. Установка плагина Docker Compose Build Step
5. visudo ansible ALL=(ALL:ALL) NOPASSWD:ALL
6. Установка на ansible-ctrl docker 
7. Установка Zabbix 
docker run --name zabbix-appliance -t \
      -p 10051:10051 \
      -p 80:80 \
      -d zabbix/zabbix-appliance:latest
