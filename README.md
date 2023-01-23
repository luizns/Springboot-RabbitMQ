# RabbitMQ - Spring Boot

API REST com Spring Boot e RabbitMQ:

- Criar uma conexão entre Spring Boot e o RabbitMQ
- Criar um produtor(producer) para enviar mensagem JSON para o RabbitMQ
- Criar um consumidor (consumer) que será responsável pela leitura das mensagens e/ou processamento.

## Pré-requisitos

IDE/Editor: Intellij, Eclipse ou VSCode 

[Java v. 17](https://openjdk.org/projects/jdk/17/)

#### [Docker - com RabbitMQ instalado e configurado](https://hub.docker.com/_/rabbitmq)
```
docker pull rabbitmq:3.10-management
```
#### Executando a imagem do  RabbitMQ no Docker Container.

```
docker run --rm -it -p 15672:15672 -p 5672:5672 rabbitmq:3.10-management
```

#### URL:  ``` http://localhost:15672  ```

**Username: ```guest```**

**Password: ```guest```**


* ### [Spring Initializr - Dependências](https://start.spring.io/#!type=maven-project&language=java&platformVersion=3.0.2&packaging=jar&jvmVersion=17&groupId=com.javaguides&artifactId=springboot-rabbitmq&name=springboot-rabbitmq&description=Demo%20project%20for%20Spring%20Boot&packageName=com.javaguides.springboot-rabbitmq&dependencies=web,amqp,lombok)
    * Spring Web
    * Spring for RabbitMQ
    * Lombok


Teste a API REST usando o Postman

GET - MESSAGE:

```
http://localhost:8080/api/v1/publish?message=sample message
```

POST - USER:  ``` http://localhost:8080/api/v1/publish ```

``` 
{
    "id": 1,
    "firstName": "first-name",
    "lastName": "last-name"
}
```


### Referências:
````
https://www.javaguides.net/p/rabbitmq-java-tutorial-with-examples.html

https://www.javaguides.net/2022/07/spring-boot-rabbitmq-send-and-receive-json-messages.html

https://www.youtube.com/playlist?list=PLGRDMO4rOGcMh2fAMOnwuBMDa8PxiKWoN

https://hub.docker.com/_/rabbitmq
````