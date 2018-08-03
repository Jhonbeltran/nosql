#Commands

## MongoDB

> API del curso: https://api.coinmarketcap.com/v2/ticker/

* `sudo service mongod start`: Iniciar el daemon
* `mongo 192.168.0.5:9999`: Conectarnos a la consola interactiva `mongo` si estamos en  local
* `show dbs`: Ver las bases de datos que tenemos
*  crear una base de datos:
      - `use <nombre db>`: Situarnos donde se va a crear la base de datos
      - `db.curso.insert({"name" : "Jhon"})`: Crear una coleccion con un contenido especifico
      - `db.createCollection("curso1")`: Crear una collecion directamente
      - `show collections`  ver las colecciones
