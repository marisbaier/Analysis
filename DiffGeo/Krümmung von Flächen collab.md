---
time: 09.11.2023 19:45
tags:
  - concept
  - status/todo
module: M18
aliases:
---
modul: [[M13 Differentialgeometrie]]
# Krümmung von Flächen

>[!mot] Setting
>Sei hier immer $F:U\rightarrow\mathbb{R}^{3}$ mit $U\subset\mathbb{R}^{2}$ eine [[Immersierte Flächenstücke|Immersion]].

>[!def] Definition 5.1
>Die Abbildung $$N:U\ni u\mapsto\frac{\partial_{1}F(u)\times\partial_{2}F(u)}{\left\lVert\partial_{1}F(u)\times\partial_{2}F(u)\right\rVert}\in\mathbb{S}^{2}\subset\mathbb{R}^{3}$$heißt **Normalenabbildung** (auch: Gauß-Abbildung) zu $F$.

>[!bem] Bemerkung 5.2
>In Def. 5.1 gilt für jedes $u\in U$:
>1. $N(u)$ erzeugt $(T_{u}F)^{\perp}\subset\mathbb{R}^{3}$.
>2. $\left\lVert N(u)\right\rVert=1$.
>3. Der Nenner ist gleich dem Flächenelement $\sqrt{\det g(u)}$.
>4. Für alle $x\in\mathbb{R}^{2}$ gilt: $$dN_{u}(x)\in T_{u}F$$

>[!def] Definition 5.3
>Die **zweite Fundamentalform** zu $F$ in $u$ ist die [[Bilinearformen und Sesquilinearformen|Bilinearform]] $$\mathrm{II}_{u}:\mathbb{R}^{2}\times\mathbb{R}^{2}\ni(x,y)\mapsto-\left\langle dN_{u}(x),dF_{u}(y)\right\rangle\in\mathbb{R}$$
>Die **zweite Fundamentalmatrix** $h(u)$ zu $F$ in $u\in U$ ist die zugehörige $2\times2$-Matrix $(h_{ij}(u))_{i,j=1}^{2}$ mit $$h_{ij}(u):=\mathrm{II}_{u}(e_{i},e_{j})=-\left\langle\partial_{i}N(u),\partial_{j}F(u)\right\rangle$$

>[!bem] Bemerkung 5.4
>1. $$\begin{align*}
&0=\partial_{i}\left\langle N,\partial_{j}F\right\rangle(u)=\left\langle\partial_{i} N(u),\partial_{j}F(u)\right\rangle+\left\langle N(u),\partial_{ij}F(u)\right\rangle\\[12pt]
\Rightarrow\,&h_{ij}(u)=\left\langle\partial_{ij}F(u),N(u)\right\rangle
\end{align*}$$
dies ist symmetrisch in $i,j$! Insbesondere ist $\mathrm{II}$ eine symmetrische Bilinearform, $h(u)$ eine symmetrische Matrix, $$h(u)=-N'(u)^{T}\cdot F'(u)=-F'(u)^{T}\cdot N'(u)$$
>2. Wegen $h_{ij}=\left\langle\partial_{ij}F,N\right\rangle$ braucht man zur Berechnung von $h_{ij}$ nicht unbedingt $\partial_{i}N$ zu berechnen.
>3. Mit $d^{2}F_{u}:\mathbb{R}^{2}\times\mathbb{R}^{2}\ni(X,Y)\mapsto\partial_{x}(\partial_{y}F)(u)=\sum\limits_{i,j=1}^{2}\partial_{ij}F(u)X_{i}Y_{j}\in\mathbb{R}$ bedeutet (1) auch: $$\mathrm{II}_{u}(X,Y)=\left\langle d^{2}F_{u}(X,Y),N(u)\right\rangle$$

>[!thm] Lemma 5.5
>Sei $u\in U$, $X\in\mathbb{R}^{2}\setminus\{0\}$.
> Dann existiert $\varepsilon\gt0$ und eine Kurve $\gamma:(-\varepsilon,\varepsilon)\rightarrow U$ mit $\gamma(0)=u$, $\dot\gamma(0)=X$ und so, dass $c:=F\circ\gamma:(-\varepsilon,\varepsilon)\rightarrow\mathbb{R}^{3}$ in der Ebene $E:=F(u)+\text{span}\{dF_{u}(X),N(u)\}$ verläuft.
> $c$ heißt dann ein **Normalschnitt** zu $F$ in $u$.
> ![[Pasted image 20231114183757.png]]

>[!mot] Proposition 5.6: Geometrische Interpretation von $\mathrm{II}_{u}(X,X)$
>Sei $V\in T_{u}F$ mit $\left\lVert v\right\rVert=1$. Sei $X\in\mathbb{R}^{2}$ der Vektor mit $dF_{u}(X)=V$. Sei $c:F\circ\gamma:(-\varepsilon,\varepsilon)\rightarrow\mathbb{R}^{3}$ ein Normalschnitt zu $F,u,V$. Sei $\kappa:(-\varepsilon,\varepsilon)\rightarrow\mathbb{R}$ die ebene [[Krümmung ebener Kurven|Krümmung]] von $c$ in der Normalenebee $E$ zu $F,u,V$, wobei $E$ so orientiert sei, dass $iV=N(u)$. Dann gilt: $$\boxed{\mathrm{II}_{u}(X,X)=\kappa(0)}$$
>![[Pasted image 20231114184832.png]]

>[!def] Definition 5.7: Weingartenabbildung
>Die **Weingartenabbildung** zu $F$ in $u$ ist die lineare Abbildung $$\boxed{A_{u}:=-(dF_{u})^{-1}\circ dN_{u}:\mathbb{R}^{2}\rightarrow\mathbb{R}^{2}}$$wobei $(dF_{u})^{-1}$ gemeint ist als die Umkehrung von $dF_{u}:\mathbb{R}^{2}\rightarrow T_{u}F$.

>[!thm] Theorem 5.8
>1. Es gilt $$\boxed{\mathrm{II}_{u}(X,Y)=\mathrm{I}_{u}(A_{u}(X),Y)}$$für alle $X,Y\in\mathbb{R}^{2}$, d.h. $A_{u}$ ist der Endomorphismus, der bzgl. des Skalarprodukts $\mathrm{I}_{u}$ zur sym. Bilinearform $\mathrm{II}_{u}:\mathbb{R}^{2}\times\mathbb{R}^{2}\rightarrow\mathbb{R}$ gehört.
>2. Die Matrix zu $A_{u}$ bzgl. der kanonischen Basis des $\mathbb{R}^{2}$ ist $$(g(u))^{-1}\cdot h(u)$$

>[!def] Definition 5.9
>1. Die **Hauptkrümmungen** zu $F$ in $u$ sind die Eigenwerte $\kappa_{1}(u),\kappa_{2}(u)$ von $A_{u}$. Diese sind reell, weil $A_{u}$ sym. bzgl. $\mathrm{I}_{u}$ ist.
>2. $X\in\mathbb{R}^{2}$ heißt eine **Hauptkrümmungsrichtung** zu $F$ in $u$, wenn $X$ Eigenvektor von $A_{u}$ ist und $\mathrm{I}_{u}(X,X)=1$, d.h. $\left\lVert dF_{u}(X)\right\rVert=1$
>3. Die **Gauß-Krümmung** zu $F$ in $u$ ist $$\kappa(u):=\kappa_{1}(u)\cdot\kappa_{2}(u)=\det A_{u}=\frac{\det h(u)}{\det g(u)}$$
>4. Die **mittlere Krümmung** von $F$ in $u$ ist $$H(u):=\frac{1}{2}(\kappa_{1}(u)+\kappa_{2}(u))=\frac{1}{2}\text{tr }A_{u}=\frac{1}{2}\text{tr}(g(u)^{-1}h(u))$$

>[!bem] Bemerkung 5.10
>1. Sei $u\in U$. Falls $\kappa_{1}(u)\ne\kappa_{2}(u)$, dann sind die zugehörigen Hauptkrümmungsrichtungn orthogonal bzgl. $I_{u}$.
>2. $\kappa_{1}(u),\kappa_{2}(u)$ sind das $\max$/$\min$ (oder umgekehrt) der Menge $\{\mathrm{II}_{u}(X,X)\vert X\in\mathbb{R}^{2},\mathrm{I}_{u}(X,X)=1\}$
>3. Aus (2) folgt mit 5.6: 
>   $\kappa_{1}(u),\kappa_{2}(u)$ sind $\max$/$\min$ der ebenen Krümmungen $\kappa(0)$ von Normalschnitten $c$ zu $F$ in $u$. Und: $\kappa(u)$ ist das Produkt dieser ebenen Krümmungen von Normalschnitten, $H(u)$ deren Mittelwert.

>[!exp] Beispiel 5.11: Katenoid
>Wir betrachten $$F:\mathbb{R}^{2}\ni(s,t)\mapsto(\cosh s\cos t,\cosh s\sin t,s)\in\mathbb{R}^{3}$$, eine Drehfläche mit Profilkurve $s\mapsto(\cosh s,0,s)$.
>**1. Fundamentalmatrix**: $$g(s,t)=\begin{pmatrix}\cosh^{2}s & 0 \\ 0 & \cosh^{2}s\end{pmatrix}$$
>**Gauß-Abbildung**: $$N(s,t)=\frac{1}{\cosh s}\begin{pmatrix}-\cos t \\ -\sin t \\ \sinh s\end{pmatrix}$$
>![[Pasted image 20231114194417.png|300]]
>**2. Fundamentalmatrix**: $$h(s,t)=\begin{pmatrix}-1 & 0 \\ 0 & 1\end{pmatrix}$$
>**Gauß-Krümmung**: $$\kappa(s,t)=-\frac{1}{\cosh^{4}s}\lt0\quad\forall(s,t),\qquad s=0\rightsquigarrow|\cdot|\text{ max.}$$
>**Weingarten-Abbildung**: $A_{(s,t)}$ hat Matrix $$\begin{pmatrix}-\frac{1}{\cosh^{2}s} & 0 \\ 0 & \frac{1}{\cosh^{2}s}\end{pmatrix}$$
>**Mittlere Krümmung**: $$H(s,t)=0$$($F$ ist **Minimalfläche**)
>**Hauptkrümmungen**: $$\{\kappa_{1}(s,t),\kappa_{2}(s,t)\}=\left\{-\frac{1}{\cosh^{2}s},\frac{1}{\cosh^{2}s}\right\}$$
>**Hauptkrümmungsrichtungen**: $$\{\pm\frac{e_{1}}{\cosh s},\pm\frac{e_{2}}{\cosh s}\}$$
>Nach Anwendung von $dF_{(s,t)}$ werden die Hauptkrümmungsrichtungen zu $\pm\frac{\partial_{s}F(s,t)}{\left\lVert\cdot\right\rVert}$ (tangential an die $s$-Linien, negativ gekrümmt bzgl. $N$) bzw.$\pm\frac{\partial_{t}F(s,t)}{\left\lVert\cdot\right\rVert}$ (tangential an die $t$-Linien, positiv gekrümmt bzgl. $N$)

>[!bem] Bemerkung 5.12: Verhalten unter Umparametrisierung
>Sei $\tilde U\subset\mathbb{R}^{2}$ offen, $\Phi:\tilde U\rightarrow U$ ein Diffeomorphismus, $\tilde F=F\circ\Phi:\tilde U\rightarrow\mathbb{R}^{3}$. Sei außerdem $U$ zusammenhöngend und sei $$\sigma:=\text{sgn}(\det(d\Phi_{\tilde u}))=\text{const.}\in\{\pm1\}$$
>Dann gilt:
>1. $$\begin{align*}
&\partial_{1}\tilde F(\tilde u)\tilde\partial_{2}\tilde F(\tilde u)=\det(d\Phi_{\tilde u})\cdot(\partial_{1}F\times\partial_{2}F)(\Phi(\tilde u))\\[12pt]
&\tilde N(\tilde u)=\sigma\cdot N(\Phi(\tilde u))
\end{align*}$$
>2. $$\begin{align*}
&\tilde{\mathrm{II}}_{\tilde u}(X,Y)=\sigma\cdot\mathrm{II}_{\Phi(\tilde u)}(d\Phi_{\tilde u}(X),d\Phi_{\tilde u}(Y))\\[12pt]
&\tilde h(\tilde u)=\sigma\cdot\Phi'(\tilde u)^{T}\cdot h(\Phi(\tilde u))\cdot\Phi'(\tilde u)
\end{align*}$$
>3. $$\tilde\kappa(\tilde u)=\kappa(\Phi(\tilde u))$$
>4. $$\tilde A_{\tilde u}=\sigma\cdot d\Phi_{\tilde u}^{-1}\circ A_{\Phi(\tilde u)}\circ d\Phi_{\tilde u}$$
>5. $$\begin{align*}
&\tilde H(\tilde u)=\sigma\cdot H(\Phi(\tilde u))\\[12pt]
&\tilde \kappa_{i}(\tilde u)=\sigma\cdot\kappa_{i}(\Phi(\tilde u)),\qquad i=1,2
\end{align*}$$
