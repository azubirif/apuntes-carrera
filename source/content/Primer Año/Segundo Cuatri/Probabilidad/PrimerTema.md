---
title: Primer Tema
---
# Experimentos Aleatorios
## Espacio muestral
Son sucesos aleatorios repetidos cuyos resultados no se pueden determinar de
antemano. El objetivo es describir el fenónemo desde un punto de vista aleatorio
que describa el proceso.
El espacio muestral es el conjunto formado por todos los posibles resultados:
$$
\Omega = \{ \omega_{1},\dots ,\omega_{n} \}
$$
Y tenemos diferentes tipos:
- Discreto: finito o numerable.
- Continuo.
Un suceso es cualquier subconjunto del espacio muestral.
El proceso de codificación es el que consiste en pasar de una variable cualitativa a una cuantitativa.
## Conjunto de partes
El conjunto de partes del espacio muestral es el conjunto de todos los posibles resultados de un experimento.
# Probabilidad
Cualesquiera que sean $A$, se tiene que $0\leq n(A)\leq n$, y que por tanto
$$
\lim_{ n \to \infty } \frac{n(A)}{n}=P(A) 
$$
Si $A$ ocurre siempre, $n(A)=n \implies P(A)=1$
Además, si $A$ y $B$ son excluyentes, se tiene que $P(A \cap B) = 0$, y que $P(A \cup B) = P(A)+P(B)$.
# Axiomas de Kolmogorov
Las propiedades anteriores dotan a $\mathbb{A}, \cap, \cup$ de una estructura de álgebra de Boole ($\sigma$-álgebra).
Una probabilidad $P$ definida sobre un álgebra de sucesos $A$, de un espacio muestral finito $\Omega$, es una función $P:A\to[0,1]$.
- $P(\Omega)=1$
- $P(A) \in [0,1] \forall A$
- Si $A$ y $B$ son excluyentes, se tiene que $P(A \cap B) = 0$, y que $P(A \cup B) = P(A)+P(B)$.
## Propiedades
- $P(\phi)=0$
- $P(\bar{A})=1-P(A)$
- $P(A-B)=P(A)-P(A \cap B)$
	- Además, si $B \subset A$, $P(A-B)=P(A)-P(B)$
- $P(A \cup B)=P(A)+P(B)-P(A \cap B)$
- $P(A_{1}\cup A_{2}\cup A_{3})=\sum_{i=1}^3P(A_{i})-\sum_{i<j}P(A_{i}\cap A_{j})+P(A_{1}\cap A_{2}\cap A_{3})$
