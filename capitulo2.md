# Optmización lineal contínua

La optimización lineal contínua es una técnica matemática que se utiliza para encontrar el valor óptimo de una función lineal sujeta a ciertas restricciones o condiciones. Esta técnica se aplica a problemas que involucran variables que pueden tomar cualquier valor en un rango específico, en lugar de solo valores discretos. Los problemas de optimización lineal contínua se pueden resolver utilizando diferentes métodos, como el método simplex o el algoritmo de punto interior. La optimización lineal contínua se utiliza en diversas áreas, como la ingeniería, la economía y la ciencia de la computación.

## Modelo general de Programación Lineal (PL)

La Programación Lineal (PL) es una técnica de optimización que se utiliza para encontrar el valor óptimo de una función de varias variables (llamada función objetivo) sujeta a un conjunto de restricciones. En el modelo general de PL, la función objetivo y las restricciones están expresadas mediante ecuaciones o inecuaciones que involucran una combinación lineal de las variables. La solución del problema de PL consiste en encontrar los valores de las variables que optimizan la función objetivo, sujeto a cumplir con las restricciones.

El modelo general de Programación Lineal (PL) puede ser representado de la siguiente manera en LaTeX:

## Variables de decisión

## Función Objetivo

## Restricciones

## Formulación de modelos de PL

## Algunos casos de estudios clásicos

## Método Gráfico

problema en forma estándar


Representar gráficamente las restricciones



```{=latex}
\begin{tikzpicture}
\begin{axis}[
    axis lines=middle,
    xmin=0, xmax=80,
    ymin=0, ymax=140,
    xtick={0,40,80},
    ytick={0,80,120,140},
    xlabel={$x_1$},
    ylabel={$x_2$}
]
\addplot[domain=0:80, samples=2, thick, blue]{80-x};
\addplot[domain=0:80, samples=2, thick, red]{(220-3*x)/2};
\addplot[domain=0:80, samples=2, thick, green]{(210-2*x)/3};
\end{axis}
\end{tikzpicture}
```


Identificar el conjunto solución factible.



```{=latex}
\begin{tikzpicture}
\begin{axis}[
    axis lines=middle,
    xmin=0, xmax=80,
    ymin=0, ymax=140,
    xtick={0,40,80},
    ytick={0,80,120,140},
    xlabel={$x_1$},
    ylabel={$x_2$},
    fill=gray, opacity=0.3
]
\addplot[domain=0:40, samples=2, thick, blue]{80-x};
\addplot[domain=40:80, samples=2, thick, blue]{120-3*x/2};
\addplot[domain=0:60, samples=2, thick, red]{(220-3*x)/2};
\addplot[domain=60:80, samples=2, thick, red]{(210-2*x)/3};
\addplot[domain=0:80, samples=2, thick, green]{(210-2*x)/3};
\filldraw[green] (0,80) -- (40,120) -- (60,80) -- cycle;
\end{axis}
\end{tikzpicture}
```



Identificar los puntos extremos del conjunto solución factible.



```{=latex}
\begin{tikzpicture}
\begin{axis}[    axis lines=middle,    xmin=0, xmax=80,    ymin=0, ymax=140,    xtick={0,40,80},    ytick={0,80,120,140},    xlabel={$x_1$},    ylabel={$x_2$},    fill=gray, opacity=0.3]
\addplot[domain=0:40, samples=2, thick, blue]{80-x};
\addplot[domain=40:80, samples=2, thick, blue]{120-3*x/2};
\addplot[domain=0:60, samples=2, thick, red]{(220-3*x)/2};
\addplot[domain=60:80, samples=2, thick, red]{(210-2*x)/3};
\addplot[domain=0:80, samples=2, thick, green]{(210-2*x)/3};
\filldraw[green] (0,80) -- (40,120) -- (60,80) -- cycle;
\draw[black,dashed] (0,80) -- (40,120) -- (60,80);
\draw[black,dashed] (0,80) -- (60,80);
\draw[black,dashed] (40,120) -- (60,80);
\filldraw[black] (0,80) circle (2pt);
\filldraw[black] (40,120) circle (2pt);
\filldraw[black] (60,80) circle (2pt);
\end{axis}
\end{tikzpicture}
```


### Casos Especiales del Método Gráfico



## Ejercicios de aplicación
