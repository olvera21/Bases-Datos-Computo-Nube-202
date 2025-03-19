## Ejemplo de datos embebidos
``` json
{
  "_id": ObjectId("65f25a1234abcd56789ef012"),
  "nombre": "Eduardo",
  "email": "eduardo@example.com",
  "direccion": {
    "calle": "Av. Siempre Viva",
    "numero": 742,
    "ciudad": "Springfield"
  },
  "telefonos": [
    {
      "tipo": "casa",
      "numero": "555-1234"
    },
    {
      "tipo": "celular",
      "numero": "555-5678"
    }
  ]
}
```

## Ejemplo de datos Referenciados
``` json
{
  "_id": ObjectId("65f25a1234abcd56789ef012"),
  "nombre": "Eduardo",
  "email": "eduardo@example.com",
  "direccion_id": ObjectId("65f25a9999abcd56789ef034")  <-- Referencia a otra colección
}
``` 
``` json
db.usuarios.aggregate([
  {
    $lookup: {
      from: "direcciones", 
      localField: "direccion_id",  
      foreignField: "_id", 
      as: "direccion"  
    }
  }
])
``` 

## Se ve asi
``` json
db.empleados.aggregate([
  {
    $graphLookup: {
      from: "empleados",        // Buscar en la misma colección
      startWith: "$_id",        // Comenzar desde el ID del empleado
      connectFromField: "_id",  // Conectar desde el campo _id
      connectToField: "jefe_id",// Conectar con el campo jefe_id
      as: "subordinados"        // Guardar los resultados en 'subordinados'
    }
  }
]).pretty();
``` 