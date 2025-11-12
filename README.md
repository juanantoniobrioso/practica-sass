# Galería Z Masters

En este proyecto debemos usar SASS para permitirnos nuevas funciones en el CSS
que de normal no podríamos usar, como el uso de variables, el anidamiento de estilos, etc

Para este proyecto habían ciertas pautas que cumplir en las cuáles diré hasta donde he llegado

## Nivel 1: Explorador (Iniciado)
### He conseguido crear las tarjetas y que se vean la imagen y el texto.
### He usado SASS, pero tengo casi todo mi código en main.scss.
### Al hacer "hover", el texto aparece, pero empuja el contenido hacia abajo o descoloca la tarjeta.
### (Autodiagnóstico: Aún no he entendido cómo position: absolute saca al elemento del flujo).

En el nivel 1 he cumplido el punto 1. El punto 2 no porque casi todo el código está en gallery.
El punto 3 lo cumplo a medias, consigo que se transparente la imagen pero no que aparezca el texto
al mover el raton y además descoloca la tarjeta
El punto 4 considero que si. Entiendo que hace position relative y absolute, pero no entiendo por que
descoloca las tarjetas

## Nivel 2: Aprendiz (En proceso)
### ¡Casi lo tengo! El overlay ya flota por encima de la imagen usando position: absolute.
### He usado SASS con anidamiento, ¡y es mucho más limpio!
### Problema: El overlay se posiciona "raro", quizás arriba a la izquierda de toda la página, no dentro de su tarjeta.
### (Autodiagnóstico: Me ha faltado poner position: relative al contenedor padre (.gallery-card) para que sirva de "ancla" al overlay absoluto).

En el nivel 2 cumplo el punto 2 (El apartado de gallery tiene anidado .gallery-card e img)
El punto 3 no lo cumplo. Aunque el overlay este mal, se pone siempre donde esté la tarjeta.
El punto 4 lo he cumplido pero aún así no funciona

## Nivel 3: Practicante (Conseguido)
### ¡Funciona perfecto! He usado position: relative en .gallery-card y position: absolute en .card-overlay.
### El overlay se oculta (quizás con opacity: 0 o display: none) y aparece perfectamente centrado sobre su imagen al hacer :hover.
### He cumplido los requisitos de SASS: He separado _variables.scss y _gallery.scss y los he importado con @use (o @import) en main.scss.
### (Autodiagnóstico: He entendido la relación padre-hijo en el posicionamiento y la utilidad de modularizar SASS).

El punto 1 está relativamente cumplido. Está hecho pero no funciona
El punto 3 está cumplido. He sabido usar el @use para importar los scss entre ellos
Considero que el punto 4 está cumplido. Mis errores radican más en el propio CSS que en el SASS

## Nivel 4: Maestro (Avanzado)
### He cumplido todo el Nivel 3.
### Además: He añadido una transition suave a la aparición del overlay (ej. transition: all 0.3s ease-in-out;) para que no sea un cambio brusco.
### Además: He usado un mixin de SASS (quizás para centrar el overlay con Flexbox) y lo he aplicado con @include.
### (Autodiagnóstico: No solo aplico los conceptos, sino que los combino para mejorar la experiencia de usuario y la eficiencia del código).

Cumplo el punto 2. La transición de la opacidad está hecha y funciona.
No he cumplido el punto 3. Aunque he entendido el uso de @mixin, no he encontrado la manera de usarlo