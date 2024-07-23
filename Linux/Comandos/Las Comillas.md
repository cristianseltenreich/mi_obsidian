Hay tres tipos de comillas utilizadas por Shell Bash: 
		comillas simples (`'`)
	comillas dobles (`"`)
	comilla invertida (`` ` ``). 
Estas comillas tienen características especiales dentro de shell bash tal como se describe a continuación.

Para entender las comillas simples y dobles, considera que a veces no quieres que el shell trate algunos caracteres como «especiales». Por ejemplo, como viste anteriormente en este laboratorio, el carácter `*` se utiliza como comodín. ¿Y que pasa si quieres que el carácter `*` signifique solamente un asterisco?

Las comillas simples evitan que el shell «interprete» o expanda todos los caracteres especiales.

A menudo, las **comillas simples** se utilizan para proteger una cadena de ser cambiada por el shell, por lo que la cadena puede ser interpretada por un comando como parámetro para afectar la forma en la cuál se ejecuta el comando.

Las **comillas dobles** detienen la expansión de los caracteres glob como el asterisco (`*`), signo de interrogación (`?`) y corchetes ( `[ ]` ). Las comillas dobles no permiten que la expansión de las variables y la sustitución de los comandos (ver comilla invertida) se lleve a cabo.

Las **comillas invertidas** causan «sustitución del comando», que permite que un comando ejecute dentro de la línea de otro comando.

Al utilizar las comillas, se deben introducir en pares o de lo contrario el shell no considerará el comando como completo.

Mientras que las comillas simples son útiles para que el shell no interprete uno o más caracteres, el shell también proporciona una manera de bloquear la interpretación de un solo carácter llamado «**escaping**». 

Para «**evadir**» el significado especial de un metacarácter del shell, se utiliza la barra invertida `\` como un prefijo para ese único carácter.


Ejecuta el siguiente comando para usar las comillas invertidas \`  para ejecutar el comando `date` dentro de la línea del comando echo:

echo Today is \`date\`

El resultado debe ser similar al siguiente:
![[Pasted image 20240401181953.png]]

También puedes colocar un `$` `(` antes del y `)` después del comando para llevar a cabo la sustitución de comandos:

echo Today is $(date)

El resultado debe ser similar al siguiente:
![[Pasted image 20240401182841.png]]

¿Por qué dos métodos diferentes pueden lograr lo mismo? Las comillas invertidas se parecen mucho a las comillas simples, por lo que es más difícil «ver» lo que un comando debería hacer. Originalmente los shell utilizaban las comillas invertidas; el formato `$(comando)` se añadió en una versión posterior del shell bash para que la instrucción fuera visualmente más clara.

Si no quieres que se usen las comillas invertidas para ejecutar un comando, coloca alrededor de ellas las comillas simples. Ejecuta lo siguiente:

echo This is the command '`date`'

El resultado debe ser similar al siguiente:
![[Pasted image 20240401183053.png]]

Ten en cuenta que también puedes colocar una barra invertida delante de cada comilla invertida. Ejecuta lo siguiente:

echo This is the command \`date\`

El resultado debe ser similar al siguiente:
![[Pasted image 20240401183152.png]]

Las comillas dobles no tienen ningún efecto sobre las comillas invertidas. El shell las seguirá utilizando como una sustitución del comando. Ejecuta lo siguiente para ver una demostración:

echo This is the command "`date`"

El resultado debe ser similar al siguiente:
![[Pasted image 20240401183250.png]]

Las comillas dobles tendrán efecto sobre los caracteres comodín de tal manera que deshabilitan su significado especial. Ejecuta lo siguiente:

echo D*
echo "D*"

El resultado debe ser similar al siguiente:
![[Pasted image 20240401183406.png]]

**Importante:**
Las comillas pueden parecer triviales y raras en este momento, pero a medida que adquieras más experiencia de trabajo en el shell de comandos, descubrirás que entender bien cómo las diferentes comillas funcionan es fundamental para el uso del shell.


[[bash]]
[[La sintaxis de la Línea de Comandos]]