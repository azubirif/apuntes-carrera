---
title: El espacio R^n
---
# El espacio $\mathbb{R}^n$
## El conjunto $\mathbb{R}^n$
$\mathbb{R}^n$ es el conjunto definido por
$$
\mathbb{R}^{n} =\{ ( x_1,\dots ,x_{n}) / x_{i} \in \mathbb{R}, 1 \leq i \leq n\}
$$
De momento, este conjunto no tiene ninguna estructura. Para ello, se introduce la noción es espacio vectorial (EV a partir de ahora)
- La suma vectorial:
$$
\mathbf{a} + \mathbf{b} = (a_{i}+b_{i},\dots a_{n}+b_{n})
$$
- Producto por escalar
$$
k \mathbf{a} = (ka_{1},\dots ,ka_{n})
$$
Con estas dos operaciones, $\mathbb{R}^{n}$ es EV, y a sus elementos, los vamos a
llamar vectores, y los denotaremos por $\mathbf{x}=(x_{1},\dots x_{n})$.\\
Con esta estructura, los elementos de $\mathbb{R}^{n}$ se pueden ordenar, por
ejemplo, en una cuadrícula.
## $\mathbb{R}^{n}$ como espacio afín
Nos será útil para definir direcciones desde cualquier punto de $\mathbb{R}^{n}$.
La estructura afín en $\mathbb{R}^{n}$ se define por la aplicación
$$
\varphi: \mathbb{R}^{n} \times \mathbb{R}^{n} \mapsto \mathbb{R}^{n}
$$
$$
(\mathbf{u}, \mathbf{v}) \mapsto \varphi(\mathbf{u}, \mathbf{v})
$$
donde $\varphi(\mathbf{u}, \mathbf{v})$ se representará como un vector cuyo punto de aplicación está en el extremo de $\mathbf{u}$ y el extremo, el de $\varphi(\mathbf{u}, \mathbf{v})$ en el extremo de $\mathbf{v}$. Es fácil comprobar que
$$
\varphi(\mathbf{u},\mathbf{v}) = \mathbf{v} - \mathbf{u}
$$
En este contexto es conveniente llamar puntos a los vectores con punto de
aplicación en el $\mathbf{0}$ y vectores a los vectores cuyo punto de aplicación es arbitrario. Los puntos también los denotaremos mediante letras mayúsculas, y los vectores con letras minúsculas.
A recordar que punto - punto define un vector, y que punto + vector = punto.
Con esto ya podemos definir direcciones.
## $\mathbb{R}^{n}$ como espacio métrico
Para medir longitudes, ángulos y distancias introduciremos en $\mathbb{R}^{n}$
el **producto escalar**.
El producto escalar entre dos vectores $\mathbf{u}$ y $\mathbf{v}$ se define como
$$
\cdot : \mathbb{R}^{n} \times  \mathbb{R}^{n} \mapsto \mathbb{R}
$$
$$
\mathbf{u} \cdot  \mathbf{v} = \sum_{i=1}^{n} u_{i}v_{i}
$$
El producto escalar tiene las propiedades siguientes:
- $\mathbf{u} \cdot  \mathbf{v} = \mathbf{v} \cdot \mathbf{u}$
- $\mathbf{u} \cdot (\mathbf{v}+\lambda\mathbf{w})= \mathbf{u} \cdot \mathbf{v} + \lambda \mathbf{u} \cdot \mathbf{w}$
- $\mathbf{u} \cdot \mathbf{u} \geq 0 \implies \mathbf{u} \cdot \mathbf{u}=0\iff \mathbf{u} = \mathbf{0}$ 
Debido a la propiedad 3, podemos definir la longitud (o norma) de un vector como
### Definición
La longitud o norma de un vector se define como:
$$
|\mathbf{u}| = \sqrt{\mathbf{u} \cdot \mathbf{u}} = \sqrt{\sum_{i=1}^{n} u_{i}^{2}}
$$
## Hiperplanos en $\mathbb{R}^n$
Si $n=3$ se llaman planos.
Si $n=2$ son rectas.
Dado $P\in \mathbb{R}^n$ y dado un vector $\mathbf{N} \in \mathbb{R}^n$ vamos a definir un hiperplano que pasa por $P$ y es perpendicular a $\mathbf{N}$ como el conjunto de puntos $X$ que satisfacen 
$$
\mathbf{PX} \cdot \mathbf{N}=0
$$
esta ecuación se puede escribir también
$$
(X-P)\cdot \mathbf{N}=0
$$
es decir
$$
X \cdot \mathbf{N} = P\cdot \mathbf{N}
$$
o en componentes
$$
\sum_{i=1}^n x_{i}N_{i} = \sum_{i=1}^n p_{i}N_{i}
$$
el vector $\mathbf{N}$ se llama el vector normal al hiperplano $H$.
Hay $1$ ecuación y $n$ incógnitas $x_{1},\dots,x_{n}$, por tanto la solución viene descrita por $n-1$ parámetros libres.
$$
dim(H)=n-1
$$
La codimensión de un objeto $H$ es la dimensión del espacio menos la dimensión del objeto.
$$
codim(H)=dim(\mathbb{R}^n)-dim(H)
$$
Como $H$ tiene dimensión $n-1$, tendrá $n-1$ vectores LI que generan a todos los vectores contenidos en el hiperplano. Si llamamos a estos vectores
$$
\mathbf{v}_{1},\dots ,\mathbf{v}_{n-1}
$$
entonces se cumplirá:
$$\mathbf{PX}=\sum_{i=1}^{n-1} a_{i}\mathbf{v}_{i}$$
Ahora lo que hacemos será hallar una relación entre la descripción de $H$ mediante parámetros libres y su descripción mediante coordenadas cartesianas.
Como estos vectores son LI, y también lo son de $\mathbf{N}$, entonces el conjunto de los vectores junto con $\mathbf{N}$ formarán una base de $\mathbb{R}^n$.
Esto, en particular, significa que
$$
\det(\mathbf{v}_{1},\dots,\mathbf{v}_{n-1}, \mathbf{N}) \neq 0
$$
---
## El símbolo de Levi-Civita o símbolo totalmente antisimétrico
En $\mathbb{R}^n$ se define por:
$$
\varepsilon_{i, \dots, i_{n}}=  \left\{\begin{matrix}
1 &\text{ si } i_{i},\dots,i_{n}\text{ es una permutación par} \\
-1 &\text{si es una permutación impar}  \\
0 &\text{ en el resto de casos, cuando un índice se repite}  \\
\end{matrix}\right.
$$
$i_{1},\dots,i_{n}$ es una permutación par $123,\dots,n$ si para transformar una en otra necesitamos un número par de trasposiciones. Una trasposición es una permutación en la que solo se intercambian dos y solo dos elementos (no tienen por qué ser adyacentes).
**Ejemplo**:
En $\mathbb{R}^4$, $\varepsilon_{4312} \to 1342 \to 1243 \to 1234 \implies~3$ trasposiciones, y $\varepsilon_{1341}=0$
Una propiedad muy útil del símbolo de Levi-Civita es que con él podemos dar una expresión cerrada a cualquier determinante $n\times n$.
$$
\begin{vmatrix}
a_{11} & \dots & a_{1n} \\
\dots  & \dots & \dots\\
a_{n-1} & \dots & a_{nn}
\end{vmatrix}= \sum_{i_{1}=1}^n \sum_{i_{2}=1}^n\dots \sum_{i_{n}=1}^n
\varepsilon_{i_{1},\dots,i_{n}}a_{1i_{1}}\dots a_{ni_{n}}
$$
Si queremos abusar todavía más de la notación, podemos usar el criterio de suma de Einstein. Este consiste en suponer que hay una suma siempre que un índice se repita, y la suma se hace en todo el rango de definición del índice:
$$
\mathbf{v} \cdot \mathbf{w} = v_{i} w_{i}
$$
---
$$
\begin{vmatrix}
\mathbf{N} \\
\mathbf{v}_{1} \\
\dots \\
\mathbf{v}_{n-1}
\end{vmatrix}=
\begin{vmatrix}
N_{1} & \dots & N_{n} \\
\dots & \dots & \dots \\
v_{n-1,1} & \dots & v_{n-1,n}
\end{vmatrix}=\varepsilon_{ij_{1}j_{2}\dots j_{n-1}}N_{i}v_{1j_{1}}v_{2j_{2}}\dots v_{n-1,j_{n-1}}
$$
### La delta de Kronecker
$$
\delta_{ij}=  \left\{\begin{matrix}
1 & i=j \\
0 & i\neq j
\end{matrix}\right.
$$
Los vectores de la base canónica cumplen que:
$$
\mathbf{e}_{i}\cdot \mathbf{e}_{j}=\delta_{ij}
$$
Las bases cuyos vectores cumplan esto se dice que son bases **ortonormales**.
**Ejemplos**:
$$
\mathbf{v}\cdot \mathbf{w}=\sum_{i=1}^{n}\sum_{j=1}^{n}v_{i}w_{i}\delta_{ij}
$$
Volviendo a donde estábamos antes, podemos expresar el determinante anterior mediante
$$
N_{i}\delta_{ij}\varepsilon_{jj_{1},\dots j_{n-1}}v_{1,j_{1}}\dots v_{n-1,j_{n-1}}
$$
Utilizando lo que teníamos antes
$$
\overset{\mathbf{N}}{N_{i}\mathbf{e}_{i}\cdot \mathbf{e}_{j}}\overset{\mathbf{V}}{\varepsilon_{jj_{1},\dots j_{n-1}}v_{1,j_{1}}\dots v_{n-1,j_{n-1}}}=\mathbf{N}\cdot \mathbf{V} \neq 0
$$
Como $\mathbf{N}$ la única condición que queremos para $\mathbf{N}$ es que sea perpendicular a $H$ y que $\mathbf{N}\cdot \mathbf{V}\neq 0$, entonces podemos elegir $\mathbf{N}=\mathbf{V}$, donde
$$
\mathbf{V}= \mathbf{N}=
\begin{vmatrix}
\mathbf{e}_{1} & \mathbf{e}_{2} & \dots & \mathbf{e}_{n} \\
v_{1,1} & v_{1,2} & \dots & v_{1,n} \\
\dots & \dots & \dots & \dots \\
v_{n,1} & v_{n,2} & \dots & v_{n-1,n}
\end{vmatrix}
$$
Observemos que en $\mathbb{R}^3$, tendríamos
$$
\begin{vmatrix}
i & j & k \\
v_{1} & v_{2} & v_{3} \\
w_{1} & w_{2} & w_{3}
\end{vmatrix}
$$
este determinante se puede ver como el vector ortogonal a $\mathbf{v}$ y $\mathbf{w}$, y es una operación interna en $\mathbb{R}^{3}$:
$$
\wedge: \mathbb{R}^{3}\times \mathbb{R}^{3} \to \mathbb{R}^{3}
$$
el llamado producto vectorial de $\mathbb{R}^{3}$.
En $\mathbb{R}^{2}$ tenemos una recta (hiperplano) con vector director $\mathbf{v}=(v_{1},v_{2})$, entonces una recta perpendicular a la misma vendrá dada por
$$
\mathbf{N}=\begin{vmatrix}
i & j \\
v_{1} & v_{2}
\end{vmatrix}= (v_{2},-v_{1})
$$
# Topología en $\mathbb{R}^n$
Usaremos la topología inducida por la métrica euclídea.
> [!info] Conjuntos abiertos
> Definimos un conjunto abierto de $\mathbb{R}^n$ a partir de la definición de bolas abiertas.
> Dado $\mathbf{x}\in \mathbb{R}^n$ y dado $r\in \mathbb{R}^+$ se define la bola abierta centrada en $\mathbf{x}$ y de radio $r$ como el conjunto
> $$
> B_{r}(\mathbf{x})=\{ \mathbf{y}\in \mathbb{R}^n: d(\mathbf{x},\mathbf{y}) < r \}
> $$
> A veces convendrá usar bolas abiertas sin el punto central (perforadas), y se denotan por $B_{r}^*(\mathbf{x})$:
> $$
> B_{r}^*(\mathbf{x})=B_{r}(\mathbf{x})- \{ \mathbf{x} \}
> $$
> Un conjunto abierto $A\subset \mathbb{R}^n$ es abierto si y solo si para todo $\mathbf{x}\in A \exists \delta >0 : B_{\delta}(\mathbf{x})\subset A$
> Además, se verifica que $ext(S)=\mathbb{R}^{n}-(S\cup\partial S)$
> 


> [!info] Conjuntos cerrados
> Un conjunto $B\subset \mathbb{R}^n$ es cerrado si y solo si
> $\mathbb{R}^n-B$ es abierto.
> Además se verifica que $ext(B)=\mathbb{R}^{n}-B$
> 


Dado cualquier conjunto $S\subset \mathbb{R}^n$,podemos clasificar los puntos de $\mathbb{R}^n$ en:
- Puntos interiores de $S$: si existe una bola centrada en dicho punto contenida en $S$.
- Puntos exteriores de $S$: si existe una bola centrada en el punto tal que $B(\mathbf{x},r) \cap S = \phi$
- Puntos frontera de $S$: si $\forall r\in \mathbb{R}^{+} B(\mathbf{x},r)\cap S \neq \phi$ y $B(\mathbf{x},r)\cap(\mathbb{R}^n-S)\neq \phi$
Todos estos conjuntos son disjuntos entre sí. Al conjunto de todos los puntos interiores de $S$ se les llama interior de $S$ y lo denotaremos por $int S$. Al conjunto de todos los puntos exteriores a $S$ se les llama exterior de $S$ y se denota por $ext S$. A los puntos frontera de $S$ se les llama frontera de $S$ y se denota por $\partial S$.
---
Un conjunto $A \subset \mathbb{R}^{n}$ es abierto si y solo si $A=int(A)$, y es cerrado si y solo si $B=int(B)\cup \partial B$.
**Ejemplos**
$A=\{ (x,y)\in \mathbb{R}^{2}: x \in (0,1), y \in(0,1) \}=(0,1)\times(0,1)$. En este caso tenemos que $ext(A)=\mathbb{R}^2-A$.

$B=\{ (x,y)\in \mathbb{R}^{2}:x \in[0,1], y \in (0,1) \}$. En este caso $B$ no es ni abierto ni cerrado.

> [!info] Adherencia
> A $int(S)\cap\partial S$ se la denomina adherencia de $S$ y se denota por $\bar{S}$.
> 

> [!info] Puntos límite
> A los puntos $\mathbf{x}$ que cumplen $B^{*}(\mathbf{x},r)\cap S\neq \phi$ se les llama puntos límite de $S$.
> 

# Funciones de $\mathbb{R}^{n}$
Sea
$$
f:D \subset \mathbb{R}^n\to \mathbb{R}^m
$$
Si $n=m=1$ entonces es una función de variable real. Si $n>1$ y $m=1$, entonces $f$ es una función real de variable vectorial o campo escalar.
Para hacernos una idea del comportamiento de estas funciones es conveniente dibujar estas funciones (cuando sea posible). Para ello nos serán útiles los **conjuntos de nivel**:

> [!info] Conjuntos de nivel
> Sea $f: \mathbb{R}^{n}\to \mathbb{R}$
> $$
> L_{f}(c)=\{ \mathbf{x}\in D : f(\mathbf{x})=c \}=f^{-1}(c)
> $$
> Que es precisamente la preimagen de $c$.

Por ejemplo, sea
$$
f(x,y,z)=\exp \left[ - \frac{x^{2}+y^{2}+z^{2}}{2} \right]
$$
Supongamos $f(x,y,z)=c, entonces$
$$
\begin{align*}
\exp \left[ - \frac{x^{2}+y^{2}+z^{2}}{2} \right]&=c\\
\frac{x^{2}+y^{2}+z^{2}}{2}&=-\ln c\\
x^{2}+y^{2}+z^{2}&=-2\ln c
\end{align*}
$$
Como $x^{2}+y^{2}+z^{2}>0$, necesitamos que $\ln c<0$, por tanto, esta ecuación tiene solución en $\mathbb{R}$ cuando $c \in (0,1]$. Esto define una superfície esférica de radio $\sqrt{ 2\ln\left( \frac{1}{c} \right) }$.