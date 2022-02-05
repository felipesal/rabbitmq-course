## Projeto
Projeto de estudo do curso de RabbitMQ com Spring Boot.

## Como executar

- Primeiramente é preciso ter um container do rabbitmq de pé. Usar o comando:
`docker run -d -p 15672:15672 -p 5672:5672 rabbitmq:management`

Nesse momento o container vai ter duas portas, a 15672 é a interface gráfica e a 5672 é a que funciona como host de filas.

- Em seguida executar o serviço producer;

- Por último executar o serviço consumer;

Para ver funcionar, utilizar o endpoint 
`localhost:8081/send` 

com o payload
```
{
  "text":"Mensagem de exemplo"
}
```

Em seguida irá aparecer a mensagem no console do consumer, mostrando que os serviços estão se comunicando através da fila

`rk.producer.aula-spring`

