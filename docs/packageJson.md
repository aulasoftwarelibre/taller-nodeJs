# Todo lo que debes saber del archivo package.json

El archivo `package.json` nos servirá de gran ayuda en nuestro proyecto, nos permitirá crear scripts y controlar mucho mejor nuestro proyecto.

Al iniciar nuestro proyecto, nuestro package.json se verá algo parecido a esto:</br>

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
  "license": "ISC"
}

```

Un ejemplo de package.json más trabajado podria ser el siguiente.</br>

```json
{
  "name": "leivaastdio",
  "version": "1.0.0",
  "description": "This is a bot developed for administrate a discord server. Made while learning about JS and some libraries. By Leivaa",
  "main": "src/index.js",
  "scripts": {
    "start": "pm2 flush LeivaaDiscordJS && pm2 start src/index.js --name LeivaaDiscordJS",
    "restart": "npm stop && npm start",
    "dev": "pm2 flush LeivaaDiscordJS && pm2 start src/index.js --name LeivaaDiscordJS --watch && npm run logs",
    "stop": "pm2 stop LeivaaDiscordJS && pm2 delete LeivaaDiscordJS",
    "logs": "pm2 logs --name LeivaDiscordJS",
    "status": "pm2 status --name LeivaDiscordJS",
    "list": "pm2 list"
  },
  "keywords": [],
  "author": "Leivaa21",
  "license": "MIT",
  "dependencies": {
    "discord.js": "^12.5.1",
    "emoji-regex": "^10.0.0",
    "esm": "^3.2.25",
    "fs": "0.0.1-security",
    "pm2": "^5.1.2",
    "replace-json-property": "^1.7.1"
  },
  "devDependencies": {
    "dotenv": "^8.2.0"
  }
}
```

Como podemos ver, el package.json será el archivo donde node guardará toda la información sobre nuestro proyecto, asi como sus dependencias, licencia, autor, scripts, etc...</br>

## Creacion de scripts en npm

Para crear un script con npm solo tendremos que añadirlo al package.json en la propiedad `"scripts"` con el formato </br>

`"Nombre": "comando a ejecutar"`</br>

Y para ejecutar el script utilizaremos:

    $ npm run Nombre

### npm start, stop & restart

Node reserva los scripts start, restart y stop por lo que podremos utilizarlos sin run, es decir</br>

    $ npm start

    $ npm stop

    $ npm restart

### Scripts pre y post

Además tambien podremos setear scripts que se ejecuten siempre antes o despues de un script en especifico de manera automatica. Para ello solo tendremos que seguir el formato:</br>

`"preNombre": "comando a ejecutar antes del script Nombre"`</br>
`"Nombre": "comando a ejecutar"`</br>
`"postNombre": "comando a ejecutar despues del script Nombre"`</br>

De esta forma, al ejecutar `npm run Nombre` se ejecutará preNombre, Nombre y postNombre en ese orden.

!!! info
    No es necesario crear un pre y post de cada script, de hecho podremos tener scripts con solo pre, con solo post, con ambos o con ninguno de los dos!

## Dependencias

Que las dependencias esten reflejadas en el package.json nos permitirá descargar un proyecto sin sus dependencias instaladas (sin tener la carpeta /node_modules) utilizando `npm install`, lo que nos dará una salida similar a esta:</br>
![EjemploSalidaNpmInstall](https://i.gyazo.com/acb1957894c3ebffb208fbc81715765a.png)

## Importancia de la licencias

Una licencia determinará que se puede y que no se puede hacer con tu codigo, por lo que es altamente recomendable utilizar una licencia que se ajuste a tus intenciones.
