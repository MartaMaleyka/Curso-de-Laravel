# Estructura de carpetas en laravel

La estructura de la aplicación en Laravel es básicamente la estructura de carpetas, subcarpetas y archivos incluidos en un proyecto. Una vez que creamos un proyecto en Laravel, obtenemos una descripción general de la estructura de la aplicación como se muestra en la imagen aquí.

La imagen que se muestra aquí se refiere a la carpeta raíz de Laravel, a saber, laravel-project . Incluye varias subcarpetas y archivos. El análisis de carpetas y archivos, junto con sus aspectos funcionales se detalla a continuación:
![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/estructura.jpg)

## Archivo .env
Es la definición de las variables de entorno. Podemos tener varios entornos donde vamos a mantener la ejecución de la aplicación con varias variables que tengan valores diferentes. Temas como si estamos trabajando con el debug activado, datos de conexión con la base de datos, servidores de envío de correo, caché, etc.
## Archivo composer.json
Que contiene información para Composer. Para conocer algo más de este fichero es mejor que te leas el Tutorial de Composer.<br>
Además en la raíz hay una serie de archivos que tienen que ver con Git, el readme, o del lado frontend el package.json o incluso un gulpfile.js que no vendria muy al caso comentar aquí porque no son cosas específicas de Laravel.
## Carpeta vendor
Laravel se basa completamente en las dependencias de Composer, por ejemplo, para instalar la configuración de Laravel o para incluir bibliotecas de terceros, etc. La carpeta Vendor incluye todas las dependencias del compositor.

Además de los archivos mencionados anteriormente, Laravel también incluye algunos otros archivos que juegan un papel principal en varias funcionalidades, como la configuración de GitHub, paquetes y bibliotecas de terceros.

Los archivos incluidos en la estructura de la aplicación se muestran a continuación:

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/vendor.jpg)
