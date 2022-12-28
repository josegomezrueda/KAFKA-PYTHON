# KAFKA-PYTHON

## Pasos a seguir

1. Instalamos docker desktop
2. Para comprobar que está correctamente instalado comprobamos los siguientes comandos: docker --version y docker-compose --version
3. Necesitamos hacer pull a la imagen de zookeeper y kafka
4. Creamos la carpeta DOCKER_KAFKA_SETUP y dentro el documento llamado: docker-compose.yml
5. Desde la terminal y la carpeta ejecutamos el siguiente comando: docker-compose -f docker-compose.yml up -d
6. Comprobamos que está levantado el docker con docker ps
7. Ejecutamos con docker exec -it kafka /bin/sh y comprobamos que tiene creadas las carpetas
8. Una vez dentro, vamos a la carpeta opt/kafka_2.13-2.7.1/bin y ejecutamos el comando para crear el topico: kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic messages 
9. En la misma dirección ejecutamos en siguiente comando para ver los topicos listados: kafka-topics.sh --list --zookeeper zookeeper:2181
10. Por último, nos salimos con el comando exit e iniciamos el entorno virtual de conda donde tengamos instalado kafka-python
11. En el entorno virtual tenemos que instalar la libreria kafka-python. 
12. Por último, ejecutamos consumer.py y producer.py simultáneamente.