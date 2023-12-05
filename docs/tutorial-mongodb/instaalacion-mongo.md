---
sidebar_position: 2
---

# Instalación - MongoDB

En esta sección, exploraremos diferentes métodos para instalar MongoDB en tu sistema. Puedes elegir entre instalarlo directamente desde la terminal en Linux o utilizar Docker para una implementación más rápida.

## Instalación desde la Terminal en Linux

Sigue estos pasos para instalar MongoDB en un sistema Linux:

1. Abre la terminal.
2. Agrega la clave GPG de MongoDB con el siguiente comando:

   ```bash
   sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 9DA31620334BD75D9DCB49F368818C72E52529D4
   ```
3. Añade el repositorio de MongoDB:
   
   ```bash
   echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu $(lsb_release -cs)/mongodb-org/4.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list
   ```
4. Actualiza la lista de paquetes e instala MongoDB:
   
   ```bash
   sudo apt-get update
   sudo apt-get install -y mongodb-org
   ```
   
## Instalación desde Docker

Para instalar MongoDB utilizando Docker en Windows, sigue estos pasos:

1. Asegúrate de tener Docker Desktop instalado en tu sistema. Puedes descargarlo desde aquí.

2. Abre PowerShell o la terminal de tu elección.

3. Ejecuta el siguiente comando para iniciar un contenedor de MongoDB:

   ```bash
   docker run -d -p 27017:27017 --name mongodb-container mongo
   ```

Esto iniciará un contenedor de Docker con MongoDB en el puerto 27017 y ya con estos pasos, habrás instalado MongoDB utilizando Docker en tu sistema, ya sea en Linux o Windows.