# Object

## Object.entries

 Es un método añadido a Object que recibe como parámetro un objeto y lo que nos devuelve es un array que contiene tantos arrays como propiedades tenga el objeto con la clave y valor de las propiedades.

```js 
const data = {
    frontend:"Said",
    backend: "Juan"
}
const entries = Object.entries(data)

output:
// [ [ 'frontend', 'Said' ], [ 'backend', 'Juan' ] ]

```

## Object.values
Este es otro método añadido a Object. Como el anterior, también recibe un objeto como parámetro y lo que nos devuelve son los valores de las propiedades del objeto pasado.

```js 
const datas = {
    frontend:"Said",
    backend: "Juan"
}

const entries = Object.values(datas)
console.log(entries)

output:
// [ 'Said', 'Juan' ]
```

## Object.keys
El método Object.keys() devuelve un array de las propiedades names de un objeto, en el mismo orden como se obtienen en un loop normal

```js
const datas = {
    frontend:"Said",
    backend: "Juan"
}

const entries = Object.keys(datas)
console.log(entries)

output:
// [ 'frontend', 'backend' ]
```

## Object.create
El método Object.create() crea un objeto nuevo, utilizando un objeto existente como el prototipo del nuevo objeto creado.

```js

```