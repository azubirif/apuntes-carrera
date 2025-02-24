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

# Derivadas parciales
Las derivadas parciales son aquellas que se hacen respecto a un eje. Si como vector unitario usamos uno de la base canónica de $\mathbb{R}^{n}$
$$
\{ \mathbf{e}_{i} \}
$$
donde
$$
(\mathbf{e}_{i})_{j}=\delta_{ij}
$$
entonces la correspondiente derivada direccional en un punto $\mathbf{x}$ es
$$
f'(\mathbf{x};\mathbf{e}_{i})
$$
es la **derivada parcial** respecto a $\mathbf{e}_{i}$, y se denota por $D_{i}f=\partial_{i}f$.
Observemos que
$$
\boxed{
f'(\mathbf{x},\mathbf{e}_{i})=\lim_{ h \to 0 } \frac{f(\mathbf{x}+h \mathbf{e}_{i})-f(\mathbf{x})}{h}= \frac{ \partial f }{ \partial x_{i} } 
}
$$
Como todos los componentes que no estén alineados con $\mathbf{e}_{i}$ no cambian, podemos tomarlos como si **fuesen constantes**, es decir, como una derivada ordinaria respecto a $x_{i}$.
# La diferencial
Las derivadas direccionales nos dan una información muy pobre del comportamiento de una función. Queremos buscar algo análogo a
$$
Df(\mathbf{x})=\lim_{ \mathbf{h} \to 0 } \frac{f(\mathbf{x}+\mathbf{h})-f(\mathbf{x})}{\mathbf{h}} 
$$
El problema es que tenemos un vector dividiendo. Vamos a tomar que $\mathbf{h}$ es un vector finito
$$
\begin{align*}
Df(\mathbf{x})+\varepsilon(\mathbf{x},\mathbf{h})&=\frac{f(\mathbf{x}+\mathbf{h})-f(\mathbf{x})}{\mathbf{h}}\\
\mathbf{h}(Df(\mathbf{x})+\varepsilon(\mathbf{x},\mathbf{h}))&=f(\mathbf{x}+\mathbf{h})-f(\mathbf{x})
\end{align*}
$$
Se tiene que cumplir que
$$
\lim_{ h \to 0 } \varepsilon(\mathbf{x},\mathbf{h})=0 
$$
ahora sigue que
$$
\begin{align*}
\mathbf{h}Df+\mathbf{h}\varepsilon &=f(\mathbf{x}+\mathbf{h})-f(\mathbf{x})
\end{align*}
$$
Para que el lado izquierdo sea escalar, $\mathbf{h}$ debe ser una matriz $n\times 1$, y $Df$ otra de $1\times n$. Podemos reescribir esto como
$$
f(\mathbf{x}+\mathbf{h})-f(\mathbf{x})=T_{\mathbf{x}}(\mathbf{h})+|\mathbf{h}|E(\mathbf{x},\mathbf{h})
$$
Como $\varepsilon\to {0}$ si $h\to 0$, entonces también lo hará $E(\mathbf{x},\mathbf{h})$. Entonces obtenemos
$$
f(\mathbf{x}+\mathbf{h})-f(\mathbf{x})=T_{\mathbf{x}}(\mathbf{h})+o(|\mathbf{h}|)
$$

> [!tip] Diferencial de una función
> Sean $f:S\subset \mathbb{R}^n\to \mathbb{R}$ y $x \in int(S)$, $B_{r}(\mathbf{x})\subset S$ y $\mathbf{v}\in \mathbb{R}^{n}$ tal que $\mathbf{x}+\mathbf{v}\in B_{r}(\mathbf{x})$.
> Decimos que $f$ es diferenciable en $\mathbf{x}$ si existe una transformación lineal $T_{\mathbf{x}}:\mathbb{R}^{n}\to \mathbb{R}$ tal que
> 
> $$
> f(\mathbf{x}+\mathbf{v})-f(\mathbf{x})=T_{\mathbf{x}}(\mathbf{v})+o(|\mathbf{v}|)
> $$

