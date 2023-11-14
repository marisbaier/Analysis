---
time: 04.11.2023 19:22
tags:
  - concept
  - status/todo
module: M18
aliases:
---
modul: [[M13 Differentialgeometrie]]
# Kurven im $\mathbb{R}^3$

>[!mot] Setting
>Im folgenden sei immer $c:I\rightarrow\mathbb{R}^{3}$ **dreimal** stetig differenzierbar.

>[!def] Definition 3.1
>Sei $c:I\rightarrow\mathbb{R}^{3}$ nach BL param. und sei $\ddot c(t)\ne0\forall t\in I$.
>1. Wir setzen $$n(t):=\frac{\ddot c(t)}{\left\lVert\ddot c(t)\right\rVert}\quad\text{ und }\quad b(t):=\dot c(t)\times n(t)$$
>   $n:I\rightarrow\mathbb{R}^{3}$ heißt das **Normalenfeld** und $b:I\rightarrow\mathbb{R}^{3}$ das **Binormalenfeld** zu $c$.
>   $\{\dot c,n,b\}$ heißt das begleitende **Frenet-Dreibein** zu $c$. Beachte: für jedes $t\in I$ ist $\{\dot c(t),n(t),b(t)\}$ eine positiv orientierte [[Bilinearformen und Sesquilinearformen|ONB]] von $\mathbb{R}^{3}$.
>2. $$\kappa(t):=\left\langle\ddot c(t),n(t)\right\rangle=\left\lVert\ddot c(t)\right\rVert\ge0$$ heißt die **Krümmung** von $c$ in $t$. $$\tau(t):=\left\langle\dot n(t),b(t)\right\rangle$$ heißt die **Torsion** von $c$ in $t$.

>[!bem] Bemerkung 3.2
>In Definition 3.1 gilt: 
>- $$\kappa(t)=\left\lVert\ddot c(t)\right\rVert=\left\lVert\dot c(t)\times\ddot c(t)\right\rVert=\frac{\left\lVert\dot c\times\ddot c\right\rVert}{\left\lVert\dot c\right\rVert^{3}}(t)$$
>- $$\tau(t)=\left\langle\frac{d}{dt}\left(\frac{\ddot c}{\left\lVert\ddot c\right\rVert}\right)(t),\dot c\times n\right\rangle=\frac{\det(\dot c,\ddot c,\dddot c)}{\left\lVert\dot c\times\ddot c\right\rVert^{2}}$$

>[!def] Definition 3.3
>Sei $c:I\rightarrow\mathbb{R}^{3}$ regulär. Dann heißt $$\kappa(t):=\frac{\left\lVert\dot c\times\ddot c\right\rVert}{\left\lVert\dot c\right\rVert}(t)$$die **Krümmung** von $c$ in $t$. Für $t\in I$ mit $\kappa(t)\ne0$ heißt $$\tau(t):=\frac{\det(\dot c,\ddot c,\dddot c)}{\left\lVert\dot c\times\ddot c\right\rVert^{2}}$$ die **Torsion** von $c$ in $t$.

>[!bem] Bemerkung 3.4
>1. Falls $c$ nach BL param. ist, dann stimmt Def. 3.3 mit Def. 3.1 überein!
>2. Wenn $c:I\rightarrow\mathbb{R}^{3}$ regulär und $\tilde c=c\circ u:J\rightarrow\mathbb{R}^{3}$ eine dreimal stetig diff'bare Umparametrisierung von $c$ ist, dann gilt für die Krümmung $\tilde\kappa$ und die Torsion $\tilde\tau$ von $\tilde c$: $$\begin{align*}
&\tilde\kappa(s)=\kappa(u(s))\quad\forall s\in J\\[12pt]
&\exists\tilde\tau(s)\Leftrightarrow\exists\tau(u(s)\Rightarrow\tilde\tau(s)=\tau(u(s))
\end{align*}$$

>[!bem] Bemerkung 3.5: Frenet-Gleichungen für Raumkurven
>Sei $c:I\rightarrow\mathbb{R}^{3}$ nach BL param., $\ddot c(t)\ne0\forall t\in I$, $\{\dot c,n,b\}$ das begeleitende Frenet-Dreibein. Dann gilt: $$\boxed{\begin{align*}
&\ddot c(t)=\kappa(t)n(t)\\[12pt]
&\dot n(t)=-\kappa(t)\dot c(t)+\tau(t)b(t)\\[12pt]
&\dot b(t)=-\tau(t)n(t)
\end{align*}}\qquad\forall t\in I$$
>Also $$\frac{d}{dt}(\dot c,n,b)(t)=(\dot c,n,b)(t)\cdot\begin{pmatrix}0 & -\kappa & 0 \\ \kappa & 0 & -\tau \\ 0 & \tau & 0\end{pmatrix}(t)\qquad\forall t\in I$$

>[!thm] Theorem 3.6: Fundamentalsatz über Raumkurven
>Sei $\kappa:I\rightarrow(0,\infty)$ stetig diff'bar, $\tau:I\rightarrow\mathbb{R}$ stetig, $t_{0}\in I$. Dann gibt es zu vorgegebenem Anfangspunkt $p\in\mathbb{R}^{3}$, Anfangsvektor $v\in\mathbb{R}^{3}$ mit $\left\lVert v\right\rVert=1$ und Anfangsnormalenvektor $w\in\mathbb{R}^{3}$, $w\perp v$ **genau eine** nach BL param. Kurve $$c:I\rightarrow\mathbb{R}^{3}$$mit Krümmung $\kappa$, Torsion $\tau$ und $$c(t_{0})=p,\qquad\dot c(t_{0})=v,\qquad n(t_{0})=w.$$

>[!thm] Theorem 3.7: Satz von Fenchel
>Sei $c:[0,L]\rightarrow\mathbb{R}^{3}$ nach BL param. und glatt geschlossen. Dann gilt: $$\int_{0}^{L}\kappa(t)\ge2\pi$$mit "$=$" $\Leftrightarrow$ $c$ ist eine **ebene**, einfach geschl. konvexe Kurve. ($c$ eben $\Leftrightarrow\exists\text{ Ebene }E\subset\mathbb{R}^{3}:\text{Bild}(c)\subset E$)
