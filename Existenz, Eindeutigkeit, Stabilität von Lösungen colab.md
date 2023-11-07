---
time: 19.10.2023 13:20
tags:
  - concept
  - status/todo
module: P3.3
aliases:
---
modul: [[P3.3 Analysis III]]
# Existenz, Eindeutigkeit, Stabilität von Lösungen

>[!exp] Gegenbeispiel
>- Fundamentalsatz: $f$ nicht stetig $\cd$ Existenz
>- $u'(t)=\sqrt{|u(t)|}$, $u(0)=0$. $$\begin{align*}
&\forall c\ge0,u_{c}\in\mathcal{C}^{1}(\mathbb{R},\mathbb{R}),\\[12pt]
&u_{c}(t)=\begin{cases}
0, & t\le c\\
\frac{1}{4}(t-c)^{2}, & t\ge0
\end{cases}\qquad\text{ ist Lsg.}\quad\cd\text{ Eind.}
\end{align*}$$

>[!thm] Theorem 1.2.1
>Sei $Y$ offen in $\mathbb{R}^{n}$, $y_{0}\in Y$, $I$ reelles Intervall, $t_{0}\in I$. $F:I\times Y\rightarrow\mathbb{R}^{n}$ stetig und lokal Lipschitz in 2. Komp., d.h.: $$\begin{align*}
&\forall(s,y)\in I\times Y:\exists\varepsilon,r,L\gt0:\forall(t,y_{1}),(t,y_{2})\in(s-\varepsilon,s+\varepsilon)\times B(y,r):\\[12pt]
&\left\lVert F(t,y_{1})-f(t,y_{2})\right\rVert\lt L\cdot\left\lVert y_{1}-y_{2}\right\rVert.
\end{align*}$$
>Dann gilt:
>1. Eindeutigkeit der Lösung:
>   $$\begin{align*}
&\exists\delta^{\pm}\gt0:\exists!u:I':=(t_{0}-\delta^{-},t_{0}+\delta^{+})\rightarrow\mathbb{R}^{n}:\\[12pt]
&u'(s)=F(s,u(s))\quad\forall s\in I'\\[12pt]
&u(t_{0})=y_{0}
\end{align*}$$
>    Für $\delta^{\pm}$ maximal gewählt: Explosionskriterium: $$u(s)\xrightarrow[\,s\rightarrow t_{0}\pm\delta^{\pm}\,]{}u_{\infty}\in\partial(Y,\mathbb{\hat R}^{n})$$
>1. Falls $F$ global Lipschitz in 2. Komp., dann: $$I'=I$$

>[!thm] Lemma: Baby-Grönwall
>Sei $a\in\mathbb{R}$, $b\in(0,\infty)$, $u\in\mathcal{C}^{0}([t_{0},t_{0}+D],\mathbb{R})$ ($D\gt0$) mit $$u(t)\le a+b\int_{t_{0}}^{t}u(s)\dd s=U(t)$$
>Dann gilt: $$u(t)\le a\cdot e^{b(t-t_{0})}\forall t\in[t_{0},t_{0}+D)$$

>[!thm] Theorem 1.2.2: Stetige Abh. von Anfangswerten
>1. Sei $\text{Def}(f)\subset\mathbb{R}\times\mathbb{R}^{k}$, $f:\text{Def}(f)\rightarrow\mathbb{R}^{k}$ [[Gleichmäßige Stetigkeit|Lipschitz]] mit LK $L$ in 2. Komp., dann gilt für $u_{t_{0},u_{0}}$ Lösung des AWPs $u'(t)=f(t,u(t))$ zu Zeit $t_{0}$, Anfangswert $u_{0}$: $$\left\lVert u_{t_{0},u_{0}}(t)-u_{t_{0},\tilde u_{0}}(t)\right\rVert\le e^{Lt}\left\lVert u_{0}-\tilde u_{0}\right\rVert\forall t\gt0$$
>2. Sei $f$ wie oben i.A. nur lokal-Lipschitz, dann ist $u_{0}\mapsto u_{t_{0},u_{0}}\vert_{[t_{0}-D,t_{0}+D]}$ stetig in [[Abbildungsräume und Konvergenz von Funktionenfolgen|sup-Norm]]. Die Lsg. einer solchen ("gutartigen") ODE hängt stetig vom Anfangswert ab.
