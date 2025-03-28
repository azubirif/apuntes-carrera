---
title: Espacio Afín
---
# El espacio afín
Dados un conjunto de elementos, siendo estos puntos, $A$, y un espacio vectorial $\mathbb{V}$, llamamos el espacio afín a la terna $(A,\mathbb{V},\varphi)$, siendo $\varphi$ una aplicación entre elementos de $A$, tal que:
$$
\varphi: A \times A \mapsto \mathbb{V}
$$
Esta terna debe cumplir que:
- $\forall p \in A \wedge \mathbf{v} \in \mathbb{V}, \exists! Q \in A/ \varphi(P,Q) = \mathbf{PQ}=\mathbf{u}=Q-P$
- Relación de Chasles: $\forall P,Q,R \in A \wedge\varphi (P,Q) + \varphi (Q,R) = \varphi (P,R)$
$$
\mathbf{PQ} + \mathbf{QR} = \mathbf{PR}
$$
**Demostración**
- $\mathbf{PQ}=Q-P$
- $\mathbf{QR}=R-Q$ 
$$
\mathbf{PQ}+\mathbf{QR} = Q-P +R-Q = R-P = \mathbf{PR} 
$$
La dimensión del espacio afín va a ser la dimensión de $\mathbb{V}$. 
## Propiedades del espacio afín
1. $\forall P \in A, \varphi(P,P)=0$
2. $\varphi(P,Q)=0 \iff P=Q$
3. $\forall P,Q \in A, \varphi(P,Q) = -\varphi(Q,P)$
4. Regla del paralelogramo: $\forall P,Q,R,S \in A$:
$$
\varphi(P,Q)=\varphi(R,S) \iff \varphi (P,R) = \varphi (Q,S)
$$
# Vector de posición
Es un vector que representa la posición de un punto en el espacio respecto a un origen, además de la distancia que separa dichos puntos. El vector $\mathbf{OP}$ es el vector que une el origen al punto $P$. Esta aplicación es **biyectiva** (injectiva y sobreyectiva).
**Demostración**
Supongamos que no es inyectiva. Es decir, existen dos $\varphi(x)=\varphi (y) / x \neq y$ 
$$
\begin{align}
\mathbf{OP}+\mathbf{PQ}&=\mathbf{OQ} \\
\mathbf{P}+\mathbf{PQ}&=\mathbf{Q} \\
\mathbf{P}=\mathbf{Q} &\implies \mathbf{OP}=\mathbf{OQ} \\
&\implies P = Q
\end{align}
$$
# Estructura afín canónica
Dado un espacio vectorial $\mathbb{V}$, la aplicación $\varphi$
$$
\varphi: \mathbb{V} \times \mathbb{V} \to \mathbb{V}; \mathbf{uv}=\mathbf{v}-\mathbf{u}
$$
satisface los axiomas de la definición de un espacio afín y define una estructura de espacio afín $(\mathbb{V}, \mathbb{V}, \varphi)$ conocida como la estructura afín canónica de $\mathbb{V}$.
## Traslación  de un vector
Dado $\mathbf{v}\in \mathbb{V}$, la traslación de un vector es la aplicación
$$
\tau_{\mathbf{v}}: A \to A
$$
$$
\tau_{\mathbf{v}} (P)=P+\mathbf{v}=Q
$$
Una traslación de vector $\mathbf{v}$ transforma el punto $P$ a otro punto $Q$.
### Propiedades de traslación
- $\tau_{\mathbf{0}}(P)=P$
- $\tau_{\mathbf{u}} \circ \tau_{\mathbf{v}}=\tau_{\mathbf{v}} \circ\tau_{\mathbf{u}}=\tau_{\mathbf{u}+\mathbf{v}}$
## Teorema
Cualquier transformación afín se puede escribir como un producto de una transformación afín.
# Suma de un punto y un vector
Fijado $P \in A$, denotaremos por $F_{P}: A \to \mathbf{A}$ a la aplicación dada por $F_{P}(Q)=\mathbf{PQ}$. Si $P \in A$ y $\mathbf{v}\in A$, el único punto $Q\in A$ dado, tal que $\mathbf{PQ}=\mathbf{v}$ se denotará como $P+\mathbf{v}$.
Como consecuencia la siguientes identidades son inmediatas:
$$
Q=P+\mathbf{PQ} \quad \mathbf{P(P+v)}=\mathbf{v}
$$
## Propiedades
- $P+\mathbf{0}=P,~\forall P\in A$
$Q = P + \mathbf{PQ}, P = Q \implies \mathbf{PQ}=\mathbf{0}$.
- $P+\mathbf{u}+\mathbf{v}=(P+\mathbf{u})+\mathbf{v}$
- $\forall P\in A,\mathbf{u},\mathbf{v}\in \mathbf{A}, \overrightarrow{(P+\mathbf{u})(P+\mathbf{v})}=\mathbf{v}-\mathbf{u}$
	- $P+\mathbf{u}=Q$
	- $P+\mathbf{v}=R$
	- $\mathbf{QR}=R-Q=\overrightarrow{(P+\mathbf{u})(P+\mathbf{v})}=\mathbf{v}+P-\mathbf{u}-P=\mathbf{v}-\mathbf{u}$
# Subespacios afines
$$
\begin{pmatrix}
a_{11}x_{1}+\dots+a_{1n}x_{n}=0 \\
a_{21}x_{1}+\dots+a_{2n}x_{n}=0 \\
\dots \\
a_{n_{1}}x_{1}+\dots+a_{nn}x_{n}=0
\end{pmatrix}
$$
Si el sistema de ecuaciones es homogéneo, este genera un **subespacio vectorial**. Si no es homogéneo, el conjunto de soluciones genera un **subespacio afín**.
El subespacio vectorial es el asociado al conjunto de soluciones del sistema no homogéneo que generan el subespacio afín.
## Definición
Sea $(A,\mathbb{V},\varphi)$ un espacio afín real. Un subconjunto no vacío $L\subset A$ es un subespacio afín de $A$ si existe un subespacio $W\subset V$ tal que $(L,W,\varphi)$ satisface la restricción de $\varphi$ A $L$.
## Dimensión
La dimensión del espacio afín es la dimensión del subespacio vectorial asociado.
Si tenemos subespacios afines $L_{1} \subseteq L_{2}\subseteq A$ entonces
$$
dim(L_{1})\leq dim(L_{2})\leq dim(A)
$$
Además, $L_{1}=L_{2} \iff dim(L_{1})=dim(L_{2})$.
### Definición
Dado un espacio afín de dimension $n$, un hiperplano es un subespacio afín de dimensión $n-1$.
### Ecuación
Un hiperplano afín en un espacio $n$-dimensional se describe por una ecuación lineal no degenerada de la siguiente forma:
$$
a_{1}x_{1}+\dots a_{n}x_{n}=b
$$
Si $b=0$, el hiperplano pasa por el origen.
### Operaciones con subespacios afines
**Intersección**
Supongamos un espacio afín $(A,\mathbb{V},\varphi)$ y otros dos subespacios afines $L_{1}$ y $L_{2}$. Sea $\{ L_{i} \}_{i\in \mathbb{N}}$ una familia de subespacios afines de $A$.
Si $\bigcap L_{i} \neq \phi$, entonces la intersección es un subespacio afín de $A$ con dirección $\bigcap W_{i}$. El subespacio afín final sería
$$
\left( \bigcap L_{i}, \bigcap W_{i}, \phi_{\cap} \right)
$$
Donde $\phi_{\cap}$ es la aplicación que relaciona la intersección de los subespacios con la intersección de los subespacios vectoriales.
Si la intersección es no vacía
$$
\overrightarrow{L_{1}\cap L_{2}}=\overrightarrow{L_{1}}\cap \overrightarrow{L_{2}}
$$
Con esto llegamos a la siguiente definición

> [!info] Subespacio afín generado
> Sea $S\subset A$ un conjunto no vacío. Definimos el subespacio afín generado por $S$, denotado por $V(S)$, como el **menor subespacio afín** de $A$ que contiene a $S$. Siendo $L_{i}$ el conjunto de espacios vectoriales tal que $S \subset L_{i} \forall L_{i}$
> 
> $$
> V(S) = \bigcap L_{i}
> $$
> Dados puntos $\{ P_{i} \}\subset A$, el subespacio afín que generan viene dado por todas sus **combinaciones lineales afines**:
> $$
> V(\{ P_{i} \})=\sum \lambda_{i}P_{i} :\lambda_{i} \in K, \sum\lambda_{i}=1
> $$
> y tiene dirección $L(\vec{P_{0}P_{1}},\vec{PoP_{r}})$

Dados un conjunto de puntos $\{ P_{i} \}$, decimos que son
- **afínmente independientes** si y solo si
$$
dim(V(\{ P_{0},\dots,P_{r} \}))=r
$$
- **afínmente generadores** de $A$ si y solo si
$$
dim(V(\{ P_{0},\dots,P_{r} \}))=dimA
$$
**Ejemplo**:
Sean dos puntos $P,Q \in A$ que generan una recta de dimensión $1$ con dirección $\mathcal{L}\{ \vec{PQ} \}$
$$
Q=P+\lambda\vec{PQ}=P+\lambda(Q-P)=P(1-\lambda)+\lambda Q
$$
Si ahora sumamos las constantes que multiplican cada punto:
$$
\sum\lambda_{i}= 1-\lambda+\lambda=1
$$
**Suma de subespacios afines**

Definimos la suma como el subespacio generado por la unión de los subespacios, que es el mínimo subespacio afín que contiene a todos los subespacios de la suma:
$$
\sum L_{i}= V\left( \bigcap L_{i} \right)
$$
Dados subespacios afines $L_{i} \subset A$ de la forma $L_{i}=P_{i}+W_{i}$, su suma es un subespacio afín que tiene por dirección
$$
\mathcal{L}\{ \vec{P_{i}P_{j}} \}+\sum W_{i}
$$
Sea la suma de $L_{1}$ y $L_{2}$ el menor subespacio afín que contiene a ambos. Si $L_{1}=P_{1}+W_{1}$ y $L_{2}=P_{2}+W_{2}$ entonces
$$
L_{1}+L_{2}=P_{1}+W_{1}+W_{2}+\mathcal{L}\{ \vec{P_{1}P_{2}} \}
$$

> [!info] Fórmula de Grassmann
> La fórmula de Grassmann relaciona la dimensión de la suma de los subespacios vectoriales y es la siguiente:
> $$
> dim(U+V)=dim(U)+dim(V)-dim(U\cap V)
> $$
> 
> Ahora podemos relacionar esta ecuación con los subespacios afines. Como la dimensión de los SEA es igual a la dimensión de su SEV, simplemente sustituimos:
> $$
> dim(L_{1}+L_{2})=dimL_{1}+dimL_{2}-dim(L_{1}\cap L_{2})+ \varepsilon
> $$
> Donde $\varepsilon$ es:
> - $\varepsilon = 0 : L_{1}\cap L_{2}\neq 0$
> - $\varepsilon=1:L_{1}\cap L_{2} = 0$

> [!info] Paralelismo
> Dados dos subespacios afines $L_{1}=P_{1}+W_{1}$ y $L_{2}=P_{2}+W_{2}$, decimos que son paralelos si $L_{1}\subset L_{2}$ o $L_{2}\subset L_{1}$.

# Aplicaciones afines
Sean $(A_{1},V_{1},\phi_{1})$ y $(A_{2},V_{2},\phi_{2})$ dos espacios afines. Diremos que una aplicación
$$
f:A_{1}\to A_{2}
$$
es una aplicación afín si existe una aplicación lineal $\bar{f}:V_{1}\to V_{2}$ tal que:
$$
\bar{f}(\mathbf{PQ})=\overrightarrow{f(P)f(Q)}
$$
y por tanto, que para todo punto $P \in A_{1}$ y todo vector en $V_{1}$ se tiene que
$$
f(Q)=f(P+\mathbf{v})=f(P)+\bar{f}(\mathbf{v})=f(P)+\bar{f}(\mathbf{PQ})
$$
La anterior aplicación lineal $\bar{f}$ se llama **aplicación lineal asociada a $f$**.

Es decir, tenemos un par de puntos $P,Q\in A_{1}$, que les corresponden dos puntos $f(P),f(Q)\in A_{2}$. El vector $\mathbf{PQ}$, sobre $A_{2}$, tiene como vector $\overrightarrow{f(P)f(Q)}$, que es la imagen de $\bar{f}(\mathbf{PQ})$.

Si tenemos dos aplicaciones afines $f,g$ tal que $f(P)=g(P)$, y además que $\bar{f}=\bar{g}$, entonces
$$
f=g
$$


> [!info] Punto fijo, doble o invariante
> Sea $(A,V,\phi)$ un espacio afín y $f$ una transformación afín de $A$. Un punto fijo es aquel que cumple que
> $$
> \boxed{f(P)=P}
> $$
> Con esto podemos definir el conjunto de puntos fijos como:
> $$
> F=\{ x \in A : f(x)=x \}
> $$
> 

> [!info] Subespacio afín invariante
> Sea $(A,V,\phi)$ un espacio afín, y $f$ una transformación afín de $A$ y $S$ un subespacio afín de $A$. Diremos que $S$ es un subespacio afín invariante de $f$ si
> $$
> f(S) \subset S 
> $$
> Con esto, se debe cumplir que:
> - Si $L \subset A$ es un subespacio afín entonces:
>   $$
>   f(L)=\{ P'\in A',~\exists P \in L: f(P)=P'\}
>   $$
> - Si $L' \subset A'$ es un subespacio afín de $A'$ entonces:
>   $$
>   L=\{ P\in A: f(P) \in L' \}
>   $$
>   También, $S$ es invariante por $f$ si
>   $$
>   \mathcal{L}(\{ \bar{f}(\mathbf{u}_{1}),\dots,\bar{f}(\mathbf{u}_{r}) \}) \subset \mathcal{L}(\{ \mathbf{u}_{1},\dots,\mathbf{u}_{r} \})
>   $$
> 

> [!tip] Teorema
> Dados un espacio afín y una transformación afín $f:A \to A$. Entonces son equivalentes:
> - Existe un conjunto fijo $V$ no trivial $(V \neq \{ 0 \})$.
> - El $1$ es autovalor de $f$.
> 
> El conjunto de puntos fijos es un subespacio afín de $A$ con subespacio vectorial asociado de $V$ de autovectores de $\bar{f}$ con autovalor $\lambda=1$.
> 

## Composición de aplicaciones afines
Sean $A_{1},A_{2},A_{3}$ espacios afines y sean $g:A_{1}\to A_{2}$ y $f:A_{2}\to A_{3}$ dos aplicaciones afines. La composición $f\circ g:A_{1}\to A_{3}$ también es una aplicación afín y su aplicación lineal asociada es:
$$
\overline{f\circ g}=\bar{f}\circ \bar{g}
$$
Dadas dos aplicaciones afines, la **suma** de aplicaciones afines y el **producto por escalares** son aplicaciones afines también.

> [!info] Razón simple de tres puntos
> Sea $A$ un espacio afín sobre $K$. Dados tres puntos alineados $P_{1}, P_{2}, P_{3}$ de $A$ tales que $P_{1}\neq P_{2}$, definimos su razón simple $(P_{1},P_{2},P_{3})$ como el elemento $\lambda \in K$ tal que
> $$
> \mathbf{P_{1}P_{3}}=\lambda \mathbf{P_{1}P_{2}}
> $$
> Las aplicaciones afines conservan la razón simple. Si $A,V, \phi: A_{n}\to A_{m}$ es una aplicación afín y $A,B,C$ son tres puntos distintos alineados tales que $\phi(A),\phi(B),\phi(C)$ también son distintos, entonces
> $$
> (A~B~C)=(\phi(A)~\phi(B)~\phi(C))
> $$
> 

 