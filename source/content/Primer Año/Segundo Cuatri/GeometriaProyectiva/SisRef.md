---
title: Sistemas de referencias y coordenadas 🤓
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
> Dados los puntos $\{ P_{i} \}$ y los escalares $\{ \lambda_{i} \}$ tal que $\sum\lambda_{i}=1$, la combinación afín es
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
# Cambio de sistema de referencia
Sea $(A,\mathbb{V},\phi)$ un espacio afín y sean
$$
\begin{align*}
R&=\{ O;B=\{ \mathbf{v}_{1},\dots,\mathbf{v}_{n} \} \}\\
R'&=\{ O',B'=\{ \mathbf{u}_{1},\dots,\mathbf{u}_{n} \}\}
\end{align*}
$$
dos sistemas de referencia afines de $A$.
Sea $P\in A:P(x_{1},\dots,x_{n})_{R}=(y_{1},\dots,y_{n})_{R'}$.
Entonces, el vector que va desde $O$ hasta $P$ se define como
$$
\boxed{\mathbf{OP}=\mathbf{OO'}+\mathbf{O'P}}
$$
Esto se cumple debido a la **relación de Chasles**.
Esta relación nos permite obtener el vector que une el origen de un sistema de referencia a un punto, si tenemos el vector que une ambos orígenes, y el vector que va desde el segundo origen al punto.
También nos permite obtener el vector que relaciona dos orígenes, si tenemos los vectores que van a un mismo punto desde dos sistemas de referencia.
El vector $\mathbf{OP}$ se define como
$$
\mathbf{OP}=\sum_{i=1}^n\lambda_{i}\mathbf{v}_{i}
$$
mientras que $\mathbf{O'P}$ se define como
$$
\mathbf{O'P}=\sum_{i=1}^n\mu_{i}\mathbf{u}_{i}
$$
Es decir, cada vector está respecto a su propia base (aquella definida por el sistema de referencia) y por tanto tendrá sus propias coordenadas.

> [!note] Cada sistema de referencia (siempre que cumpla las condiciones adecuadas) es válido, y no existe una preferencia para un determinado sistema. Por tanto, es conveniente buscar un sistema de referencia (siempre que sea posible) que simplifique el problema a resolver.

## Matriz de cambio de sistema de referencia
Esta matriz se define como
$$
M_{R'R}= \begin{pmatrix}
1 & 0 \\
a & M_{B'B}
\end{pmatrix}
$$
Donde $a$ son las coordenadas de $O'$ respecto de $R$, y es una matriz de $n\times 1$.
Esta matriz es la de cambio de sistema de referencia de $R'$ a $R$.

> [!tip] Corolario
> Si se desarrolla el determinante (por adjuntos) de $M_{R'R}$ por la primera fila, se observa que esta es igual al determinante de la matriz $M_{B'B}$. Como esta última tiene determinante distinto de $0$ (ya que esta matriz debe ser invertible), entonces la matriz $M_{R'R}$ es también invertible.
> 
> $$
> M_{R'R}=M_{R R'}^{-1}
> $$

A menudo esta ecuación acaba siendo
$$
P_{R}=O'+M_{B'B}P_{R'}
$$
Con esto se dan diversas situaciones. Supongamos dos sistemas de referencia como descritos anteriormente.
- Si se cumple que $O=O'$, entonces el punto de referencia es el mismo y por tanto solo cambia la base.
- Si $\forall i~\mathbf{u}_{i}=\mathbf{v}_{i}$, entonces los vectores de la base no cambian (la matriz de cambio de sistema es la identidad) y por tanto solo estamos trasladando el origen.
- Si se cumplen ambas propiedades, (evidentemente) ambos sistemas de referencia coinciden.

## Teorema
Cualquier transformación afín se puede escribir como un producto entre una transformación afín y una traslación que deja invariante un punto. Se pueden escribir en forma matricial como

$$
\begin{pmatrix}
M & v \\
0 & 1
\end{pmatrix}=
\begin{pmatrix}
I & v \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
M & 0 \\
0 & 1
\end{pmatrix}
$$
La matriz $M$ es la transformación que deja un punto $P$ fijo, y $v$ representa el vector de la traslación.

Sean dos espacios afines, y sea $R=\{ O,\mathcal{B}=\{ \mathbf{v}_{i} \} \}$ la referencia cartesiana de la primera. Sea $O'$ un punto cualquiera de $A'$ y sean $\{ \mathbf{v}_{i}' \}$ vectores cualesquiera de $\mathbb{V}'$.
Existe una única **aplicación afín** $f$ tal que $f(O)=O'$ y cuya aplicación lineal asociada cumple que
$$
\bar{f}(\mathbf{v}_{i})=\mathbf{v}_{i}'
$$
Además, dados $\{ P_{i} \}~n+1$ puntos **afínmente indepedientes** de $A$, y $\{ P_{i}' \}~n+1$ puntos de $A'$ existe una única aplicación afñin tal que
$$
f(P_{i})=P_{i}'
$$
Si se tienen dos espacios afines de dimensión $n$, teniendo una aplicación afín $f$ de $\mathbb{A}$ a $\mathbb{A'}$, las siguientes afirmaciones son equivalentes:
1. $f$ es un isomorfismo afín.
2. Existe una referencia cartesiana $\{ O;B \}$ de $\mathbb{A}$ que $f$ transforma en una referencia cartesiana de $\mathbb{A}'$.
3. Existe un conjunto de $n+1$ puntos afínmente independientes de $\mathbb{A}$ que $f$ transforma en un conjunto de $n+1$ puntos afínmente independientes de $\mathbb{A}'$.

Teniendo dos espacios afines de dimensión $n$ y $m$, cada uno con sus respectivas referencias cartesianas $R$ y $R'$, con la aplicación afín $f:A\to A'$ y su respectiva aplicación lineal asociada $\bar{f}$, y siendo $M$ la matriz de $\bar{f}$ respecto de las bases $B$ y $B'$.
Si las coordenadas de $P\in A$ de $R$ son $(x_{i})$ y las coordenadas de $f(P)$ respecto de $A'$ son $(y_{i})$, se tiene que
$$
M\cdot X+D=Y
$$
Donde $X=(x_{1},\dots,x_{n})^{T}$ y $D$ es la matriz fila traspuesta formada por las coordenadas de $f(O)$ respecto a $R'$.
Realmente estamos afirmando que
$$
f(P)=f(O')+M\cdot P
$$
# Composiciones de aplicaciones afines con matrices
Sean tres espacios afines con sus respectivas referencias cartesianas $R_{1},R_{2}R_{3}$. Sean $h:A_{1}\to A_{2}$ y $g:A_{2}\to A_{3}$ dos aplicaciones afines, sea $f=g\circ h =g(h)$. Entonces
$$
M_{R_{1}R_{3}}(f)=M_{R_{2}R_{3}}(g)\cdot M_{R_{1}R_{2}}(h)
$$
**Propiedades**
1. Dados dos espacios afines, cada uno con dos referencias cartesianas $R_{1},R_{2}$ y $R_{1}',R_{2}'$, siendo $f:A\to A'$, entonces
   $$
M_{R_{2}R_{2}'}(f)=M_{R_{1}'R_{2}'}\cdot M_{R_{1}R_{1}'}(f)\cdot M_{R_{2}R_{1}}
$$

![[propiedad_matrices_referencias.excalidraw]]
1. Teniendo dos espacios afines de la misma dimensión, con sus respectivas referencias cartesianas $R,R'$, y siendo $f:A\to A'$ un isomorfismo afín, entonces $M_{R R'}(f)$
   $$
M_{R'R}(f^{-1})=(M_{R R'}(f))^{-1}
$$