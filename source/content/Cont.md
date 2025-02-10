---
title: Límites y continuidad
---
> [!info] Límite
> Dada $\mathbf{f}:D\subset \mathbb{R}^{n}\to \mathbb{R}^{m}$, si $\mathbf{a}$ es un punto límite de $D$, decimos que $\mathbf{f}(\mathbf{x})$ tiende a $\mathbf{b}$ cuando $\mathbf{x}$ tiende a $\mathbf{a}$, y se denota por
> 
> $$
> \lim_{ \mathbf{x} \to \mathbf{a} } \mathbf{f}(\mathbf{x})=\mathbf{b}
> $$
> Si se cumple que
> 
> $$
> \forall \varepsilon > 0 \exists\delta>0 : |\mathbf{x}-\mathbf{a}|<\delta \implies |\mathbf{f}(\mathbf{x}) - \mathbf{b}|<\varepsilon
> $$
> 
> Esta definición es equivalente al límite
> 
> $$
> \lim_{ |\mathbf{x}-\mathbf{a}| \to 0 } |\mathbf{f}(\mathbf{x})-\mathbf{b}| = 0 
> $$
> 
> En estas definiciones no decimos cómo el punto $\mathbf{x}$ se acerca a $\mathbf{a}$. Por tanto, si el límite depende de por donde nos acerquemos a $\mathbf{a}$, entonces este no existe.

Para evitar utilizar la definición a la hora de calcular límites, utilizaremos los siguientes teoremas.

> [!info] Teorema
> Sean $\mathbf{f}:D\to \mathbb{R}^{m}$ y $\mathbf{g}:C\to \mathbb{R}^{m}$ con $D\cap C \neq \phi$, y sea $\mathbf{a}$ un punto límite de $D\cap C$, y además suponemos que
> $$
> \lim_{ \mathbf{x} \to \mathbf{a} } \mathbf{f}(\mathbf{x})=\mathbf{b}
> $$
> $$
> \lim_{ \mathbf{x} \to \mathbf{a} } \mathbf{g}(\mathbf{x})=\mathbf{c}
> $$
> Entonces se cumple que
> - $\lim_{ \mathbf{x} \to \mathbf{a} } \mathbf{f}(\mathbf{x})+\mathbf{g}(\mathbf{x})=\mathbf{b}+\mathbf{c}$
> - $\lim_{ \mathbf{x} \to \mathbf{a} } \lambda\mathbf{f}(\mathbf{x})=\lambda\mathbf{b}$
> - $\lim_{ \mathbf{x} \to \mathbf{a} } \mathbf{f}(\mathbf{x})\cdot\mathbf{g}(\mathbf{x})=\mathbf{b}\cdot\mathbf{c}$
> - $\lim_{ \mathbf{x} \to \mathbf{a} }|\mathbf{f}(\mathbf{x})|=|\mathbf{b}|$

**Demostración**
Por hipótesis, $|\mathbf{f}(\mathbf{x})-\mathbf{b}|=0$, $|\mathbf{g}(\mathbf{x})-\mathbf{c}|=0$
$$
|\mathbf{f}(\mathbf{x})+\mathbf{g}(\mathbf{x})-\mathbf{b}-\mathbf{c}|\leq
|\mathbf{f}(\mathbf{x})-\mathbf{b}|+|\mathbf{g}(\mathbf{x})-\mathbf{c}| \to 0
$$
Y así deducimos $a$.
Pasando al $c$
$$
\begin{align*}
|\mathbf{f}(\mathbf{x})\cdot \mathbf{g}(\mathbf{x})-\mathbf{b}\cdot \mathbf{c}| &= |(\mathbf{f}(\mathbf{x})-\mathbf{b})(\mathbf{g}(\mathbf{x})-\mathbf{c})+\mathbf{f}(\mathbf{x})\cdot \mathbf{c}+\mathbf{b}\cdot \mathbf{g}(\mathbf{x})-2\mathbf{b}\cdot \mathbf{c}|\\
&=|(\mathbf{f}(\mathbf{x})-\mathbf{b})(\mathbf{g}(\mathbf{x})-\mathbf{c})+\mathbf{f}(\mathbf{x})\cdot \mathbf{c}+\mathbf{b}\cdot \mathbf{g}(\mathbf{x})-\mathbf{b}\cdot \mathbf{c}-\mathbf{b}\cdot \mathbf{c}|\\
&=|(\mathbf{f}(\mathbf{x})-\mathbf{b})(\mathbf{g}(\mathbf{x})-\mathbf{c})+(\mathbf{f}(\mathbf{x})-\mathbf{b})\cdot \mathbf{c}
+\mathbf{b}\cdot (\mathbf{g}(\mathbf{x})-\mathbf{c})|\\
&\leq |(\mathbf{f}(\mathbf{x})-\mathbf{b})(\mathbf{g}(\mathbf{x})-\mathbf{c})| + |(\mathbf{f}(\mathbf{x})-\mathbf{b})\cdot \mathbf{c}|+|\mathbf{b}\cdot (\mathbf{g}(\mathbf{x})-\mathbf{c})|\\
&\leq 0\\
|\mathbf{f}(\mathbf{x})\cdot \mathbf{g}(\mathbf{x})-\mathbf{b}\cdot \mathbf{c}|&\to 0
\end{align*}
$$

También es útil el siguiente teorema
> [!info] Teorema
> Sean $\mathbf{f}$ y $\mathbf{g}$ tales que
> $$
> \lim_{ \mathbf{x} \to \mathbf{a} }\mathbf{g}=\mathbf{b} 
> $$
> y
> $$
> \lim_{ \mathbf{y} \to \mathbf{b} } \mathbf{f}=\mathbf{c}
> $$
> De modo que tenga sentido $\mathbf{f}\circ \mathbf{g}$. Entonces
> $$
> \lim_{ \mathbf{x} \to \mathbf{a} } (\mathbf{f}\circ \mathbf{c})=\mathbf{c}
> $$
