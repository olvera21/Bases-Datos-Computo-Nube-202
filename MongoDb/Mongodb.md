# CRUD y consultas en MongoDB

## Crear una base de datos
- Solo se crea si contiene por lo menos una colección
use bd1

## Cómo crear una colección
``` json
use bd1
db.createCollection("Empleado")
``` 

## Mostrar las colecciones
``` json
show collections
``` 

## Insertar un documento
```json
db.coleccion.insertOne(
    {
        nombre: 'Estefany',
        apellido1: 'Vazquez',
        edad: 22,
        ciudad: 'Huehuetoca'
    }
)
```

## Inserción de un documento más complejo con array
``` json
db.alumnos.insertOne(
 {
   nombre: "Martha",
   apellido: "Trinidad",
   apellido2: "Hernandez",
   edad: 19,
   aficiones: [
                 "Dibujo", "Videojuegos", "Musica"
              ]
 }
 )
 
```
 ## Inserción de documentos más complejos con documentos anidados
 ``` json
db.alumnos.insertOne(
 {
    nombre: "Naomi",
    apellido: "Mondragon",
    apellido2: "Martinez",
    edad: 20,
    estudios: [
      "Licenciatura en Derecho",
      "Licenciatura en Psicología",
      "Licenciatura en Logística"
    ],
       esperiencia: {
        lenguaje: "SQL", sbd: "SQL Server", AniosExp: 2
        }
 }
 )
```


``` json
db.alumnos.insertOne(
 {
    nombre: "Sorge",
    apellido: "Huaso",
    apellido2: "Villegas",
    edad: 23,
    aficiones: [
      "Dinero",
      "Hombres",
      "Fiesta"
    ],
       talenos: { 
        embriagarse: true,
        bañarse: false
        }
 }
 ) 
 ```

 # Practica1 

 ## Busquedas. Condiciones simples de Igualdad. Metodo Find()

``` json
db.libros.find({editorial:'Biblico'})
``` 

3. Mostrar Todos los documentos que el precio sea 25

4. Seleccionar todos los documentos donde el titulo sea json para todos

``` json
db.libros.find({titulo:'JSON para todos'})
``` 

## Operadores de comparacion

 [Operaciores de comparacion](https://www.mongodb.com/docs/manual/reference/operator/query/)

 [Operadores de comparacion](/IMG/Operadores-Mongo.png)

1. Mostrar todos los documentos donde el precio sea mayor 25

``` json
db.libros.find({ precio: { $gt: 25}})
``` 

2. Mostrar los documentos que sean iguales a 25
``` json
db.libros.find({ precio: { $eq: 25}})
``` 
3. Mostrar los documentos cuya cantidad sea menor a 5
``` json
db.libros.find({ cantidad: { $lt: 5}})
``` 

4. Mostrar los documentos que pertenezcan a la editorial Biblio o planeta
``` json
db1> db.libros.find({ editorial: {$in:['Biblio', 'Planeta']}})
``` 
5. Mostrar todos los documentos de libros que cuesten 20 o 25

``` json
db1> db.libros.find({ precio: {$in:[20, 25]}})
``` 

6. Mostrar todos los documentos de libros que no cuesten 20 0 25

``` json
db1> db.libros.find({ precio: {$nin:[20, 25]}})
``` 

7. Mostrar el primer documento de libros que cuesten 20 o 25

``` json
db1> db.libros.findOne(
... {precio:{$in:[20,25]}
... }
... )
{
  _id: 1,
  titulo: 'El aleph',
  autor: 'Borges',
  editorial: 'Planeta',
  precio: 20,
  cantidad: 50
}
``` 
[Operadores Logicos](https://www.mongodb.com/docs/manual/reference/operator/query/)

[Operadores de comparacion](/IMG/Operadores%20Logicos.png)

### Operador AND 

Dos posibles opciones de AND

1. La simple, mediante condiciones separadas por comas.

**Sintaxis**

dn.coleccion.find((condicion1, condicion2)) ->Con  esto asume que es un **AND**

2. Usando el operador $and

**sintaxis**
``` json
db.coleccion.find({$and: [{condicion1},{condicion2}]})
```
**EJERCICIOS**

1. Mostrar todos aquellos libros que cuesten mas de 25 y cuya cantidad se infrerior a 15

**Forma simple**

``` json
db1> db.libros.find( {precio: { $gt: 25 },  cantidad: { $lt: 15 }} )
```

2. Mostrar todos aquellos libros que cuestan mas de 25 cuya cantidad sea inferiror a 

``` json
db1> db.libros.find( {precio: { $gt: 25 },  cantidad: { $lt: 15 }, _id:4 })
```

**Operardor and**

1. Mostrar todos aquellos libros que cuesten mas de 25 y cuya cantidad se infrerior a 15
``` json

db1> db.libros.find(
... {$and:[{precio:{$gt:25}}, {cantidad:{$lt:15}}]})
[
  {
    _id: 2,
    titulo: 'Martin Fierro',
    autor: 'Jose Hernandez',
    editorial: 'Siglo XXI',
    precio: 50,
    cantidad: 12
  },
  {
    _id: 4,
    titulo: 'Java en 10 minutos',
    editorial: 'Siglo XXI',
    precio: 45,
    cantidad: 1
  }
]
``` 

## Mostrar todos aquellos que muestren mas de 25 cuya cantidad sea infrerior a 15 
``` json
  db1>  db.libros.find( { $or: [ { precio: { $gt: 25 } }, { cantidad:{$lt:15 } }] } )

```

## AND Y OR Conbinadas

1. Mostrar los libros de la editorial Biblio o Precio mayor a 40 o Libros de la editorial Planetas con precio mayor a 10.
``` json
db.libros.find(
  {
  $or:[
        { $and:[{editorial: 'Biblio'},{precio:{$gt:30}}]},
        { $and:[{editorial: {$eq: 'Planeta'}},{precio:{$gt:20}}]}
  ]
  }
)
``` 
## Modo simple
``` json
db.libros.find( 
      {
      $or: [ 
        {editorial:'Biblio',precio:{ $gt:30}},
        {editorial:{$eq:'Planeta'},precio:{$gt:20}}
      ]
    }
    )
``` 

*** Sintaxis ***
``` json
db.coleccion.find(filtro,columnas)

db.libros.find({},{titulo:1})

```
1. Seleccionar todos los documentos mostrando el titulo y la editorial
``` json
db.libros.find({},{titulo:1, editorial:1})
```
## Para quitar el Id.
``` json
db.libros.find({},{titulo:1, editorial:1,_id:0})
```

2. Seleccionar todos los documentos los documentos de la editorial Planeta mostrando el titulo y la editorial 
``` json
db.libros.find({editorial:'Planeta'},{_id:0, titulo:1, editorial:1})
```
## Insertamos un documento
 ``` json
db.libros.insertOne({
    _id: 10,
    titulo: 'Mongo en entornos graficos',
    editorial: 'Terra',
    precio: 125
})
```
## Operador exist(Permite saner si un campo se encuentra o no en un documento)
``` json
db.libros.find( { editorial: { exists: true } })
```
``` json

1. Mostrar todos los documentos que no contengan el campo cantidad

``` json
db.libros.find( { cantidad: { $exists: false }})

``` 

## Operador Type ( Permite preguntar si un determinado campo corresponde con un tipo )

[Operador Type](https://www.mongodb.com/docs/manual/reference/operator/query/type/#mongodb-query-op.-type )

2. Mostrar todos los documentos donde el precio sean dobles
``` json

 db.libros.find({precio:{$type:16}})

```
``` json
db.libros.inserOne(
  {
    _id:11,
    editorial: 'Terra',
    precio:125.4
    cantidad:20
  }
)

``` json

 db.libros.find({precio:{$type:1}}, {_id:0})

```

``` json

 db.libros.find({precio:{$type:1}}, {_id:0, cantidad:0})

```


``` json

db.libros.insertMany([
 {
    _id: 12,
    titulo: 'IA',
    editorial: 'Terra',
    precio: 125, 
	cantidad: 20
  },
  {
    _id: 13,
    titulo: 'Python para todos',
    editorial: 2001,
    precio: 200, 
	cantidad: 30
  }]
  )
```

1. Seleccionar los documentos donde la editorial sea de tipo entero
``` json
db1> db.libros.find({editorial:{$type:16}})
db1> db.libros.find({editorial:{$type:int}})
```

2. Seleccionar todos los documentos donde la editorial sea string

``` json
db1> db.libros.find({editorial:{$type:16}})
db1> db.libros.find({editorial:{$type:'string'}})
```

## Practica de consultas
1. Instalar las tools de mongosh
[DatabaseTools](https://www.mongodb.com/try/download/database-tools)



