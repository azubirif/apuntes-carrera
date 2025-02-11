---
title: Segundo Tema
---
# Combinatoria
Supongamos que tenemos $m$ elementos, y vamos a generar grupos. Cada grupo contiene $n$ elementos.
## Variaciones
> [!info] Variaciones con repetición
> Se llaman variaciones de repetición de $m$ elementos, tomados de $n$ en $n$, a los distintos grupos que se pueden formar de tal manera que cada grupo contiene $n$ elementos distintos o iguales, y que un grupo se diferencia de los demás o bien en algún elemento o su posición.
> El número total es
> 
> $$
> VR_{m}^n=m^{n}
> $$

> [!info] Variaciones sin repetición
> Se les llama a las diferentes formas en las que se pueden ordenar $m$ elementos formados en grupos de $n$ elementos. El número total es
> 
> $$
> V_{m,n}=\frac{m!}{(m-n)!}
> $$ 

> [!info] Permutaciones ordinarias
> Si se tienen permutaciones de $n$ elementos, buscamos los distintos grupos que se pueden formar ordenando de diferentes formas $n$ elementos:
> 
> $$
> P_{n}=n!
> $$

> [!info] Permutaciones con repetición
> Donde el primer elemento se repite $\alpha$ veces, el segundo $\beta$ veces, y así hasta el último que se repite $\gamma$ veces. La suma $\alpha+\beta+\dots+\gamma=n$. A los distintos grupos de $n$ elementos que se pueden formar con los $m$ elementos, donde cada grupo se compone de $\alpha$ veces el primer elemento, $\beta$ veces el segundo, etc, el número total es
> 
> $$
> P_{n}= \frac{n!}{\alpha!\beta!\dots\gamma!}
> $$

> [!info] Combinaciones ordinarias o sin repetición
> De $m$ elementos, tomados de $n$ a $n$, a los diferentes grupos que se pueden formar de tal manera que cada grupo contenta $n$ elementos distintos (el orden no importa). La cantidad total es
> 
> $$
> C_{m,n} = \begin{pmatrix}
> m \\ n
\end{pmatrix} = \frac{m!}{n!(m-n)!}
> $$



> [!info] Combinaciones con repetición
> De $m$ elementos, los diferentes grupos que se pueden formar tal que cada grupo contiene $n$ elementos distintos, en cada grupo se pueden repetir elementos, y cada grupo se diferencia al menos en un elemento. El número total es:
> 
> $$
> CR_{m,n} = \begin{pmatrix}
> m+n-1 \\ n
\end{pmatrix} = \frac{(m+n-1)!}{n!(m-1)!}
>$$



