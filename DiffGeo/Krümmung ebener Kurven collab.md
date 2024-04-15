---
time: 18.10.2023 11:51
tags:
  - concept
module: M13
aliases:
---
modul: [[M13 Differentialgeometrie]]
# Krümmung ebener Kurven

>[!bem] Setting
>Sei nun immer $c:I\rightarrow\mathbb{R}^{2}$ zweimal stetig diff'bar.

>[!mot] Bemerkung 2.1: Intuitive Anforderung an Krümmung
>- Geraden sollen Krümmung $0$ haben.
>- Kreise sollen umso größere Krümmung haben, je kleiner ihr Radius ist.
>
>Wir werden Kurven lokal durch sogenannte Schmiegkreise approximieren und damit die Krümmung definieren.

>[!thm] Lemma 2.2
>Sei $c:I\rightarrow\mathbb{R}^{2}$ nach BL parametrisiert.
>1. Es gilt: $$\textcolor{Aquamarine}{\left\langle\ddot c(t),\dot c(t)\right\rangle=0\qquad\forall t\in I}$$
>2. Sei $t_{0}\in I$ und $\ddot c(t_{0})\ne0$. Dann existiert $\varepsilon\gt0$, sodass gilt: Für jedes Tripel $t_{1}\lt t_{2}\lt t_{3}$ in $(t_{0}-\varepsilon,t_{0}+\varepsilon)\cap I$ liegen $c(t_{1}),c(t_{2}),c(t_{3})$ nicht auf einer Geraden.
>3. Sei $t_{0}\in I$, $\ddot c(t_{0})\ne0$, und sei $\varepsilon\gt0$ wie in 2.
>   Für $t_{1}\lt t_{2}\lt t_{3}$ in $(t_{0}-\varepsilon,t_{0}+\varepsilon)\cap I$ sei jeweils $m(t_{1},t_{2},t_{3})$ der Mittelpunkt des Kreises durch $c(t_{1}),c(t_{2}),c(t_{3})$. Dann gilt: $$\textcolor{Aquamarine}{\lim_{(t_{1},t_{2},t_{3})\rightarrow(t_{0},t_{0},t_{0})}m(t_{1},t_{2},t_{3})=c(t_{0})+\frac{\ddot c(t_{0})}{\left\lVert\ddot c(t_{0})\right\rVert^{2}}=:M(t_{0})}$$
>   ![[Pasted image 20231018140314.png|300]]

>[!bew]- Beweis 2.2
>1. Nach Vorauss. gilt $\left\lVert\dot c(t)\right\rVert=1\forall t\in I$. Daher: $$0=\frac{d}{dt}\left\langle\dot c(t),\dot c(t)\right\rangle=2\left\langle\ddot c(t),\dot c(t)\right\rangle\forall t\in I.$$
>2. Vorüberlegung: Wenn $c(t_{1})$, $c(t_{2})$, $c(t_{3})$ auf einer Geraden liegen, $\nu\ne0$ ein Normalenvektor zu dieser Geraden, $f(t):=\left\langle c(t),\nu\right\rangle$, dann folgt: $$\begin{align*}
&f(t_{1})=f(t_{2})=f(t_{3})\xRightarrow[]{\text{MWS}}\exists\xi_{1}\in(t_{1},t_{2}),\xi_{2}\in(t_{2},t_{3})\text{ mit }f'(\xi_{1})=f'(\xi_{2})=0\\[12pt]
&\xRightarrow[]{\text{MWS}}\exists\eta\in(\xi_{1},\xi_{2})\text{ mit }f''(\eta)=0
\end{align*}$$
>Das bedeutet: $\dot c(\xi_{1})\perp\nu,\dot c(\xi_{2})\perp\nu,\ddot c(\eta)\perp\nu$.
>Insbesondere folgt: $\det(\dot c(\xi_{1}),\ddot c(\eta))=0$.
>Angenommen nun, es gäbe kein $\varepsilon\gt0$ wie in der Behauptung. Dann gäbe es in $I$ Folgen $t_{1,k}\lt t_{2,k}\lt t_{3,k}$ mit $t_{1,k}\rightarrow t_{0}$, $t_{2,k}\rightarrow t_{0}$, $t_{3,k}\rightarrow t_{0}$ für $k\rightarrow\infty$, sodass $c(t_{1,k}),c(t_{2,k}),c(t_{3,k})$ jeweils auf einer Geraden liegen. Aus der Vorüberlegung folgt: Es gäbe also $\xi_{1,k},\eta_{k}$ mit $\xi_{1,k}\rightarrow t_{0}$, $\eta_{k}\rightarrow t_{0}$ für $k\rightarrow\infty$ und $\det(\dot c(\xi_{1,k}),\ddot c(\eta_{k}))=0\forall k$. Weil $\dot c,\ddot c$ stetig sind, folgt: $\det(\dot c(t_{0}),\ddot c(t_{0}))=0$. Das ist aber ein Widerspruch zu $\dot c(t_{0})\ne0$ (Norm $1$), $\ddot c(t_{0})\ne 0$ (Vorauss.), $\left\langle\dot c(t_{0}),\ddot c(t_{0})\right\rangle=0$ (1.).
>3. Skript $\square$

>[!def] Definition 2.3
>Sei $c:I\rightarrow\mathbb{R}^{2}$ nach BL parametrisiert. Sei $t_{0}\in I$.
>1. Wenn $\ddot c(t_{0})\ne0$, dann heißt der Kreis mit Mittelpunkt $$\textcolor{Aquamarine}{M(t_{0}):=c(t_{0})+\frac{\ddot c(t_{0})}{\left\lVert\ddot c(t_{0})\right\rVert^{2}}}$$durch $c(t_{0})$, d.h. mit Radius $\frac{1}{\left\lVert\ddot c(t_{0})\right\rVert}$ der **Schmiegkreis** an $c$ in $t_{0}$.
>2. Für beliebiges $t\in I$ heißt $$\textcolor{Aquamarine}{\boxed{\kappa(t):=\det(\dot c(t),\ddot c(t))}}$$ die (ebene) **Krümmung** von $c$ in $t$.

>[!bem] Bemerkung 2.4
>In Def. 2.3 (also für $c$ nach BL param.) gilt: 
>1. $$\textcolor{Aquamarine}{\kappa(t)}=\det(\dot c(t),\ddot c(t))=\left\langle\ddot c(t),D^{90}\dot c(t)\right\rangle=\textcolor{Aquamarine}{\left\langle\ddot c(t),n(t)\right\rangle}$$mit $$\textcolor{Emerald}{n(t):=D^{90}\dot c(t)=i\dot c(t)}$$wobei $D^{90}:\mathbb{R}^{2}\rightarrow\mathbb{R}^{2}$ die positive Drehung um $90°$ sei (linear, mit Matrix $\begin{pmatrix}0 & -1 \\ 1 & 0\end{pmatrix}$; in $\mathbb{C}\simeq\mathbb{R}^{2}$: Multiplikation mit $i$)
>    ![[Pasted image 20231027145529.png]]
>2. $\ddot c(t)\parallel n(t)$ wegen 2.2.1, also $$\textcolor{Aquamarine}{\boxed{\kappa(t)=\pm\left\lVert\dot c(t)\right\rVert}}$$
>3. Falls $\ddot c(t_{0})\ne0$, dann $\kappa(t_{0})=\pm\frac{1}{\text{Radius des Schmiegkreises an }c\text{ in }t_{0}}$
>4. Falls $\ddot c(t_{0})=0$, dann $\kappa(t_{0})=0$. Das passt heuristisch zu "$0=\frac{1}{\infty}$" mit $\infty$=Radius des "degenerierten Schmiegkreises" $c(t_{0})+\mathbb{R}\dot c(t_{0})$

>[!def] Definition 2.5
>Sei $c:I\rightarrow\mathbb{R}$ regulär. Dann heißt $$\textcolor{Aquamarine}{\boxed{\kappa(t):=\frac{\det(\dot c(t),\ddot c(t))}{\left\lVert\dot c(t)\right\rVert^{3}}}}$$die **ebene Krümmung** von $c$ in $t$.

>[!bem] Bemerkung 2.6
>1. Wenn $c$ nach BL param. ist, dann stimmt Def. 2.5 mit Def. 2.3 überein.
>2. Wenn $c:I\rightarrow\mathbb{R}^{2}$ regulär und $\tilde c=c\circ u:J\rightarrow\mathbb{R}^{2}$ eine orientierungserhaltende (bzw. orientierungsumkehrende) Umparametrisierung von $c$ ist, dann gilt für die Krümmung $\tilde \kappa$ von $\tilde c$: $$\textcolor{Aquamarine}{\tilde \kappa(s)=\pm\kappa(u(s))\qquad\forall s\in J}$$

>[!bem] Bemerkung 2.7: Frenet-Gleichungen
>Sei $c:I\rightarrow\mathbb{R}^{2}$ nach BL parametrisiert. Dann gilt: $$\textcolor{Aquamarine}{\boxed{\begin{align*}
&\ddot c(t)=\kappa(t)n(t)\\[12pt]
&\dot n(t)=-\kappa(t)\dot c(t)
\end{align*}}\qquad\forall t\in I}$$
>Also $\frac{d}{dt}(\dot c,n)(t)=(\dot c,n)(t)\cdot\begin{pmatrix}0 & -\kappa \\ \kappa & 0\end{pmatrix}(t)$.

>[!def] Definition/Bemerkung 2.8
>1. Für eine reguläre Kurve $c:I\rightarrow\mathbb{R}^{2}$ heißt $n:I\rightarrow\mathbb{R}^{2}$ mit $$\textcolor{Aquamarine}{n(t):=D^{90}\left(\frac{\dot c(t)}{\left\lVert\dot c(t)\right\rVert}\right)=i\left(\frac{\dot c(t)}{\left\lVert\dot c(t)\right\rVert}\right)}$$das zugehörige Normalenvektorfeld. Diese Def. stimmt mit oben überein, falls $c$ nach BL param.
>2. Die zweite Frenet-Gleichung $$\textcolor{Aquamarine}{\dot n=-\kappa\dot c}$$gilt für jede reguläre Kurve $c$.

>[!thm] Theorem 2.9: Fundamentalsatz über ebene Kurven
>Sie eine stetige Fkt. $\kappa:I\rightarrow\mathbb{R}$ gegeben. Sei $t_{0}\in I$. Dann existiert zu vorgegebenem Anfangspunkt $p\in\mathbb{R}^{2}$ und Anfangs-Geschwindigkeitsvektor $v_{0}\in\mathbb{R}^{2}$ mit $\left\lVert v_{0}\right\rVert=1$ **genau eine** nach BL param. Kurve $c:I\rightarrow\mathbb{R}^{2}$ mit Krümmung $\kappa$ und $c(t_{0})=p$, $\dot c(t_{0})=v_{0}$.

>[!bew]- Beweis 2.9
>Betrachte zunächst AWP $$\dot A(t)=A(t)\cdot\underbrace{\begin{pmatrix}0 & -\kappa(t) \\ \kappa(t) & 0\end{pmatrix}}_{=:K(t)},\qquad A(t_{0})=(v_{0},iv_{0})$$für $A:I\rightarrow\mathbb{R}^{2\times2}$.
>[[Existenz und Eindeutigkeit von Lösungen|Theorie gew. lin. DGL]] $\Rightarrow$ $\exists!$ Lsg. $A\in\mathcal{C}^{1}(I,\mathbb{R}^{2\times2})$. [[Orthogonal und unitär|Es folgt]] $A(t)\in\text{SO}(2)\forall t$, denn:
>- $A(t_{0})\in\text{SO}(2)$, und $$\begin{align*}
\frac{d}{dt}(AA^{T})&=\dot AA^{T}+A\dot A^{T}=AKA^{T}+A(AK)^{T}\\[12pt]
&=AKA^{T}+AK^{T}A^{T}\xlongequal[]{K^{T}=-K}0
\end{align*}$$dementsprechend $AA^{T}=\text{const.}$, also $A(t)\in O(2)\forall t$. Aus [[Kompakte und zusammenhängende metr. Räume|Stetigkeit]] folgt $A(t)\in\text{SO}(2)\forall t\in I$.
>**Existenz** von $c$:
>Setze $v(t):=$ 1. Spalte von $A(t)$. Dann $\left\lVert v(t)\right\rVert=1\forall t$. Setze $c(t):=p+\int_{t_{0}}^{t}v(\tau)\dd\tau\in\mathbb{R}^{2}$. Dann $\dot c(t)=v(t)$, also $c$ 2-mal stetig diff'bar und nach BL param. Außerdem $c(t_{0})=p$ und $\dot c(t_{0})=v(t_{0})=$ 1. Spalte von $A(t_{0})=v_{0}$.
>$c$ hat Krümmung $\kappa$: $$n(t)=i\dot c(t)=iv(t)=i(\text{1. Spalte von }A(t))=\text{2. Spalte von }A(t)$$
>Krümmung von $c$ in $t$ ist (nach 2.4.1): $$\left\langle\ddot c(t),n(t)\right\rangle=\left\langle\underbrace{\text{1. Sp. von }\dot A(t)}_{=\kappa(t)\cdot\text{2. Sp. von }A(t)},\text{2. Sp. von }A(t)\right\rangle=\kappa(t)$$
>**Eindeutigkeit** von $c$:
>Sei $\tilde c:I\rightarrow\mathbb{R}^{2}$ irgendeine nach BL param. Kurve mit Krümmung $\kappa$, $\tilde c(t_{0})=p$, $\dot{\tilde c}(t)=v_{0}$. Sei $\tilde n:=i\dot{\tilde c}$, und sei $\tilde A:=(\dot{\tilde c},\tilde n)$. Wegen 2.7 erfüllt $\tilde A$ dann dieselbe Differentialgleichung wie $A$, und $\tilde A(t_{0})=(v_{0},iv_{0})=A(t_{0})$ (selbes AWP) $$\begin{align*}
&\Rightarrow\qquad\tilde A(t)=A(t)\qquad\forall t\in I\\[12pt]
&\Rightarrow\qquad\dot{\tilde c}(t)=v(t)\qquad\forall t\in I\\[12pt]
&\Rightarrow\qquad\tilde c(t)=p+\int_{t_{0}}^{t}v(\tau)\dd\tau=c(t)\qquad\forall t\in I\qquad\Rightarrow\tilde c=c&&\square
\end{align*}$$

>[!thm] Proposition 2.10: Interpretation der Krümmung als Winkeländerung von $\dot c$
>Sei $c:[a,b]\rightarrow\mathbb{R}^{2}$ nach BL param.
>1. Es existiert eine stetig diff'bare Fkt. $\varphi:[a,b]\rightarrow\mathbb{R}$ so, dass $$\textcolor{Aquamarine}{\dot c(t)=(\cos(\varphi(t)),\sin(\varphi(t)))=e^{i\varphi(t)}}\qquad\forall t\in[a,b]$$
>   Wenn $\psi,\varphi$ zwei solche Fkt. sind, dann $\exists k\in\mathbb{Z}:\varphi(t)=\psi(t)+2\pi k\forall t\in[a,b]$ (klar)
>2. Für $\varphi$ aus 1. gilt: $\textcolor{Aquamarine}{\varphi'(t)=\kappa(t)}\forall t\in[a,b]$

>[!def] Definition 2.11
>1. $c:[a,b]\rightarrow\mathbb{R}^{n}$ heißt **glatt geschlossen**, wenn $c=\hat c\vert_{[a,b]}$ für eine zweimal stetig diff'bare Kurve $\hat c:\mathbb{R}\rightarrow\mathbb{R}^{n}$, die $(b-a)$-periodisch ist, d.h. $\hat c(t+b-a)=\hat c(t)\forall t\in\mathbb{R}$.
>2. $c$ heißt **einfach glatt geschlossen**, wenn $c$ glatt geschlossen ist und $c(s)\ne c(t)\forall s\gt t$ mit $s\ne a$ oder $t\ne b$. $c(t))$ ist also injektiv für $t\in[a,b)$.

>[!bem] Bemerkung 2.12
>Sei $c:[a,b]\rightarrow\mathbb{R}^{2}$ glatt geschlossen und nach BL parametrisiert. Sei $\varphi$ wie in 2.10.1. Dann gilt: $$\textcolor{Aquamarine}{\int_{a}^{b}\kappa(t)\dd t=\varphi(b)-\varphi(a)\in2\pi\mathbb{Z}}$$

>[!thm] Theorem 2.13: Umlaufsatz
>Sei $c:[a,b]\rightarrow\mathbb{R}^{2}$ einfach glatt geschlossen und nach BL param. Dann gilt: $$\textcolor{Aquamarine}{\boxed{\int_{a}^{b}\kappa(t)\dd t=\pm2\pi}}$$

>[!def] Definition 2.14: Konvexität
>Eine reguläre Kurve $c:I\rightarrow\mathbb{R}^{2}$ heißt **konvex**, wenn für jedes $t_{0}\in I$ gilt: $c(I)$ liegt ganz auf einer Seite der Tangente an $c$ in $t_{0}$, d.h. $$\textcolor{Aquamarine}{\left\langle c(t)-c(t_{0}),n(t_{0})\right\rangle\ge0\qquad\forall t\in I}\qquad\textcolor{red}{{\text{bzw. }\le}}$$

>[!bem] Bemerkung 2.15
>Für eine konvexe Kurve hängt "$\ge$", "$\le$" in 2.14 nicht von $t_{0}$ ab. Also: $$c\text{ konvex }\Leftrightarrow\begin{cases}
&\textcolor{Aquamarine}{\left\langle c(t)-c(t_{0}),n(t_{0})\right\rangle\ge0\qquad\forall t,t_{0}\in I} & \text{oder} \\
&\textcolor{red}{\left\langle c(t)-c(t_{0}),n(t_{0})\right\rangle\le0\qquad\forall t,t_{0}\in I}
\end{cases}$$

>[!thm] Theorem 2.16
>Sei $c:[a,b]\rightarrow\mathbb{R}^{2}$ regulär und einfach geschlossen. Dann sind die folgenden Aussagen äquivalent zueinander: $$c\text{ konvex }\qquad\Leftrightarrow\qquad\kappa(t)\ge0\text{ oder }\le0\quad\forall t\in[a,b]$$

>[!thm] Lemma 2.17
>Sei $c:[a,b]\rightarrow\mathbb{R}^{2}$ regulär, einfach glatt geschlossen und konvex. Wenn eine Gerade $G$ das Bild von $c$ in drei verschiedenen Punkten schneidet, dann durchläuft $c$ ein ganzes Segment von $G$, dass diese Punkte enthält.

>[!def] Definition 2.18: Scheitel
>Sei $c:I\rightarrow\mathbb{R}^{2}$ regulär, und die zugehörige Krümmung $\kappa:I\rightarrow\mathbb{R}$ sei stetig diff'bar. $c$ hat in $t_{0}$ einen **Scheitel**, wenn $\kappa'(t_{0})=0$.

>[!thm] Theorem 2.19: Vierscheitelsatz
>Sei $c:[a,b]\rightarrow\mathbb{R}^{2}$ regulär, einfach glatt geschlossen und konvex. Sei die zugehörige Krümmung $\kappa$ stetig diff'bar. Dann hat $c\vert_{[a,b)}$ **mindestens vier Scheitel**.

>[!bem] Bemerkung 2.20
>Ohne die Voraussetzung "einfach geschl." gilt der Vierscheitelsatz i.A. nicht: ![[Pasted image 20231031161916.png|400]]
