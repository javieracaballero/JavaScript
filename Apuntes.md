_Video 1_

# Contexto #
**Brendan Eich** es el inventor de JavaScript.
EcmaScript6 el actual a 2020 es el ES10

# Isomorfismo #

JavaScript es capaz de ejecutarse en las 3 capas de una aplicaión:
1. Frontend (JavaScript).
2. Backend (NodeJs).
3. Persistencia de datos (MongoDB, CouchDB, Postgre, Firebase, ...)

# Características #
* Interpretado de alto nivel.
* Interpretado.
* Dinámico.
* Débil / tipado.
* Multiparadigma.
* Casesensitive.
* No necesita ; a final de línea.

_Vídeo 2_
# Identificadores #
Variables
Declaación: comienzo (letra, $, _), nunca con números o con caracteres especiales.

# Descripción de Variables #
Variables descriptivas.
* snake_case -> para ARCHIVOS (nombre_archivo.ext).
* UPPER_CASE -> para CONSTANTES (CONSTANTE_PI).
* UpperCamelCase -> para CLASES (UnaClase).
* LowerCamelCase -> paa OBJETOS (miObjeto), PRIMITIVOS (unaCadena), FUNCIONES (unaFuncion), INSTANCIAS

# Ordenación de código y buenas prácticas #
1. Imporación de módulos.
2. Declaración de variables.
3. Declaración de funciones.
4. Ejecución de código.

# Tipos de datos #
## Primitivos: acceso directo
  string

  number

  boolean

  null (*)

  undefined (*)
``
  NaN (*)

## Compuestos: accesos por referencia
object = {}

array = []

function() {}

class{}

_Video 3_
Plugins de Visual Studio Code: ESLint, Live Server, Prettier

# VARIABLES #
## Declaración ##
<pre>
var variable
</pre>
JavaScript -> tiene ámbito de bloque.

``var`` -> ámbito GLOBAL. Se almacenan en el scope global del documento.

``let`` -> ámbito de BLOQUE. 

El objeto ``window`` marca todo el objeto de la ventana del navegador ``var`` -> en Window.

Las variables definidas con ``var`` se pueden llamar como ``window.``variable.

# COMENTARIOS #

<pre>
//

/*
  Otro comentario
*/
</pre>

_Video 4_

# CONSTANTES #

## Definición ##

<pre>const constante</pre>

??? Deben tener siempre valor a la definicón con 


_Video 5_
- - -
En JS, todo es un objeto.

MDN -> Mozilla Developer Network. Documentación.

String

# STRINGS #
<pre>
let variable = "valor"
let variable = new String("valor");
</pre>
Este último aparece como un array.

_variable_
<pre>
includes ("cadena");
.trim()
.split()
</pre>
_Video 6_

## Características cadenas texto ##

Concatenar (+).

Interpretación de variables.

// Template string

``let saludo 2 = \`Hola mi nombre $(nombre) $(apellido)´;  <- con los back tic si se puede saltar de línea

variable += <- asignación.

_Video 7_

# NÚMEROS #
<pre>
let a = 2
let b = new Number(1);
</pre>

``let c = 7.19;`` -> ``c.toFixed(5); `` <-- 5 posiciones decimales.

``parseInt(c)`` -> parte entera o pasa un string a número.

``typeof(variable)`` -> devuelve tipo de variable

__JavaScript, no es muy bueno con los float.__

``parseFloat(string)`` <- cuelga del constructor del obejeto ``number.parseFloat()``.

_Video 8_

# BOOLEANOS #

Se pueden crear:
<pre>
let v = true;
let v = Boolean(true);

let f = false;
leg f = Boolean(false);
</pre>

Valores que tienden a true (truthy): -7, " ".
Valores que tienden a false (truthy):  , "", undefined, NaN.

_Video 9_
- - -
null -> la vareiba ha sido asignada como vacía.
undefined -> la variable no ha sido inicializda pero sí definida (o no).

_Video 10_

# VALORES COMPLETOS #

## FUNCIONES ##

Declara una sola vez y se llama las veces que necesties.

Son objetos.

Pueden tener argumenteos y se peude pasar como argumento.

## DECLARACIÓN ##

Declaración tipo.

<pre>
function _NombreFuncion_ (_parámetros_)
{
  return (_valor_);
}
</pre>

Cuando una función devuelve un valor, y se encuentra la sentencia de return, detiene ahí su ejecución, e ignora las sentencias posteriores.

La llamada se realiza ``NombreFuncion()``.

Cuando queremos asignar valores por defecto a la función.

<pre>
function NombreFuncion (parametro1=valor, parametro2=valor)
{

}
</pre>

## Función expresada ó anónima ##
???
<pre>
tipo FuncionExpresado = function () {
  <i>sentencias</i>
};
</pre>

Si llamamos a este tipo de funciones antes de definiras nos dará un error porque no será declaracda _"Error de referencia."_
Esta forma evita errores de compliacion en el código.

_Video 11_
# ARRAYS #

Podemos añadir un array dentro de un ``const`` si no va a cambiar.

Es una colección de elementos.

<u>Definición:</u>
<pre>
tipo nombreArray = [];
* tipo nombreArray = [1, true, _valor_ , ["A", "B", "C"] ];
</pre>

Comienzan en la posición 0.
<pre>
tipo nombreArray = Array.of(elemento1, elemento2, ...)
</pre>

## Inicializar arrays con valores ##
<pre>
tipo nombreArray = Array().fill(valor);
</pre>

* ``.length()`` -> método nos da el número de elementos del array.

### Añadir elementos ###

* ``nombreArray.push(valor);``
* ``nombreArray.pop(valor);``
* ``array.forEach()`` <- ???

_Video 12_
# OBJETOS #

En JS todo es un objeto.

Es una buena práctica definir un objeto comos constante.

<u>Definición:</u>

<pre>
const objeto = {
}
  const jon = {
    nombre: "Jon ",
    apellido: "Mircha",
    edad: 35,
    pasatiempos: ["Correr", "Hacer sudokus","programar"],
    soltero: false,
    contacto: {
    email: "jonmircha@gmail.com",
    twitter: "@jonmircha",
    contacto: "123456789",
  }
}
</pre>

## Acceso al objeto 

Variables --> abritutos/ propiedades.

<pre>
nombreObjeto.atributo;
nombreObjeto["propiedad"];
</pre>

<u>p.e.:</u> ``jon.contacto.twitter``

Los atributos deben de llevar o estar incluidos en funciones que necesiten una entrada de datosvalor, sin embargo, las funciones son independientes.
</pre>

_Video 12_
- - -
## .this 
<pre>
objeto {
  nombre:   "Jon",
  apellido: "Mircha",
  decirMiNombre: function() {
    console.log('hHola me llamo ${this.nombre}, ${apellido});
  }
}
</pre>

Hacer referencia al mismo objeto.

<u>Métodos:</u>

``console.log(Objeto.keys(jon));`` <-- devuelve todo con lo que cuenta el objeto.
``Object.value(jon);`` <-- devuelve todos los valores de keys, excepto las funciones que las marca como tales.
``jon.hasOunPropertry("nombre") <-- devuelve un boleano si cuenta con ese atributo.

_Video13_
# Operadores
## Aritméticos
 \+  -  \* / % (módulo, resto de la división)

## Relacionales
<, >, >=, <=, ==, ===, !=, !==

= -> asignación

== -> comparación de valores 

<pre>
"7" == 7 -> True
</pre>

=== -> comapración de tipo de dato y valor

<pre>
"7" === 7 -> False
  7 === / -> True
  0 === false -> false
</pre>

## Incremento y decremento

<pre>
i = 1;
i = i + 2; -> i += 2
i = i / 2; -> i /= 2
i = i * 2; -> i *= 2
</pre>

### Unario
<pre>
i++;  ++i;
i--;  --i;
</pre>

_Video 14_
- - -

## Lógicos 
! -> not

|| -> or

&& -> and

# Esctructuras de control
Controla el flujo del código.

## Condicionales

### if _ else

<pre>
if (condición) {
  sentencias true
} else {
  sentencias false
}
</pre>

Cuando en la condición usamos < ó > excluimos el valor. Para incluirlo <= ó >=, en este caso si que alcanza el valor.

### if _ else if ... _ else

<pre>
if (condición) {
  sentencias true
} else if (condición2) {
  sentencias true condición2
} else if (condición3) {
  sentencias true condición3
} else {
  sentencias false
}
</pre>

### Operador ternario
<pre>
(condición)?true:false;
</pre>

Va únicamente en una sola línea.

### switch _ case

<pre>
switch (variable) {

  case valor:
    sentencias;
    break;

  case valor:
    sentencias;
    break;

  [...]

  default:
    sentencias si no cumple ninguna;
    break
}
</pre>

_video 15_
# Bucles

## while
Mientras...
<pre>
while (condición) {
  sentencias;
}
</pre>

El bucle se cumple mientras la condición sea true.

## do
<pre>
do {
  sentencias;
} while (condición)
</pre>

Realiza la operación por lo menos una vez.

## for
<pre>
for (inciailización variable;
     condición;
     incrementeo/decremento) {
  sentencias;
}
</pre>

## for ( in )
Presenta las propiedades de un objeto.
<pre>
for (cont key in object) {
  sentencias;
}
</pre>

<u>Ejemplo:</u>
<pre>
const jon = {
  nombre: "Jon";
  apellido: "Mircha";
  edad: 34
}

for (const propiedad in jon) {
  console.log(propiedad);
}
</pre>

Si queremos ver también los valores del objeto...

<pre>
for (const propiedad in jon) {
  console.log(`Key:${propiedad}, Value: ${jon[propiedad]}`);
}
</pre>