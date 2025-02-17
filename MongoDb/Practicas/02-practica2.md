## Consultas 

1. Cargar el archivo empleaos.json

- En local:
    Comando:
      mongoimport --db curso --collection empleados --file empleados.json

- Docker:
    comando:
      mongoimport --port 80 --db curso --collection empleados --file empleados.json

2. Utilizar la base de datos Cursos

``` json
use curso
```

3. Buscar todos los empleados que trabajen en google
``` json
db.Empleados.find({ empresa: 'Google' } )
```
4. Empleados que vivan en peru
``` json
db.Empleados.find({ pais: 'Peru' } )
```
5. Empleados que ganen mas de 8000 dolares.
``` json
 db.Empleados.find(
... {
... salario: {$gt:8000}
... }
... )
```
6. Empleados con ventas inferiores a 10000.
``` json
db.Empleados.find( { ventas: { $lt: 10000 } } )
```
7. Realizar la consulta anterior pero devolviendo una sola fila.
``` json
 db.Empleados.findOne( { ventas: { $lt: 10000 } } )
 ```
8. Empleados que trabajan en Google o en yahoo con el operador $in
``` json
db.Empleados.find({ empresa: { $in: ['Google', 'Yahoo'] } } ) 
 ```
9. Empleado de amazon que ganen mas de 10,000 dolares
``` json
db.Empleados.find({
    $and:[{empresa:'Amazon'},
        {salario:{$gt:9000}}]
})
 ```
10. Empleados que trabajaen en yahoo que ganen mas de 6000 o empleados 
que trabajaen en google que tengan ventas inferiores a 20000
``` json
db.Empleados.find({ $or: 
[{ $and: [{ empresa: 'Yahoo' }, { salario: { $gt: 6000 } }] },
{ $and: [{ empresa: { $eq: 'Google' } }, { salario: { $lt: 20000 }}]}] 
} 
)
```
11. Visualizar el nombre apellido y el pais de cada empleado
``` json
 db.Empleados.find( {}, { _id: 0, nombre: 1, apellidos: 1, pais: 1 }) 
 ```