---
title: Espacio Afín
---
# El espacio afín
Dados un conjunto de elementos, siendo estos puntos, $A$, y un espacio vectorial $\mathbb{V}$, llamamos el espacio afín a la terna $(A,\mathbb{V},\varphi)$, siendo $\varphi$ una aplicación entre elementos de $A$, tal que:
$$
\varphi: A \times A \mapsto \mathbb{V}
$$
Esta terna debe cumplir que:
- $\forall p \in A \wedge \vec{v} \in \mathbb{V}, \exists! Q \in A/ \varphi(P,Q) = \vec{PQ}=\vec{u}=Q-P$
- Relación de Chasles: $\forall P,Q,R \in A \wedge\varphi (P,Q) + \varphi (Q,R) = \varphi (P,R)$
$$
\vec{PQ} + \vec{QR} = \vec{PR}
$$
**Demostración**
- $\vec{PQ}=Q-P$
- $\vec{QR}=R-Q$ 
$$
\vec{PQ}+\vec{QR} = Q-P +R-Q = R-P = \vec{PR} 
$$
La dimensión del espacio afín va a ser la dimensión de $\mathbb{V}$. 
## Propiedades del espacio afín
1. $\forall P \in A, \varphi(P,P)=0$
2. $\varphi(P,Q)=0 \iff P=Q$
3. $\forall P,Q \in A, \varphi(P,Q) = -\varphi(Q,P)$
4. Regla del paralelogramo: $\forall P,Q,R,S \in A$:
$$
\varphi(P,Q)=\varphi(R,S) \iff \varphi (P,R) = \varphi (Q,S)
$$
