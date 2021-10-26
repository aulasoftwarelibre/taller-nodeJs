# Todo lo que debes saber del archivo package.json

El archivo `package.json` nos servirá de gran ayuda en nuestro proyecto, nos permitirá crear scripts y controlar mucho mejor nuestro proyecto.

Al iniciar nuestro proyecto, nuestro package.json se verá algo parecido a esto:</br>
![ejemploPkgJson](https://i.gyazo.com/e03cf8cffc88eb20b673e4272f0d5caa.png)</br>

Un ejemplo de package.json más trabajado podria ser el siguiente.</br>
![ejemploPkgJsonDiscordJS](https://i.gyazo.com/b8cf2f20894377c428da0758260eb989.png)</br>

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

## Dependencias

Que las dependencias esten reflejadas en el package.json nos permitirá descargar un proyecto sin sus dependencias instaladas (sin tener la carpeta /node_modules) utilizando `npm install`, lo que nos dará una salida similar a esta:</br>
![EjemploSalidaNpmInstall](https://i.gyazo.com/acb1957894c3ebffb208fbc81715765a.png)

## Importancia de la licencias

Una licencia determinará que se puede y que no se puede hacer con tu codigo, por lo que es altamente recomendable utilizar una licencia que se ajuste a tus intenciones.
