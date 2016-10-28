Huayra-clonar
=============

> Grabá imáganes ISO booteables en Pen-drives o memorias SD, o cualquier dispositivo extraible.

***

Basado en ETCHER [**Download**](http://etcher.io) 

Licencia
--------

Huayra-clonar es software libre distribuido bajo licencia GPL [license](https://github.com/resin-io/etcher/blob/master/LICENSE).



*Instrucciones para Compilar y empaquetar en Huayra*

Para compilar correctamente la aplicación se deberan realizar los siguientes pasos:

1- exportar las siguientes variables:

export npm_config_target=1.4.4
export npm_config_arch=x64
export npm_config_target_arch=x64
export npm_config_disturl=https://atom.io/download/atom-shell
export npm_config_runtime=electron
export npm_config_build_from_source=true

2- ejecutar el comando:

npm install --save-dev electron-rebuild

3- ejecutar: 

$ ./node_modules/.bin/electron-rebuild
$ npm install
$ bower install

A esta altura la aplicación ya debería ejecutarse correctamente con el comando: $ electron .


4- ejecutamos el siguiente comando para eliminar las dependecias de desarrollo:

$ npm prune --production


 5- Listo!

*Empaquetado Debian*

El paquete deberá instalar los siguientes directorios y el archivo "package.json" en la ruta:

/usr/share/electron/resources/huayra-clonar

+ bower_components/
+ build/
+ lib/
+ node_modules/
+ package.json


La aplicación se ejecutará con el comando:

$ electron /usr/share/electron/resources/huayra-clonar
