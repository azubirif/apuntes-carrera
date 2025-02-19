---
title: Campo Eléctrico
---
# Campo eléctrico
Definimos la **fuerza de Coulomb** entre dos cargas, siendo una fija (foco) y otra la que se mueve (receptora).
$$
\vec{F} = \frac{1}{4\pi \varepsilon_{0}} \frac{q_1q_2}{r^{2}}\vec{u}_{r}= k_{0} \frac{q_1q_2}{r^{2}}\vec{u}_{r}~(N)
$$
Siendo $k_{0} = 9 \cdot 10^{9}~( \frac{Nm^{2}}{r^{2}})$, $\varepsilon_{0}$ la permitividad eléctrica del vacío, y $\vec{u}_{r}$ el vector que va desde el foco al receptor.

El campo eléctrico es una region en el espacio alrededor de una carga en la que se pueda situar otra carga receptora para que esta sufra una fuerza repulsora o atractora.
$$
\vec{E} = \frac{1}{4\pi \varepsilon_{0}}\frac{q}{r^{2}}\vec{u}_{r}\left(\frac{N}{C}\right)
$$
Podemos representar un campo eléctrico mediante punto-vector o líneas de fuerza. Las líneas de fuerza es aquella que tienen como origen el foco, y su vector tangente es el campo eléctrico en cada uno de sus puntos.
## Sistema de cargas puntuales
Supongamos un conjunto de $N$  cargas $q_{1},\dots ,q_{n}$ y están situadas en
sus vectores $\vec{r}_{1},\dots ,\vec{r}_{n}$. La fuerza que actúa sobre una
carga receptora $Q$ cuyo vector posición es $\vec{r}_{p}$ es la suma vectorial
de las fuerzas creadas por el resto de las cargas:
$$
\begin{align*}
\vec{F}_{p} &= \sum_{i=1}^{N} \frac{1}{4\pi\varepsilon_{0}}
		\frac{q_{i}Q}{|r_{p}-r_{i}|^{3}}(r_{p}-r_{i}) ~(N)\\
					&= \frac{Q}{4\pi\varepsilon_{0}}\sum_{i=1}^{N}
					\frac{q_{i}}{|r_{p}-r_{i}|^{3}}(r_{p}-r_{i})~(N)\\
					&= Q \sum_{i=1}^{N} \vec{E}_{i}~(N)
\end{align*}
$$
# Sistemas de coordenadas
Para unas coordenadas necesitamos un origen $\vec{0}$, y una base. Para unas coordenadas cartesianas, tenemos los vectores $\vec{i}$ y $\vec{j}$:
![[plano_cartesiano.png]]
Sin embargo, también podemos utilizar las coordenadas polares, que consisten en una distancia al origen $r$, y un ángulo respecto al eje horizontal $\phi$.![[coords_polares.png]]
Para definir el ángulo, hay que tener en cuenta que, al desplazar el vector un ángulo, proyectamos el vector sobre el eje $x$ positivo, y giramos el vector en sentido anti horario hasta alcanzar la posición del vector original. Ese ángulo es nuestra coordenada $\phi$.
Si trazamos el vector unitario de $r$, su vector perpendicular $\vec{u}_{\phi}$ es tangencial al ángulo $\phi$.
Para poder cambiar entre coordenadas cartesianas y polares, utilizamos las siguientes ecuaciones:
$$
\boxed{\begin{align}
x &= |r|\cos \phi\\ y &= |r|\sin \phi\\r^{2}&= x^{2}+y^{2} \\
\phi &= \arctan \frac{y}{x}\\
\vec{u}_{r} &= (\cos \phi, \sin \phi) \\
\vec{u}_{\phi} &= (-\sin \phi, \cos \phi)
\end{align}}
$$
Respecto a la velocidad en coordenadas polares, tenemos el siguiente desarrollo:
$$
\begin{align}
v^{2}&=\dot{x}^{2}+\dot{y}^{2} \\
&=\dot{r}^{2}\cos ^{2}\phi-2\dot{r} r \dot{\phi}\sin \phi \cos \phi+r^{2}\sin ^{2}\phi
\dot{\phi}^{2} \\
&+\dot{r}^{2}\sin ^{2}\phi+2 \dot{r}r \dot{\phi}\sin \phi \cos \phi+ r^{2}\cos ^{2}\phi \dot{\phi}^{2} \\
&= \dot{r}^{2}+r^{2} \dot{\phi}^{2}
\end{align}
$$
## Distribución de cargas continuas
En estas distribuciones se considera que no se pueden distinguir dos cargas vecinas. Por tanto, consideramos que la carga total $Q$ se distribuye de forma continua a lo largo de un determinado volumen, superfície, etc. Esta aproximación es válida cuando se estudia el campo eléctrico a grandes distancias del objeto cargado.
Vamos a estudiar las diferentes distribuciones:
- **Lineal**: se considera que la carga está distribuida a lo largo de un determinado camino:
$$
\lambda=\frac{Q}{l}
$$
Cuando este valor es constante, la densidad es **homogénea**. Si tomamos un incremento de longitud $dl$, encontramos un diferencial de carga $dq$, obteniendo que
$$
\lambda = \frac{dq}{dl}
$$
- **Superficial**: se asume que toda la carga está distribuida a lo largo de toda la superficie. En este caso:
$$
\sigma = \frac{dq}{dS}
$$
- **Volumétrica**: de la misma forma, la carga se distribuye a lo largo de un determinado volumen:
$$
\rho = \frac{dq}{dV}
$$
# Flujo eléctrico
El flujo eléctrico es una medida del flujo del campo eléctrico que atraviesa una superfície:
$$
\phi = \int_{S} \mathbf{E}\cdot \mathbf{n}~dA~\left( \frac{N\cdot m^{2}}{C} \right)
$$
Donde $\mathbf{E}$ es el campo eléctrico y $\mathbf{n}$ es el vector normal a la superfície en cada punto.
Si dividimos la superficie total en áreas infinitesimalmente pequeñas $dA$. El flujo infinitesimal $d\phi$ que atraviesa esa superficie es
$$
d\phi=\mathbf{E}\cdot \mathbf{n}~dA
$$
El flujo que atraviesa una superficie cerrada se expresa de la siguiente forma:
$$
\phi = \oint_{S} \mathbf{E}\cdot d \mathbf{s}
$$
## Teorema de Gauss
El teorema establece que el flujo **neto** que atraviesa una superficie cerrada $A$ es igual a la carga total $Q$ entre la permitividad del espacio encerrada por la superficie:
$$
\phi_{neto}=\oint_{A} \mathbf{E}\cdot \mathbf{n}~dA=\frac{Q_{interior}}{\varepsilon_{0}}
$$

# Coordenadas cilíndricas
![[coords_cil.png]]
Las coordenadas cilíndricas se definen como
$$
\mathbf{r}=(\rho, \phi, z)
$$
Donde $\rho$ es el radio en el plano $XY$, $\phi$ es el ángulo (en sentido antihorario) con respecto al eje $X$, y $z$ es la "altura" o desplazamiento respecto al eje $XY$. En coordenadas cartesianas, esto sería
$$
\mathbf{r}=(\rho \cos \phi, \rho \sin \phi, z)
$$
La base definida por este sistema de coordenadas es:
$$
\{(\cos \phi,\sin \phi,0), (-\sin \phi,\cos \phi), (0,0,1) \}
$$
# Coordenadas esféricas
El punto $P$ se define mediante unas coordenadas esféricas.
$$
P = (r,\phi,\theta):~\theta \in[0,\pi],~\phi \in[0,2\pi]
$$
En coordenadas cartesianas, esto pasa a ser:
$$
P=(r\sin\theta \cos \phi, r\sin\theta \sin \phi, r\cos\theta)
$$
![[spher_coords.jpg]]
# Electrización de un cuerpo
> [!info] Dipolo eléctrico
> Un sistema formado por un centro de carga (positivo y negativo). La carga positiva es igual y opuesta a la negativa. La distancia entre ambos centros son constantes.

> [!info] Momento dipolar
> A todo dipolo se le asocia un momento dipolar $\mathbf{p}$. El origen de este vector está en el **centro de carga negativo**. La dirección de este es la recta que une el centro de carga negativo con el positivo.
> El módulo de este viene dado por
> 
> $$
> |\mathbf{p}|=q\cdot d~(C\cdot m)=(e\cdot pm)
> $$
> 
> Cada enlace tendrá asociado un momento dipolar, y el total será la suma de todos ellos. Una molécula es **apolar** si su momento dipolar total es $0$.

## Campo eléctrico creado por un dipolo
Viene dado por las siguientes ecuaciones
$$
\begin{align*}
\mathbf{E}_{r}&=\frac{2p\cos\theta}{4\pi\varepsilon_{0}r^{3}} \mathbf{u}_{r}\\
\mathbf{E}_{\theta}&= \frac{p \sin\theta}{4\pi\varepsilon_{0}r^{3}}\mathbf{u}_{\theta}
\end{align*}
$$
## Par de fuerza sobre un dipolo en un campo exterior
Situamos un dipolo en el interior de un campo eléctrico dado por $\mathbf{E}=E_{0}\mathbf{u}_{r}$. El dipolo gira, y se genera un momento de fuerza dado por
$$
\vec{\tau}= \vec{p}\times \vec{E}
$$
![[dipolo_en_E.jpg]]
Se puede observar como el torque final es **entrante** al plano.

---
Un metal se caracteriza por una estructura formada por átomos de carácter metálico, tiene un elevado número atómico, y las estructuras son **cristalinas compacta**.
El científico Drude estableció que, un metal está formado por una red compacta de iones positivos, y de una nube de electrones de valencia que están **ligeramente** unidos a los núcleos de los átomos. Cuando se eleva la energía térmica los electrones se mueven a los átomos colindantes. El resultado es la nube electrónica que rodea a la red iónica positiva. Cuando se aplica un campo eléctrico, los electrones de valencia se mueven por la red. En general existen dos bandas diferenciadas de electrones:
- Banda de electrones de valencia: electrones próximos al átomo que se mantienen confinados dentro del propio átomo.
- Banda de electrones de conducción: electrones que se van a mover ante un campo eléctrico, y son responsables de la conducción eléctrica (electrones deslocalizados).
Si se acerca una carga a un conductor, se produce un movimiento de los electrones en la banda de conducción de tal forma que los electrones se sitúan en la superficie del cuerpo. La carga en el interior siempre es nula, y por tanto el campo eléctrico en el interior es también nulo.
