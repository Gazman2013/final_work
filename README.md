# final_work
1. Устанока 2-х инстанцев в GCP. instance ansible-ctrl для использования blaybook-ов, zabbix-сервера. docker. Jenkins для сервера jenkins, docker.  
2. Сбока приложения выполняется в docker-compose. https://github.com/Gazman2013/docker-compose-final-work исходное приложение. Там же находится Jenkinsfile
3. Установка и настройка ansible в https://github.com/Gazman2013/final_work/tree/main/Ansible. С помощью playbook установлен docker, jenkins, zabbix-agent.
4. Zabbix server http://35.184.58.235/
5. Установка Zabbix на ansible-ctrl 
docker run --name zabbix-appliance -t \
      -p 10051:10051 \
      -p 80:80 \
      -d zabbix/zabbix-appliance:latest
6. ![image](https://user-images.githubusercontent.com/78871778/114745101-036b2080-9d57-11eb-99b7-75930d03a9c3.png)

## Jenkins 
