# Introducción a la investigación operativa

#io #book

::: {#def-io}
## Investigacion de operaciones

La Investigación de Operaciones es una disciplina que se ocupa del estudio y análisis de sistemas de producción y servicios. Su objetivo es encontrar las mejores soluciones posibles a los problemas que surgen en la toma de decisiones en dichos sistemas. La disciplina se originó durante la Segunda Guerra Mundial, cuando se necesitaba optimizar la producción de material bélico y mejorar la eficiencia logística. Desde entonces, ha tenido un papel importante en la mejora de la productividad y la eficiencia en diversos campos, como la manufactura, la ingeniería, la logística, la finanzas, la salud y la educación, entre otros:
:::

La Investigación de Operaciones (IO) es un campo de la matemática y la informática que se dedica a la resolución de problemas prácticos mediante el uso de modelos matemáticos y algoritmos. Estos problemas pueden ser de diversa índole, tales como la optimización de recursos en una empresa, el diseño de un plan de producción eficiente, la gestión de inventarios, entre otros. La IO utiliza técnicas formales para analizar y resolver estos problemas de manera óptima y eficiente.

## Técnicas y aplicaciones de la IO

La Investigación de operaciones (IO) es una disciplina que se ocupa del estudio y análisis de sistemas complejos y procesos de decisión en diversos contextos, con el objetivo de mejorar su eficiencia y efectividad. Para ello, se utilizan diversas técnicas y herramientas matemáticas y estadísticas. Algunas de las técnicas más comunes en la IO son:

-   Programación lineal: permite optimizar una función objetivo, sujeta a un conjunto de restricciones, mediante el uso de técnicas de optimización matemática.
-   Análisis de transporte: se utiliza para determinar la forma más eficiente de mover un producto o material desde un origen hasta un destino, minimizando costos de transporte.
-   Programación dinámica: permite modelar y resolver problemas que involucran decisiones a lo largo del tiempo, considerando factores como el costo y la incertidumbre.
-   Simulación: es una técnica que permite evaluar el comportamiento de un sistema o proceso a través de la repetición de escenarios hipotéticos.
-   Teoría de colas: se utiliza para modelar y analizar sistemas de atención y espera, como por ejemplo, una fila de personas esperando ser atendidas en una institución bancaria.

Algunas de las aplicaciones de la IO son:

-   Diseño y gestión de sistemas de producción y distribución.
-   Diseño y optimización de sistemas de transporte y logística.
-   Gestión de inventarios y suministros.
-   Diseño y gestión de sistemas de atención y servicio al cliente.
-   Gestión de proyectos y programas.
-   Diseño y optimización de sistemas de información y tecnología.

## Fundamentos de álgebra matricial

Los fundamentos de álgebra matricial son un conjunto de conceptos y herramientas matemáticas que se utilizan para trabajar con matrices, es decir, arreglos de números dispuestos en filas y columnas. Algunos de los conceptos fundamentales de álgebra matricial son:

-   Suma y resta de matrices: para sumar o restar dos matrices, deben tener la misma dimensión (es decir, el mismo número de filas y columnas). Se realiza elemento por elemento, es decir, se suman o restan los elementos correspondientes de cada matriz.

-   Multiplicación de una matriz por un escalar: para multiplicar una matriz por un escalar (un número), se multiplican todos los elementos de la matriz por ese escalar.

-   Multiplicación de matrices: para multiplicar dos matrices, deben cumplirse ciertas condiciones. La matriz resultante tendrá tantas filas como la primera matriz y tantas columnas como la segunda. El elemento ij-ésimo de la matriz resultante se obtiene multiplicando cada elemento de la i-ésima fila de la primera matriz por el elemento correspondiente de la j-ésima columna de la segunda matriz, y sumando todos esos productos.

-   Transpuesta de una matriz: la transpuesta de una matriz A es una matriz A\^T que se obtiene intercambiando filas por columnas en A.

-   Matriz inversa: una matriz inversa es una matriz A\^(-1) que, al multiplicarla por la matriz A original, da como resultado la matriz identidad.

-   Determinante de una matriz: el determinante de una matriz es un número que se puede calcular a partir de los elementos de la matriz y que tiene ciertas propiedades. Por ejemplo, si el determinante de una matriz es cero, la matriz no tiene inversa.

## Matriz inversa según el método de Gauss

Para obtener la matriz inversa de una matriz A mediante el método de Gauss, se puede seguir el siguiente proceso:

1.  Escribir la matriz A junto con la matriz identidad (I) de tamaño igual a la matriz A. Esto se conoce como la matriz aumentada (A\|I).

2.  Aplicar las operaciones elementales necesarias para convertir la matriz A en la matriz diagonal (en la que sólo hay elementos distintos de cero en la diagonal principal). Estas operaciones deben aplicarse también a la matriz identidad para mantener la relación entre ambas.

3.  Una vez que se ha obtenido la matriz diagonal, se puede obtener la matriz inversa aplicando las mismas operaciones elementales a la matriz identidad, pero en orden inverso y con los coeficientes cambiados de signo.


::: {.cell}

```{.r .cell-code}
# Para calcular la matriz inversa de una matriz A en R, puedes utilizar la 
# función solve() de la siguiente manera:
# Primero, debes cargar la matriz A

A <- matrix(c(1, 2, 3, 4), nrow = 2, ncol = 2)
# A
# Luego, puedes calcular la inversa de A utilizando solve()

A_inv <- solve(A)
# A_inv

# También puedes utilizar la función ginv() del paquete MASS, que utiliza el 
# método de Moore-Penrose para calcular la inversa generalizada de una matriz:

# Primero, debes cargar la matriz A y el paquete MASS

A <- matrix(c(1, 2, 3, 4), nrow = 2, ncol = 2)
library(MASS)

# Luego, puedes calcular la inversa de A utilizando ginv()
A_inv <- ginv(A)
```
:::


::: {#exm-ejemplo1}
Para obtener la matriz inversa de A.



```{=tex}
\begin{equation*}
A_{2 \times 2}=
\begin{pmatrix}
1 & 2 \\
3 & 4 
\end{pmatrix} _{2 \times 2}
\end{equation*}
```


Se puede seguir el siguiente proceso:

La matriz aumentada es A\|I =



```{=tex}
\begin{equation*}
A_{2 \times 2}=
\begin{pmatrix}
1 & 2 & 1 & 0 \\
3 & 4 & 0 & 1 
\end{pmatrix} _{2 \times 2}
\end{equation*}
```


Aplicar una operación elemental de intercambio de filas para convertir el primer elemento de la matriz A en 1:



```{=tex}
\begin{equation*}
A_{2 \times 2}=
\begin{pmatrix}
3 & 4 & 0 & 1 \\
1 & 2 & 1 & 0 
\end{pmatrix} _{2 \times 2}
\end{equation*}
```


Aplicar una operación elemental de multiplicación de fila por un escalar para que el primer elemento de la segunda fila sea -1:



```{=tex}
\begin{equation*}
A_{2 \times 2}=
\begin{pmatrix}
3 & 4 & 0 & 1 \\
-1 & -2 & -1 & 0 
\end{pmatrix} _{2 \times 2}
\end{equation*}
```


Aplicar una operación elemental de suma de filas para eliminar el primer elemento de la segunda fila:



```{=tex}
\begin{equation*}
A_{2 \times 2}=
\begin{pmatrix}
3 & 4 & 0 & 1 \\
0 & 0 & 0 & 1 
\end{pmatrix} _{2 \times 2}
\end{equation*}
```


Aplicar las operaciones elementales necesarias a la matriz identidad para obtener la matriz inversa:



```{=tex}
\begin{equation*}
A_{2 \times 2}=
\begin{pmatrix}
1/3 & -2/3 & 0 & -1/3 \\
0 & 0 & 0 & 1 
\end{pmatrix} _{2 \times 2}
\end{equation*}
```


Por tanto, la matriz inversa de A es:



```{=tex}
\begin{equation*}
A_{2 \times 2}=
\begin{pmatrix}
1/3 & -2/3 \\
0 & 1 
\end{pmatrix} _{2 \times 2}
\end{equation*}
```


:::
