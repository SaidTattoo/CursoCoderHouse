# Métodos de Array 

## ForEach
El forEach es un metodo para iterar cada elemento de un array y ejecutar una función. este recibe como parametro un **callback**, y opcionalmente la referencia al array **thisArg** , el callback lleva como parametro el **CurrentValue** que es el elemento actual siendo procesado en el array, como parametro opcional el **Index** es el indice del elemento actual siendo procesado en el array,  y el **Array** El vector que el foreach esta utilizando para iterar.  

```js 

const data = ["React", "Angular", "Vue"]

data.forEach(()=> {
//iteración
})

data.forEach((currentValue)=> {
console.log(currentValue)
})

output:
//'React'
//'Angular'
//'Vue'

data.forEach((currentValue, index)=> {
console.log( index, currentValue)
})

output:
//0 'React'
//1 'Angular'
//2 'Vue'

data.forEach((currentValue, index ,array)=> {
console.log( index," ", currentValue," ",array)
})


output:
// 0 'React' [ 'React', 'Angular', 'Vue' ]
// 1 'Angular' [ 'React', 'Angular', 'Vue' ]
// 2 'Vue' [ 'React', 'Angular', 'Vue' ]
```

El **ThisArg** mencionado anteriormente, solo es valido con funciones normales, ya que este argumento en las funciones de flecha apuntan al Windows


```js 

data.forEach(function(e){
    console.log(e, this)
}, data)

output:
// 'React' [ 'React', 'Angular', 'Vue' ]
// 'Angular' [ 'React', 'Angular', 'Vue' ]
// 'Vue' [ 'React', 'Angular', 'Vue' ]

```
Otro ejemplo para entender **ThisArg**

```js 
arr=[0];

arr.forEach(function(item) {
    console.log(this === window); //true
    console.log(this === arr);    //false
});

arr.forEach(function(item) {
    console.log(this === window); //true
    console.log(this === arr);    //false
},this);

arr.forEach(function(item) {
    console.log(this === window); //false
    console.log(this === arr);    //true
},arr);

arr.forEach(function(item) {
    console.log(this === window); //false
    console.log(this === arr);    //false
},0);
```
## Includes
**(Array.prototype.includes(var))**

El método includes retorna un booleano al buscar si el valor que se ingresa por parámetro existe en el array.


```js 
const arr = ["a","b","c"]
console.log(arr.includes("a"))  //true
console.log(arr.includes("f"))  //false
```
Esto viene a remplazar el **indexOf** que para validar si existe tenia que ser distinto a -1

```js 
let numbers = [1, 2, 3, 4];
if(numbers.indexOf(2) !== -1) {  console.log('Array contiene el valor');}
```

## Reduce

-- por hacer 
