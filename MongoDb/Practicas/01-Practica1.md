# Practica 1 Base de datos Colecciones e Inserts

1. Conectarnos a mongosh a mongodb
1. Crear una base de datos llamada cursos
1.Comprobar que la base de datos no exista. 
1. Crear una coleccion que se llame facturas y mostrarla

      ``` json
     db.createCollection ("facturas")
      ```

      ``` json
      show collections
      ```

5. Insertar un documento con los siguientes datos:
cod_facturas: 10
cliente: "Fruntas Ramirez",
      ``` json
      db.collection.insertOne(
            {
                
            }
      )
      ```
6. Crear una coleccion nueva pero usuandp directamente el insterOne.
      Insertar un documento en la coleccion
      productos con los siguientes datos.

      | Codigo   | Valor   |
      |-------------|------|
      | Cod_Factura | 10   |
      | Ciente | Frutas Ramirez |
      | Total | 223 |


      ``` json
      db.productos.insertOne(
            {
                  cod_factura:20,
                  cliente: "Materiales",
                  Total:512
            }
      )
      ```
      7. Crear un nuevo documento de producto que contenga un array
      con los siguientes datos.

      | Codigo   | Valor   |
      |-------------|-------------|
      | Cod_Producto | 2 |
      | Nombre | Martillo tubular |
      | Precio | 90 |
      | Unidades | 50 |
      | Fabricantes | fab1, fab2, fab3, fab4 |

     ``` json
      db.productos.insertOne(
    {
         cod_Producto: 2,
         Nombre: "Martillo tubular",
         Precio: 90,
         unidades: 50,
         fabricantes: [ "fab1", "fab2", "fab3", "fab4"]
            }
      )
      ```
      8. Borrar la Coleccion facturas y comprobar que
      se borró
      ``` json
      db.facturas.drop()

      show collections
      ```

      9. Insertar un documentos en una coleccion 
      denominada **fabricantes** para probar los
      subdocumentos y la clave _id personalizado

      | Codigo   | Valor   |
      |-------------|-------------|
      | id | 1 |
      | Nombre | fab1 |
      | localidad | Ciudad: Buenos aires, pais:Argentina, Cp:5725|

      
     ``` json
      db.productos.insertOne(
    {
         id_: 1,
         Nombre: "fab1",
         localidad: {
            ciudad: "Buenos aires",
            pais: "Argentina",
            calle: "Calle pez 29",
            cod_postal: "5725"
            }
      }
      )
      ```

      10. Realizar la insercion de varios documentos 
      en la coleccion productos

      
      | Codigo   | Valor   |
      |-------------|-------------|
      | id | 1 |
      | Nombre | fab1 |
      | localidad | |




      




