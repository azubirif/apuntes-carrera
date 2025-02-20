---
title: Cálculo Diferencial
---
# Derivadas de campos escalares
La derivada de un campo escalar, $f$ en un punto $\mathbf{x}$ sería entonces
$$
Df(\mathbf{x})=\lim_{ \mathbf{h} \to 0 } \frac{f(\mathbf{x}+\mathbf{h})-f(\mathbf{x})}{\mathbf{h}} 
$$
Pero la división por vectores no está definida, por lo que vamos a necesitar otra forma.
Por tanto, vamos a definir la **derivada respecto de un vector**.

> [!info] Derivada direccional
> La derivada de una función $f$ respecto de un vector $\mathbf{v}$ se define como
> 
> $$
> f'(\mathbf{x})_{\mathbf{v}} = \lim_{ h \to 0 } \frac{f(\mathbf{x}+h\mathbf{v})-f(\mathbf{x})}{h} 
> $$

> [!example] Ejemplos
> Siendo $f(\mathbf{x})=\sin(xy)$ y $\mathbf{v}=(3,2)$, entonces
> 
> $$
> \begin{align*}
> f'(\mathbf{x}, \mathbf{v}) &= \lim_{ h \to 0 } \frac{\sin[(x+h\cdot 3)(y+h\cdot 2)]-\sin(xy)}{h} \\
> &= \lim_{ h \to 0 } \frac{\sin(xy + h(2x+3y)+6h)-\sin(xy)}{h}\\
> &= \lim_{ h \to 0 } \frac{\sin(xy)\cos(h(2x+3y+6h))+\sin(h(2x+3y+6h))\cos(xy)-\sin(xy)}{h} \\
> &= \lim_{ h \to 0 } \frac{\sin(xy)(\cos[h(2x+3y+6h)]-1)+\cos(xy)\sin[h(2x+3y+6h)]}{h}\\
> &= \lim_{ h \to 0 } \frac{\sin(xy)(1-[h(2x+3y+6h)]^{2} / 2+O(h^{2})-1)+\cos(xy)[h(2x+3y+6h)+O(h)]}{h} \\
> &= \lim_{ h \to 0 } \sin(xy)\left[ -\frac{h}{2}(2x+3y+6h)^{2} +O(h)\right]+\cos(xy)(2x+3y+6h+O(1))\\
> &= \cos(xy)(2x+3y)
> \end{align*}
> $$

Como estas derivadas son un verdadero dolor de calcular, vamos a definir otra forma de calcularlas

> [!success] Teorema
> Sea $g(t)=f(\mathbf{x}+t\mathbf{v})$. Si $g'(t)$ o $f'(\mathbf{x}+t\mathbf{v}, \mathbf{v})$ existe, entonces también existe la otra y son iguales. En particular, cuando $t=0$,
> 
> $$
> f'(\mathbf{x},\mathbf{v})=g'(0)
> $$

> [!tip] Demostración
> 
> $$
> \begin{align*}
> g'(t) &= \lim_{ h \to 0 } \frac{g(t+h)-g(t)}{h}\\
> &= \lim_{ h \to 0 } \frac{f(\mathbf{x}+t\mathbf{v}+h\mathbf{v})-f(\mathbf{x}+t\mathbf{v})}{h}\\
> &= f'(\mathbf{x}+t\mathbf{v},\mathbf{v})
> \end{align*}
> $$

> [!success] Teorema del valor medio
> Sean $f$ y $\mathbf{v}$ tales que $f(\mathbf{x}+t\mathbf{v})$ está definida para todo $t\in [0,1]$ y supongamos que $\exists f'(\mathbf{x}+t\mathbf{v},\mathbf{v}) \forall t\in [0,1]$, entonces
> 
> $$
> \exists \tau \in(0,1):f(\mathbf{x}+\mathbf{v})-f(\mathbf{x})=f'(\mathbf{x}+\tau \mathbf{v},\mathbf{v})
> $$
> 

 > [!tip] Demostración
 > 
 > $$
> g(t)=f(\mathbf{x}+t\mathbf{v})
> $$
> $g$ cumple las condiciones del teorema del valor medio para funciones de una variable:
> 
> $$
> g(1)-g(0)=g'(\tau)(1-0): \tau \in(0,1)
> 
> $$
> Y por tanto
> 
> $$
> f(\mathbf{x}+\mathbf{v})-f(\mathbf{x})=f'(\mathbf{x}+\tau \mathbf{v},\mathbf{v})
> $$

El problema de estas derivadas respecto de un vector es que no se tiene en cuenta la distancia que separa los puntos donde evaluamos $f$, pues esta es
$$
\lvert \mathbf{x}+h\mathbf{v}-\mathbf{x} \rvert =\lvert h\mathbf{v} \rvert 
$$
Para solucionar este problema, utilizaremos vectores de norma $1$. Entonces la derivada se llama **derivada direccional**.
