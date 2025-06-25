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
# Estadística descriptiva
Dada una variable aleatoria discreta $X$, se define esperanza de $X$ como
$$
\mu=E(X)=\sum_{i}x_{i}P(X=x_{i})
$$
también la moda, que se define como el valor con mayor probabilidad.
La mediana se define como el valor que se encuentra en la mitad del resto de los valores:
$$
P(-\infty, med]=F(X=med) \geq \frac{1}{2}
$$
## Distribución de una variable condicionada por un suceso $A$
Dada una función de masa $P(X)$, la probabilidad de que $X$ tome $x_{i}$ si ha ocurrido $A$ viene dada por
$$
P(X=x_{i}|A)=\frac{P(\{ \omega \in \Omega|X(\omega)=x_{i} \}\cap A)}{P(A)}
$$
y entonces
$$
E(X|A)=\sum x_{i}P(x_{i}|A)
$$
# Momentos respecto al origen
Se denomina momento respecto al origen de orden $r \forall r \in \mathbb{N}$ y se denota como $\alpha_{r}$:
$$
\alpha_{r}=E[X^{r}] = \sum_{i=0}^{n} x_{i}^{r}P(X=x_{i})
$$
El momento de orden $1$ es el valor medio. Con esto podemos definir la varianza como
$$
\sigma^{2}=E[X^{2}]-E[X]^{2}
$$
También definimos
$$
\mu_{r} = \sum(x-\bar{x})^rP(x)
$$
# Entropía
Definimos la entropía asociada a una variable aleatoria $X$ como
$$
H(X)= -\sum p(x_{i}) \log[p(x_{i})]
$$
