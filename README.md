# jQuery.Scrollbar´s

### jQuery Plugin ###
Scrollbar´s puede utilizarse para el desplazamiento del contenido.
Fue construido usando la biblioteca jQuery javascript,
fue diseñado para ser una utilidad dinámica y ligera que da a los diseñadores web una manera
potente de la mejora la  interfaz del usuario en sus sitios web.

El propósito de este plugin es añadir una barra de desplazamiento para el elemento de su elección,
para ver cualquier contenido que sea más grande que el tamaño visible,
espacio de un div por ejemplo. Está dirigido a las personas que no quieren un defecto
de desplazamiento y que tienen muy poco conocimiento de esta librería.

## Forma de uso
Incluya este script después de jQuery.

``` html
<script src='jquery.min.js'></script>
<script type="text/javascript" src="js/jquery.scroll.js"></script>
```
``` javascript
<script>
  $("#scroll").scrollbars({
  	// No animar scroll
		animate:false,
		// No ocultar barra
		hide: false
	})
</script>
```

## Ejemplo

``` javascript
// Crear scrollbars.
  $("#scroll").scrollbars({
		// Distancia a bajar cada vez que se ejecuta la funcion mousewhell
		wheel : 120,
		// Velocidad de la animacion
		speed: 550, 
		// Tamaño de la barra
		bar_size : 207,
		// Mostrar msgs
		debug : true,
		// Ocultar barra
		hide: true
		/*easing : 'easeOutQuart' //easeOutCirc'*/

	// Mover scroll al 50%
  }).trigger( 'goto', [ "50%" ] );
  
  // Esto es equivalente
  //$("#scroll").scrollbars( "goto", "50%" );
  
  /* Actualizar scroll
  $("#scroll").scrollbars( "update" );
  
  // Destruir
  $("#scroll").scrollbars( "destroy" );
  
  // Llevar contenido arriba
  $("#scroll").scrollbars( "gototop" );
  
  // Llevar contenido abajo 
  $("#scroll").scrollbars( "gotobottom" );
  
  */
```

## Callbacks
```javascript
	// Crear scrollbars.
	$("#scroll").scrollbars({ // Eventos 
		init			: function(){ },
		
		// Llamada cuando el scroll llega al inicio
		onScrollTop   	: function(){ },
		// Llamada cuando el scroll llega al final
		onScrollEnd   	: function(){ },
		// Cuando se actualiza el scroll
		onUpdate   		: function(){ },
		// Evento mousewheel
		onScrolling		: function(){ },
	});
```


## Depends

* jQuery >=1.4.2

## Licencia

Copyright(c) 2013 CREACIÓN WEB AMALFI
Licensed under the MIT license.
