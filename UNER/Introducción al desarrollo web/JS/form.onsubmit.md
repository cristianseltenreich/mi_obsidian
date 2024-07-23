```js
form.onsubmit()
	e.preventDefault()
```



form.onsubmit()	registra un _event handler_ para manejar el evento de envío del un formulario. 

El controlador de eventos llama inmediatamente al método _e.preventDefault()_ para evitar el manejo por defecto del envío de formularios. El método por defecto enviaría los datos al servidor y causaría una nueva solicitud GET, lo cual no queremos que suceda.

