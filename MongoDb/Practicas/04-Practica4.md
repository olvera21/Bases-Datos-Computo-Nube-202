# Arrays y documentos anidados

1. Para hacer esta práctica vamos a cargar unos datos ficticios de empresas.

2. Tienes un fichero denominado “personas.json”

3. Debes poner el resultado de las consultas en cada apartado

- Buscar las personas que vivan en Colombia
```json
db.Personas.find({ "direccion.pais": "Colombia" })
```

```json
{
  _id: ObjectId('67da3bdc9d62f731cac95a9a'),
  nombre: 'Anni Niño',
  direccion: {
    calle: '207 Taylor Cliffs',
    ciudad: 'Buenaventura',
    pais: 'Colombia'
  },
  colores: [
    'yellow',
    'salmon',
    'yellow'
  ],
  ingresos: 7387
}
```
- Personas a las que le guste el color rosa
```json
db.Personas.find({ "colores": { $in: ["pink", "rosa"] } })
```

```json
{
  _id: ObjectId('67da3bdc9d62f731cac95a92'),
  nombre: 'Laura Oquendo',
  direccion: {
    calle: '2800 Samir Trail',
    ciudad: 'Bijelo Polje',
    pais: 'Montenegro'
  },
  colores: [
    'pink',
    'blue',
    'teal'
  ],
  ingresos: 8707
}
```

```json
{
  _id: ObjectId('67da3bdc9d62f731cac95a9f'),
  nombre: 'Lorena Saiz',
  direccion: {
    calle: '1611 Oscar Walk',
    ciudad: 'The Pas',
    pais: 'Canada'
  },
  colores: [
    'orchid',
    'teal',
    'pink'
  ],
  ingresos: 10407
}
```
- Personas cuyo tercer color preferido sea el amarillo (yellow). Recuerda que los arrays comienzan por Cero. Deben salir 3
```json
db.Personas.find({ "colores.2": "yellow" })
```
```json
{
  _id: ObjectId('67da3bdc9d62f731cac95a93'),
  nombre: 'Laura Salcedo',
  direccion: {
    calle: '11046 Cayla Centers',
    ciudad: 'Rosso',
    pais: 'Mauritania'
  },
  colores: [
    'indigo',
    'green',
    'yellow',
    'salmon'
  ],
  ingresos: 7435
}
```
```json
{
  _id: ObjectId('67da3bdc9d62f731cac95a9a'),
  nombre: 'Anni Niño',
  direccion: {
    calle: '207 Taylor Cliffs',
    ciudad: 'Buenaventura',
    pais: 'Colombia'
  },
  colores: [
    'yellow',
    'salmon',
    'yellow'
  ],
  ingresos: 7387
}
```
```json
{
  _id: ObjectId('67da3bdc9d62f731cac95a9b'),
  nombre: 'Andrea Paredes',
  direccion: {
    calle: '09438 Vandervort Drives',
    ciudad: 'San Antonio',
    pais: 'Puerto Rico'
  },
  colores: [
    'green',
    'indigo',
    'yellow',
    'salmon',
    'grey',
    'violet'
  ],
  ingresos: 6340
}
```
```json
db.Personas.find({
  "colores.2": "yellow",
  "direccion.pais": "Mauritania"
})
```
```json
{
  _id: ObjectId('67da3bdc9d62f731cac95a93'),
  nombre: 'Laura Salcedo',
  direccion: {
    calle: '11046 Cayla Centers',
    ciudad: 'Rosso',
    pais: 'Mauritania'
  },
  colores: [
    'indigo',
    'green',
    'yellow',
    'salmon'
  ],
  ingresos: 7435
}
```
- Usando el operador $all averiguar las personas que les gusta el plata (silver) y el salmon (salmon)
```json
db.Personas.find({
  "colores": { $all: ["silver", "salmon"] }
})
```
```json
{
  _id: ObjectId('67da3bdc9d62f731cac95a97'),
  nombre: 'Ángel Anguiano',
  direccion: {
    calle: '20780 McLaughlin Union',
    ciudad: 'Paramaribo',
    pais: 'Suriname'
  },
  colores: [
    'plum',
    'silver',
    'olive',
    'salmon',
    'silver'
  ],
  ingresos: 5712
}
```

- Con el operador $elemMatch, averigua las personas que les guste el rosa (Pink) o el rojo (red)