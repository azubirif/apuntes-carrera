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

Vamos a ver si la diferencial es capaz de detectar discontinuidades.
Supongamos que $f:D\subset \mathbb{R}^n\to \mathbb{R}$ es diferenciable en $\mathbf{x}\in int(D)$. Veamos si esto implica continuidad en $\mathbf{x}$:
Si $f$ es continua en $\mathbf{x}$ se cumplirá
$$
\lim_{ \mathbf{h} \to \mathbf{0} } f(\mathbf{x}+\mathbf{h})=f(\mathbf{x})
$$
Cálculemos entonces este límite:
$$
\begin{align*}
\lim_{ h \to 0 } f(\mathbf{x}+\mathbf{h})&=\lim_{ \mathbf{h} \to 0 } f(\mathbf{x})+T_{\mathbf{x}}+o(|\mathbf{h}|)\\
&=f(\mathbf{x})+T_{\mathbf{x}}(\mathbf{0})+\lim_{ \mathbf{h} \to 0 } |\mathbf{h}|o(1)\\
&=f(\mathbf{x})
\end{align*}
$$
Por tanto, si $f$ es diferenciable en $\mathbf{x}$, también es continua en ese punto.
Ahora, ¿cómo son las derivadas de una función diferenciable?
Calculemos la derivada de $f$ respecto de un $\mathbf{v}$ en $\mathbf{x}$:
$$
\begin{align*}
f'(\mathbf{x},\mathbf{v})&= \lim_{ h \to 0 } \frac{f(\mathbf{x}+h\mathbf{v})-f(\mathbf{x})}{h}\\
&=\lim_{ h \to 0 } \frac{T_{\mathbf{x}}(h\mathbf{v})+o(h)}{h}\\
&=\lim_{ h \to 0 } \frac{hT_{\mathbf{x}}(\mathbf{v})+h\cdot o(1)}{h}\\
&=\lim_{ h \to 0 } T_{\mathbf{x}}(\mathbf{v})+o(1)\\
&=T_{\mathbf{x}}(\mathbf{v})\\
f'(\mathbf{x},\mathbf{v})&=T_{\mathbf{x}}(\mathbf{v})
\end{align*}
$$
Si $\mathbf{v}=(v_{1},\dots,v_{n})\in \mathbb{R}^{n}$, entonces se puede escribir como combinación lineal de vectores de la base canónica de $\mathbb{R}^{n}$.
$$
\mathbf{v}=\sum v_{i}\mathbf{e}_{i}
$$
entonces
$$
T_{\mathbf{x}}(\mathbf{v})=T_{\mathbf{x}}\left( \sum v_{i}\mathbf{e}_{i} \right)=\sum v_{i}T_{\mathbf{x}}(\mathbf{e}_{i})
$$
Sabemos que una aplicación se define por cómo actua esta en los vectores de la base. Como sabemos que $f'(\mathbf{x},\mathbf{v})=T_{\mathbf{x}}(\mathbf{v})$, entonces
$$
=\sum v_{i}f'(\mathbf{x},\mathbf{e}_{i})=\sum v_{i} \frac{ \partial f }{ \partial x_{i} } 
$$
La conclusión de esto es que
$$
\boxed{f'(\mathbf{x},\mathbf{v})=\sum v_{i} \frac{ \partial f }{ \partial x_{i} } }
$$
> [!note] Operador Nabla
> El operador Nabla es un operador lineal que se define como
> 
> $$
> \nabla = \left( \frac{ \partial  }{ \partial x_{i} },\dots,\frac{ \partial  }{ \partial x_{n} }   \right)
> $$
> 
> Luego $\nabla f$ es el **gradiente** de $f$.

Por tanto, si $f$ es diferenciable entonces
$$
f'(\mathbf{x},\mathbf{v})=\nabla f\cdot \mathbf{v}
$$
Con el gradiente es fácil determinar en qué direcciones $f$ crece más deprisa.
Sea $\mathbf{u}$ un vector unitario, entonces:
$$f'(\mathbf{x},\mathbf{u})=\mathbf{u}\cdot \nabla f=|\nabla f|\cos\theta$$
> [!tip] Lema
> Si $\mathbf{v}=\lambda \mathbf{w}\neq \mathbf{0}$ y $f$ es un campo escalar para el que existe $f'(\mathbf{x},\mathbf{v})$ entonces
> 
> $$
> f'(\mathbf{x},\mathbf{v})=\lambda f'(\mathbf{x},\mathbf{w})
> $$

> [!success] Demostración
> 
> $$
> \begin{align*}
> f'(\mathbf{x},\mathbf{v})&=\lim_{ h \to 0 } \frac{f(\mathbf{x}+\mathbf{v}h)-f(\mathbf{x})}{h}\\
> &= \lim_{ h \to 0 } \frac{f(\mathbf{x}+\lambda h\mathbf{w})-f(\mathbf{x})}{h}\\
> &= \lim_{ \hbar \to 0 } \frac{f(\mathbf{x}+\hbar \mathbf{w})-f(\mathbf{x})}{\hbar / \lambda}\\
> &= \lambda \lim_{ \hbar \to 0 } \frac{f(\mathbf{x}+\hbar \mathbf{w})-f(\mathbf{x})}{\hbar}\\
> &=\lambda f'(\mathbf{x},\mathbf{w})
> \end{align*}
> $$

Para reconocer si una función es diferenciable usaremos el siguiente teorema:

> [!tip] Teorema
> Si existen las derivadas parciales $\frac{ \partial f }{ \partial x_{i} }$ en una cierta bola $B_{r}(\mathbf{x})$ y son continuas en $\mathbf{x}$ entonces $f$ es diferenciable en $\mathbf{x}$.
# Cálculo de planos tangentes a funciones en puntos
Supongamos que tenemos una función $f(x,y)$. Vamos a definir una función de la forma
$$
g(x,y,z)=f(x,y)-z
$$
Ahora, evaluaremos la función $f(x_{1},x_{2})$, y calcularemos
$$
\nabla g(x_{1},x_{2},f(x_{1},x_{2}))= (\alpha,\beta,\gamma)
$$
Ahora definiremos un plano como
$$
\pi \equiv \alpha x+\beta y+\gamma z+c=0
$$
Para calcular $c$, sustituimos en el plano los valores de $x_{1},x_{2},f(x_{1},x_{2})$, y despejamoss.
# Diferencial para campos vectoriales
Cada una de las componentes de un campo vectorial $\mathbf{f}(\mathbf{x})=(f_{1}(\mathbf{x}),\dots,f(\mathbf{x})_{m})$ es un campo escalar, y si cada una de ellas es diferenciable en $\mathbf{x}$, podemos introducir la matriz **jacobiana** como
$$
D\mathbf{f}(\mathbf{x})= \begin{pmatrix}
\nabla f_{1}(\mathbf{x}) \\
\dots \\
\nabla f_{m}(\mathbf{x})
\end{pmatrix}
$$
Geométricamente, si tenemos una curva $\mathbf{c}(t)$, que se mappea a $\mathbb{R}^{m}$ como $\mathbf{f}(\mathbf{c}(t))$, se tiene que su vector tangente $\mathbf{v}$ en $\mathbf{x}$ es $D[\mathbf{f}(\mathbf{x})]\mathbf{v}$.
# Derivadas parciales de orden superior
$$
\frac{ \partial  }{ \partial x_{j} } \frac{ \partial f }{ \partial x_{i}}
= \frac{ \partial^{2} f }{ \partial x_{j} \partial x_{i} } 
$$
> [!note] Funciones de clase $\mathcal{C}^{r}$
> Una función $f:A\to \mathbb{R}$ es de clase $\mathcal{C}^{r}$  en $A$, con $r \in \mathbb{N}_{0}$ si todas sus derivadas parciales de orden $r$ existen y son continuas.

> [!success] Teorema de Schwarz
> Si $f\in \mathcal{C}^{2}$, entonces
> 
> $$
> \frac{ \partial^{2}f }{ \partial x_{i}x_{j} } = \frac{ \partial^{2}f }{ \partial x_{j}x_{i} }  
> $$

# Polinomio de Taylor
Sea $A\subset \mathbb{R}^{n}$ un conjunto abierto y convexo (si $\mathbf{a},\mathbf{b}\in A$ está contenido en $A$, entonces $\mathbf{ab}$ está contenido en $A$). Si $f\in \mathcal{C}^{k}$, entonces, definimos el polinomio de Taylor de grado $k$ centrado en $\mathbf{a}$ como
$$
\begin{align*}
P_{\mathbf{a},k}f(\mathbf{x})=f(\mathbf{a})+\sum_{i=1}^{n}\frac{ \partial f }{ \partial x_{i} }(\mathbf{a})(x_{i}-a_{i}) (FALTA~ACABAR)
\end{align*}
$$

Con esto se puede demostrar que
$$
f(\mathbf{x})-P(\mathbf{x})=o(||\mathbf{x}-\mathbf{a}||^{k})
$$
Es decir, que el error se hace más pequeño cuanto más cerca esté $\mathbf{x}$ y $\mathbf{a}$.
Con esto introducimos la **matriz hessiana**, denotada por $H_{f}(\mathbf{a})$, cuyos componentes son
$$
(H_{f}(\mathbf{a}))_{ij}=\frac{ \partial^{2}f }{ \partial x_{i}\partial x_{j} }(\mathbf{a}) 
$$
# Regla de la cadena
$$
D(\mathbf{f}\circ \mathbf{g})(\mathbf{x})=D(\mathbf{f}(\mathbf{g}(\mathbf{x})))D\mathbf{g}(\mathbf{x})
$$
Cada uno de los componentes se define como
$$
[D(\mathbf{f}\circ \mathbf{g})(\mathbf{x})]_{ij} = \frac{ \partial f_{i}(\mathbf{g}(\mathbf{x})) }{ \partial x_{j} }=\sum_{k=1}^{p} \frac{ \partial f_{i} }{ \partial g_{k} }\frac{ \partial g_{k} }{ \partial x_{j} }  
$$
## Derivada de un campo escalar a lo largo de una curva
$$
\frac{d}{dt} (f\circ \mathbf{c}) = \sum_{i=1}^{n} \frac{ \partial f }{ \partial x_{i} }(\mathbf{x}) \frac{d x_{i}}{dt}  
$$
	
