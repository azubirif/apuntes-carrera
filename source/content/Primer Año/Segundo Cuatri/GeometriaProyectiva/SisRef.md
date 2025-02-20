---
title: Sistemas de referencias y coordenadas
---
Para definir un espacio afín, tenemos dos elementos:
- Una referencia formada por un conjunto de puntos.
- Un sistema de coordenadas.
Podemos definir cualquier punto como
$$
Q=P+\mathbf{v}
$$
por tanto, un subespacio afín como
$$
L=P+\mathcal{L}\{ \mathbf{v}_{i} \}
$$
y finalmente, nuestro espacio afín como
$$
A=P+\mathbb{V}
$$
Como el espacio vectorial tendrá una base $B$, podemos definir el espacio como
$$
A=P+B
$$

> [!info] Combinación afín
> Dados los puntos $\{ P_{i} \}$ y los escalares $\{ \lambda_{i} \}$ tal que $\lambda_{i}=1$, la combinación afín es
> 
> $$
> P=\sum_{i=0} \lambda_{i} \mathbf{P_{0}P_{i}}
> $$
> 
> Entonces se dice que $P$ es combinación afín de los puntos $P_{0},\dots,P_{r}$

> [!success] Corolario
> Sea $A$ un SA de dimensión $n$ con puntos $P_{0},\dots,P_{r}$. Entonces
> - Si $P_{0},\dots,P_{r}$  son afínmente independientes, $r \leq n$
> - Si $P_{0},\dots,P_{r}$ son afínmente generadores, $r \geq n$
> - Si $P_{0},\dots,P_{r}$ son referencia afín, $r=n+1$
>   

> [!tip] Sistema de referencia
> Sea un espacio afín $(A,V,\phi)$ de dimensión $n$, llamamos sistema de referencia a cualquier conjunto de $n+1$ puntos de $A$ tal que, fijado uno de ellos, se obtiene una base $B$ del sistema vectorial $\mathbb{V}$.
> - **Base**: $B=\{ \mathbf{P_{1}P_{2}},\dots,\mathbf{P_{1}P_{n+1}} \}$
> - **SR**: $\{ O,B \}$
>   

> [!tip] Sistema de referencia cartesiano
> Es aquel donde el origen $O$ es el punto $0$ y la base es la base canónica.

Existe una correspondencia entre la referencia cartesiana y la afín. Dada una referencia cartesiana
$$
R_{c}=\{ O;B=\{ \mathbf{v}_{1},\dots,\mathbf{v}_{n} \} \}
$$
le asociamos la referencia afín
$$
R_{\alpha}=\{ P_{0}=O,P_{1}=O+\mathbf{v}_{1},\dots,P_{n}=O+\mathbf{v}_{n} \}
$$

> [!success] Teorema de la base
> En todo espacio vectorial finitamente generado existe siempre una base con tantos elementos como dimensión del espacio vectorial.

# Coordenadas
## Afines de un punto
Teniendo una base $B=\{ \mathbf{v}_{1},\dots,\mathbf{v}_{n} \}$, un punto $X$, el vector $\mathbf{OX}$ se podrá expresar únicamente como
$$
\mathbf{OX}=\sum_{i=1}^n\lambda_{i}\mathbf{v}_{i}
$$
Y los valores $\lambda_{i}$ son las **coordenadas afines** del punto $X$ respecto a nuestro sistema de referencia.
## De un vector por dos puntos
Dados dos puntos $A,B$, el vector se define como
$$
\mathbf{AB}=(b_{1}-a_{1},\dots,b_{n}-a_{n})
$$
La aplicación  que envía un punto $P$ a las coordenadas de $P$ respecto a $R$ es un **isomorfismo afín**.
## Del punto medio de un segmento
Teniendo dos puntos $A,B$ y el $M$ el punto medio del segmento $\mathbf{AB}$, entonces
$$
\mathbf{OM}=\mathbf{OA}+\frac{1}{2}\mathbf{AB}
$$
## Baricéntricas
Sean $P_{0},\dots,P_{n}$ puntos afínmente independientes. Entonces una referencia afín
$$
R=\{ P_{0},\dots,P_{n} \}
$$
es un sistema de referencia baricéntrico de $A$. Dado un punto $X$, si $x_{0},\dots,x_{n}$ son los únicos escalares tales que
$$
x_{0}\mathbf{XP_{0}}+\dots+x_{n}\mathbf{XP_{n}}=0,~ x_{0}+\dots+x_{n}=1
$$
entonces $X=(x_{0},\dots,x_{n})$ son sus coordenadas baricéntricas.