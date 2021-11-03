# Mención especial a TypeScript

Como mención especial, decir que NodeJs tambien es compatible con TypeScript, por lo que podremos desarrollar nuestros proyectos de manera segura y tipada con typescript y luego correrlos en un entorno de nodejs como si de javascript se tratase.

!!! info
    TypeScript fue desarrollado por Microsoft en 2012. Typescript **NO** es un lenguaje de programacion en si mismo, si no que es un superset que añadido a JavaScript forma TypeScript. Por este motivo TypeScript necesita ser compilado en JavaScript para correr correctamente.

!!! info
    Algunos paquetes npm estan 100% pensados para JavaScript y no soportarán el tipado de typescript, pero una gran cantidad de paquetes si lo soportarán!

## Instalar TypeScript

Para instalar typescript de manera global en nuestro PC utilizaremos el comando</br>

    $ sudo npm typescript -g

## Crear un proyecto en NodeJs utilizando Ts

Primero crearemos nuestro proyecto de node con `npm init`</br>
Una vez tengamos el proyecto de node, inicializaremos nuestro proyecto</br>
de typescript con `tsc --init`

    $ npm init

    $ tsc --init

Esto nos creara el archivo de configuracion de typescript `tsconfig.json`</br>
En este archivo buscaremos en la linea 50 la propiedad `"outDir"` y la descomentaremos.</br>
Utilizaremos como directorio de salida por ejemplo el directorio /build, para ello:</br>
`"outDir": "./build"`</br>

Y configuraremos algunas cosas del `package.json`:</br>

```json

{
  "name": "ejemplo2",
  "version": "1.0.0",
  "description": "",
  "main": "build/index.js",
  "scripts": {
    "prestart": "tsc -b",
    "start": "node build/index.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}

```

De esta forma podremos programar nuestra aplicación utilizando typescript y cuando ejecutemos npm start se autocompilara.

Este seria el codigo en index.ts por ejemplo:</br>

```ts

let num:number;

for(num = 0 ; num < 10; num++ ){
    console.log(num);
}

```

Y esta seria la salida de consola al ejecutar `npm start`:
![ejemploTs](https://i.gyazo.com/4efe791eff370b2c349ed9f0e57855c7.png)
