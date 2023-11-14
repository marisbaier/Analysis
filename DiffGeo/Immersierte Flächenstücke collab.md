---
time: 09.11.2023 10:12
tags:
  - concept
  - status/todo
module: M18
aliases:
  - Immersion
---
modul: [[M13 Differentialgeometrie]]
# Immersierte Flächenstücke

>[!def] Definition 4.1: Immersion
>Sei $U\subset\mathbb{R}^{m}$ offen. Eine [[Höhere Ableitungen|glatte]] Abbildung $F:U\rightarrow\mathbb{R}^{n}$ heißt **Immersion**, wenn für jedes $u\in U$ das zugehörige [[Differenzial im Mehrdimensionalen|Differential]] $$dF_{u}:\mathbb{R}^{m}\rightarrow\mathbb{R}^{n}$$injektiv ist, äquivalent dazu: wenn die [[Gradient, Jacobi-Matrix und Hessematrix|Jacobi-Matrix]] $$F'(u)=\left(\frac{\partial F_{i}}{\partial u_{j}}(u)\right)_{i,j=1}^{n,m}$$Rang $m$ hat.
>Ein **immersiertes Flächenstück** in $\mathbb{R}^{3}$ ist eine Immersion $$F:U\rightarrow\mathbb{R}^{3}$$mit $U\subset\mathbb{R}^{2}$ offen.

>[!def] Definition 4.2: Tangentialraum
>Sei $F:U\rightarrow\mathbb{R}^{3}$ eine Immersion wie in 4.1. Sei $u\in U$.
>1. $T_{u}F:=\text{Bild}(dF_{u})\subset\mathbb{R}^{3}$ heißt der **Tangentialraum** zu $F$ in $u$.
>2. Sei $\{e_{1},e_{2}\}$ die [[Basis|Standardbasis]] des $\mathbb{R}^{2}$. Dann heißt $$\{dF_{u}(e_{1}),dF_{u}(e_{2})\}=\{\partial_{1}F(u),\partial_{2}F(u)\}$$die **Standardbasis** (bzgl. $F$) von $T_{u}F$.

>[!exp] Beispiel 4.3
>Sei $U:=\{u\in\mathbb{R}^{2},\left\lVert u\right\rVert\lt1\}$, $F:U\ni u\mapsto(u,\sqrt{1-\left\lVert u\right\rVert^{2}})\in\mathbb{R}^{3}$. Das Bild von $F$ ist die obere Hemisphäre von $\mathbb{S}^{2}\subset\mathbb{R}^{3}$ (ohne Äquator).
>Offenbar $dF_{u}(x)=\left(x,-\frac{\left\langle u,x\right\rangle}{\sqrt{1-\left\lVert u\right\rVert^{2}}}\right)$ und $F$ Immersion. Und $$T_{u}F=\left.\left\{\left(x,-\frac{\left\langle u,x\right\rangle}{\sqrt{1-\left\lVert u\right\rVert^{2}}}\right)\right\vert x\in\mathbb{R}^{2}\right\}=\{v\in\mathbb{R}^{3}\vert v\perp(u,\sqrt{1-\left\lVert u\right\rVert^{2}})\}$$
>![[Pasted image 20231109154741.png|300]]
>Standardbasis bzgl. $F$ von $T_{u}F$: $\left\{\left(1,0,\frac{-u_{1}}{\sqrt{1-\left\lVert u\right\rVert^{2}}}\right),\left(0,1,\frac{-u_{2}}{\sqrt{1-\left\lVert u\right\rVert^{2}}}\right)\right\}$

>[!def] Definition 4.4
>Sei $F:U\rightarrow\mathbb{R}^{3}$ eine Immersion. Die **erste Fundamentalform** $\mathrm{I}_{u}$ zu $F$ in $u\in U$ ist die [[Bilinearformen und Sesquilinearformen|Bilinearform]] $$\mathrm{I}_{u}:\mathbb{R}^{2}\times\mathbb{R}^{2}\ni(X,Y)\mapsto\left\langle dF_{u}(X),dF_{u}(Y)\right\rangle\in\mathbb{R}$$
>Die **erste Fundamentalmatrix** $g(u)$ zu $F$ in $u\in U$ ist die zugehörige $2\times2$-Matrix $(g_{ij}(u))_{i,j=1}^{2}$ mit $$g_{ij}(u):=\mathrm{I}_{u}(e_{i},e_{j})=\left\langle\partial_{i}F(u),\partial_{j}F(u)\right\rangle$$

>[!bem] Bemerkung
>Offenbar gilt $$g(u)=F'(u)^{T}\cdot F'(u)$$

>[!bem] Bemerkung 4.5
>1. Offenbar ist jedes $\mathrm{I}_{u}$ in 4.4 symmetrisch und positiv definit (weil $dF_{u}$ injektiv), also: $\mathrm{I}_{u}$ ist ein [[Kanonisches Skalarprodukt|euklidisches SKP]] auf $\mathbb{R}^{2}$.
>2. Die $g_{ij}:U\rightarrow\mathbb{R}$ sind glatte Funktionen.

>[!def] Definition 4.6
>Sei $F:U\rightarrow\mathbb{R}^{3}$ eine Immersion.
>1. Das **Flächenelement** zu $F$ in $u\in U$ ist die Zahl $$\sqrt{\det g(u)}=\sqrt{\left\lVert\partial_{1}F\right\rVert^{2}\left\lVert\partial_{2}F\right\rVert^{2}-\left\langle\partial_{1}F,\partial_{2}F\right\rangle^{2}}(u)=\left\lVert\partial_{1}F(u)\times\partial_{2}F(u)\right\rVert$$
>2. Für Lebesgue-messbare Mengen $A\subset U$ heißt $$\text{area}_{F}(A):=\int_{A}\sqrt{\det g(u)}\dd u$$der Flächeninhalt von $A$ bzgl. $F$. (dieser hängt von $F$ nur mittels $g$ ab!)

>[!bem] Bemerkung 4.7
>1. Wenn in 4.6.2 zusätzlich $F\vert_{A}$ injektiv ist, oder (schwächer) wenn es eine Lebesgue-Nullmenge $N\subset A$ gibt, sodass $F\vert_{A\setminus N}$ injektiv ist, dann ist $\text{area}_{F}(A)$ zugleich der Flächeninhalt des Bildes $F(A)$.
>2. Wegen der Formel in 4.6 gilt für glatte Abbildungen $F:U\rightarrow\mathbb{R}^{3}$: $$F\text{ Immersion }\Leftrightarrow\det g(u)\ne0\forall u\in U$$

>[!bem] Bemerkung 4.9: Invarianz des Flächeninhaltes unter Umparametrisierung
>Sei $F:U\rightarrow\mathbb{R}^{3}$ eine Immersion, $\tilde U\subset\mathbb{R}^{2}$ offen, $\Phi:\tilde U\rightarrow U$ ein $\mathcal{C}^{\infty}$-[[Koordinatentransformationen und der Satz über den lokalen Diffeomorphismus|Diffeomorphismus]], d.h. glatt, bijektiv, Umkehrung glatt. Sei $\tilde F:=F\circ\Phi:\tilde U\rightarrow\mathbb{R}^{3}$. Dann ist $\tilde F$ ebenfalls eine Immersion, denn für jedes $\tilde u\in\tilde U$ ist $d\tilde F_{\tilde u}=\underbrace{dF_{\Phi(\tilde u)}}_{\text{inj.}}\circ\underbrace{d\Phi_{\tilde u}}_{\text{bij.}}$ injektiv. Außerdem gilt für die 1. Fundamentalform $\tilde{\mathrm{I}}$, 1. Fundamentalmatrix $\tilde g$ zu $\tilde F$:
>1. $$\begin{align*}
&\tilde{\mathrm{I}}_{\tilde u}(X,Y)=\mathrm{I}_{\Phi(\tilde u)}(d\Phi_{\tilde u}(X),d\Phi_{\tilde u}(Y))\\[12pt]
&\tilde g(\tilde u)=\Phi'(\tilde u)^{T}\cdot g(\Phi(\tilde u))\cdot\Phi'(\tilde u)
\end{align*}$$
>2. $$\sqrt{\det\tilde g(\tilde u)}=\sqrt{\det g(\Phi(\tilde u))}\cdot|\det\Phi'(\tilde u)|$$und folglich:
>3. Für Lebesgue-messbare $\tilde A\subset\tilde U$ und $A:=\Phi(\tilde A)$: $$\begin{align*}
\text{area}_{\tilde F}(\tilde A)&=\int_{\tilde A}\sqrt{\det\tilde g(\tilde u)}\dd\tilde u=\int_{\tilde A}\sqrt{\det g(\Phi(\tilde u))}|\det\Phi'(\tilde u)|\dd\tilde u\\[12pt]
&=\int_{A}\sqrt{\det g(u)}\dd u=\text{area}_{F}(A)
\end{align*}$$
