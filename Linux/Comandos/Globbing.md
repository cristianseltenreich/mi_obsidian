
El uso de los caracteres glob en Linux es similar a lo que muchos sistemas operativos se refieren como caracteres «wildcard». Utilizando los caracteres glob haces coincidir los nombres de archivos usando patrones.

Los caracteres glob son una característica del shell, no es algo propio de algún comando específico. Como resultado de ello, puedes utilizar los caracteres glob con cualquier comando de Linux.

Cuando se utilizan los caracteres glob, el shell «expande» todo el patrón para coincidir con todos los archivos en el directorio especificado que coincide con el patrón.

A efectos de demostración, vamos a utilizar el comando `echo` para visualizar este proceso de expansión.

Utiliza el siguiente comando `echo` para mostrar todos los nombres de archivo en el directorio actual que coincide con el patrón global `*`:

echo *

El resultado debe ser similar al siguiente:
![[Pasted image 20240401172659.png]]

El asterisco `*` busca «cero o más» coincidencias de caracteres en un nombre de archivo. En el ejemplo anterior, esto se traduce en la adecuación de todos los nombres del archivo en el directorio actual.

El comando `echo`, a su vez, muestra los nombres del archivo que fueron agrupados.

Los siguientes comandos mostrarán todos los archivos en el directorio actual que comienzan con la letra `D` y la letra `P`:

echo P*
echo D*

El resultado debe ser similar al siguiente:
![[Pasted image 20240401173031.png]]

Piensa en el segundo ejemplo, `D*`, como «coincidencia con todos los nombres de archivo en el directorio actual que comienzan con la letra `d` en mayúscula y tienen cero o más de cualquier otro carácter después de la letra `D`».

El asterisco `*` se puede utilizar en cualquier lugar de la cadena. El siguiente comando mostrará todos los archivos en tu directorio actual que terminan en la letra `s`:

echo  \*s

El resultado debe ser similar al siguiente:
![[Pasted image 20240401173543.png]]


Observa que el asterisco también puede aparecer varias veces o en medio de varios caracteres:

echo D\*n\*s

El resultado debe ser similar al siguiente:
![[Pasted image 20240401173756.png]]


El siguiente metacarácter glob que vamos a examinar es el signo de interrogación `?`. El signo de interrogación coincide exactamente con un carácter. Este único carácter puede ser cualquier carácter posible.

Al igual que el asterisco, se puede utilizar en cualquier lugar de una cadena y puede aparecer varias veces.

Dado que cada signo de interrogación coincide con un carácter desconocido, introduciendo seis de ellos coincidirán con los nombres de archivo de seis caracteres. Introduce lo siguiente para mostrar los nombres de los archivos que tienen exactamente seis caracteres:

echo ??????

El resultado debe ser similar al siguiente:
![[Pasted image 20240401173915.png]]

Utilizando el signo de interrogación con otros caracteres se limitarán las coincidencias. Escribe lo siguiente para mostrar los nombres de los archivos que comienzan con la letra D y tienen exactamente nueve caracteres:

echo D????????

El resultado debe ser similar al siguiente:
![[Pasted image 20240401174113.png]]


Los comodines o caracteres glob pueden combinarse entre sí. El siguiente comando mostrará los nombres de archivo que tienen al menos seis caracteres y terminan en la letra `s`.

echo ?????*s

El resultado debe ser similar al siguiente:
![[Pasted image 20240401174408.png]]

Piensa en el patrón `?????*s` en el sentido de «coincide con los nombres de archivo que comienzan con cualquier cinco caracteres, y luego tenga cero o más caracteres y luego termine con el carácter


El siguiente glob es similar al glob signo de interrogación para especificar un carácter. Este glob utiliza un par de corchetes `[ ]` para especificar qué se le permitirá a un carácter. Los caracteres permitidos se pueden especificar como una serie, una lista, o por lo que se conoce como una clase de caracteres.

Los caracteres permitidos también pueden ser anulados con un signo de exclamación `!`.

En el primer ejemplo, el primer carácter del nombre de archivo puede ser o bien una `D` o una `P`. En el segundo ejemplo, el primer carácter puede ser cualquier carácter excepto una `D` o `P`:

echo [DP]*
echo [!DP]*

El resultado debe ser similar al siguiente:
![[Pasted image 20240401174655.png]]


En estos siguientes ejemplos se especifica una serie de caracteres. En el primer ejemplo, el primer carácter del nombre de archivo puede ser cualquier carácter que comienze cualquier carácter entre la  `D` y la `P`. En el segundo ejemplo, este rango de caracteres es negado, lo que significa cualquier carácter individual coincidirá, excepto si está entre la letra `D` y la `P`:

echo [D-P]*
echo [!D-P]*

El resultado debe ser similar al siguiente:
![[Pasted image 20240401174914.png]]

Te podrías preguntar «¿quién decide qué letras haya entre la `D` y la `P`? ». En este caso la respuesta es bastante obvia (`E`, `F`, `G`, `H`, `I`, `J`, `K`, `L`, `M`, `N` y `O`), pero ¿qué tal que el rango fuese `[1-A]`?

Para determinar el rango de caracteres se utiliza la tabla de texto ASCII. Puedes consultar esta tabla mediante su búsqueda en Internet o introduciendo el comando siguiente, el comando [[ascii]].


Por lo tanto, ¿con qué caracteres coincidirá el glob `[1-A]` ? De acuerdo con la tabla de texto ASCII: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `:`, `;`, `<`, `=`, `>`, `?`, `@` y `A`.