Revisa el archivo Dockerfile en la carpeta users-svc y compáralo con el mismo archivo en la carpeta ws-server. ¿Qué te llama la atención? Ahora revisa la sentencia command para los respectivos servicios en el archivo docker-compose.yml. ¿Qué concluyes?


Lo que llama la atención es que dos servicios con funcionalidades diferentes (gestión de usuarios vs servidor de websockets) utilizan el mismo Dockerfile. Esto sugiere que cualquier diferencia en su comportamiento no proviene del Dockerfile, sino de los archivos y código fuente específicos que se copian en el contenedor, y posiblemente de cómo se inician estos servicios.

Revisa el archivo Dockerfile en la carpeta frontend. ¿Qué te llama la atención? ¿En qué es diferente de los otros archivos Dockerfile?


Utiliza un proceso de construcción en múltiples etapas.
Incorpora la construcción de una aplicación frontend y luego su despliegue usando Nginx.
Utiliza una versión diferente de Node.js.
En lugar de simplemente preparar un entorno de Node.js, este Dockerfile también se preocupa por servir la aplicación a través de un servidor web (Nginx).

Flyway es una herramienta de migración de bases de datos. Ayuda a gestionar y rastrear cambios en la estructura de la base de datos. Con Flyway, puedes versionar tu base de datos, aplicar migraciones para avanzar a una nueva versión o deshacer cambios para retroceder a una versión anterior.

¿Para qué sirve el servicio flyway? ¿Qué pasa al hacer docker ps con respecto a este servicio?

Las principales características y usos de Flyway incluyen:

Versionamiento de la Base de Datos: Puedes tener un historial controlado y ordenado de todas las modificaciones de la estructura de la base de datos.
Migraciones: Flyway permite aplicar cambios en la base de datos de forma ordenada y controlada.
Validaciones: Antes de aplicar una migración, Flyway puede validar que la estructura actual de la base de datos coincide con lo que se espera.
Reparación: En caso de que una migración no se aplique correctamente, Flyway tiene un comando de reparación que ayuda a corregir la situación.
En el contexto de un proyecto, utilizar Flyway puede ser especialmente útil en entornos de desarrollo colaborativo, donde múltiples desarrolladores pueden necesitar aplicar cambios en la base de datos. Flyway asegura que estos cambios se apliquen de manera consistente y en el orden correcto.