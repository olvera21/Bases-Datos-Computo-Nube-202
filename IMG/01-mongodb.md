# CRUD y consultas en MongoDB

## Crear una base de datos
Solo se crea si contiene por lo menos una colección
use bd1

## Cómo crear una colección
use bd1
db.createCollection("Empleado")

## Mostrar las colecciones
show collections

## Insertar un documento
json
db.coleccion.insertOne(
    {
        nombre: 'Estefany',
        apellido1: 'Vazquez',
        edad: 22,
        ciudad: 'Huehuetoca'
    }
)


## Inserción de un documento más complejo con array
json
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
 

 ## Inserción de documentos más complejos con documentos anidados
 json
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
# Inserción de documentos muy complejos
db.alumnos.insertMany([
  {
    _id: 12,
    nombre: "Roberto Gomez",
    apellido: "Gomez",
    edad: "23",
    descripcion: "Es un Comediante bueno"
  },
  {
    nombre: "Luiz",
    apellido: "Suarez",
    edad: 43,
    habilidades: ["Correr", "dormir", "Morder"],
    direcciones: {
      calle: "del infierno",
      numero: 666
    },
    esposas: [
      {
        nombre: "Marisol",
        edad: 20,
        pension: 350,
        hijos: ["Joaquin", "Bridget"]
      },
      {
        nombre: "Dorien",
        edad: 46,
        pension: 6500,
        complaciente: true
      }
    ]
  }
])

# Practica 
1. Bases de Datos, colecciones e insert
    -Nos conectamos con mongosh a mongodb
    -Crear una base de datos denominada curso
    -Verificar que la base de datos no existe
    -Crear una colecion denomidad facturas 
    db.create collectio