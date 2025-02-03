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
\vec{a} + \vec{b} = (a_{i}+b_{i},\dots a_{n}+b_{n})
$$
- Producto por escalar
$$
k \vec{a} = (ka_{1},\dots ,ka_{n})
$$
Con estas dos operaciones, $\mathbb{R}^{n}$ es EV, y a sus elementos, los vamos a
llamar vectores, y los denotaremos por $\vec{x}=(x_{1},\dots x_{n})$.\\
Con esta estructura, los elementos de $\mathbb{R}^{n}$ se pueden ordenar, por
ejemplo, en una cuadrícula.
## $\mathbb{R}^{n}$ como espacio afín
Nos será útil para definir direcciones desde cualquier punto de $\mathbb{R}^{n}$.
La estructura afín en $\mathbb{R}^{n}$ se define por la aplicación
$$
\varphi: \mathbb{R}^{n} \times \mathbb{R}^{n} \mapsto \mathbb{R}^{n}
$$
$$
(\vec{u}, \vec{v}) \mapsto \varphi(\vec{u}, \vec{v})
$$
donde $\varphi(\vec{u}, \vec{v})$ se representará como un vector cuyo punto
de aplicación está en el extremo de $\vec{u}$ y el extremo, el de $\varphi(
\vec{u}, \vec{v})$ en el extremo de $\vec{v}$. Es fácil comprobar que
$$
\varphi(\vec{u},\vec{v}) = \vec{v} - \vec{u}
$$
En este contexto es conveniente llamar puntos a los vectores con punto de
aplicación en el $\vec{0}$ y vectores a los vectores cuyo punto de aplicación
es arbitratio. Los puntos también los denotaremos mediante letras mayúsculas,
y los vectores con letras minúsculas.
A recordar que punto - punto define un vector, y que punto + vector = punto.
Con esto ya podemos definir direcciones.
\subsection{$\mathbb{R}^{n}$ como espacio métrico}
Para medir longitudes, ángulos y distancias introduciremos en $\mathbb{R}^{n}$
el **producto escalar**.
El producto escalar entre dos vectores $\vec{u}$ y $\vec{v}$ se define como
$$
\cdot : \mathbb{R}^{n} \times  \mathbb{R}^{n} \mapsto \mathbb{R}
$$
$$
\vec{u} \cdot  \vec{v} = \sum_{i=1}^{n} u_{i}v_{i}
$$
El producto escalar tiene las propiedades siguientes:
- $\vec{u} \cdot  \vec{v} = \vec{v} \cdot \vec{u}$
- $\vec{u} \cdot (\vec{v}+\lambda\vec{w})= \vec{u} \cdot \vec{v} + \lambda \vec{u} \cdot \vec{w}$
- $\vec{u} \cdot \vec{u} \geq 0 \implies \vec{u} \cdot \vec{u}=0\iff \vec{u} = \vec{0}$ 
Debido a la propiedad 3, podemos definir la longitud (o norma) de un vector como
> [!info] Definición
> Lalongitud o norma de un vector se define como:
> $$
|\vec{u}| = \sqrt{\vec{u} \cdot \vec{u}} = \sqrt{\sum_{i=1}^{n} u_{i}^{2}}
$$

