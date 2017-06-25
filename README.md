storm-twitter-word-count
========================

Contador de Palabras de Twitter Utilizando la Herramienta Apache Storm Basado en https://github.com/davidkiss/storm-twitter-word-count y utlizando las caracterísitcas de Streaming del mismo.

Este es un repositorio que se utilizará para un proyecto de investigación de la Escuela Colombiana de Ingeniería Julio Garavito

Se ha actualizado el proyecto para ser usado en apache storm 1.1.0, y se ha ampliado para ser usado no sólo en modo local si no también en modo cluster.

Actualmente el repositorio contiene 2 ramas:

-Master (Para Correr En Modo Local)
-Cluster (Para Correr En Modo Cluster)

Rama Cluster:
  Para Ejecutar Esta Aplicación Es Necesario:
  1. Clonar el repositorio
  2. Ir a la carpeta del repositorio y ejecutar el comando :
    mvn clean package assembly:single
  3. En el nodo nimbus ir a la carpeta de apache storm y ejecutar el comando 
    bin/storm jar /home/ubuntu/experimentos/TwitterStorm1/target/storm-twitter-word-count-jar-with-dependencies.jar com.kaviddiss.storm.Topology storm-twitter-word-count
    
  Para cambiar la cantidad de trabajadores solamente es editar la línea
  config.setNumWorkers(3); en Topology.java

   
