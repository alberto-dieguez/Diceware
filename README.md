[Generador Diceware](https://alberto-dieguez.gitlab.io/diceware/)

Está web es un generador de contraseñas con el sistema diceware, en el que se 
tiran 5 dados, se anota el número y se busca en una lista la palabra
correspondiente a ese nombre. Es un método famoso ya que aporta bastante
entropía a nuestra contraseña, aproximadamente 12.9 bits por palabra, luego
si añades por tu cuenta un simbolo (lo cual recomiendo) serían unos 10 bits
más aprox, lo cual nos da una contraseña bastante segura.
La lógica de esta web la planteé de la siguiente manera:
Primera valido que el número de palabras que se introduce está entre 1 y 9, 
el cual ya valido en el 'form', si es 'true' genero la pass si es 'false'
notifico un error.
Luego genero un número aleatorio y compruebo que esté en la lista ( porque no 
todos los números están en la lista), si está en la lista. Luego guardo el 
punto donde empieza ese número que he buscado, y en esa misma linea busco
el siguiente salto de linea y copio la linea entera. Sería algo así:

Una linea nomal:
33333 \t dogma \n

Aunque en la lista no venga el tabulador y el salto de linea si que existen.
Entonces copio desde el primer '3' hasta '\n'. Luego guardo la pass igual
pero copiando deste '\t' hasta '\n'.
Ahora que ya tengo la linea y la pass, lo ejecuto todo en un bucle 'for'
y le doy los saltos de linea para que queden bien.