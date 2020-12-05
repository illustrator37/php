# php
funciones vasicas de PHP
https://www.aulaclic.es/paginas-web/index.htm
Documentacion Oficial: https://www.php.net/manual/es/index.php

echo y print

El código PHP no se muestra en la página. Por eso, si queremos escribir código HTML, debemos de hacerlo utilizando las funciones echo o print.

Ambas funciones se comportan casi igual. Escribirá el texto que le pasemos como parámetro.

Existe una diferencia entre pasarle el texto entre comillas simples o comillas dobles. Si el texto, va entre comillas simples, se mostrará tal cual, mostrando el nombre de las variables que pueda incluir, y sin convertir caracteres escapados. Si le pasamos el texto entre comillas dobles, se imprimirá el valor de las variables, y se convertiran los caracteres escapados (por ejemplo, convierte \n en un salto de línea).

Los parentesis podemos omitirlos, y funciona igual.

$jug1 = "Juan";
$jug2 = "Pedro";
echo('1  ¡$jug1 gana!\n$jug2 pierde.');
print('2  ¡$jug1 gana!\n$jug2 pierde.');
echo("3  ¡$jug1 gana!\n$jug2 pierde.");
print("4  ¡$jug1 gana!\n$jug2 pierde.");

1 ¡$jug1 gana!/n$jug2 pierde.

2 ¡$jug1 gana!/n$jug2 pierde.

3 ¡Juan gana!/n
Pedro pierde.

4 ¡Juan gana!/n
Pedro pierde.

Si queremos escribir comillas dobles dentro de una cadena delimitada por comillas dobles, debemos de escaparlas (\").
isset

La función isset($variable), comprueba si una variable ha sido definida. Devuelve verdadero si lo ha sido y falso si no.
mail

La función mail envía un correo electrónico. Tiene la siguiente estructura:

 mail("email_destino", "asunto", "cuerpo_mensaje");

Donde "email_destino" es la dirección de correo a la que queremos enviar el mensaje, "asunto" es el asunto del mensaje, y "cuerpo_mensaje" es el contenido del mensaje.
include

Sirve para incluir, en esa ubicación, otro archivo. Sería como copiar el contenido de ese archivo, y pegarlo ahí.

include("pagina.php");

strip_tags

Elimina el código HTML de una cadena:

strip_tags("<p class="centrado">Hola <span>mundo</span></p>") devuelve Hola mundo.
trim

Quita los espacios al principio y final de una cadena

trim("   Hola    mundo    ") devuelve Hola   mundo.
ceil

Redondea un valor numérico a un entero mayor.

ceil(2.5) devuelve 3, ceil(2.1) devuelve 3, ceil(2.9) devuelve 3.
count

Devuelve el número de elementos que hay en un array.
header

Nos permite escribir la cabecera de la página.

Por ejemplo, escribiendo :

header("Location: http://www.aulaclic.es"); 
 exit;  

Redirigimos la página a la web de aulaClic.
exit

Finaliza la ejecución del código PHP.
