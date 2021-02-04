[<<<<-----Regresar al indice](https://martamaleyka.github.io/Curso-de-Laravel/index) 

# Estructura de carpetas en laravel

La estructura de la aplicación en Laravel es básicamente la estructura de carpetas, subcarpetas y archivos incluidos en un proyecto. Una vez que creamos un proyecto en Laravel, obtenemos una descripción general de la estructura de la aplicación como se muestra en la imagen aquí.

La imagen que se muestra aquí se refiere a la carpeta raíz de Laravel, a saber, laravel-project . Incluye varias subcarpetas y archivos. El análisis de carpetas y archivos, junto con sus aspectos funcionales se detalla a continuación:

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/esructura.jpg)


## Archivo .env
Es la definición de las variables de entorno. Podemos tener varios entornos donde vamos a mantener la ejecución de la aplicación con varias variables que tengan valores diferentes. Temas como si estamos trabajando con el debug activado, datos de conexión con la base de datos, servidores de envío de correo, caché, etc.

## Archivo composer.json
Que contiene información para Composer. Para conocer algo más de este fichero es mejor que te leas el Tutorial de Composer.<br>
Además en la raíz hay una serie de archivos que tienen que ver con Git, el readme, o del lado frontend el package.json o incluso un gulpfile.js que no vendria muy al caso comentar aquí porque no son cosas específicas de Laravel.

## Carpeta app
Es la carpeta de la aplicación e incluye todo el código fuente del proyecto. Contiene eventos, excepciones y declaración de middleware. La carpeta de la aplicación comprende varias subcarpetas como se explica a continuación:

**Carpeta console**

La consola incluye los comandos artesanales necesarios para Laravel. Incluye un directorio llamado Commands , donde todos los comandos se declaran con la firma adecuada. El archivo Kernel.php llama a los comandos declarados en Inspire.php .

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/console.jpg)

Si necesitamos llamar a un comando específico en Laravel, entonces deberíamos hacer los cambios apropiados en este directorio.

**Carpeta events**

Esta carpeta incluye todos los eventos del proyecto.

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/events.jpg)

Los eventos se utilizan para desencadenar actividades, generar errores o validaciones necesarias y proporcionar una mayor flexibilidad. Laravel mantiene todos los eventos en un directorio. El archivo predeterminado incluido es event.php donde se declaran todos los eventos básicos.

**Carpeta Excepciones**

Esta carpeta contiene todos los métodos necesarios para manejar excepciones. También contiene el archivo handle.php que maneja todas las excepciones.

**Carpeta Http**

La carpeta Http tiene subcarpetas para controladores, middleware y solicitudes de aplicaciones. Como Laravel sigue el patrón de diseño MVC, esta carpeta incluye el modelo, los controladores y las vistas definidas para los directorios específicos.

La subcarpeta **Middleware** incluye un mecanismo de middleware, que comprende el mecanismo de filtro y la comunicación entre la respuesta y la solicitud.

La subcarpeta **Requests** incluye todas las solicitudes de la aplicación.

**Carpeta Jobs**

El directorio jobs mantiene las actividades en cola para la aplicación Laravel. La clase base se comparte entre todos los trabajos y proporciona una ubicación central para colocarlos bajo un mismo techo.

**Carpeta Listeners**

Los listeners dependen de los eventos e incluyen métodos que se utilizan para manejar eventos y excepciones. Por ejemplo, el evento de inicio de sesión declarado incluye un evento LoginListener .

**Carpeta policies**

Las políticas son las clases de PHP que incluyen la lógica de autorización. Laravel incluye una función para crear toda la lógica de autorización dentro de las clases de políticas dentro de esta subcarpeta.

**Carpeta providers**

Esta carpeta incluye todos los proveedores de servicios necesarios para registrar eventos para servidores centrales y configurar una aplicación Laravel.

## Carpeta bootstrap
Esta carpeta incluye todos los scripts de arranque de la aplicación. Contiene una subcarpeta llamada caché , que incluye todos los archivos asociados para almacenar en caché una aplicación web. También puede encontrar el archivo app.php , que inicializa los scripts necesarios para bootstrap.

## Carpeta Config
La carpeta de configuración incluye varias configuraciones y parámetros asociados necesarios para el buen funcionamiento de una aplicación Laravel. Varios archivos incluidos dentro de la carpeta de configuración se muestran en la imagen aquí. Los nombres de archivo funcionan según la funcionalidad asociada a ellos.

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/configfolder.jpg)

## Carpeta database

Como sugiere su nombre, este directorio incluye varios parámetros para las funcionalidades de la base de datos. Incluye tres subdirectorios como se indica a continuación:

- Seeders : contiene las clases utilizadas para las pruebas unitarias.

- Migrations : esta carpeta ayuda en las consultas para migrar la base de datos utilizada en la aplicación web.

- Factories : esta carpeta se utiliza para generar una gran cantidad de registros de datos.

## Carpeta Public
Es la carpeta raíz que ayuda a inicializar la aplicación Laravel. Incluye los siguientes archivos y carpetas:

- .htaccess : este archivo proporciona la configuración del servidor.

- javascript y css : estos archivos se consideran activos.

- index.php : este archivo es necesario para la inicialización de una aplicación web.

## Carpeta Resources
El directorio de recursos contiene los archivos que mejoran su aplicación web. Las subcarpetas incluidas en este directorio y su propósito se explican a continuación:

- assets : la carpeta de assets incluye archivos como LESS y SCSS, que son necesarios para diseñar la aplicación web.

- lang : esta carpeta incluye la configuración para la localización o internalización.

- views : las vistas son archivos HTML o plantillas que interactúan con los usuarios finales y desempeñan un papel principal en la arquitectura MVC.

Observe que el directorio de recursos se acoplará en lugar de tener una carpeta de assets. La representación del mismo se muestra a continuación:

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/resource.jpg)

## Carpeta Storage
Esta es la carpeta que almacena todos los registros y archivos necesarios que se necesitan con frecuencia cuando se ejecuta un proyecto de Laravel. Las subcarpetas incluidas en este directorio y su propósito se detallan a continuación:

- app : esta carpeta contiene los archivos que se llaman en sucesión.

- framework : contiene sesiones, caché y vistas a las que se llama con frecuencia.

- logs : todas las excepciones y los registros de errores se rastrean en esta subcarpeta.

## Carpeta tests
Todos los casos de prueba unitaria están incluidos en este directorio. La convención de nomenclatura para nombrar las clases de casos de prueba es camel_case y sigue la convención según la funcionalidad de la clase.

## Carpeta vendor
Laravel se basa completamente en las dependencias de Composer, por ejemplo, para instalar la configuración de Laravel o para incluir bibliotecas de terceros, etc. La carpeta Vendor incluye todas las dependencias del compositor.

Además de los archivos mencionados anteriormente, Laravel también incluye algunos otros archivos que juegan un papel principal en varias funcionalidades, como la configuración de GitHub, paquetes y bibliotecas de terceros.

Los archivos incluidos en la estructura de la aplicación se muestran a continuación:

![Image](https://martamaleyka.github.io/Curso-de-Laravel/Imagenes/vendor.jpg)

[<<<<-----Regresar al indice](https://martamaleyka.github.io/Curso-de-Laravel/index) 
