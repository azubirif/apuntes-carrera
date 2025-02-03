---
title: Cálculo en varias variables
---

# Bibliografía
- Stewart, J. Cálculo en varias variables.
- Apuntes de Pepe Aranda.
- Tom M. Apostol, "Calculus"
- Tom M. Apostol, Análisis Matemático.
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

