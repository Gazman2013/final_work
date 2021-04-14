# final_work
## Подготовка 
1. Устанока 2-х инстанцев в GCP. instance ansible-ctrl для использования blaybook-ов, zabbix-сервера. docker. Jenkins для сервера jenkins, docker.  
2. Сбока приложения выполняется в docker-compose. https://github.com/Gazman2013/docker-compose-final-work исходное приложение. Там же находится Jenkinsfile
3. Установка и настройка ansible в https://github.com/Gazman2013/final_work/tree/main/Ansible. С помощью playbook установлен docker, jenkins, zabbix-agent.
4. ![image](https://user-images.githubusercontent.com/78871778/114749849-09afcb80-9d5c-11eb-92d9-794f6c872261.png)

## Zabbix server http://35.184.58.235/
1. Установка Zabbix на ansible-ctrl 
docker run --name zabbix-appliance -t \
      -p 10051:10051 \
      -p 80:80 \
      -d zabbix/zabbix-appliance:latest
2. На zabbix-agent устаналивает адрес сервера, listenport, hostname. На сервере добавляем его в группу и templates. 
3. ![image](https://user-images.githubusercontent.com/78871778/114745101-036b2080-9d57-11eb-99b7-75930d03a9c3.png)
4. ![image](https://user-images.githubusercontent.com/78871778/114746381-5b565700-9d58-11eb-9621-791c81f213c8.png)

## Jenkins 
