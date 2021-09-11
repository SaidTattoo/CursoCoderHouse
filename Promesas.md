# Promesas

Llamamos a resolve cuando lo que estabamos haciendo resulto con exito
en el ejemplo se utiliza el setTimeOut para simular un codigo asincrono,

La comunicación asíncrona es un método de intercambio de mensajes entre dos o más partes, en la que cada parte recibe y procesa el mensaje cuando sea conveniente o posible de realizar, en vez de hacerlo inmediatamente al recibirlo. Adicionalmente, los mensajes pueden ser enviados sin esperar el acuse de recibo de los mismos, bajo el entendimiento de que si ocurre algún problema, quien los recibe solicitará las correcciones o manejara la situación.


en este caso se utilizan promesas para comunicarse con apis externas y no se quiere continuar con el proceso hasta que esta retorne su respuesta. 


```js
let miPrimeraPromise = new Promise((resolve, reject) => {
    setTimeout(function(){
    resolve("¡Éxito!"); // ¡Todo salió bien!
  }, 250);
}
```

