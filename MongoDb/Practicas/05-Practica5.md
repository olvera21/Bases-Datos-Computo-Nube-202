# Agregaciones

1. Para hacer esta práctica vamos a cargar unos datos ficticios de empresas.
2. Tienes un fichero denominado “productos.json”
3. Debes poner el resultado de las consultas en cada apartado

- Cuenta los productos de tipo “medio”, usando un método básico

```json
db.products.find({ tipo: "medio" }).count()
```
```json
25
```
```json
{
  _id: ObjectId('67da3b9c9d62f731cac95a4d'),
  codigo: 1,
  nombre: 'Rustic Concrete Pants',
  unidades: 66,
  precio: 279,
  fabricante: 'Mercury General',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a4e'),
  codigo: 2,
  nombre: 'Small Soft Fish',
  unidades: 96,
  precio: 189,
  fabricante: 'Primoris Services',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a50'),
  codigo: 4,
  nombre: 'Ergonomic Metal Ball',
  unidades: 5,
  precio: 246,
  fabricante: 'Seaboard',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a53'),
  codigo: 7,
  nombre: 'Handmade Steel Chair',
  unidades: 16,
  precio: 337,
  fabricante: 'CIT Group',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a56'),
  codigo: 10,
  nombre: 'Handmade Plastic Hat',
  unidades: 7,
  precio: 253,
  fabricante: "Dick's Sporting Goods",
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a5a'),
  codigo: 14,
  nombre: 'Small Concrete Fish',
  unidades: 40,
  precio: 126,
  fabricante: 'Precision Castparts',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a5f'),
  codigo: 19,
  nombre: 'Handcrafted Steel Chicken',
  unidades: 55,
  precio: 113,
  fabricante: 'State Street Corp.',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a63'),
  codigo: 23,
  nombre: 'Handcrafted Metal Tuna',
  unidades: 63,
  precio: 320,
  fabricante: 'Williams-Sonoma',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a66'),
  codigo: 26,
  nombre: 'Intelligent Plastic Bike',
  unidades: 39,
  precio: 241,
  fabricante: 'Tractor Supply',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a68'),
  codigo: 28,
  nombre: 'Handcrafted Granite Cheese',
  unidades: 27,
  precio: 304,
  fabricante: 'Lennar',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a69'),
  codigo: 29,
  nombre: 'Unbranded Soft Computer',
  unidades: 33,
  precio: 69,
  fabricante: 'Delta Tucker Holdings',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a6b'),
  codigo: 31,
  nombre: 'Generic Fresh Keyboard',
  unidades: 69,
  precio: 16,
  fabricante: 'WestRock',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a6c'),
  codigo: 32,
  nombre: 'Sleek Soft Towels',
  unidades: 68,
  precio: 68,
  fabricante: 'Alere',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a6e'),
  codigo: 34,
  nombre: 'Practical Cotton Keyboard',
  unidades: 43,
  precio: 25,
  fabricante: 'AutoNation',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a70'),
  codigo: 36,
  nombre: 'Rustic Soft Table',
  unidades: 73,
  precio: 331,
  fabricante: 'Werner Enterprises',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a73'),
  codigo: 39,
  nombre: 'Handmade Soft Chips',
  unidades: 56,
  precio: 208,
  fabricante: 'State Farm Insurance Cos.',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a74'),
  codigo: 40,
  nombre: 'Handmade Frozen Salad',
  unidades: 13,
  precio: 85,
  fabricante: 'Nordstrom',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a76'),
  codigo: 42,
  nombre: 'Licensed Granite Ball',
  unidades: 74,
  precio: 92,
  fabricante: 'SunPower',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a7b'),
  codigo: 47,
  nombre: 'Practical Frozen Chips',
  unidades: 0,
  precio: 305,
  fabricante: 'Delta Air Lines',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a7e'),
  codigo: 50,
  nombre: 'Awesome Frozen Shoes',
  unidades: 33,
  precio: 125,
  fabricante: 'Comerica',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a81'),
  codigo: 53,
  nombre: 'Licensed Plastic Hat',
  unidades: 96,
  precio: 38,
  fabricante: 'Best Buy',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a82'),
  codigo: 54,
  nombre: 'Generic Metal Sausages',
  unidades: 84,
  precio: 77,
  fabricante: 'DST Systems',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a83'),
  codigo: 55,
  nombre: 'Small Metal Tuna',
  unidades: 46,
  precio: 43,
  fabricante: 'Raymond James Financial',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a87'),
  codigo: 59,
  nombre: 'Handcrafted Granite Chicken',
  unidades: 26,
  precio: 164,
  fabricante: 'Comcast',
  tipo: 'medio'
}
{
  _id: ObjectId('67da3b9c9d62f731cac95a8e'),
  codigo: 66,
  nombre: 'Incredible Concrete Fish',
  unidades: 96,
  precio: 336,
  fabricante: 'Darling Ingredients',
  tipo: 'medio'
}
```
- Indicar con un distinct, las empresas (fabricantes) que hay en la colección
```json
db.Productos.distinct("fabricante")
```

```json
[
  'A.O. Smith',
  'Alere',
  'American Tire Distributors Holdings',
  'Anthem',
  'Archrock',
  'Ascena Retail Group',
  'AutoNation',
  'Best Buy',
  'CIT Group',
  'Cabot',
  'Comcast',
  'Comerica',
  'Core-Mark Holding',
  'DST Systems',
  'Darling Ingredients',
  'Delta Air Lines',
  'Delta Tucker Holdings',
  "Dick's Sporting Goods",
  'First Solar',
  'HCA Holdings',
  'Hanesbrands',
  'Hartford Financial Services Group',
  'Hawaiian Holdings',
  'HealthSouth',
  'Hyatt Hotels',
  'Kar Auction Services',
  'Kelly Services',
  'Kemper',
  'Kimberly-Clark',
  'Lennar',
  'Mercury General',
  'Mondelez International',
  'Motorola Solutions',
  'Nasdaq OMX Group',
  'National Oilwell Varco',
  'Nordstrom',
  'OneMain Holdings',
  'Oneok',
  'Orbital ATK',
  'Pep Boys-Mann',
  'Pool',
  'Precision Castparts',
  'Primoris Services',
  'Raymond James Financial',
  'Seaboard',
  'Securian Financial Group',
  'Simon Property Group',
  'State Farm Insurance Cos.',
  'State Street Corp.',
  'SunPower',
  'TEGNA',
  'Telephone & Data Systems',
  'Total System Services',
  'Tractor Supply',
  'TransDigm Group',
  'Trinity Industries',
  'TrueBlue',
  'Universal American',
  'Universal Health Services',
  'WGL Holdings',
  "Wendy's",
  'Werner Enterprises',
  'WestRock',
  'Williams-Sonoma'
]
```
- Usando aggregate, visualizar los productos que tengan más de 80 unidades
```json
db.Productos.aggregate([
  { $match: { unidades: { $gt: 80 } } },
  { $project: { 
      _id: 0,
      codigo: 1, 
      nombre: 1, 
      unidades: 1, 
      fabricante: 1 
  }}
])
```
```json
{
  codigo: 0,
  nombre: 'Fantastic Wooden Fish',
  unidades: 95,
  fabricante: 'Kimberly-Clark'
}
{
  codigo: 2,
  nombre: 'Small Soft Fish',
  unidades: 96,
  fabricante: 'Primoris Services'
}
{
  codigo: 12,
  nombre: 'Refined Concrete Salad',
  unidades: 90,
  fabricante: 'Universal Health Services'
}
{
  codigo: 30,
  nombre: 'Small Rubber Pants',
  unidades: 89,
  fabricante: 'Hanesbrands'
}
{
  codigo: 33,
  nombre: 'Generic Concrete Hat',
  unidades: 82,
  fabricante: 'American Tire Distributors Holdings'
}
{
  codigo: 53,
  nombre: 'Licensed Plastic Hat',
  unidades: 96,
  fabricante: 'Best Buy'
}
{
  codigo: 54,
  nombre: 'Generic Metal Sausages',
  unidades: 84,
  fabricante: 'DST Systems'
}
{
  codigo: 61,
  nombre: 'Sleek Rubber Keyboard',
  unidades: 82,
  fabricante: 'Alere'
}
{
  codigo: 61,
  nombre: 'Sleek Rubber Keyboard',
  unidades: 82,
  fabricante: 'Alere'
}
```
- Con $project visualizar solo el nombre, unidades y precio de los productos que tengan menos de 10 unidades
``` JSON
db.products.aggregate([
  { $match: { unidades: { $lt: 10 } } },
  { $project: { 
      _id: 0,
      nombre: 1, 
      unidades: 1, 
      precio: 1 
  }}
])
```
``` JSON
{
  nombre: 'Ergonomic Metal Ball',
  unidades: 5,
  precio: 246
}
{
  nombre: 'Handmade Plastic Hat',
  unidades: 7,
  precio: 253
}
{
  nombre: 'Ergonomic Metal Table',
  unidades: 0,
  precio: 94
}
{
  nombre: 'Practical Frozen Chips',
  unidades: 0,
  precio: 305
}
{
  nombre: 'Fantastic Metal Pants',
  unidades: 5,
  precio: 129
}
{
  nombre: 'Intelligent Frozen Sausages',
  unidades: 3,
  precio: 111
}
{
  nombre: 'Rustic Plastic Mouse',
  unidades: 5,
  precio: 24
}
``` 
```JSON
db.Productos.aggregate([
  { $match: { unidades: { $lt: 10 } } },
  { $project: { 
      _id: 0,
      nombre: 1, 
      unidades: 1, 
      precio: 1,
      empresa: "$fabricante"
  }}
])
```
```JSON
[
  {
    nombre: 'Ergonomic Metal Ball',
    unidades: 5,
    precio: 246,
    empresa: 'Seaboard'
  },
  {
    nombre: 'Handmade Plastic Hat',
    unidades: 7,
    precio: 253,
    empresa: "Dick's Sporting Goods"
  },
  {
    nombre: 'Ergonomic Metal Table',
    unidades: 0,
    precio: 94,
    empresa: 'Kelly Services'
  },
  {
    nombre: 'Practical Frozen Chips',
    unidades: 0,
    precio: 305,
    empresa: 'Delta Air Lines'
  },
  {
    nombre: 'Fantastic Metal Pants',
    unidades: 5,
    precio: 129,
    empresa: 'OneMain Holdings'
  },
  {
    nombre: 'Intelligent Frozen Sausages',
    unidades: 3,
    precio: 111,
    empresa: 'A.O. Smith'
  },
  {
    nombre: 'Rustic Plastic Mouse',
    unidades: 5,
    precio: 24,
    empresa: 'Orbital ATK'
  }
]
```
- Añadir a la consulta anterior un campo calculado que se llame total y que multiplique precio por unidades.
```JSON
db.Productos.aggregate([
  { $match: { unidades: { $lt: 10 } } },
  { $project: { 
      _id: 0,
      nombre: 1, 
      unidades: 1, 
      precio: 1,
      empresa: "$fabricante",
      total: { $multiply: ["$precio", "$unidades"] }
  }}
])
```

```json
{
  nombre: 'Ergonomic Metal Ball',
  unidades: 5,
  precio: 246,
  empresa: 'Seaboard',
  total: 1230
}
{
  nombre: 'Handmade Plastic Hat',
  unidades: 7,
  precio: 253,
  empresa: "Dick's Sporting Goods",
  total: 1771
}
{
  nombre: 'Ergonomic Metal Table',
  unidades: 0,
  precio: 94,
  empresa: 'Kelly Services',
  total: 0
}
{
  nombre: 'Practical Frozen Chips',
  unidades: 0,
  precio: 305,
  empresa: 'Delta Air Lines',
  total: 0
}
{
  nombre: 'Fantastic Metal Pants',
  unidades: 5,
  precio: 129,
  empresa: 'OneMain Holdings',
  total: 645
}
{
  nombre: 'Intelligent Frozen Sausages',
  unidades: 3,
  precio: 111,
  empresa: 'A.O. Smith',
  total: 333
}
{
  nombre: 'Rustic Plastic Mouse',
  unidades: 5,
  precio: 24,
  empresa: 'Orbital ATK',
  total: 120
}
```
- Hacer que el nombre salga en mayúsculas con el operador $toUpper
```JSON
db.Productos.aggregate([
  { $match: { unidades: { $lt: 10 } } },
  { $project: { 
      _id: 0,
      nombre: { $toUpper: "$nombre" }, 
      unidades: 1, 
      precio: 1,
      empresa: "$fabricante",
      total: { $multiply: ["$precio", "$unidades"] }
  }}
])
```
```json
[
  {
    unidades: 5,
    precio: 246,
    nombre: 'ERGONOMIC METAL BALL',
    empresa: 'Seaboard',
    total: 1230
  },
  {
    unidades: 7,
    precio: 253,
    nombre: 'HANDMADE PLASTIC HAT',
    empresa: "Dick's Sporting Goods",
    total: 1771
  },
  {
    unidades: 0,
    precio: 94,
    nombre: 'ERGONOMIC METAL TABLE',
    empresa: 'Kelly Services',
    total: 0
  },
  {
    unidades: 0,
    precio: 305,
    nombre: 'PRACTICAL FROZEN CHIPS',
    empresa: 'Delta Air Lines',
    total: 0
  },
  {
    unidades: 5,
    precio: 129,
    nombre: 'FANTASTIC METAL PANTS',
    empresa: 'OneMain Holdings',
    total: 645
  },
  {
    unidades: 3,
    precio: 111,
    nombre: 'INTELLIGENT FROZEN SAUSAGES',
    empresa: 'A.O. Smith',
    total: 333
  },
  {
    unidades: 5,
    precio: 24,
    nombre: 'RUSTIC PLASTIC MOUSE',
    empresa: 'Orbital ATK',
    total: 120
  }
]
```
- Añadir un campo calculado que ponga el nombre del producto y el tipo concatenado con el operador $concat. Le llamamos al campo “completo”
```JSON
db.Productos.aggregate([
  { $match: { unidades: { $lt: 10 } } },
  { $project: { 
      _id: 0,
      nombre: { $toUpper: "$nombre" }, 
      unidades: 1, 
      precio: 1,
      empresa: "$fabricante",
      total: { $multiply: ["$precio", "$unidades"] },
      completo: { $concat: ["$nombre", " - ", "$tipo"] }
  }}
])
```
```JSON
{
  unidades: 5,
  precio: 246,
  nombre: 'ERGONOMIC METAL BALL',
  empresa: 'Seaboard',
  total: 1230,
  completo: 'Ergonomic Metal Ball - medio'
}
{
  unidades: 7,
  precio: 253,
  nombre: 'HANDMADE PLASTIC HAT',
  empresa: "Dick's Sporting Goods",
  total: 1771,
  completo: 'Handmade Plastic Hat - medio'
}
{
  unidades: 0,
  precio: 94,
  nombre: 'ERGONOMIC METAL TABLE',
  empresa: 'Kelly Services',
  total: 0,
  completo: 'Ergonomic Metal Table - avanzado'
}
{
  unidades: 0,
  precio: 305,
  nombre: 'PRACTICAL FROZEN CHIPS',
  empresa: 'Delta Air Lines',
  total: 0,
  completo: 'Practical Frozen Chips - medio'
}
{
  unidades: 5,
  precio: 129,
  nombre: 'FANTASTIC METAL PANTS',
  empresa: 'OneMain Holdings',
  total: 645,
  completo: 'Fantastic Metal Pants - basico'
}
{
  unidades: 3,
  precio: 111,
  nombre: 'INTELLIGENT FROZEN SAUSAGES',
  empresa: 'A.O. Smith',
  total: 333,
  completo: 'Intelligent Frozen Sausages - basico'
}
{
  unidades: 5,
  precio: 24,
  nombre: 'RUSTIC PLASTIC MOUSE',
  empresa: 'Orbital ATK',
  total: 120,
  completo: 'Rustic Plastic Mouse - avanzado'
}
```
- Ordena el resultado por el campo “total”
```JSON
db.Productos.aggregate([
  { $match: { unidades: { $lt: 10 } } },
  { $project: { 
      _id: 0,
      nombre: { $toUpper: "$nombre" }, 
      unidades: 1, 
      precio: 1,
      empresa: "$fabricante",
      total: { $multiply: ["$precio", "$unidades"] },
      completo: { $concat: ["$nombre", " - ", "$tipo"] }
  }},
  { $sort: { total: -1 } }
])
```
```JSON
[
  {
    unidades: 7,
    precio: 253,
    nombre: 'HANDMADE PLASTIC HAT',
    empresa: "Dick's Sporting Goods",
    total: 1771,
    completo: 'Handmade Plastic Hat - medio'
  },
  {
    unidades: 5,
    precio: 246,
    nombre: 'ERGONOMIC METAL BALL',
    empresa: 'Seaboard',
    total: 1230,
    completo: 'Ergonomic Metal Ball - medio'
  },
  {
    unidades: 5,
    precio: 129,
    nombre: 'FANTASTIC METAL PANTS',
    empresa: 'OneMain Holdings',
    total: 645,
    completo: 'Fantastic Metal Pants - basico'
  },
  {
    unidades: 3,
    precio: 111,
    nombre: 'INTELLIGENT FROZEN SAUSAGES',
    empresa: 'A.O. Smith',
    total: 333,
    completo: 'Intelligent Frozen Sausages - basico'
  },
  {
    unidades: 5,
    precio: 24,
    nombre: 'RUSTIC PLASTIC MOUSE',
    empresa: 'Orbital ATK',
    total: 120,
    completo: 'Rustic Plastic Mouse - avanzado'
  },
  {
    unidades: 0,
    precio: 94,
    nombre: 'ERGONOMIC METAL TABLE',
    empresa: 'Kelly Services',
    total: 0,
    completo: 'Ergonomic Metal Table - avanzado'
  },
  {
    unidades: 0,
    precio: 305,
    nombre: 'PRACTICAL FROZEN CHIPS',
    empresa: 'Delta Air Lines',
    total: 0,
    completo: 'Practical Frozen Chips - medio'
  }
]
```
- Haciendo una nueva consulta, averiguar el numero de productos por tipo de producto
```JSON
db.Productos.aggregate([
  { $group: { 
      _id: "$tipo", 
      cantidad: { $sum: 1 } 
  }},
  { $project: {
      _id: 0,
      tipo: "$_id",
      cantidad: 1
  }},
  { $sort: { tipo: 1 } }
])
```
```JSON
{
  cantidad: 18,
  tipo: 'avanzado'
}
{
  cantidad: 24,
  tipo: 'basico'
}
{
  cantidad: 25,
  tipo: 'medio'
}
```
- Añadir el valor mayor y el menor
```JSON
db.Productos.aggregate([
  { $group: { 
      _id: "$tipo", 
      cantidad: { $sum: 1 },
      precio_minimo: { $min: "$precio" },
      precio_maximo: { $max: "$precio" }
  }},
  { $project: {
      _id: 0,
      tipo: "$_id",
      cantidad: 1,
      precio_minimo: 1,
      precio_maximo: 1
  }},
  { $sort: { tipo: 1 } }
])
```
```JSON
{
  cantidad: 18,
  precio_minimo: 18,
  precio_maximo: 331,
  tipo: 'avanzado'
}
{
  cantidad: 24,
  precio_minimo: 16,
  precio_maximo: 285,
  tipo: 'basico'
}
{
  cantidad: 25,
  precio_minimo: 16,
  precio_maximo: 337,
  tipo: 'medio'
}
```
- Añade el total de unidades por cada tipo
```JSON
db.Productos.aggregate([
  { $group: { 
      _id: "$tipo", 
      cantidad_productos: { $sum: 1 },
      total_unidades: { $sum: "$unidades" },
      precio_minimo: { $min: "$precio" },
      precio_maximo: { $max: "$precio" }
  }},
  { $project: {
      _id: 0,
      tipo: "$_id",
      cantidad_productos: 1,
      total_unidades: 1,
      precio_minimo: 1,
      precio_maximo: 1
  }},
  { $sort: { tipo: 1 } }
])
```
```JSON
{
  cantidad_productos: 18,
  total_unidades: 773,
  precio_minimo: 18,
  precio_maximo: 331,
  tipo: 'avanzado'
}
{
  cantidad_productos: 24,
  total_unidades: 1067,
  precio_minimo: 16,
  precio_maximo: 285,
  tipo: 'basico'
}
{
  cantidad_productos: 25,
  total_unidades: 1224,
  precio_minimo: 16,
  precio_maximo: 337,
  tipo: 'medio'
}
```
- Con el operador $set y el operador “$substr” visualiza todos los datos del producto "Small Metal Tuna" y los primeros 5 caracteres del nombre.
```JSON
db.Productos.aggregate([
  { $match: { nombre: "Small Metal Tuna" } },
  { $set: { 
      primeros_caracteres: { $substr: ["$nombre", 0, 5] }
  }}
])
```
```JSON
{
  _id: ObjectId('67da3b9c9d62f731cac95a83'),
  codigo: 55,
  nombre: 'Small Metal Tuna',
  unidades: 46,
  precio: 43,
  fabricante: 'Raymond James Financial',
  tipo: 'medio',
  primeros_caracteres: 'Small'
}
```
- Creamos una salida que tenga el nombre del articulo y el total (precio por unidades) y lo guardamos en una colección denominada productos2
```json
db.products.aggregate([
  { $project: { 
      _id: 0,
      nombre: 1,
      total: { $multiply: ["$precio", "$unidades"] }
  }},
  { $out: "productos2" }
])
```

- Comprobamos que se ha creado
```json
db.productos2.find()
```
- Hacemos un find para comprobar el resultado
```json
db.productos2.find()
```
- Usando $cond y $project vamos a visualizar el nombre del producto, el precio y un campo llamado valoración que ponga “barato” si el precio es menor de 250 y caro si es mayor o igual
```JSON
db.Productos.aggregate([
  { $project: { 
      _id: 0,
      nombre: 1,
      precio: 1,
      valoracion: { 
        $cond: { 
          if: { $lt: ["$precio", 250] }, 
          then: "barato", 
          else: "caro" 
        }
      }
  }}
])
```
```JSON
 { nombre: 'Fantastic Wooden Fish', precio: 291, valoracion: 'caro' },
  { nombre: 'Rustic Concrete Pants', precio: 279, valoracion: 'caro' },
  { nombre: 'Small Soft Fish', precio: 189, valoracion: 'barato' },
  { nombre: 'Practical Soft Pants', precio: 67, valoracion: 'barato' },
  { nombre: 'Ergonomic Metal Ball', precio: 246, valoracion: 'barato' },
  { nombre: 'Small Steel Gloves', precio: 37, valoracion: 'barato' },
  {
    nombre: 'Ergonomic Wooden Shirt',
    precio: 238,
    valoracion: 'barato'
  },
  { nombre: 'Handmade Steel Chair', precio: 337, valoracion: 'caro' },
  {
    nombre: 'Handcrafted Soft Gloves',
    precio: 282,
    valoracion: 'caro'
  },
  {
    nombre: 'Fantastic Concrete Salad',
    precio: 265,
    valoracion: 'caro'
  },
  { nombre: 'Handmade Plastic Hat', precio: 253, valoracion: 'caro' },
  { nombre: 'Refined Wooden Tuna', precio: 212, valoracion: 'barato' },
  {
    nombre: 'Refined Concrete Salad',
    precio: 129,
    valoracion: 'barato'
  },
  { nombre: 'Unbranded Soft Fish', precio: 178, valoracion: 'barato' },
  { nombre: 'Small Concrete Fish', precio: 126, valoracion: 'barato' },
  {
    nombre: 'Refined Concrete Bike',
    precio: 180,
    valoracion: 'barato'
  },
  { nombre: 'Tasty Cotton Pants', precio: 52, valoracion: 'barato' },
  {
    nombre: 'Incredible Granite Gloves',
    precio: 290,
    valoracion: 'caro'
  },
  {
    nombre: 'Practical Metal Mouse',
    precio: 190,
    valoracion: 'barato'
  },
  {
    nombre: 'Handcrafted Steel Chicken',
    precio: 113,
    valoracion: 'barato'
  }
]
[
  { nombre: 'Ergonomic Metal Table', precio: 94, valoracion: 'barato' },
  { nombre: 'Tasty Wooden Ball', precio: 76, valoracion: 'barato' },
  { nombre: 'Unbranded Soft Table', precio: 284, valoracion: 'caro' },
  { nombre: 'Handcrafted Metal Tuna', precio: 320, valoracion: 'caro' },
  {
    nombre: 'Incredible Frozen Shirt',
    precio: 173,
    valoracion: 'barato'
  },
  {
    nombre: 'Licensed Fresh Chicken',
    precio: 233,
    valoracion: 'barato'
  },
  {
    nombre: 'Intelligent Plastic Bike',
    precio: 241,
    valoracion: 'barato'
  },
  { nombre: 'Sleek Steel Chicken', precio: 131, valoracion: 'barato' },
  {
    nombre: 'Handcrafted Granite Cheese',
    precio: 304,
    valoracion: 'caro'
  },
  {
    nombre: 'Unbranded Soft Computer',
    precio: 69,
    valoracion: 'barato'
  },
  { nombre: 'Small Rubber Pants', precio: 16, valoracion: 'barato' },
  {
    nombre: 'Generic Fresh Keyboard',
    precio: 16,
    valoracion: 'barato'
  },
  { nombre: 'Sleek Soft Towels', precio: 68, valoracion: 'barato' },
  { nombre: 'Generic Concrete Hat', precio: 70, valoracion: 'barato' },
  {
    nombre: 'Practical Cotton Keyboard',
    precio: 25,
    valoracion: 'barato'
  },
  { nombre: 'Sleek Frozen Hat', precio: 110, valoracion: 'barato' },
  { nombre: 'Rustic Soft Table', precio: 331, valoracion: 'caro' },
  { nombre: 'Awesome Soft Gloves', precio: 18, valoracion: 'barato' },
  { nombre: 'Rustic Steel Shoes', precio: 257, valoracion: 'caro' },
  { nombre: 'Handmade Soft Chips', precio: 208, valoracion: 'barato' }
]
[
  { nombre: 'Handmade Frozen Salad', precio: 85, valoracion: 'barato' },
  { nombre: 'Awesome Cotton Cheese', precio: 277, valoracion: 'caro' },
  { nombre: 'Licensed Granite Ball', precio: 92, valoracion: 'barato' },
  { nombre: 'Sleek Frozen Table', precio: 77, valoracion: 'barato' },
  { nombre: 'Sleek Steel Ball', precio: 236, valoracion: 'barato' },
  { nombre: 'Fantastic Soft Pants', precio: 103, valoracion: 'barato' },
  {
    nombre: 'Intelligent Metal Bike',
    precio: 141,
    valoracion: 'barato'
  },
  { nombre: 'Practical Frozen Chips', precio: 305, valoracion: 'caro' },
  { nombre: 'Refined Plastic Hat', precio: 81, valoracion: 'barato' },
  {
    nombre: 'Licensed Concrete Soap',
    precio: 68,
    valoracion: 'barato'
  },
  { nombre: 'Awesome Frozen Shoes', precio: 125, valoracion: 'barato' },
  {
    nombre: 'Fantastic Metal Pants',
    precio: 129,
    valoracion: 'barato'
  },
  { nombre: 'Ergonomic Metal Hat', precio: 85, valoracion: 'barato' },
  { nombre: 'Licensed Plastic Hat', precio: 38, valoracion: 'barato' },
  {
    nombre: 'Generic Metal Sausages',
    precio: 77,
    valoracion: 'barato'
  },
  { nombre: 'Small Metal Tuna', precio: 43, valoracion: 'barato' },
  {
    nombre: 'Intelligent Frozen Sausages',
    precio: 111,
    valoracion: 'barato'
  },
  { nombre: 'Practical Fresh Fish', precio: 331, valoracion: 'caro' },
  {
    nombre: 'Refined Concrete Shirt',
    precio: 49,
    valoracion: 'barato'
  },
  {
    nombre: 'Handcrafted Granite Chicken',
    precio: 164,
    valoracion: 'barato'
  }
]
[
  { nombre: 'Practical Frozen Salad', precio: 250, valoracion: 'caro' },
  { nombre: 'Sleek Rubber Keyboard', precio: 33, valoracion: 'barato' },
  { nombre: 'Ergonomic Steel Fish', precio: 94, valoracion: 'barato' },
  { nombre: 'Rustic Plastic Mouse', precio: 24, valoracion: 'barato' },
  { nombre: 'Awesome Cotton Mouse', precio: 285, valoracion: 'caro' },
  {
    nombre: 'Intelligent Soft Towels',
    precio: 93,
    valoracion: 'barato'
  },
  {
    nombre: 'Incredible Concrete Fish',
    precio: 336,
    valoracion: 'caro'
  }
]
```