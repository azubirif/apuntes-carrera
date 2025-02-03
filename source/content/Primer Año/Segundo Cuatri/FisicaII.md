---
title: Física II
---
# Campo eléctrico
>[!info] Definición
>Definimos la **fuerza de Coulomb** entre dos cargas, siendo una fija (foco) y otra la que se mueve (receptora).
> $$
\vec{F} = \frac{1}{4\pi \varepsilon_{0}} \frac{q_1q_2}{r^{2}}\vec{u}_{r}= k_{0} \frac{q_1q_2}{r^{2}}\vec{u}_{r}~(N)
>$$
>Siendo $k_{0} = 9 \cdot 10^{9}~( \frac{Nm^{2}}{r^{2}})$, $\varepsilon_{0}$ la permitividad eléctrica del vacío, y $\vec{u}_{r}$ el vector que va desde el foco al receptor.

>[!info] Definición
>El campo eléctrico es una region en el espacio alrededor de una carga en la que se pueda situar otra carga receptora para que esta sufra una fuerza repulsora o atractora.
>$$
\vec{E} = \frac{1}{4\pi \varepsilon_{0}}\frac{q}{r^{2}}\vec{u}_{r}\left(\frac{N}{C}\right)
>$$

Podemos representar un campo eléctrico mediante punto-vector o líneas de fuerza.

>[!info] Definición
>Las líneas de fuerza es aquella que tienen como origen el foco, y su vector tangente es el campo eléctrico en cada uno de sus puntos.
## Sistema de cargas puntuales
Supongamos un conjunto de $N$  cargas $q_{1},\dots ,q_{n}$ y están situadas en
sus vectores $\vec{r}_{1},\dots ,\vec{r}_{n}$. La fuerza que actúa sobre una
carga receptora $Q$ cuyo vector posición es $\vec{r}_{p}$ es la suma vectorial
de las fuerzas creadas por el resto de las cargas:
$$
\begin{align}
\vec{F}_{p} &= \sum_{i=1}^{N} \frac{1}{4\pi\varepsilon_{0}}
		\frac{q_{i}Q}{|r_{p}-r_{i}|^{3}}(r_{p}-r_{i}) ~(N)\\
					&= \frac{Q}{4\pi\varepsilon_{0}}\sum_{i=1}^{N}
					\frac{q_{i}}{|r_{p}-r_{i}|^{3}}(r_{p}-r_{i})~(N)\\
					&= Q \sum_{i=1}^{N} \vec{E}_{i}~(N)
\end{align}
$$
# Sistemas de coordenadas
Para unas coordenadas necesitamos un origen $\vec{0}$, y una base. Para unas coordenadas cartesianas, tenemos los vectores $\vec{i}$ y $\vec{j}$:
![[plano_cartesiano.png]]
Sin embargo, también podemos utilizar las coordenadas polares, que consisten en una distancia al origen $r$, y un ángulo respecto al eje horizontal $\phi$.![[coords_polares.png]]
Para definir el ángulo, hay que tener en cuenta que, al desplazar el vector un ángulo, proyectamos el vector sobre el eje $x$ positivo, y giramos el vector en sentido anti horario hasta alcanzar la posición del vector original. Ese ángulo es nuestra coordenada $\phi$.
Si trazamos el vector unitario de $r$, su vector perpendicular $\vec{u}_{\phi}$ es tangencial al ángulo $\phi$.