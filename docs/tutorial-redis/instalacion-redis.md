---
sidebar_position: 2
---

# Instalación - Redis

Redis es conocido por su sencilla instalación y su capacidad para operar eficientemente tanto en sistemas Linux como en entornos Docker. A continuación, te proporcionamos pasos detallados para instalar Redis en ambas plataformas.

## Instalación en Linux

Sigue estos pasos para instalar Redis en un sistema Linux:

1. Abre la terminal.

2. Ejecuta el siguiente comando para actualizar los paquetes:

   ```bash
   sudo apt-get update
   ```

3. Instala Redis con el siguiente comando:

   ```bash
   sudo apt-get install redis-server
   ```

4. Una vez instalado, Redis debería iniciarse automáticamente. Puedes verificar su estado con:

   ```bash
   redis-cli ping
   ```

## Instalación con Docker

Si prefieres utilizar Docker, sigue estos pasos:

1. Asegúrate de tener Docker instalado en tu sistema. Puedes seguir las instrucciones de instalación aquí.

2. Ejecuta el siguiente comando para obtener una instancia de Redis en un contenedor:

   ```bash
   docker run -d --name redis-container -p 6379:6379 redis
   ```

3. Puedes verificar si Redis está en ejecución utilizando:

   ```bash
   docker ps
   ```

Con estos pasos, Redis estará instalado y listo para su uso en tu sistema Linux o en un contenedor Docker. ¡Ahora puedes comenzar a explorar la potencia de esta base de datos en memoria!