# webcam_circleis

HOUGH TRANSFORM

La transformada de Hough es una técnica para encontrar diferentes tipos de figuras que pueden ser expresadas matemáticamente, (como un circulo, un cuadrado, un triangulo…) en una imagen.

Para aplicar la transformada de Hough antes aplicaremos la detección de bordes en la imagen , esto se hace para que el algoritmo sea más eficientes, ya que habrá menos puntos a recorrer.

Para aplicar la transformada de Hough ,antes tenemos que definir la ecuación de la figura que queremos detectar.
Para ello hay que definir el tipo de figura y los parámetros que debe cumplir. Por ejemplo, para detectar círculos debemos indicar que las figuras a detectar son círculos y definir los parámetros que estos círculos tienen que cumplir, como el radio mínimo o máximo que debe tener o la distancia de circulo que debe haber, por ejemplo, si solo aparece medio circulo podemos detectar o no que eso es un circulo. Con esto último definiremos la sensibilidad de la transformada, como más sensible sea más probabilidades tenemos de obtener falsos círculos, pero como más estrictos seamos, más posibilidades tendremos de no detectar círculos que queríamos detectar.

A continuación, la transformada de Hough detectará los conjuntos de puntos que cumplen la ecuación.

Por ejemplo, si en el proyecto webcam_circles queremos que sea más estricto definiendo que es o no un circulo, ya que vemos que detecta muchos falsos círculos modificaremos el MIN_CIRCLE_DIST.
Por ejemplo, si ponemos “const double MIN_CIRCLE_DIST = 80;” podremos observar que se detectan muchos menos círculos que antes.
Otra modificación que podríamos hacer para ver el funcionamiento de cada parámetro seria modificar el intervalo del radio del circulo.
“const int MIN_RADIUS = 50;“
“const int MAX_RADIUS = 50;“
En este caso, podremos observar que ahora solamente nos mostrara los círculos de radio 50.

Referencias

- https://rua.ua.es/dspace/bitstream/10045/17323/4/caracteristicas.pdf
- http://iie.fing.edu.uy/investigacion/grupos/gti/timag/trabajos/2004/deteccion_circulos/though1.html
- https://es.wikipedia.org/wiki/Transformada_de_Hough
- http://iaci.unq.edu.ar/materias/vision/archivos/apuntes/Transformada%20de%20Hough.pdf
- http://docs.opencv.org/2.4/doc/tutorials/imgproc/imgtrans/hough_lines/hough_lines.html
