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

* Para agregar un documento a una colección usando una variable `db.<collection>.insert(nombre_var)`

* Para agregar un solo documento a una colección usando una variable `db.<collection>.insertOne(nombre_var2)`

* Para insertar varios documentos a una colección usando un array de variables `db.<collection>.insertMany([a,b])`

* Para eliminar una colección `db.<collection>.drop()`

* `db.<collection>.find()` Imprime los primeros 20 documentos que encuentre.

* `db.<collection>.findOne()` Imprime solo el primer documentos que encuentre.

* `db.ticker.find({"last_updated" : "1506462510"})` Busqueda simple

* `db.ticker.find({"last_updated" : "1506462510" , "avaible_supply" : "16588625.0"})` Busqueda compuesta

* `db.ticker.find({"last_updated" : "1506462510" , "avaible_supply" : "16588625.0"}).pretty()` Formato más legible

* `db.ticker.findOne({"last_updated" : "1506462510"})` findOne directamente es más legible

* `db.ticker.find({"last_updated" : "1506462510"}).limit(1).pretty()` De esta forma limitamos el find a un solo documento

* `db.ticker.find({"last_updated" : {$gt: "1506462510"}}).pretty()` Mayor que

* `db.ticker.find({"last_updated" : {$lt: "1506462511"}}).pretty()` Menor que

* `db.ticker.find({"last_updated" : {$lte: "1506462511"}}).pretty()` Menor o igual

* `db.ticker.find({"last_updated" : {$gte: "1506462510"}}).limit(3).pretty()` Mayor o igual

* `db.ticker.find({"last_updated" : {$gte: "1506462510"}},{id: 0,price_btc : 0, rank: 0}).limit(2).pretty()` Marcamos en 0 id para que no se muestre igual con price_btc y rank
