# contapalavras
 Conta Palavras

Iniciar Kafka no docker
 
```
docker-compose up
```

Iniciando o projeto

```
mvn spring-boot:run
```

Para gerar eventos podemos usar o script do próprio kafka para emitir alguns eventos no tópico `entrada`
 
```
docker-compose exec kafka kafka-console-producer --bootstrap-server localhost:9092 --topic entrada
```

Conferido os resultados
 
```
docker-compose exec kafka kafka-console-consumer --bootstrap-server localhost:9092 --topic resultado --from-beginning
```