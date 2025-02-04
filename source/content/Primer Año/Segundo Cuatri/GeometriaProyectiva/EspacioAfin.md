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
Sea $(A,\mathbb{V},\varphi)$ un espacio afín real. Un subconjunto no vacío $L\subset A$ es un subespacio afín de $A$ si existe un subespacio $W\subset V$ tal que $(L,W,\varphi)$ tiene estructura de espacio.
## Propiedades
Dado $P \in L$, existe $W \subset V$ tal que $L=P+W$. Todos los puntosFijado un punto ￼￼ el conjunto es un subespacio vectorial de ￼￼ si de $L$ se pueden expresar como $P+\mathbf{w}$, con $\mathbf{w}\in W$.
Además, existe $P\in L$ tal que la imagen de la aplicación
$$
\varphi_{L}:L\to V
$$
$\varphi(Q)=\mathbf{PQ}$ es un subespacio vectorial de $V$.
## Dimensión
La dimensión del espacio afín es la dimensión del subespacio vectorial asociado.