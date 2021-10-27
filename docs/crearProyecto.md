# Crear nuestro primer proyecto en NodeJs

## Inicializar un proyecto

Para iniciar nuestro proyecto de node utilizaremos la herramienta</br>

    $ npm init

Y nos comenzará a pedir informacion sobre nuestro proyecto, tales como nombre, licencia, version etc...</br>
Cada parametro tiene su valor por defecto el cual viene entre parentesis al lado del parametro, si no introducimos nada se seteará dicho valor. Si no tiene valor por defecto es un campo que podremos dejar vacio.</br>
![EjemploInitBasico](https://i.gyazo.com/d9318838a13d77b3136ef86b26c18288.png)

Otra opcion que tenemos será utilizar la opcion -y junto a npm init, lo que generará un package.json con los valores por defecto sin preguntar nada.</br>

    $ npm init -y

![EjemploInitY](https://i.gyazo.com/dfaa33807e8507defb58ecab3463cdd1.png)

## Ejemplo de aplicacion

Un ejemplo de una aplicación node podria ser el siguiente, donde se crea un servidor http.

```js

const http = require('http')

const hostname = '127.0.0.1'
const port = 3000

const server = http.createServer( (req, res ) => {
    res.statusCode = 200
    res.setHeader('Content-Type', 'text-plain')
    res.end('Este es mi primer servidor en node!\n')
})

server.listen( port, hostname, () => {
    console.log(`Server runnint at https://${hostname}:${port}/`)
})

```

Esta seria la salida que tendriamos en localhost.
![vista-servidor](https://i.gyazo.com/d3848a54b8294617b3a71993976d4e18.png)</br>
