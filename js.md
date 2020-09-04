# Referencias JavaScript
##### *Un lenguaje moderno*
---
## 1 - Uso de JavaScript

Incluir JavaScript en una página html
```html
<script type="text/javascript">
//JS código
</script>
```
Llamada a un archivo JavaScript externo
```html
<script src="myscript.js"></script><code></code>
```
Including Comments
```javascript
// Comentario
Comentarios de una linea

/* Comentario
 * multilinea
 */
 Comentarios multineas

```
---
## 2 - Variables
Es un espacio reservado en memoria al cual le ponemos un nombre o indicador para poder recuperarla donde almacenaremos un valor.
### **var**  
El tipo de variable mas común, se puede reasignar su valor cuando queramos y son creadas antes que ejecutar cualquier código.
```javascript
// Declaración e inicialización en la misma linea
var producto = 'Tele 50';
// Declaración e inicialización posterior
var producto;
producto = 'Tele 50'
```
JavaScript es un lenguaje dinamico por lo que es posible cambiar el tipo de variables, por lo que no es necesario definir el tipo de variables.
```javascript
// Cambio del tipo de valor
var valor = 'Luis';
valor = 32;
valor = true;
```
Nomenclatura mas usada para crear variables en JavaScript
```javascript
// camelCase
var nombreProducto;
```
### **const**  
Es un tipo de variable que no puede ser reasignada una vez declarada, su valor no cambia a lo largo de la ejecución del programa.
Nomenclatura mas usada para crear variables en JavaScript
```javascript
// UPPER_CASE
var NOMBRE_PRODUCTO;
```
### **let**  
Este tipo sirve para declarar variables de alcance local con ambito de bloque.
**let** te permite declarar variables limitando su alcance (scope) al bloque, declaración, o expresión donde se está usando. Lo anterior diferencia  **let** de la palabra reservada **var** , la cual define una variable global o local en una función sin importar el ámbito del bloque.
Nomenclatura mas usada para crear variables tipo let en JavaScript
```javascript
// camelCase
let nombreProducto;
```
---
## 3 - String
Es un objeto destinado a manipular cadena de caracteres. Se debe declarar entre comillas simples o dobles. Este objeto nos permite realizar operaciones con cadenas como concatenar, dividir, buscar texto, extraer parte de él...
```javascript
// Formas de declarar e iniciar un String
let productoUno = 'Monitor 20 pulgadas';
let productoDos = String('Monitor 24 pulgadas');
let productoTres = new String('Monitor 32 pulgadas');
```
### Secuencias de escape
Todas ellas comienzas por **/**, y nos ayudan a introducir en una cadena algunos caracteres especiales que de otra forma seria imposible de representar mediante texto.
```
\' - Comillas simples
\" - Comillas dobles
\\ - Barra invertida
\b - Retroceso
\f - Salto de pagina
\n - Nueva línea
\r - Retorno de carro
\t - Tabulador horizontal
\v - Tabulador vertical
```
### Concatenación de cadenas
Es la unión secuencial de cadenas para formar una sola. En JavaScript tenemos varios métodos.
```javascript
const plato = 'Macarrones';
const precioPlato = 5;

// Mediante el método concat
console.log(plato.concat(': ' + precioPlato));

// Concatenación con signo + de variables y String
console.log('El precio de ' + plato + ', es de ' + precioPlato + ' Euros.');

// Usando un Template String
console.log(`Los ${plato} tienen un precio de ${precioPlato} €`);
```
### Métodos mas comunes
Los métodos sirven para realizar acciones, en este caso con el objeto String, podemos encontrar métodos que nos ayuden a contar los caracteres del texto, a eliminar espacios en blancos a unir varias cadenas de texto...
#### - length
Esta propiedad nos devuelve la longuitud de la cadena
```javascript
let nombre = 'Luis';
console.log(nombre.length);
4
```
#### - indexOf( )
Nos devuelve el indice de la primera letra del texto que hemos buscado en una cadena, si no lo encuentra nos devolvera -1.
```javascript
let nombre = 'Luis Quesada';
console.log(nombre.indexOf('Quesada'));
5
```
#### - includes( )
Este método determina mediante true o false si una cadena puede ser encontrada o no dentro de otra. Este método es case sensitive, diferencia entre mayusculas y minusculas.
```javascript
let nombre = 'Luis Quesada';
console.log(nombre.includes('Quesada'));
true
```
#### - trim( )
Elimina cualquier espacio en blanco que tenga el String
```javascript
const marcaCoche = '     Alfa Romeo  ';
console.log(marcaCoche.trim());
Alfa Romeo
```
#### - trimStart( )
Elimina los espacio en blanco al inicio del String
```javascript
const marcaCoche = '     Alfa Romeo  ';
console.log(marcaCoche.trimStart());
Alfa Romeo  
```
#### - trimEnd( )
Elimina los espacio en blanco al final del String
```javascript
const marcaCoche = '     Alfa Romeo  ';
console.log(marcaCoche.trimEnd());
     Alfa Romeo
```
#### - replace( )
Busca y reemplaza un texto dentro de una cadena
```javascript
let helado = 'Cono de fresa';
console.log(helado.replace('fresa', 'Vainilla'));
Cono de Vainilla
```
#### - charAt( )
Devuelve el caracter en una determinada posición de un String
```javascript
let helado = 'Cono de fresa';
console.log(helado.charAt(0));
C
```
#### - slice( )
Devuelve una copia de una tarde del texto o array en un nuevo array desde el inicio hasta el final, este último no incluido. Sino se especifica una final, extrae hasta el final.
```javascript
let helado = 'Cono de fresa';
console.log(helado.slice(8, 9));
f
```
#### - substring( )
Extrae caracteres desde un inicio hasta un final sin incluirlo, si se omite el final extraerá hasta el final del String.
```javascript
let helado = 'Cono de fresa';
console.log(helado.substring(8, 9));
f
```
#### - repeat( )
Repite el numero de veces que le pasemos por parametro el String.
```javascript
let signo = '!';
console.log(raza.repeat(5));
!!!!!
```
#### - split( )
Divide un texto en un array de subcadenas, mediante un caracter especificado como separador.
```javascript
let hobbies = "cantar,programar,bailar,leer"
console.log(hobbies.split(","));
(4) ["cantar", "programar", "bailar", "leer"]
0: "cantar"
1: "programar"
2: "bailar"
3: "leer"
```
#### - toLowerCase( )
Convierte un String a minusculas
```javascript
let tratamiento = "Limpieza facial";
console.log(tratamiento.toLowerCase());
limpieza facial
```
#### - toUpperCase( )
Convierte un String a mayusculas
```javascript
let tratamiento = "Limpieza facial";
console.log(tratamiento.toUpperCase());
LIMPIEZA FACIAL
```
#### - toString( )
Devueve una cadena de texto que representa al objeto
```javascript
let precioTratamiento = 300;
console.log(precioTratamiento.toString());
300 // Devuelve 300 como String
```
#### - valueOf( )
Devuleve el valor primitivo de un objeto
```javascript
let precioTratamiento = '300';
console.log(precioTratamiento.valueOf());
300 // Devuelve 300 como numero
``
