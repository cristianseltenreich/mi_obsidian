 ● Se puede creer que cada página Web es devuelta en una única respuesta HTTP desde el servidor Web hacia nuestro navegador esto no es en realidad lo que sucede. 
 ● El navegador cliente, que solicita la página HTML y una vez devuelta analiza el código para encontrar todos los recursos a los que se hace referencia desde dentro, como imágenes, hojas de estilo y scripts. 
	 – Solo cuando se han recuperado todos los archivos, la página está completamente cargada para el usuario. 
	 – Una sola página web puede hacer referencia a docenas de archivos y requiere muchas solicitudes y respuestas HTTP.
	![[Pasted image 20240329195305.png]]

Podemos ver en el siguiente gráfico el tráfico HTTP que requiere una Web a través de las herramientas para desarrolladores con las que cuentan los navegadores Web.
![[Pasted image 20240329195239.png]]
● Renderizado: 
– La acción de interpretar todo el documento HTML junto con las imágenes y otros recursos para mostrarlos dentro de la ventana del navegador se denomina renderizado de la página web. 
– Este proceso increíblemente complejo se implementa de manera diferente para cada navegador (Firefox, Chrome, Safari, Explorer y Opera) y es la causa de que los sitios se vean diferentes en diferentes navegadores. 

[[Motores renderizado]] más comunes

● Caché de navegación: – Una vez descargada una página Web del servidor, es posible que el usuario, poco tiempo después, desee ver la misma página Web y actualice el navegador o vuelva a solicitar la URL. 
	– Si bien parte del contenido puede haber cambiado (por ejemplo, una nueva publicación de blog), es probable que la mayoría de los archivos a los que se hace referencia no hayan cambiado, por lo que no es necesario volver a descargarlos. 
	– El almacenamiento en caché del navegador tiene un impacto significativo en la reducción del tráfico de red


[[Fundamentos de la WWW]]
