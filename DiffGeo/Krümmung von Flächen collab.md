---
time: 09.11.2023 19:45
tags:
  - concept
module: M18
aliases:
---
modul: [[M13 Differentialgeometrie]]
# Krümmung von Flächen

>[!mot] Setting
>Sei hier immer $F:U\rightarrow\mathbb{R}^{3}$ mit $U\subset\mathbb{R}^{2}$ eine [[Immersierte Flächenstücke|Immersion]].

>[!def] Definition 5.1: Gauß-Abbildung
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
>Die **Weingartenabbildung** zu $F$ in $u$ ist die lineare Abbildung $$A_{u}:=−(dF_{u})^{−1}\circ dN_{u}:\mathbb{R}^{2}\rightarrow\mathbb{R}^{2}$$wobei $(dF_{u})^{-1}$ gemeint ist als die Umkehrung von $dF_{u}:\mathbb{R}^{2}\rightarrow T_{u}F$.

>[!thm] Theorem 5.8
>1. Es gilt $\mathrm{II}_{u}(X,Y)=\mathrm{I}_{u}(A_{u}(X),Y)$ für alle $X,Y\in\mathbb{R}^{2}$, d.h. $A_{u}$ ist der Endomorphismus, der bzgl. des Skalarprodukts $\mathrm{I}_{u}$ zur sym. Bilinearform $\mathrm{II}_{u}:\mathbb{R}^{2}\times\mathbb{R}^{2}\rightarrow\mathbb{R}$ gehört.
>2. Die Matrix zu $A_{u}$ bzgl. der kanonischen Basis des $\mathbb{R}^{2}$ ist $(g(u))^{−1}\cdot h(u)$

>[!def] Definition 5.9
>1. Die **Hauptkrümmungen** zu $F$ in $u$ sind die Eigenwerte $\kappa_{1}(u),\kappa_{2}(u)$ von $A_{u}$. Diese sind reell, weil $A_{u}$ sym. bzgl. $\mathrm{I}_{u}$ ist.
>2. $X\in\mathbb{R}^{2}$ heißt eine **Hauptkrümmungsrichtung** zu $F$ in $u$, wenn $X$ Eigenvektor von $A_{u}$ ist und $\mathrm{I}_{u}(X,X)=1$, d.h. $\left\lVert dF_{u}(X)\right\rVert=1$
>3. Die **Gauß-Krümmung** zu $F$ in $u$ ist $κ(u):=κ_{1}(u)⋅κ_{2}(u)=\det A_{u}=\det h(u)\det g(u)$
>4. Die **mittlere Krümmung** von $F$ in $u$ ist $H(u):=\frac{1}{2}(\kappa_{1}(u)+\kappa_{2}(u))=\frac{1}{2}\text{tr }A_{u}=\frac{1}{2}\text{tr}(g(u)^{−1}h(u))$

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

>[!thm] Satz 5.13: Lokale Normalform von $F$
>Sei $u_{0}\in U$. Dann existieren 
>- eine offene Menge $U'\subset U$ mit $u_{0}\in U'$
>- eine offene Menge $\Omega\subset T_{u_{0}}F$ mit $0\in\Omega$
>- ein [[Koordinatentransformationen und der Satz über den lokalen Diffeomorphismus|Diffeomorphismus]] $\Phi:\Omega\rightarrow U'$ mit $\Phi(0)=u_{0}$, $d\Phi_{0}=(dF_{u_{0}})^{-1}$
>- und eine Funktion $f:\Omega\rightarrow\mathbb{R}$ mit $f(0)=0$, $d_{0}f=0$
>
>so, dass für $\tilde F:=F\circ\Phi:\Omega\rightarrow\mathbb{R}^{3}$ gilt: $$\boxed{\tilde F(V)=F(u_{0})+f(V)N(u_{0})}$$
>_$\tilde F(V)$ parametrisiert das Bild von $F$ lokal als Graph über_ $F(u_{0})+\Omega\subset F(u_{0})T_{u_{0}}F$.
>![[Pasted image 20231118133429.png]]

>[!mot] Proposition 5.14
>Seien $u_{0},\tilde F,f$ wie in 5.13. Dann gilt:
>1. $d^{2}_{0}f=\mathrm{II}_{u_{0}}(dF_{u_{0}}^{-1}(\cdot),dF_{u_{0}}^{-1}(\cdot))$.
>2. Das [[Taylor-Reihen|Taylorpolynom]] 2. Grades um $0\in\Omega\subset T_{u_{0}}F$ zur lokalen Normalform $\tilde F$ ist die Abbildung $$T_{u_{0}}F\ni V\mapsto F(u_{0})+V+\frac{1}{2}\mathrm{II}_{u_{0}}(dF_{u_{0}}^{-1}(V),dF_{u_{0}}^{-1}(V))\cdot N(u_{0})\in\mathbb{R}^{3}$$

>[!def] Definition 5.15: Schmiegparaboloid
>Das Bild $$\begin{align*}
Q_{u_{0}}&:=\{F(u_{0})+V+\frac{1}{2}\mathrm{II}_{u_{0}}(dF_{u_{0}}^{-1}(V),dF_{u_{0}}^{-1}(V))\cdot N(u_{0})\vert V\in T_{u_{0}}F\}\\[12pt]
&=\{F(u_{0})+dF_{u_{0}}(X)+\frac{1}{2}\mathrm{II}_{u_{0}}(X,X)\cdot N(u_{0})\vert X\in\mathbb{R}^{2}\}
\end{align*}$$des 2. Taylorpolynoms um $0$ der Normalform $\tilde F$ zu $F$ in $u_{0}$ heißt das **Schmiegparaboloid** zu $F$ in $u_{0}$.

>[!bem] Bemerkung 5.16
>1. Wenn $X,Y\in\mathbb{R}^{2}$ eine $I_{u_{0}}$-ONB aus Hauptkrümmungsrichugngen zu $\kappa_{1}(u_{0})$ bzw. $\kappa_{2}(u_{0})$ bilden, dann gilt mit $V:=dF_{u_{0}}(X)$, $W:=dF_{u_{0}}(Y)$: $$Q_{u_{0}}=\left\{F(u_{0})+\lambda V+\mu W+\frac{1}{2}(\kappa_{1}(u_{0})\lambda^{2}+\kappa_{2}(u_{0})\mu^{2})\cdot N(u_{0})\vert\lambda,\mu\in\mathbb{R}\right\}$$
>2. Insbesondere:
>    - $\kappa(u_{0})\gt0\Leftrightarrow\kappa_{1}(u_{0}),\kappa_{2}(u_{0})=\ne0$, gleiches Vorzeichen $\Leftrightarrow Q_{u_{0}}$ ein elliptisches Paraboloid
>       ![[Pasted image 20231118142557.png|100]]
>    - $\kappa(u_{0})\lt0\Leftrightarrow\kappa_{1}(u_{0}),\kappa_{2}(u_{0})\ne0$, verschiedene Vorzeichen $\Leftrightarrow Q_{u_{0}}$ ein hyperbolisches Paraboloid
>      ![[Pasted image 20231118142622.png|100]]
>    - $\kappa(u_{0})=0\Leftrightarrow$ mindestens ein $\kappa_{i}(u_{0})=0\Leftrightarrow Q_{u_{0}}$ ein parabolischer Zylinder oder eine Ebene
>      ![[Pasted image 20231118142631.png|200]]

>[!def] Definition 5.17
>1. $u_{0}$ heißt ein **elliptischer** bzw. **hyperbolischer** Punkt von $F$, wenn $\kappa(u_{0})\gt0$ bzw. $\kappa(u_{0})\lt0$ gilt.
>2. $u_{0}$ heißt ein **parabolischer** bzw. **planarer** Punkt von $F$, wenn $\kappa_{i}(u_{0})=0$ für genau ein $i\in\{1,2\}$ bzw. für beide $i\in\{1,2\}$
>3. $u_{0}$ heißt ein **Nabelpunkt** von $F$, wenn $\kappa_{1}(u_{0})=\kappa_{2}(u_{0})$
>   ($\Leftrightarrow Q_{u_{0}}$ ein Rotationsparaboloid oder eine Ebene)

>[!thm] Satz 5.18
>Wenn jedes $u\in U$ Nabelpunkt und $U$ zusammenhängend ist, dann liegt $F(U)$ in einer Ebene oder einer Sphäre!

>[!def] Definition 5.19
>1. $X\in\mathbb{R}^{2}$ heißt eine **Asymptotenrichtung** zu $F$ in $u$, wenn $\mathrm{II}_{u}(X,X)=0$ und $\mathrm{I}_{u}(X,X)=1$ ist.
>2. Eine reguläre Kurve $\gamma:I\rightarrow U$ heißt eine **Krümmungslinie** zu $F$, wenn für jedes $t\in I$ gilt: $$\frac{\dot\gamma(t)}{\sqrt{\mathrm{I}_{\gamma(t)}(\dot\gamma(t),\dot\gamma(t))}}$$ ist eine Hauptkrümmungsrichung zu $F$ in $\gamma(t)$.
>3. Eine reguläre Kurve $\gamma:I\rightarrow U$ heißt eine **Asymptotenlinie** zu $F$, wenn für jedes $t\in I$ gilt: $$\frac{\dot\gamma(t)}{\sqrt{\mathrm{I}_{\gamma(t)}(\dot\gamma(t),\dot\gamma(t))}}$$ ist eine Asymptotenrichtung zu $F$ in $\gamma(t)$.

>[!bem] Bemerkung 5.20
>1. Statt $X$ bezeichnet man auch $dF_{u}(X)\in T_{u}F$ als HKR bzw. Asy.R. und statt $\gamma$ auch $c:=F\circ\gamma:I\rightarrow\text{Bild }F$ als Krümmungslinie bzw. Asymptotenlinie, wenn dadurch keine Mehrdeutigkeit entsteht, z.B. wenn $F$ injektiv ist.
>2. Genau dann sind alle Parameterlinien $F(\cdot,u_{2}),F(u_{1},\cdot)$ Krümmungslinien (im Sinne von (1)) wenn $\frac{e_{1}}{\sqrt{\mathrm{I}_{u}(e_{1},e_{1})}}$ und $\frac{e_{2}}{\sqrt{\mathrm{I}_{u}(e_{2},e_{2})}}$ für jedes $u\in U$ HKR sind, d.h. EV zu $A_{u}$. $\Leftrightarrow$ wenn $g^{-1}(u)\cdot h(u)$ diagonal ist $\forall u\in U$. Z.B. ist dies bei allen Drehflächen aus ÜA10 der Fall! Dort sind also Breitenkreise ($\varphi$-Linien) und Meridiane ($s$-Linien) immer Krümmungslinien.

>[!thm] Proposition 5.21
>Sei $\gamma:I\rightarrow U$ regulär, $c:=F\circ\gamma\rightarrow\text{Bild }F\subset\mathbb{R}^{3}$. Dann gilt:
>1. $\gamma$ (bzw. $c$) Krümmungslinie $$\Leftrightarrow(N\circ\gamma)'(t)\parallel\dot c(t)\quad\forall t\in I$$
>2. $$\boxed{\mathrm{II}_{\gamma(t)}(\dot\gamma(t),\dot\gamma(t))=-\left\langle(N\circ\gamma)'(t),\dot c(t)\right\rangle=\left\langle\ddot c(t),N(\gamma(t))\right\rangle}$$insbesondere: $\gamma$ (bzw. $c$) Asymptotenlinie $$\Leftrightarrow(N\circ\gamma)'(t)\perp\dot c(t)\quad\forall t\in I\qquad\Leftrightarrow\qquad\ddot c(t)\perp N(\gamma(t))\quad\forall t\in I$$

>[!def] Definition 5.23
>Ein $3$-fach-orthogonales Flächensystem ist eine glatte Abbildung $\Psi:W\rightarrow\mathbb{R}^{3}$, wobei $W\subset\mathbb{R}^{3}$ offen und $\Psi$ so, dass für jedes $w\in W$ die Vektoren $\partial_{1}\Psi(w),\partial_{2}\Psi(w),\partial_{3}\Psi(w)$ eine Orthogonalbasis von $\mathbb{R}^{3}$ bilden.

>[!thm] Satz 5.24: Satz von Dupin
>"_Die Parameterlinien eines $3$-fach orthogonalen Flächensystems sind Krümmungslinien_", d.h.
>Sei $\Psi:W\rightarrow\mathbb{R}^{3}$ ein $3$-fach orthog. Flächensystem. Sei $w_{3}\in\mathbb{R}$ und $U:=\{(w_{1},w_{2})\in\mathbb{R}^{2}\vert(w_{1},w_{2},w_{3})\in W\}\ne\emptyset$. Sei $F:U\ni(w_{1},w_{2})\mapsto\Psi(w_{1},w_{2},w_{3})\in\mathbb{R}^{3}$ ($\Rightarrow F$ Immersion $\checkmark$) Dann sind die Parameterlinien von $F$ Krümmungslinien. (Analog für jedes feste $w_{1}$ bzw $w_{2}$ statt festem $w_{3}$)

>[!mot] Ziel jetzt zz.:
>Die Gaußsche Krümmung $K$ ist bereits durch die 1. Fundamentalform festgelegt!

>[!def] Definition 5.24
>Die **Christoffelsymbole** zu $F$ sind die glatten Funktionen $\Gamma_{ij}^{k}:U\rightarrow\mathbb{R}\quad(i,j,k\in\{1,2\})$, die definiert sind durch $$\partial_{ij}F(u)=\Gamma_{ij}^{1}(u)\partial_{1}F(u)+\Gamma_{ij}^{2}(u)\partial_{2}F(u)+h_{ij}(u)N(u)$$

>[!bem] Bemerkung 5.25
>1. Definition 5.24 macht SInn, weil $\{\partial_{1}F(u),\partial_{2}F(u),N(u)\}$ eine Basis von $\mathbb{R}^{3}$ sind (Koeff. eindeutig bestimmt)
>2. Wegen $\partial_{ij}F=\partial_{ji}F$ gilt: $$\Gamma_{ij}^{k}=\Gamma_{ji}^{k}\qquad\forall i,j,k\in\{1,2\}$$

>[!thm] Proposition 5.26
>Die Christoffelsymbole hängen **nur** von der 1. Fundamentalform ab! Genauer: Schreibe $(g(u))^{-1}=:(g^{ij}(u))_{i,j=1,2}$, dann gilt: $$\boxed{\Gamma_{ij}^{k}=\frac{1}{2}\sum\limits_{l=1}^{2}g^{kl}(\partial_{i}g_{jl}+\partial_{j}g_{il}-\partial_{l}g_{ij})}$$

>[!thm] Satz 5.27: Theorema Egregium von Gauß
>Die Gauß-Krümmung $K=\frac{\det h}{\det g}:U\rightarrow\mathbb{R}$ hängt **nur** von $g:U\rightarrow\text{Mat}(2,2,\mathbb{R})$ ab! Genauer gilt: $$\boxed{\det h=\sum\limits_{m=1}^{2}\left[\partial_{2}\Gamma_{11}^{m}-\partial_{1}\Gamma_{12}^{m}+\sum\limits_{a=1}^{2}(\Gamma_{11}^{a} \Gamma_{2a}^{m}-\Gamma_{12}^{a} \Gamma_{1a}^{m})\right]\cdot g_{m2}}$$
>$K$ lässt sich also durch die $g_{ij}$ und deren Ableitungen erster und zweiter ORdnung ausdrücken!

>[!bem] Bemerkung 5.28
>Seien $F,\hat F:U\rightarrow\mathbb{R}^{3}$ zwei Immersionen. Genau dann haben $F,\hat F$ gleiche 1. Fundamentalform $I=\hat I$ ($\Leftrightarrow g=\hat g$) wenn für **jede** stetig diff'bare $\gamma:[a,b]\rightarrow U$ gilt: $$L(F\circ\gamma)=L(\hat F\circ\gamma)$$

>[!bem] Folgerung 5.29: _"$\not\exists$ längentreue Landkarten der Erdoberfläche"_
>Wenn $F$ **längentreu** ist, d.h. $L(F\circ\gamma)=L(\gamma)$ für alle stetig diff'baren Kurven $\gamma:[a,b]\rightarrow U$, dann folgt: $K=0$! Insbesondere: Es gibt **keine** längentreue Immersion $F:U\rightarrow\mathbb{R}^{3}$ mit $\text{Bild }F\subset\mathbb{S}^{2}$. (Denn dann $K=1$, Widerspruch zu $K=0$)
