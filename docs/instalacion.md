# Instalación de Node y NPM

## Instalación

!!! warning
    Cada distribución de linux es un mundo, aqui solo veremos como instalarlo en un equipo con el gestor de paquetes apt o con el gestor de paquetes pacman, aunque será muy similar la instalación en cualquier equipo linux.

Para instalar nodeJs en linux, podremos instalarlo mediante apt o pacman sin problemas.

En Ubuntu o cualquier distro con apt utilizaremos:</br>

    $ sudo apt install nodejs

    $ sudo apt install npm

En Arch utilizaremos el mismo comando pero utilizando pacman:</br>

    $ sudo pacman -S nodejs

    $ sudo pacman -S npm

Para comprobar la version que tenemos de node o npm podremos utilizar los comandos:</br>

    $ node -v

    $ node --version

    $ npm -v

    $ npm --version

## Desinstalación

Para desinstalar node y npm solo tendremos que utlizar el siguiente comando:</br>

    $ sudo apt-get remove nodejs

    $ sudo pacman -R nodejs

## Controla que version exacta usas con NVM

Si quisieramos poder cambiar la version de node en cualquier momento deberemos de utilizar la herramienta nvm

Para instalar nvm necesitaremos previamente wget</br>
Podemos comprobar si tenemos wget instalado simplemente escribiendo `wget` en la consola.</br>
En caso de no tener wget, se instalará con:

    $ sudo apt install wget

    $ sudo pacman -S wget

Para instalar nvm utilizaremos:</br>

    $ wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash

    $ source ~/.profile

Para saber las versiones de node disponibles utilizaremos:</br>

    $ nvm ls-remote

Para instalar una version en especifico utilizaremos:</br>

    $ nvm install ${numeroVersion}

Para desinstalar node en caso que quisieramos primero tendremos que desactivar nvm con:</br>

    $ nvm deactivate

Y desinstalar las versiones de node que utilizemos con:</br>

    $ nvm uninstall ${numeroVersion}
