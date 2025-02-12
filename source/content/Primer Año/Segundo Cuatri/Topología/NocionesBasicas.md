---
title: Nociones Básicas
---
## Relaciones
Existen dos tipos de relaciones:
- De orden
- De equivalencia
Una relación $R$ de $A$ en $B$ es cualquier subconjunto de $A \times B$:
$$
R \subset A \times B
$$
Y denotamos $(a,b) \in R$ por $a~R~b$, diciendo que $a$ está relacionado con $b$.
### Relaciones de equivalencia
Podemos hablar de relaciones **internas** $(a=b)$ o **externas** $(a \neq b)$.
Sea $A \neq \phi$, una relación de equivalencia definida sobre $A$ es una relación que satisface las siguientes propiedades:
1. $\forall x \in A,~x \sim x$ (reflexiva).
2. Dados $x$ e $y$ en $A$, si $x\sim y$, entonces $y \sim x$ (simetría).
3. Dados $x\sim y$, e $y \sim z$, entonces $x \sim z$ (transitiva).
Todo esto se lee como $x$ equivalente a $y$. Todas estas propiedades se deben cumplir.
Para escribir esto como subconjuntos del producto cartesiano:
$$
x \sim x \equiv (x,x) \in \sim
$$
Si tenemos un conjunto $A$, y este esta dividido en subconjuntos disjuntos, entonces dados dos elementos en $A$, estos son equivalentes sí y solo sí ambos pertenecen al mismo subconjunto.
$$
S_{i} \subset A, x \sim y \iff x,y \in S_{i}~ :~ A = S_{1} \cap\dots \cap S_{n}
$$
**Ejemplos**:
Tomamos en $\mathbb{Z}$, dado un entero $n>1$, entonces definimos para $a,b \in \mathbb{Z}$,
$$
a \equiv b ~ mod_{n} \iff n | b -a
$$
$a$ congruente con $b$ módulo $n$.
Esto define una relación de equivalencia en $\mathbb{Z}$ de módulo $n$.
Debemos demostrar que esa relación cumple las propiedades definidas anteriormente para poder afirmar que es de equivalencia.
4. Es reflexiva: dado un $a \in \mathbb{Z}$, $n | a-a$, ya que $a-a = 0$, entonces $a$ es congruente con $a ~ mod_{n} \forall a \in \mathbb{Z}$.
5. Es simétrica: dados dos $a,b \in \mathbb{Z}$, si $a \equiv b ~mod_{n} \iff n|b-a$, entonces $n |a-b \iff b \equiv a ~mod_{n}$.
6. Es transitiva: dados $a,b,c \in \mathbb{Z} / a \equiv b~ mod_{n}$ y $b \equiv c ~ mod_{n}$, entonces $n |b-a$ y $n|c-b$, por tanto $b-a = nx$ y $c-b = ny$, entonces $c-a=n(x+y)=nz \implies n |c-a$.
Como cumple con las propiedades, es una relación de equivalencia.
Si $n>1$, ¿cuáles son las clases de equivalencia de la congruencia módulo $n$?
Sean $a,b\in \mathbb{Z}$, y los dividimos entre $n$:
$$
a = q_{1}n+r_{1}:0\leq r_{1}<n
$$
$$
b=q_{2}n+r_{2}:0\leq r_{2}<n
$$
¿Qué pasa si $a$ es congruente con $b$ módulo $n$?
Entonces, $n |b-a$, y $b-a=n(q_{2}-q_{1}) +r_{2}-r_{1}$. Si $n|b-a$, entonces $\exists m \in \mathbb{Z}: b-a=nm \implies nm=(q_{2}-q_{1})n+r_{2}-r_{1}\implies n(m-q_{2}+q_{1})=r_{2}-r_{1}$.
Pero como $0\leq|r_{2}-r_{1}|<n$. Sabiendo que $r_{2}-r_{1} = kn$, y $r_{2}-r_{1} < n$, entonces la única posibilidad es que $k=0$. Esto implica que $\frac{n}{a}$ y $\frac{n}{b}$ tienen el mismo resto.
Vamos a demostrar ahora el recíproco:
Supongamos ahora que $a = qn+r$ y $b=q'n+r$. Entonces, $b-a = n(q'-q)$ es decir, $n|b-a$, y por tanto, $a \sim b~mod_{n}$
Con esto podemos afirmar para $a\in \mathbb{Z}$,
$$
[a] = \{ b \in \mathbb{Z}:n\%a=n\%b \}
$$
Es decir, el conjunto de todos los $b$ congruentes con $a$ módulo $n$. Como los residuos de dividir un entero entre $n$ van desde $[0,n-1]$, las clases son las clases de $[0],[1],\dots,[n-1]$. Entonces la clase de un número $r$ es
$$
[r]= \{ qn+r:q\in \mathbb{Z} \}
$$
Por ejemplo, si dividimos un número entre $3$, solo podemos obtener resto $0,1$ o $2$.
### Teorema
Sea $A \neq \phi$ y $\sim$ una relación de equivalencia sobre $A$. Entonces
$$
a\sim b\iff[a]=[b]
$$
$$
a\not\sim b \iff [a] \cap  [b]=\phi
$$
**Demostración**
Supongamos que $a\sim b$. Sea $x \in[a]$, entonces $x\sim a$. Como es una relación de equivalencia, $x\sim b$ y por tanto $x \in [b]$, y por tanto, como se cumple para todo elemento, $[a]=[b]$.
Supongamos $[a]=[b]$. Por la reflexividad, $b\in[b]$, entonces $b\in[a]$, y por tanto $a\sim b$.
Para la segunda parte, si $x \in[a]\cap[b]\iff x\sim a$ y $x\sim b\iff a\sim b$. Por tanto, dos clases de equivalencia de una misma relación o son iguales o son disjuntas.
Sea $X$ un conjunto. Una partición de $X$ es un conjunto $P$ cuyos elementos son subconjuntos de $X= \cup A : A \in P$ y $A \in P \wedge B \in P \implies A \cap B = \phi$.
**Corolario**
Si $\sim$ es una relación de equivalencia definida sobre $A$, entonces el conjunto de todas las clases de equivalencia distintas es una partición.

---
Vamos a tomar en el plano $\mathbb{R}^2$, decimos que dos puntos $P$ y $Q$ son equivalentes (o están relacionados) sí y solo sí la distancia de $P$ al origen es la distancia de $Q$ al origen, donde $\vec{O} = (0,0)$. Vamos a ver si cumple las propiedades:
$$
P \sim Q \iff d(P,O)=d(Q,O)
$$
7. Es reflexivo: $P \sim P \iff d(P,O) = d(P,O)$. Esto se cumple por sí mismo.
8. Es simétrico: $P\sim Q \iff d(P,O) = d(Q,O)$, y se cumple que como $d(Q,O)=d(P,O) \iff Q\sim P$.
9. Es transitivo: $P\sim Q \iff d(P,O) = d(Q,O)$. Si $Q\sim R \iff d(Q,O) = d(R,O)$, entonces si sustituimos tenemos que $d(P,O)=d(R,O) \iff P \sim R$.
### Definición
Sea $A \neq \phi$ y $\sim$ una relación de equivalencia sobre $A$. Entonces $\forall a \in A$, el conjunto $[a] = \{ x \in A : a \sim x \}$ se llama la clase de equivalencia de $a$.
### Definición
El conjunto de todas las clases de equivalencia que define la relación $\sim$ sobre $A$, se llama el conjunto cociente de la relación y se denota por
$$
\boxed{A / \sim}
$$
Para la congruencia de módulo $n$ en $\mathbb{Z}$:
$$
\frac{\mathbb{Z}}{\sim} = \{ [0],[1],\dots,[n-1] \} \equiv \mathbb{Z}_{n}
$$
### Definición
$f:X\to Y$ es una función si y solo si:
1. Para cada elemento $x \in X \exists y \in y : (x,y) \in f$
2. $(x,y) \in f \wedge (x,z) \in F \implies y = z$
Si $(x,y) \in f$, escribimos $f(x)=y$. El conjunto $X$ se llama **dominio** de la función, y el conjunto $Y$ se llama **rango** o **codominio** o **conjunto de llegada** de $f$.
Además, la **imagen** de $f$ es el conjunto
$$
\mathrm{Im}(f)=\{ y \in Y : (\exists x \in X)(f(x)=y) \} \subset Y
$$
$$
Dom (f) = X
$$
Por ejemplo, para buscar el dominio de la función $f$ dada por la fórmula
$$
f(x)=\sqrt{ x^{2}-1 }:x \in \mathbb{R}
$$
Necesitamos saber el conjunto de valores de $x$ para los cuales $f(x)$ existe. Es decir, para los cuales $\sqrt{ x^{2}-1 }$ tiene sentido. En este caso, esto se cumple cuando
$$
x^{2}-1\geq 0 \implies |x|\geq 1
$$
---
Dado un conjunto $A \subset X$, definimos
$$
f(A)= \{ f(x) / x \in A \}
$$
y además, definimos la **preimagen** de un conjunto $B \subset Y$:
$$
f^{-1}(B)= \{ x \in X : f(x) \in B \}
$$
Es decir, teniendo $y \subset Y$:
$$
\begin{align}
f^{-1}(y)&= \{ x \in X : f(x)=y \}\\ \\
f^{-1}(\{ y \})&= \{ x \in X : f(x)\in \{ y \} \}\\ \\
f(x) \in \{  y \}&\iff f(x)=y
\end{align}
$$
## Tipos de funciones
Sea $f:X\to Y$. $f$ es **injectiva** (o 1:1) si y solo si:
$$
f(x_{1})=f(x_{2}) \implies x_{1}=x_{2}~ \forall x_{1},x_{2}\in X
$$
O, equivalentemente
$$
x_{1}\neq x_{2} \implies f(x_{1})\neq f(x_{2})
$$
Una función es **sobreyectiva** si y solo si:
$$
\mathrm{Im}(f)=Y
$$
Es decir, $\forall y \in Y \exists x \in X:f(x)=y$
Si ocurren ambas propiedades, la función es **biyectiva**.
Con esto podemos deducir que:
- $f:A\to B. \#A=\#B \iff~f$ es biyectiva.
Sea $f:X\to Y$ una función biyectiva. Sea $g:Y\to X : g(y)=x \iff f(x)=y$.
¿$g$ define una función de $Y\to X$?
Es decir, ¿$\forall y \in Y$, existe un único $x \in X : g(y)=x$?
Dado $y \subset Y$, sabemos que $\exists x \in X : f(x)=y$, ya que $f$ es sobreyectiva. Entonces $g(y)=x$.
Demostremos que si $\exists ! x \in X :g(y)=x$. Esto se cumple ya que $f$ es inyectiva. Por tanto, tenemos una función $g:Y\to X : g(y)=x \iff f(x)=y$. Esta función se llama la **inversa** de $f$ y la denotamos por $f^{-1}$.
$$
f^{-1}:Y\to X: f^{-1}(y)=x\iff f(x)=y
$$
### Definición
Sean $f:X\to Y$, $g:Y\to Z$ dos funciones. Definimos la composición de $f$ con $g$ como la función $g\circ f: X\to Z:(g\circ f)(x)=g(f(x))$.
Esto se puede entender como un producto de funciones no conmutativo, pero sí es asociativa:
$$
h\circ(g\circ f)=(h\circ g)\circ f
$$
Si $f:X\to Y$ es biyectiva, entonces
$$
(f\circ f^{-1})(y)=y \iff (f^{-1}\circ f)(x)=x
$$
La función que cumple que $f(x)=x \forall x$ se llama la función **identidad**:
$$
id:X\to X
$$
---
Sea $X$ un conjunto no vacío. $f:X\to Y$ una función sobreyectiva. Definimos la siguiente relación: dados $x_{1},x_{2}\in X$, decimos que $x_{1} \sim x_{2} \iff f(x_{1})=f(x_{2})$.
¿Es una relación de equivalencia?
- Reflexiva: $f(x)=f(x) \iff x \sim x$
- Simétrica: $x_{1}\sim x_{2} \implies f(x_{1})=f(x_{2})\iff f(x_{2})=f(x_{1})\iff x_{2}\sim x_{1}$
- Transitiva: $x_{1}\sim x_{2} \wedge x_{2}\sim x_{1} \implies f(x_{1})=f(x_{2}), f(x_{2})=f(x_{3})\implies f(x_{1})=f(x_{3})\implies x_{1}\sim x_{3}$
Consideremos el conjunto cociente $\frac{X}{\sim}$, es decir, el conjunto formado por todas las clases de equivalencia. Entonces, ¿existe una biyección entre $X / \sim$ e $Y$?
Sea $\hat{f}:X / \sim \to Y : \hat{f}([x])=f(x)$
$\hat{f}$ está bien definida ya que $[x_{1}]=[x_{2}] \implies x_{1}\sim x_{2} \implies f(x_{1})=f(x_{2})$. Por tanto, $\hat{f}([x_{1}])=\hat{f}([x_{2}])$. Por tanto todos los elementos de $\frac{X}{\sim}$ tienen imagen y esta es única. Dado $y \in Y$, como $f$ es sobreyectiva $\exists x \in X:y=f(x)$, pero como $f(x)=\hat{f}([x])$, entonces dado $y \in Y$ existe $[x] \in \frac{X}{\sim}:\hat{f}([x])=y$.
Además, podemos definir la función $\pi:X \to \frac{X}{\sim}$ como la **proyección canónica**.
$$
\pi(x)=[x] \forall x \in X
$$

> [!info] Definición de una topología
> Sea $X$ un conjunto no vacío. Una colección $\mathbf{T}$ de subconjuntos $X$ se dice que es una topología sobre $X$ si
> 1. $X$ y el conjunto vacío $\phi$ pertenecen a $\mathbf{T}$.
> 2. La unión de cualquier número (finito o infinito) de conjuntos de $\mathbf{T}$ pertenece a $\mathbf{T}$.
> 3. La intersección de dos conjuntos cualesquiera de $\mathbf{T}$ pertenece a $\mathbf{T}$
> El par $(X,\mathbf{T})$ se llama **espacio topológico**.
> Por la propiedad 3 y mediante inducción, se puede demostrar que si $A_{i}$ conjuntos están en $\mathbf{T}$, entonces
> 
> $$
> \bigcap A_{i} \in \mathbf{T}
> $$
> 

> [!warning] La pertenencia no es transitiva
> 

> [!info] Topología discreta
> Sea $X$ no vacío, y $\mathbf{T}$ la colección de todos los subconjuntos de $X$. Entonces $\mathbf{T}$ es una **topología discreta** sobre $X$, y $(X,\mathbf{T})$ es un **espacio discreto**.
> Si para un espacio topológico, se cumple que $\forall x \in X, \{ x \} \in \mathbf{T}$, entonces $\mathbf{T}$ es una topología discreta.
> La topología formada por $(X,\phi)$ es la topología indiscreta.
> 

El conjunto $X$ de la definición anterior puede ser cualquier conjunto no vacío, por tanto, hay una cantidad infinita de espacios discretos para cada conjunto no vacío $X$.

> [!info] Definición
> Dado un espacio topológico $(X,\mathbf{T})$, los elementos de $\mathbf{T}$ se llaman **conjuntos abiertos**.
> 

> [!info] Definición
> Sea $(X, \mathbf{T})$ un espacio topológico. Un subconjunto $S$ de $X$ es cerrado en $(X,\mathbf{T})$ si su complemento es abierto.
> 
