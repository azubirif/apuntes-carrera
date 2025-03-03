---
title: Potencial Eléctrico
---
# Trabajo y energía potencial
Supongamos una carga $q_{2}$, sometida a un determinado campo eléctrico $\mathbf{E}$, generado por una carga $q_{1}$ (en reposo). La carga $q_{2}$ se sitúa inicialmente  en $\mathbf{r}_{i}$, y se desplaza, bajo el efecto del campo eléctrico, hasta $\mathbf{r}_{f}$.
![[trabajoElectrico.png]]
Este trabajo, aplicando la ley de Coulomb, termina siendo
$$
W=\int_{r_{i}}^{r_{f}} \frac{1}{4\pi\varepsilon_{0}} \frac{q_{1}q_{2}}{r^2}dr = -\left( \frac{q_{1}q_{2}}{4\pi\varepsilon_{0}r_{f}} - \frac{q_{1}q_{2}}{4\pi\varepsilon_{0}r_{i}} \right)=U_{i}-U_{f}=-\Delta U
$$
de aquí se deduce que el trabajo depende de la función **energía potencial** $U$. Esta depende únicamente de la posición de la partícula $q_{2}$ en cada momento $t$, y viene dada por
$$
\boxed{
U=\frac{1}{4\pi\varepsilon_{0}} \frac{q_{1}q_{2}}{|r|}
}
$$
El trabajo realizado al desplazar la carga de $\mathbf{r}_{i}$ a $\mathbf{r}_{f}$ se puede expresar como la diferencia de la energía potencial:
$$
W=-\Delta U
$$
De aquí se puede deducir que el trabajo realizado para desplazar no depende de la trayectoria, sino únicamente de lo punto inicial y final.
# Potencial eléctrico
Si la carga receptora $q_{2}$ está sometida a un campo eléctrico $\mathbf{E}$, se cumple que la fuerza generada es $\mathbf{F}=q_{2}\mathbf{E}$. Por tanto, el trabajo realizado por el campo eléctrico al desplazar $q_{2}$ se puede definir como
$$
\begin{align*}
W&=\int_{r_{i}}^{r_{f}}q_{2}\mathbf{E}\cdot \mathbf{dr}\\
\frac{W}{q_{2}} &= \int_{r_{i}}^{r_{f}}\mathbf{E}\cdot \mathbf{dr}\\
\frac{W}{q_{2}}&= \frac{q_{1}}{4\pi\varepsilon_{0}r_{i}}-\frac{q_{1}}{4\pi\varepsilon_{0}r_{f}}=-\Delta V
\end{align*}
$$
por tanto, definimos el **potencial eléctrico** como
$$
\boxed{
V(r) = \frac{q_{1}}{4\pi\varepsilon_{0}r}~ \left( \frac{J}{C} \right) = \frac{U}{q_{2}}~(V)
}
$$
que es la energía potencial por unidad de carga. También podemos deducir que
$$
[E]=\left[ \frac{V}{m} \right]
$$
# Campo Vectorial
Supongamos una carga $q_{1}$ que genera un campo eléctrico $\mathbf{E}$ sobre una carga de $1~(C)$ a una distancia $r$ del foco. Se dice que $\mathbf{E}$ es conservativo si cumple que:
- $\mathbf{E}$ solo depende de la posición, y no depende explícitamente del tiempo.
- Si se cumple $1$, existe una función $V(\mathbf{r})$ tal que $V(\mathbf{r}_{i})-V(\mathbf{r}_{f})=\frac{W}{q_{2}}$. La diferencia de potencial solo depende de la posición inicial y final de la carga desplazada.
- La integral del trabajo a lo largo de un camino cerrado es $0$. Consecuentemente, la circulación de un vector siempre es nula.
- $dV=-\mathbf{E}\cdot \mathbf{dr}$
