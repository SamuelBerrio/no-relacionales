---
sidebar_position: 2
---

# Instalación - Cassandra

## Instalación desde la Terminal en Linux

Sigue estos pasos para instalar Cassandra en tu sistema Linux:

1. Abre la terminal.

2. Agrega el repositorio de Apache Cassandra al archivo sources.list.d:

   ```bash
   echo "deb http://www.apache.org/dist/cassandra/debian 311x main" | sudo tee -a /etc/apt/sources.list.d/cassandra.sources.list
   ```

3. Importa la clave del repositorio:
  
   ```bash
   sudo apt-get update
   sudo apt-get install -y openjdk-8-jdk     # Instala Java si no lo tienes
   sudo apt-key adv --keyserver pool.sks-keyservers.net --recv-key A278B781FE4B2BDA
   ``` 

4. Actualiza la lista de paquetes e instala Cassandra:

   ```bash
   sudo apt-get update
   sudo apt-get install -y cassandra
   ``` 

5. Inicia el servicio de Cassandra:

   ```bash
   sudo service cassandra start
   ``` 

¡Ahora Cassandra está instalada y en ejecución en tu sistema Linux!

## Instalación desde Docker

Si prefieres utilizar Docker, sigue estos pasos:

1. Asegúrate de tener Docker instalado en tu sistema. Puedes seguir las instrucciones de instalación aquí.

2. Ejecuta el siguiente comando para obtener una instancia de Cassandra en un contenedor:

   ```bash
   docker run -d --name cassandra-container -p 9042:9042 cassandra
   ``` 
   Esto iniciará un contenedor de Docker con Cassandra en el puerto 9042.

Con estos métodos de instalación, podrás empezar a trabajar con Cassandra en tu entorno Linux, ya sea directamente o a través de Docker.