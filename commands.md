#Commands

## MongoDB

> API del curso: https://api.coinmarketcap.com/v2/ticker/

* `sudo service mongod start`: Iniciar el daemon
* `mongo 192.168.0.5:9999`: Conectarnos a la consola interactiva `mongo` si estamos en  local
* `show dbs`: Ver las bases de datos que tenemos
*  Crear una base de datos:
      - `use <nombre db>`: Situarnos donde se va a crear la base de datos
      - `db.curso.insert({"name" : "Jhon"})`: Crear una coleccion con un contenido especifico
      - `db.createCollection("curso1")`: Crear una collecion directamente
      - `show collections`  ver las colecciones

En mongo tambien podemos usar javascript modificado para tratamiento de datos. Los cuales pueden ser usados directamente desde la terminal de mongo o ser cargados usando la funcion load() ej: `load("scripts/functions.js")`

* Podemos crear un documento usando: `nombre_var = {"_id": 1, "name": "Bitcoin",}`

* Para agregar un documento a una colección usando una variable `db.ticket.insert(nombre_var)`

* Para agregar un solo documento a una colección usando una variable `db.ticket.insertOne(nombre_var2)`

* Para insertar varios documentos a una colección usando un array de variables `db.ticker.insertMany([a,b])`
