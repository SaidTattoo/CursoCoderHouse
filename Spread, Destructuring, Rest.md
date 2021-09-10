# JavaScript 

## Operador spread

El operador spread permite simplificar las concatenaciones de arrays y el empleo de estos elementos como parámetros. Para estudiar su funcionamiento comparemos el uso de la notación spread frente a una concatenación de arrays empleando el método concat.

```js 
const arrayA = [1,2,3]
const arrayB = [4,5,6]
//usando el metodo concat 
const arrayConcat = arrayA.concat(arrayB)
//usando el operador spread
const arraySpread = [...arrayA, ...arrayB]

```


Otro ejemplo de uso de spread


```js 
const datosEnComun = {
  curso:"CoderHouse",
  seccion:"14430"
}

const misDatos = {
  ...datosEnComun,
   edad:34,
   email:"said@mail.cl"
}

const otrosDatos = {
   ...datosEnComun,
   edad:33,
   email:"otro@mail.cl"
}
```
## Parámetros Rest 

La sintaxis de los parámetros rest nos permiten representar un número indefinido de argumentos como un array.

```js
const sumar =(a, b ,...c) =>{
  let suma = a + b
   c.forEach((e)=> {
     suma += e
   }) 
  return suma
}
```


```js
const multiplicacion = (n,...numeros) => numeros.map(x => x * n);
console.log(multiplicacion(5,10,20));  // [50, 100]

```
## Desestructuración
La desestructuración es una característica muy conveniente al desarrollar con javascript, es una expresión que nos permite desempaquetar valores de arrays u objetos en grupos de variables, permitiéndonos simplificar y crear código más legible.


```js
const datos = ["CoderHouse", "JavaScript", "Frotend"];
const [escuela,curso,carrera] = datos;
console.log(escuela); //CoderHouse
console.log(curso);   //JavaScript  
console.log(carrera); //Frotend

```


```js
/*{
  usuario:"CODERHOUSE",
  email:"coder@mail.cl",
  password:"123123",
  __V:"0"
}*/

const consultarApiLogin = async (id) => {
  const usuario = await findUserById(id)
  const {__v, password, ...restoDatos } = usuario
  return  restoDatos
}

/*{
  usuario:"CODERHOUSE",
  email:"coder@mail.cl",
}*/

```
