# Apache Kafka
Project Kafka template


Install Kafka

link: https://kafka.apache.org/downloads

Depois que fizer o download colocar a pasta raiz na variaveis de ambiente KAFKA_HOME e no path %KAFKA_HOME%\bin\windows

Atualizar o diretorio do log em dois arquivos (zookeeper.properties | server.properties) no diretorio %KAFKA_HOME%\config

Execução sempre primeiro o zookeeper depois o kafka

comando de execução do zookeper -> zookeeper-server-start.bat  %KAFKA_HOME%\config\zookeeper.properties
comando de execução do kafka ->  kafka-server-start.bat %KAFKA_HOME%\config\server.properties

Listar topicos -> kafka-topics.bat --bootstrap-server localhost:9092 --list

Instalação do WSL 2 no Windows: https://docs.microsoft.com/pt-br/windows/wsl/install-manual

Instalação do Docker: https://www.docker.com/products/docker-desktop

Comando para executar o docker-compose.yaml -> docker-compose up -d

create topic -> kafka-topics.bat --bootstrap-server localhost:29092 --create --topic teste --particions 2

producer topic -> kafka-console-producer.bat --broker-list localhost:29092 --topic teste

producer topic com chave e valor -> kafka-console-producer.bat --broker-list localhost:29092 --topic teste --property "parse.key=true" --property "key.separator=," 

consumer topic com chave e valor -> kafka-console-consumer.bat --bootstrap-server localhost:29092 --topic teste --property "parse.key=true" --property "key.separator=," --group grupo1

consumer topic com  valor somente -> kafka-console-consumer.bat --bootstrap-server localhost:29092 --topic teste --property "parse.key=false" --property "key.separator=," --group grupo1

consumer topic -> kafka-console-consumer.bat --bootstrap-server localhost:29092 --topic teste

consumer topic begin -> kafka-console-consumer.bat --bootstrap-server localhost:29092 --topic teste --from-beginning

consumer topic group -> kafka-console-consumer.bat --bootstrap-server localhost:29092 --topic teste --group 1

alterando partições topic -> kafka-topics.bat --bootstrap-server localhost:29092 --alter --topic teste --partitions 10

informações topic -> kafka-topics.bat --bootstrap-server localhost:29092 --topic teste --describe

delete topic -> kafka-topics.bat --bootstrap-server localhost:29092 --topic teste --delete - Com o windows não funciona, existe um bug
list topic -> kafka-topics.bat --bootstrap-server localhost:29092 --topic teste --list


Install Conduktor

https://www.conduktor.io/download
