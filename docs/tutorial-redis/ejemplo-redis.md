---
sidebar_position: 3
---

# Ejemplo de Uso de Redis

En este ejemplo, crearemos una base de datos simple en Redis para almacenar información sobre estudiantes universitarios. Utilizaremos distintas estructuras de datos de Redis para representar los datos de cada estudiante.

## Configuración Inicial

Antes de empezar, asegúrate de tener Redis instalado y en ejecución en tu sistema.

### Creación de un Estudiante

Vamos a crear un estudiante con la siguiente información:

- **Nombre:** Juan
- **Apellido:** Pérez
- **Edad:** 22
- **Ciudad:** Ciudad de México
- **Cédula:** 123456789

## Ejemplo de Utilización

1. **Conectar a Redis:**

   Utiliza la interfaz de línea de comandos de Redis ejecutando:

   ```bash
   redis-cli
   ```

2. **Almacenar la Información del Estudiante:**

   Utilizaremos una estructura de datos de tipo hash para representar a cada estudiante. Ejecuta los siguientes comandos:

   ```bash
   HMSET estudiante:123456789 nombre "Juan" apellido "Pérez" edad 22 ciudad "Ciudad de México"
   ```
   Esto crea un hash llamado estudiante:123456789 con los campos nombre, apellido, edad, y ciudad.

3. **Obtener la Información del Estudiante:**

   Para recuperar la información del estudiante, ejecuta:

   ```bash
   HGETALL estudiante:123456789
   ```

4. **Modificar la Edad del Estudiante:**

   Si necesitas actualizar la información, puedes hacerlo fácilmente:

   ```bash
   HSET estudiante:123456789 edad 23
   ```

5. **Listar Estudiantes:**

   Vamos a utilizar una lista para mantener un registro de todas las cédulas de los estudiantes. Ejecuta:

   ```bash
   RPUSH lista_estudiantes 123456789
   ```

   Ahora puedes recuperar la lista completa de estudiantes con:

   ```bash
   LRANGE lista_estudiantes 0 -1
   ```

   Esto mostrará todas las cédulas almacenadas.

Este ejemplo ilustra cómo Redis puede ser utilizado para crear y gestionar una base de datos simple de estudiantes universitarios. Explora más comandos y estructuras de datos de Redis para adaptarlos a tus necesidades específicas.