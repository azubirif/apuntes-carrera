## Relaciones
Existen dos tipos de relaciones:
- De orden
- De equivalencia
Una relación $R$ de $A$ en $B$ es cualquier subconjunto de $A \times B$:
$$
R \subset A \times B
$$
Y denotamos $(a,b) \in R$ por $a~R~b$, diciendo que $a$ está relacionado con $b$.
### Relaciones de equivalencia
Podemos hablar de relaciones **internas** $(a=b)$ o **externas** $(a \neq b)$.
Sea $A \neq \phi$, una relación de equivalencia definida sobre $A$ es una relación que satisface las siguientes propiedades:
1. $\forall x \in A,~x \sim x$ (reflexiva).
2. Dados $x$ e $y$ en $A$, si $x\sim y$, entonces $y \sim x$ (simetría).
3. Dados $x\sim y$, e $y \sim z$, entonces $x \sim z$ (transitiva).
Todo esto se lee como $x$ equivalente a $y$. Todas estas propiedades se deben cumplir.
Para escribir esto como subconjuntos del producto cartesiano:
$$
x \sim x \equiv (x,x) \in \sim
$$
Si tenemos un conjunto $A$, y este esta dividido en subconjuntos disjuntos, entonces dados dos elementos en $A$, estos son equivalentes sí y solo sí ambos pertenecen al mismo subconjunto.
$$
S_{i} \subset A, x \sim y \iff x,y \in S_{i}~ :~ A = S_{1} \cap\dots \cap S_{n}
$$
**Ejemplos**:
Tomamos en $\mathbb{Z}$, dado un entero $n>1$, entonces definimos para $a,b \in \mathbb{Z}$,
$$
a \equiv b ~ mod_{n} \iff n | b -a
$$
$a$ congruente con $b$ módulo $n$.
Esto define una relación de equivalencia en $\mathbb{Z}$ de módulo $n$.
Debemos demostrar que esa relación cumple las propiedades definidas anteriormente para poder afirmar que es de equivalencia.
1. Es reflexiva: dado un $a \in \mathbb{Z}$, $n | a-a$, ya que $a-a = 0$, entonces $a$ es congruente con $a ~ mod_{n} \forall a \in \mathbb{Z}$.
2. Es simétrica: dados dos $a,b \in \mathbb{Z}$, si $a \equiv b ~mod_{n} \iff n|b-a$, entonces $n |a-b \iff b \equiv a ~mod_{n}$.
3. Es transitiva: dados $a,b,c \in \mathbb{Z} / a \equiv b~ mod_{n}$ y $b \equiv c ~ mod_{n}$, entonces $n |b-a$ y $n|c-b$, por tanto $b-a = nx$ y $c-b = ny$, entonces $c-a=n(x+y)=nz \implies n |c-a$.
Como cumple con las propiedades, es una relación de equivalencia.
Si $n>1$, ¿cuáles son las clases de equivalencia de la congruencia módulo $n$?
Sean $a,b\in \mathbb{Z}$, y los dividimos entre $n$:
$$
a = q_{1}n+r_{1}:0\leq r_{1}<n
$$
$$
b=q_{2}n+r_{2}:0\leq r_{2}<n
$$
¿Qué pasa si $a$ es congruente con $b$ módulo $n$?
Entonces, $n |b-a$, y $b-a=n(q_{2}-q_{1}) +r_{2}-r_{1}$. Si $n|b-a$, entonces $\exists m \in \mathbb{Z}: b-a=nm \implies nm=(q_{2}-q_{1})n+r_{2}-r_{1}\implies n(m-q_{2}+q_{1})=r_{2}-r_{1}$.
Pero como $0\leq|r_{2}-r_{1}|<n$. Sabiendo que $r_{2}-r_{1} = kn$, y $r_{2}-r_{1} < n$, entonces la única posibilidad es que $k=0$. Esto implica que $\frac{n}{a}$ y $\frac{n}{b}$ tienen el mismo resto.

---
Vamos a tomar en el plano $\mathbb{R}^2$, decimos que dos puntos $P$ y $Q$ son equivalentes (o están relacionados) sí y solo sí la distancia de $P$ al origen es la distancia de $Q$ al origen, donde $\vec{O} = (0,0)$. Vamos a ver si cumple las propiedades:
$$
P \sim Q \iff d(P,O)=d(Q,O)
$$
1. Es reflexivo: $P \sim P \iff d(P,O) = d(P,O)$. Esto se cumple por sí mismo.
2. Es simétrico: $P\sim Q \iff d(P,O) = d(Q,O)$, y se cumple que como $d(Q,O)=d(P,O) \iff Q\sim P$.
3. Es transitivo: $P\sim Q \iff d(P,O) = d(Q,O)$. Si $Q\sim R \iff d(Q,O) = d(R,O)$, entonces si sustituimos tenemos que $d(P,O)=d(R,O) \iff P \sim R$.
### Definición
Sea $A \neq \phi$ y $\sim$ una relación de equivalencia sobre $A$. Entonces $\forall a \in A$, el conjunto $[a] = \{ x \in A : a \sim x \}$ se llama la clase de equivalencia de $a$.