# Práctica 10. Programación Gráfica en JavaScript. HTML. La API Canvas. Camino Aleatorio.
### Factor de ponderación: 8

### Objetivos
Los objetivos de esta práctica son:
 
* Poner en práctica conceptos de Programación Gráfica en JavaScript usando la API Canvas.
* Practicar el uso de elementos HTML básicos.
* Practicar el uso de algunas propiedades básicas de CSS para dotar de estilo a una página web simple.
* Poner en práctica metodologías y conceptos de Programación Orientada a Objetos en JavaScript.
* Profundizar en el uso de pruebas de software (testing) utilizando Mocha y Chai.

### Rúbrica de evaluacion del ejercicio
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva)
que se tendrán en cuenta a la hora de evaluar esta práctica:

* El comportamiento del programa debe ajustarse a lo solicitado en este enunciado.
* Deben usarse estructuras de datos adecuadas para representar los diferentes elementos que intervienen en el problema.
* Capacidad del programador(a) de introducir cambios en el programa desarrollado.
* Se comprobará que el código que el alumnado escribe se adhiere a las reglas de la 
  [Guía de Estilo](https://google.github.io/styleguide/jsguide.html).
* El código ha de estar documentado con [JSDoc](https://jsdoc.app/). 
  Haga que la documentación del programa generada con JSDoc esté disponible a través de una web alojada en su máquina IaaS de la asignatura.
* El alumnado ha de acreditar su capacidad para configurar y ejecutar 
  [ESLint](https://eslint.org/)
  en sus programas.
* El alumnado ha de acreditar que sabe depurar sus programas usando Visual Studio Code.
* Se comprobarán los tests unitarios que el alumnado ha desarrollado para todos sus códigos usando Mocha y Chai, así como
  su capacidad para ejecutar esos tests unitarios desde la interfaz de VSC. 
  Todo el código de los tests que realice para desarrollar la aplicación estarán ubicados en el directorio
  `test` de proyecto.
* Se comprobará el cubrimiento de código que se consigue con los tests usando la herramienta 
  [CodeCov](https://about.codecov.io/)
  y el informe que la misma genera a través de una web.
* El programa debe ajustarse al paradigma de Orientación a Objetos.
* Todo el código estará ubicado en el directorio `src` del proyecto. Use subdirectorios de éste si le resulta
  conveniente.

### Camino Aleatorio
El [camino aleatorio](https://en.wikipedia.org/wiki/Random_walk)
o paseo aleatorio, abreviado en inglés como RW (*Random Walks*), es una formalización matemática 
de la trayectoria que resulta de hacer sucesivos pasos aleatorios. 
Por ejemplo, la ruta trazada por una molécula mientras viaja por un líquido o un gas, el camino que sigue un animal en su 
búsqueda de comida, el precio de una acción fluctuante y la situación financiera de un jugador pueden tratarse como un camino aleatorio.

### La clase *RandomWalk*
En esta práctica se propone desarrollar una clase `RandomWalk` 
que posibilite la visualización en una página web de un camino aleatorio.
La clase ha de encapsularse en un módulo ES6 `random-walk.js`.

Previo a la implementación de la clase, diseñe y desarrolle un conjunto de tests para probar el correcto
funcionamiento de todos los métodos de la clase.

La visualización de la ejecución del programa se realizará a través de una página web alojada
en la máquina IaaS-ULL de la asignatura y cuya URL tendrá la forma:

[3] `http://10.6.129.123:8080/einstein-albert-random-walk.html`

en la que se incustará un canvas para dibujar el camino aleatorio.
Sustituya *Albert Einstein* por su nombre y apellido en la URL de su página.

Trate de usar elementos HTML y CSS que le permitan imitar -en la medida de lo posible- la estética de la
página anterior.
No se propone en esta práctica que dote de interactividad a los elementos (botones, campos de texto,
selectores, etc.) que figuran en la página anterior.
Sí debe Ud. tratar de imitar los enlaces que aparecen en la página, el tipo de letra o los colores de la
misma.

Diseñe asimismo otra página HTML simple 

[5] `http://10.6.129.123:8080/index.html`

que sirva de "página índice" para los ejercicios de la sesión de evaluación de la práctica.
La página [3] será uno de los enlaces de [5] y a su vez [3] tendrá un enlace "Home" que apunte a [5].
Enlace también en la página índice [5] las páginas que contienen los informes de documentación y de
cubrimiento de código de su proyecto.

Tenga en cuenta las siguientes especificaciones a la hora de diseñar su programa:

* Haga que el canvas ocupe la mayor parte del viewport de su navegador.

* Antes de comenzar a dibujar el camino aleatorio (CA), 
el programa mostrará en el lienzo una cuadrícula con una determinada densidad (número de intersecciones).
Esta [figura](https://raw.githubusercontent.com/fsande/PAI-P09-RandomWalk/master/random-walk.png)  
muestra ejemplos de caminos dibujados sobre retículas de diferente densidad.

* Elija para la cuadrícula inicial una densidad que le parezca apropiada para que el comportamiento del programa sea visualmente atractivo a un usuario final.

* El CA comenzará a dibujarse automáticamente una vez cagada la página en el navegador, sin esperar por ninguna interacción por parte del usuario.

* El CA ha de comenzar a dibujarse en el centro del canvas y finalizará cuando el camino alcance cualquiera de los bordes del canvas.

* El CA (tal como muestra la [figura](https://raw.githubusercontent.com/fsande/PAI-P09-RandomWalk/master/random-walk.png)) 
se dibujará de modo que sólo recorre líneas de la cuadrícula (no se pueden trazar líneas de forma arbitraria en el lienzo).

* El CA se irá dibujando segmento a segmento, partiendo del centro del lienzo y dejando trancurrir 0,5 segundos entre el dibujo de un segmento y el siguiente que se dibuje.

Se deja libertad para cada que cada autor/a diseñe la página HTML en la que se embebe el lienzo (canvas) de la manera que
prefiera, pero la aplicación deberá al menos contemplar las especificaciones contempladas en este documento.
El diseño del HTML de esa página brinda una oportunidad para practicar los elementos HTML que se han estudiado hasta ahora.
No se pretende que se utilicen elementos CSS o HTML no estudiados hasta esta fecha.

Se sugiere que, debajo del canvas la página muestre
* Un breve texto explicativo de lo que es un camino aleatorio
* Enlaces a páginas de referencia que se hayan utilizado para realizar este trabajo.
* Cualquier elemento que les parezca oportuno e interesante.
Para visualizar esa información habría que desplazarse (*scroll*) en la página puesto que la vista inicial de la misma debiera estar ocupada en su mayor parte por el lienzo que muestra el camino aleatorio.

