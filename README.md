# final_work
## Подготовка 
1. Устанока 3-х инстанцев в GCP. 
![image](https://user-images.githubusercontent.com/78871778/114931595-1c4f0100-9e3f-11eb-8600-668a66c1d939.png)

instance ansible-ctrl для использования blaybook-ов, zabbix-сервера. docker. Jenkins для сервера jenkins, docker. Kibana для просмотра метрик.  
3. Сбока приложения выполняется в docker-compose. https://github.com/Gazman2013/docker-compose-final-work исходное приложение. Там же находится Jenkinsfile
4. Установка и настройка ansible в https://github.com/Gazman2013/final_work/tree/main/Ansible. С помощью playbook установлен docker, jenkins, zabbix-agent.
5. ![image](https://user-images.githubusercontent.com/78871778/114749849-09afcb80-9d5c-11eb-92d9-794f6c872261.png)

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

## Git
1. git config --global user.name ”Maxim Rodionov”
2. git config --global user.email rodionov.gazman2013@gmail.com
3. git clone https://github.com/Gazman2013/final_work
4. git pull
5. nano docker-compose.yml именяем порт
6. git add docker-compose.yml
7. git commit -m "edit port compose file"
8. git push вводим логин и пароль


## Jenkins 
1. http://35.232.202.39:8080/

2. Настройка Item 
![image](https://user-images.githubusercontent.com/78871778/114930857-2c1a1580-9e3e-11eb-9b7b-538f4c8f65c9.png)

![image](https://user-images.githubusercontent.com/78871778/114930907-3a683180-9e3e-11eb-9869-feb42cd88c8b.png)

![image](https://user-images.githubusercontent.com/78871778/114930985-4c49d480-9e3e-11eb-89c9-830cb41d3f09.png)


3. ![image](https://user-images.githubusercontent.com/78871778/114750666-e6395080-9d5c-11eb-8e82-3c8c146aa40b.png)

4. ![image](https://user-images.githubusercontent.com/78871778/114750572-cd309f80-9d5c-11eb-871a-9d0a858c1d83.png)

5. При изменениях на git, по расписанию запускается build приложения
![image](https://user-images.githubusercontent.com/78871778/114921375-2c60e380-9e33-11eb-823f-9b927c37c089.png)

6. ![image](https://user-images.githubusercontent.com/78871778/114921420-371b7880-9e33-11eb-89da-c91ba1ab925b.png)

7. ![image](https://user-images.githubusercontent.com/78871778/114921488-439fd100-9e33-11eb-80be-816a342cebd5.png)

8. Изменения номера порта в docker ps
![image](https://user-images.githubusercontent.com/78871778/114931471-f6c1f780-9e3e-11eb-8e98-b9249bdfd561.png)

 
