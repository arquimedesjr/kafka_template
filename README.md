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
