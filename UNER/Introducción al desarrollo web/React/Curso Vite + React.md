
Sergie Code youtube 2024

## Componentes

Los creamos con un snipet, el hace todo por nosotros jeje

#### Snipets => ES7+ React/Redux/React-Native 

- Para crear componente: **rafce**
	
	![[Pasted image 20240521184931.png]]
	Para importar este componente se debe usar esta sintaxis del ejemplo en el main.jsx:
	
		import PrimerComponete from './PrimerComponete'

luego agregar entre las etiquetas React.StrictMode el nombre del componente dentro de su etiqueta que se autocierra como en el ejemplo:

![[Pasted image 20240521185014.png]]
				
	


## Variables

### Declaración
//las variables y constantes las declaro por fuera de la función

const string = "esto es un texto";

const number = 123456;

const array = [1, 200, "pepe", "pedro"];

const boolean = true;

const funcion = () => 1 + 100;

const objeto = { curso: "React", duracion: 4 };

const fecha = new Date

  
### resultado dentro de la function
  
const R00Variables = () => {

  return (

    <>//est es un fragmento, los elementos de react deben estar siempre dentro de fragmentos

      <h1>Variables en JSX</h1>

      <p>{string}</p>

      <p>{number}</p>

      <p>{array}</p>

      <p>{boolean}</p> //no muestra nada por pantalla react

      <p>{funcion()}</p> //no muestra nada por pantalla react si no le ponemos ()

      //el objeto solo da error, para renderizar usamos JSON.stringify

      <p>{JSON.stringify(objeto)}</p>

      //fecha también es un objeto entonces aplica lo anterior

      <p>{JSON.stringify(fecha)}</p>

    </>

## CSS
Se linquea en el main,jsx el css principal el estilo general que queremos aplicar

import './styles.css'

pero por cada componente podemos crear un css que aplique solo a ese y sobreescriba el principal por ejemplo:

import './primercomponente.css' 

## Props

Son las propiedades -de ahí el nombre props- son mecanismos utilizados para pasar infomación de un componente padre a un componente hijo.
Son objetos que tienen propiedades que permiten la comunicación entre componentes.
Creamos el componente props
![[Pasted image 20240526155721.png]]
donde props.propTypes contiene el props por defecto para que no nos arroje errores si del elemento padre no traemos ninguna prop por ej

el padre en este caso está en el main.jsx

![[Pasted image 20240526155935.png]]


## Eventos
Mecanismos por lo que los componentes pueden reaccionar ante la interacción del usuario







