# categorizadorpalavras
 Categorizador de Palavras

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
 
1. Palavras pequenas de até 3 caracteres
```
docker-compose exec kafka kafka-console-consumer --bootstrap-server localhost:9092 --topic pequenas --from-beginning
```
2. Palavras médias de 4 até 6 caracteres
```
docker-compose exec kafka kafka-console-consumer --bootstrap-server localhost:9092 --topic medias --from-beginning
```
3. Palavras grandes maior de 6 caracteres
```
docker-compose exec kafka kafka-console-consumer --bootstrap-server localhost:9092 --topic grandes --from-beginning
```
