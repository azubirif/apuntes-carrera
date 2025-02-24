---
title: Tema 3
---
# Probabilidad condicionada
- Modelos dinámicos: experimentos que se realizan a lo largo del tiempo. Los experimentos son dependientes entre sí.
- Modelos estáticos: mismo período de tiempo.

La probabilidad de que ocurra $B$ si ocurre $A$ es
$$
P(B|A)= \frac{P(A\cap B)}{P(A)}
$$

> [!tip] Regla del producto
> Supongamos un modelo dinámico donde ocurren sucesos de forma consecutiva $\{ A_{1},\dots,A_{n} \}$, se cumple que
> 
> $$
> \begin{align*}
> &P(A_{1}\cap\dots \cap A_{n})=\\ &P(A_{1})P(A_{2}|A_{1})P(A_{3}|A_{1}\cap A_{2})\dots P(A_{n}|A_{1}\cap\dots \cap A_{n-1})
> \end{align*}
> $$
> 

> [!example] Ejemplo 1
> Se extraen cartas de una baraja española. Una vez extraída una carta, no se reemplaza. Halla la probabilidad de extraer:
> 1. Rey de copas
> 2. Figura de espadas
> 3. Una de oro
> $$
> \begin{align*}
> P(A_{1}\cap A_{2}\cap A_{3})&=
> P(A_{1})P(A_{2}|A_{1})P(A_{3}|A_{1}\cap A_{2})\\
> &= \frac{1}{40} \frac{3}{39} \frac{10}{38}
> \end{align*}
> $$
> 

## Diagrama de árbol
![[tree_diagram.png]]

> [!example] Ejemplo 2
> Tenemos una moneda equilibrada y dos urnas. La urna 1 contiene 1 bola blanca y 1 bola negra. La urna 2 contiene 3 bolas blancas y 1 bola negra. Se realiza el siguiente sorteo que cumple las reglas que se indican a continuación. Lanzamos una moneda. Si sale cara, elegimos una bola de la urna 1. Sin embargo, si sale cruz, seleccionamos una bola de la urna 2. ¿Cuál es el espacio muestral del modelo dinámico? . Halla la probabilidad de elegir bola negra.
> ![[diagrama_arbol_ej2.png]]
> Con esto, la probabilidad de obtener negra sería:
> 
> $$
> \begin{align*}
> P(N)&=P(A_{1}\cap N)+P(A_{2}\cap N)\\&=P(A_{1})P(N|A_{1})+P(A_{2})P(N|A_{2})\\
> &= 0.5\cdot 0.5+0.5\cdot 0.25 \\ &= \frac{3}{8}
> \end{align*}
> $$
> 

> [!info] Definición
> $A$ y $B$ son sucesos independientes si
> $$
> P(A\cap B)=P(A)\cdot P(B)
> $$
> 

> [!info] Sucesos completamente independientes
> Sea $H$ una familia de sucesos que no incluyen al espacio vacío. Se dice que $H$ está formada por sucesos completamente independientes, si para todo subconjunto de $H$ se verifica que $H=\{ \Delta_{1},\dots,\Delta_{k} \}$
> 
> $$
> P(\Delta_{1}\cap\dots \cap\Delta_{n})=\prod_{i=1}^j P(\Delta_{i})
> $$
> 

> [!tip] Teorema de la probabilidad total
> Dado un modelo matemático probabilístico representado por $(\Omega, \mathcal{A}, P)$, un sistema completo formado por $\{ A_{1},\dots,A_{n} \}\in \mathcal{A}$ (con todos ellos excluyentes), y sabiéndose $\exists B \in \mathcal{A}P(B|A_{i})\forall i$, se verifica que
> 
> $$
> P(B)=\sum P(A_{i}) P(B|A_{i})
> $$
> 
> Entonces se verifica que
> 
> $$
> P(A_{i}|B) = \frac{P(A_{i})P(B|A_{i})}{P(B)}
> $$
> 

## Independencia condicional
Si se verifica que
$$
P(A\cap B|C)=P(A|C)P(B|C)
$$
Entonces $A$ y $B$ son condicionalmente independientes dado $C$.