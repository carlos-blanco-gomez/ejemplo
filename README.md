Subir un repositorio local a GitHub implica varios pasos. Aquí tienes una guía paso a paso para hacerlo desde la línea de comandos:

1. Crear un Repositorio en GitHub
Primero, necesitas crear un nuevo repositorio en tu cuenta de GitHub:

Ingresa a GitHub y asegúrate de haber iniciado sesión.
En la esquina superior derecha, haz clic en el signo +, luego selecciona "New repository".
Asigna un nombre a tu repositorio, elige la visibilidad (público o privado) y, si lo deseas, inicializa con un archivo README (esto es opcional, especialmente si ya tienes un archivo README en tu repositorio local).
Haz clic en "Create repository".

2. Inicializar tu Repositorio Local
Si aún no lo has hecho, deberás inicializar tu proyecto local como un repositorio de Git:


cd /path/to/your/project
git init

3. Añadir Archivos al Repositorio Local
Luego, añade los archivos de tu proyecto al repositorio. Si ya tienes archivos, puedes añadirlos con:



git add .

Este comando añade todos los archivos en el directorio actual. Si solo quieres añadir archivos específicos, puedes hacerlo con:


git add <archivo1> <archivo2>

4. Hacer el Primer Commit
Ahora debes hacer un commit con los archivos que has añadido:


git commit -m "Tu mensaje de commit"

5. Conectar tu Repositorio Local con GitHub
Conecta tu repositorio local al repositorio de GitHub que acabas de crear:


git remote add origin https://github.com/tu-usuario/tu-repositorio.git


Aquí, debes reemplazar tu-usuario con tu nombre de usuario de GitHub y tu-repositorio.git con el nombre que le diste a tu repositorio en GitHub.

6. Push (subir) tu Código a GitHub
Finalmente, sube tu código a GitHub con:


git push -u origin master

En el caso de que la rama principal se llame main (esto ha cambiado recientemente en los nuevos repositorios de GitHub), deberás usar:


git push -u origin main

El comando -u hace que tu repositorio local "recuerde" la rama a la que estás haciendo push, así que para futuros push simplemente podrías usar git push.

Posibles Problemas de Autenticación
Si estás utilizando Git en la línea de comandos por primera vez, es posible que te encuentres con problemas de autenticación. GitHub ya no permite la autenticación con nombre de usuario y contraseña para las operaciones de Git, por lo que tendrás que utilizar un token de acceso personal (PAT). Puedes crear y gestionar tus tokens de acceso personal en la configuración de tu cuenta de GitHub.

Una vez que hayas subido tu código a GitHub, podrás ver tu repositorio en la web y administrar colaboradores, hacer seguimiento de issues, utilizar GitHub Actions, y más.

Recuerda siempre revisar los archivos antes de subirlos a un repositorio público para asegurarte de que no estás compartiendo accidentalmente contenido sensible como contraseñas, claves API, etc.
