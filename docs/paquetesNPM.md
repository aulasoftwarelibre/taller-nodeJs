# Paquetes NPM - Reutiliza los avances de la comunidad

NodeJS es una plataforma de bajo nivel, esto significa que funciona como soporte de otras herramientas, para hacer las cosas más sencillas existen librerias creadas por la comunidad.

Con npm tenemos acceso a más de 1,000,000 de librerias de codigo libre las cuales puedes utilizar.
Dentro de estos toda esta cantidad de librerias o paquetes, podremos distinguir infinidad de tipos:

## Paquetes enfocados en facilitar el desarrollo de aplicaciones

> * **nodemon** nos permitirá correr nuestra aplicacion de forma que cuando actualizemos un fichero
>   se reiniciará el programa para facilitarnos el desarrollo.
> * **pm2** funciona como un gestor de procesos que nos permitirá que nuestra aplicacion se reinicie
>   en cuanto suceda una excepcion, nos permitirá monitorear la aplicacion o correrla en segundo
>   plano
> * **dotenv** nos permitirá tener variables privadas en un fichero externo .env, esto nos servirá
>   por si tenemos variables que no queremos que se vea su contenido al subir el codigo a github
>   por ejemplo

## Paquetes enfocados en funcionalidades para tu aplicacion

> * **shelljs** nos permitirá programar scripts de bash en node
> * **fs** nos permitirá tratar con ficheros

## Paquetes orientados a hacer una aplicacion web más especifica - FrameWorks

!!! warning
    Una aplicacion web no tiene por que significar siempre pagina web.

!!! info
    Discord es una aplicacion web hecha en React por ejemplo! Esto es gracias a que node y sus frameworks pueden hacer que entornos web funcionen de forma interna en tu ordenador y no necesiten un buscador web!

### Frontend FrameWorks

> * **React.Js**
> * **Angular.Js**
> * **Vue.Js**

### Backend FrameWorks

> * **Express.js**
> * **Nest.js**
> * **Socket.io**

## Instalacion de paquetes NPM

Para instalar un paquete de npm tan solo tendremos que utilizar el comando </br>

    $ npm install nombre

Si queremos instalar un paquete de manera global en nuestro equipo utilizaremos </br>

    $ npm install nombre -g

Una vez instalemos algun paquete npm aparecerá una carpeta `./node_modules` en nuestro proyecto y se registrará el modulo utilizado en nuestro fichero `package.json`.</br>

## Utilizar un paquete NPM en nuestra aplicacion

Para este ejemplo utilizaremos el paquete `shelljs`</br>

Para instalarlo utilizaremos `npm install shelljs`</br>

![EjemploInstalacionPkg](https://i.gyazo.com/84ed833357ee4d7a05a49de4ddbffca4.png)</br>

De esta forma en nuestro fichero package.json quedará registrado nuestra dependencia</br>

    ```json
    {
        "name": "mynewapp",
        "version": "1.0.0",
        "description": "Esto es una descripcion",
        "main": "index.js",
        "scripts": {
          "test": "test \n"""
        },
        "keywords": [
          "ejemplo",
          "tallernodejs"
        ],
        "author": "leivaa21",
        "license": "ISC",
        "dependencies":{
            "shelljs": "^0.8.4"
        }
    }
    ```

Para el ejemplo tenemos este pequeño programa que creara una carpeta, la copiará y pondra dos mensajes por consola.</br>

    ```js
    const shelljs = require('shelljs')

    shelljs.echo("Creamos una carpeta de ejemplo y una copia de seguridad")
    shelljs.mkdir("../CarpetaDeEjemplo")
    shelljs.cp("-R", "../CarpetaDeEjemplo", "../CopiaDeSeguridad")
    shelljs.echo("He terminado")
    ```

Al ejecutar este codigo obtendremos esta salida por consola</br>

![EjemploSalida](https://i.gyazo.com/1716ef243573d796468a685b33f07fab.png)</br>

Y a su vez podremos ver que se han creado ambas carpetas</br>

![EjemploCarpetas](https://i.gyazo.com/935729559c9ccd6b6c6ff1b84e3533d9.png)</br>
