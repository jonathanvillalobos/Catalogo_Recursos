## ¿Qué ventaja tiene registrar las dependencias en `requirements.txt` en lugar de compartir `.venv`?

`requirements.txt` permite compartir una lista pequeña y portable de las dependencias necesarias, incluidas sus versiones, para que cada persona pueda instalarlas en su propio entorno con `pip install -r requirements.txt`. Así se facilita reproducir la configuración del proyecto en distintos equipos y sistemas, sin enviar una carpeta `.venv` que puede ocupar mucho espacio y contener rutas, archivos y binarios específicos de la computadora donde se creó.


## ¿Por qué el repositorio local no es el mismo concepto que el fork de GitHub?

Aunque ambos contienen archivos y el historial de Git, representan cosas distintas. El fork es una copia del repositorio original alojada en GitHub, dentro de una cuenta y con su propio espacio remoto. El repositorio local es la copia de trabajo guardada en la computadora, donde se editan archivos y se pueden crear commits sin que esos cambios aparezcan todavía en GitHub.

Se relacionan mediante Git: al clonar el fork se obtiene una copia local, y `push` y `pull` permiten enviar y traer cambios entre ambas. Por eso pueden tener contenidos o historiales diferentes si todavía no se han sincronizado. En resumen, el fork es la copia remota en GitHub y el repositorio local es la copia de trabajo en la computadora; no son necesariamente dos proyectos distintos, sino dos ubicaciones que pueden corresponder al mismo proyecto.


## Preguntas individuales

**¿Cómo identificaste el comando necesario cuando la práctica no lo proporcionó?**

Se la pregunte a la IA las que no recordaba 

**¿Qué diferencia existe entre preparar un archivo para un commit y crear el commit?**

Preparar un archivo con `git add` lo incorpora al área de preparación (staging), es decir, selecciona los cambios que formarán parte del próximo registro. Crear el commit con `git commit` guarda esos cambios preparados en el historial local del repositorio, normalmente acompañados de un mensaje.

**¿Cómo puedes comprobar en qué rama estás trabajando?**

Puedes ejecutar `git branch --show-current`, que muestra el nombre de la rama activa. También puedes usar `git status`, que indica la rama actual al inicio de su salida.

**¿Cómo puedes determinar qué archivos fueron modificados antes de registrarlos?**

`git status` muestra los archivos modificados y señala si sus cambios todavía no están preparados o ya fueron añadidos al área de preparación.

**¿Cómo puedes observar exactamente qué cambió dentro de un archivo?**

`git diff` muestra las diferencias que todavía no están preparadas para el commit. Para revisar las diferencias que ya están preparadas, puedes usar `git diff --cached`.

**¿Por qué debe reconstruirse `.venv` después de obtener un repositorio?**

`.venv` es un entorno local que puede contener rutas, ejecutables y componentes específicos de la computadora donde se creó, por lo que no es portable ni suele incluirse en Git. Se reconstruye en el equipo propio y se instalan las dependencias del proyecto desde `requirements.txt`.

**¿Qué relación existe entre `requirements.txt` y `.gitignore`?**

`requirements.txt` registra qué paquetes necesita el proyecto y sus versiones; `.gitignore` indica a Git qué archivos o carpetas locales no debe incluir en el repositorio, como `.venv`. Así se comparte la receta para reconstruir el entorno, pero no el entorno instalado.

**¿Por qué la colaboración se realiza desde una rama y no directamente desde `main`?**

Una rama permite trabajar de forma aislada sin alterar directamente la rama principal. Los cambios pueden revisarse y probarse mediante un Pull Request antes de integrarlos, lo que ayuda a mantener `main` estable y facilita la colaboración.

**¿Por qué una solicitud de cambios no requiere crear un Pull Request nuevo?**

Si la solicitud corresponde al mismo trabajo y a la misma rama que un Pull Request abierto, basta con enviar los nuevos commits a esa rama: GitHub actualiza el Pull Request existente automáticamente. Se crea otro Pull Request cuando se trata de una tarea o una rama distinta.

**Después de realizar el merge en GitHub, ¿por qué todavía es necesario actualizar el repositorio local?**

El merge actualiza el repositorio remoto en GitHub, pero no cambia automáticamente la copia local. Hay que actualizarla, por ejemplo cambiando a la rama `main` y ejecutando `git pull origin main`, para traer el merge y mantener el trabajo local sincronizado.
