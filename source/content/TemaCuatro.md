---
title: Tema Cuatro
---
# Variable aleatoria
Existen varias formas de clasificar variables:
- Cualitativa: en función de una cualidad
- Cuantitativa: se puede medir y evaluar con un número.
- Cuasi-cuantitativa: se ordenan en función de una magnitud que puede pertenecer a diferentes intervalos.
Dado un modelo matemático $(\Omega, \mathcal{A}, P)$ formada por un espacio muestral $\Omega$, un álgebra de sucesos $\mathcal{A}$, y una probabilidad $P$.
Una variable discreta $X$ definida sobre el modelo es una función definida como
$$
X:\Omega\to \mathbb{R}
$$
Que se denomina como función de masa $X_{i}$.
Se llama función de distribución de $X$ a la función $F(X)$ que
$$
F(X=x_{j})=P(\{ \omega \in\Omega:X(\omega)\leq x_{j} \})=P(-\infty,x_{j}]
$$
- $\lim_{ x \to -\infty }F(X)=0$
- $\lim_{ x \to \infty }F(X)=1$
- $F$ es monótona decreciente.
- $F$ es continua por la derecha.
- $P(x_{1}< x\leq x_{2})=F(x_{2})-F(x_{1})$
