# Защита проекта DataEngineer 2023-05-24

Требования:

<b>Docker:</b>
  1. Подготовить docker-образ Postgresql. PostgreSQL собрать из исходников, указав NAMEDATALEN = 256
  
  2. Указать в docker/docker-compose.yaml:
  
      2.1. Имя подготовленного образа PostgreSQL postgres/image
  
      2.2. POSTGRES_USER
  
      2.3. POSTGRES_PASSWORD
  
      2.4. POSTGRES_DB
  
      2.5. NIFI_WEB_PROXY_HOST
      
  3. Запустить docker-compose up -d

<b>Apache NiFi:</b>
  1. Импортировать template ELT_1C_v1.xml
  2. Указать в сервисе PGPool данные СУБД PostgreSQL
  3. Указать в процессоре InvokeHTTP в группе ExtractData:
  
      3.1. Адрес сервиса 1C Odata
    
      3.2. Логин сервиса 1C Odata
    
      3.3. Пароль сервиса 1C Odata
