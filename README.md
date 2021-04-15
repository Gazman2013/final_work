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
2. На zabbix-agent устаналиваем server address сервера, listenport, hostname. На сервере добавляем его в группу и templates. 
3. ![image](https://user-images.githubusercontent.com/78871778/114745101-036b2080-9d57-11eb-99b7-75930d03a9c3.png)
4. ![image](https://user-images.githubusercontent.com/78871778/114746381-5b565700-9d58-11eb-9621-791c81f213c8.png)

## ELK http://104.198.211.198:5601/
Установка была вручную по статьям
1. https://habr.com/ru/post/538840/
2. https://habr.com/ru/post/538974/
3. Установка метрик для Docker
4. ![image](https://user-images.githubusercontent.com/78871778/114916605-a8582d00-9e2d-11eb-9fbc-ac52c1234cfa.png)
5. 



## Jenkins 
1. http://35.232.202.39:8080/
2. ![image](https://user-images.githubusercontent.com/78871778/114750666-e6395080-9d5c-11eb-8e82-3c8c146aa40b.png)
3. ![image](https://user-images.githubusercontent.com/78871778/114750572-cd309f80-9d5c-11eb-871a-9d0a858c1d83.png)
4. 
