## Modelo de Datos en MongoDB

- Modelos 
    - Embebidos
    - Referenciados

- Modelos Embebidos

## Uno a Uno 
``` json

    [
        _id:1,
        nombre:"Tecnologias de la informacion",
        responsable:{
            nombre: 'Monico',
            apellidos:'Martinez Perez'
        },
        descripcion:'ejemplo de departamento'
        },
        {
            _id:2,
        nombre:"Contabilidad",
        responsable:{
            nombre: 'Monico',
            apellidos:'Lopez Hernandez'
        },
        descripcion:'ejemplo de departamento'
        }
    }
    ]
    )
``` 
    - Modelos Referenciados

## Uno a Uno
``` Json

db.localidades.insertMany(
    [
        {
            _id:'BA',
            ciudad: Buenos Aires,
            Pais: Argentina,
            poblacion: '16 millones',
            turismo:["edificios", "tango", "gastronomia", "museos", "parques"],
            direccion: "Avanida Tortolos",
            cod_departamento:1

        }
    ]
)
