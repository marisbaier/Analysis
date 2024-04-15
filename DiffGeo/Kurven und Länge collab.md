---
time: 17.10.2023 11:31
tags:
  - concept
module: M13
aliases:
---
modul: [[M18 Partielle Differentialgleichungen]]
# Kurven und Länge

>[!def] Definition 1.1: Kurve
>Eine (parametrisierte) Kurve in $\mathbb{R}^{n}$ ist eine [[Mehrdimensionale Konvergenz und Stetigkeit|stetige]] Abbildung $$c:I\rightarrow\mathbb{R}^{n}$$wobei $I\subset\mathbb{R}$ ein bel. Intervall ist.

>[!exp] Beispiele 1.2
>1. $c:\mathbb{R}\ni t\mapsto(a\cos t,b\sin t)\in\mathbb{R}^{2}$ mit $$c(\mathbb{R})=\left\{(x,y)\in\mathbb{R}^{2}\vert\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}=1\right\}$$![[Pasted image 20231018133111.png|200]]
>2. $c:[0,\infty)\ni t\mapsto(t\cos t,t\sin t)$
>   ![[Pasted image 20231018133125.png|200]]
>3. $c:\mathbb{R}\ni t\mapsto(t^{3},t^{2})\in\mathbb{R}^{2}$ mit $$c(\mathbb{R})=\left\{(x,y)\in\mathbb{R}^{2}\vert y=\sqrt[3]{x^{2}}\right\}$$![[Pasted image 20231018133144.png|200]]

>[!def] Definition 1.3: Rektifizierbarkeit und Länge
>Sei $c:[a,b]\rightarrow\mathbb{R}^{n}$ Kurve.
>1. Für jede [[Das Jordan-Volumen|Zerlegung]] $z=\{t_{0},...,t_{k}\}$ von $[a,b]$ setzen wir $$L_{z}(c):=\sum\limits_{i=1}^{k}\left\lVert c(t_{i})-c(t_{i-1})\right\rVert$$
>2. $c$ heißt **rektifizierbar**, wenn die Menge $$\{L_{z}(c)\vert z\text{ Zerlegung von }[a,b]\}$$nach oben beschränkt ist.
>3. Falls $c$ rektifizierbar ist, dann heißt $$L(c):=\sup\{L_{z}(c)\vert z\text{ Zerlegung von }[a,b]\}$$die **Länge** von $c$.

>[!exp] Beispiel 1.4: Eine nicht rektifizierbare Kurve
>Sei $c:[-1,0]\rightarrow\mathbb{R}^{2}$ definiert durch $$c(t):=\begin{cases}
&(t,t\cos(\frac{\pi}{t})) & \text{für }t\in[-1,0) \\
&(0,0) & \text{für }t=0
\end{cases}$$
>$c$ ist stetig: Klar in jedem $t\in[-1,0)$, auch in $t=0$, denn: $$\left\lVert c(t)-c(0)\right\rVert=\left\lVert c(t)\right\rVert=\sqrt{t^{2}+t^{2}\cos^{2}\left(\frac{\pi}{t}\right)}=|t|\sqrt{1+\cos^{2}\left(\frac{\pi}{t}\right)}\le|t|\sqrt{2}\xrightarrow[t\rightarrow0]{}0$$
>$c$ ist nicht rektifizierbar: Für jedes $n\in\mathbb{N}$ betrachte die Zerlegung $$z_{n}:=\left\{-1,-\frac{1}{2},-\frac{1}{3},...,-\frac{1}{n},0\right\}$$von $[1,0]$. Dann gilt: $$\begin{align*}
&L_{z_{n}}(c)=\left\lVert c\left(-\frac{1}{2}\right)-c(-1)\right\rVert+...+\left\lVert c\left(-\frac{1}{n}\right)-c\left(-\frac{1}{n-1}\right)\right\rVert+\left\lVert c(0)-c\left(-\frac{1}{n}\right)\right\rVert\\[12pt]
&\stackrel{(\star)}{\ge}\frac{2}{2}+\frac{2}{3}+...+\frac{2}{n}=2\left(\frac{1}{2}+\frac{1}{3}+...+\frac{1}{n}\right)\xrightarrow[\,n_{\infty}\,]{}\infty
\end{align*}$$
>Dementsprechend findet sich keine obere Schranke für $\{L_{z}(c)\vert z\text{ Zerlegung von }[-1,0]\}$.
>Bew. $\star$ : Es gilt $\left\lVert c\left(-\frac{1}{k}\right)-c\left(-\frac{1}{k-1}\right)\right\rVert\ge\frac{2}{k}\forall k\in\{2,...,n\}$, denn: $$\begin{align*}
&\left\lVert c\left(-\frac{1}{k}\right)-c\left(-\frac{1}{k-1}\right)\right\rVert\stackrel{y-\text{K.}}{\ge}\left|-\frac{1}{k}\cos\left(\frac{\pi}{-1/k}\right)+\frac{1}{k-1}\cos\left(\frac{\pi}{-1/(k-1)}\right)\right|\\[12pt]
&=\left\vert-\frac{1}{k}\cos(\pi k)+\frac{1}{k-1}\underbrace{\cos(\pi(k-1))}_{-\cos(\pi k)}\right\vert=\left\vert-\frac{1}{k}-\frac{1}{k-1}\right\vert\cdot|\cos(\pi k)|=\frac{1}{k}+\frac{1}{k-1}\ge\frac{2}{k}&&\square
\end{align*}$$

>[!thm] Lemma 1.5
>Sei $c:[a,b]\rightarrow\mathbb{R}^{n}$ rektifizierbar. Dann gilt:
>1. $L(c)\ge|c(b)-c(a)|$
>2. Für alle $a\le t\le\tilde t\le b$ ist auch $c\vert_{[t,\tilde t]}$ rektifizierbar.
>3. Für alle $a\lt t\lt b$ gilt: $L(c)=L(c\vert_{[a,t]})+L(c\vert_{[t,b]})$

>[!bew]- Beweis 1.5
>1. Klar nach Def., denn auch $\{a,b\}$ ist Zerlegung von $[a,b]$
>2. Wäre die Menge der Polygonzuglängen $L_{\tilde z}(c\vert_{[t,\tilde t]})$ für Zerlegungen $\tilde z$ von $[t,\tilde t]$ unbeschränkt, dann auch für Zerlegungen $z$ von $[a,b]$. (denn für $z=\{a\}\cup\tilde z\cup\{b\}$ gilt $L_{z}(c)\ge L_{\tilde z}(c\vert_{[t,\tilde t]})$)
>3. "$\ge$": Linke Seite $=\sup_{z}L_{z}(c)$, rechte Seite $=\sup_{z\text{ mit }t\in z}L_{z}(c)$
>   "$\le$": $z$ beliebige Zerlegung von $[a,b]\Rightarrow z':=z\cup\{t\}$ erfüllt $L_{z}(c)\le L_{z'}(c)$. ($\Delta$-Ugl.) $\square$

>[!thm] Theorem 1.6 (Bew. unten)
>Sei $c\in\mathcal{C}^{1}([a,b],\mathbb{R}^{n})$ (d.h. $c$ stetig diff'bar). Dann ist $c$ rektifizierbar, und es gilt: $$L(c)=\int_{a}^{b}\left\lVert\dot c(t)\right\rVert\dd t$$

>[!thm] Lemma 1.7: "Kontinuierliche Dreiecksungleichung"
>Sei $X:[a,b]\rightarrow\mathbb{R}^{n}$ stetig. Dann gilt: $$\left\lVert\int_{a}^{b}X(t)\dd t\right\rVert\le\int_{a}^{b}\left\lVert X(t)\right\rVert\dd t$$

>[!bew]- Beweis 1.7
>Setze $V:=\int_{a}^{b}X(t)\dd t\in\mathbb{R}^{n}$. Behauptung klar für $V=0$. Sei also $V\ne0$. Es gilt $$\begin{align*}
&\left\lVert V\right\rVert^{2}=\left\langle\int_{a}^{b}X(t)\dd t,V\right\rangle=\int_{a}^{b}\left\langle X(t),V\right\rangle\dd t\stackrel{\text{CSU}}{\le}\int_{a}^{b}\left\lVert X(t)\right\rVert\cdot\left\lVert V\right\rVert\dd t\\[12pt]
&\Leftrightarrow\left\lVert V\right\rVert\le\int_{a}^{b}\left\lVert X(t)\right\rVert\dd t&&\square
\end{align*}$$

>[!bew]- Beweis 1.6
>Für jede Zerlegung $z=\{t_{0},t_{1},...,t_{k}\}$ von $[a,b]$ gilt: $$L_{z}(c)=\sum\limits_{i=1}^{k}\left\lVert c(t_{i})-c(t_{i-1})\right\rVert=\sum\limits_{i=1}^{k}\left\lVert\int_{t_{i-1}}^{t_{i}}\dot c(t)\dd t\right\rVert\stackrel{1.7}{\le}\sum\limits_{i=1}^{k}\int_{t_{i-1}}^{t_{i}}\left\lVert\dot c(t)\right\rVert\dd t=\int_{a}^{b}\left\lVert\dot c(t)\right\rVert\dd t$$
>Also $c$ rektifizierbar, und $L(c)\le\int_{a}^{b}\left\lVert\dot c(t)\right\rVert\dd t$. Zz. bleibt Gleichheit.
>Für jedes $t\in[a,b]$ setze $l(t):=L(c\vert_{[a,t]})$. Wir werden zeigen: $l$ ist Stammfunktion von $t\mapsto\left\lVert\dot c(t)\right\rVert$. Dann folgt die Beh. wegen $L(c)=l(b)$ und $l(a)=0$. 
>Für alle $t\gt t_{0}$ in $[a,b]$ gilt: $$\begin{align*}
&\left\lVert c(t)-c(t_{0})\right\rVert\le L(c\vert_{[t_{0},t]})\le\int_{t_{0}}^{t}\left\lVert\dot c(\tau)\right\rVert\dd\tau\\[12pt]
\Rightarrow\,&\underbrace{\left\lVert\frac{c(t)-c(t_{0})}{t-t_{0}}\right\rVert}_{\xrightarrow[\,t\rightarrow t_{0}\,]{}\left\lVert\dot c(t_{0})\right\rVert}\le\frac{l(t)-l(t_{0})}{t-t_{0}}\le\underbrace{\frac{\int_{t_{0}}^{t}\left\lVert\dot c(\tau)\right\rVert\dd\tau}{t-t_{0}}}_{\xrightarrow[\,t\rightarrow t_{0}\,]{}\left\lVert\dot c(t_{0})\right\rVert\text{ (MWS)}}
\end{align*}$$
>Also muss auch $\frac{l(t)-l(t_{0})}{t-t_{0}}\xrightarrow[\,t\rightarrow t_{0}\,]{}\left\lVert\dot c(t_{0})\right\rVert\left\lVert\dot c(t_{0})\right\rVert$.
>Gilt ebenso für $t\lt t_{0}$ (Vertausche $t$ und $t_{0}$...). Also $\dot l(t)=\left\lVert\dot c(t)\right\rVert$. $\square$

>[!def] Definition 1.8
>Sei $c:I\rightarrow\mathbb{R}^{n}$ eine Kurve.
>1. $c$ heißt **regulär**, wenn $\dot c(t)\ne0\forall t\in I$.
>2. $c$ heißt **nach Bogenlänge parametrisiert**, wenn $\left\lVert\dot c(t)\right\rVert=1\forall t\in I$
>3. Eine **Umparametrisierung** von $c$ ist eine Kurve $$\tilde c=c\circ u:J\rightarrow\mathbb{R}^{n}$$wenn $u\in\mathcal{C}^{1}(J,I)$ bijektiv ist und $u'(s)\ne0\forall s\in J$ gilt.

>[!bem] Bemerkung 1.9
>In Def. 1.8.3 gilt, weil $u'$ stetig ist:
>- Entweder $u'(s)\gt0\forall s\in J$ $\rightsquigarrow$ **orientierungserhaltende Umparametrisierung**
>- Oder $u'(s)\lt0\forall s\in J$ $\rightsquigarrow$ **orientierungsunerhaltende Umparametrisierung**

>[!thm] Lemma 1.10
>Wenn $\tilde c:[\alpha,\beta]\rightarrow\mathbb{R}^{n}$ eine Umparametrisierung von $c:[a,b]\rightarrow\mathbb{R}^{n}$ ist, dann gilt: $$L(\tilde c)=L(c)$$

>[!bew]- Beweis 1.10
>Für $\tilde c=c\circ u$ wie in 1.8 gilt: $$\left\lVert\dot{\tilde c}(s)\right\rVert=\left\lVert\dot c(u(s))\cdot u'(s)\right\rVert=\left\lVert\dot c(u(s))\right\rVert\cdot|u'(s)|$$
>Daher nach 1.6:
>- Falls $u'\gt0$: $$L(\tilde c)=\int_{\alpha}^{\beta}\left\lVert\dot c(u(s))\right\rVert\cdot u'(s)\dd s\xlongequal[\dd t=u'(s)\dd s]{t=u(s)}\int_{a}^{b}\left\lVert\dot c(t)\right\rVert\dd t=L(c)$$
>- Falls $u'\lt0$: $$L(\tilde c)=\int_{\alpha}^{\beta}\left\lVert\dot c(u(s))\right\rVert\cdot (-u'(s))\dd s\xlongequal[\dd t=u'(s)\dd s]{t=u(s)}-\int_{b}^{a}\left\lVert\dot c(t)\right\rVert\dd t=L(c)\qquad\square$$

>[!thm] Lemma 1.11: Umparametrisierung nach Bogenlänge
>Wenn $c:[a,b]\rightarrow\mathbb{R}^{n}$ regulär ist, dann existiert eine orientierungserhaltende Umparametrisierung $\tilde c:[0,L(c)]\rightarrow\mathbb{R}^{n}$ von $c$ mit $\left\lVert\dot{\tilde c}(s)\right\rVert=1\forall s\in[0,L(c)]$

>[!bew]- Beweis 1.11
>Setze $l:[a,b]\ni t\mapsto\int_{a}^{t}\left\lVert\dot c(\tau)\right\rVert\dd\tau\in\mathbb{R}$. Dann ist $l$ stetig diff'bar, und $l'(t)=\left\lVert\dot c(t)\right\rVert\gt0\forall t$. Also ist $l$ bijektiv auf sein Bild $[0,L(c)]$, und es existiert eine $\mathcal{C}^{1}$-Umkehrfunktion $u:[0,L(c)]\rightarrow[a,b]$ zu $l$.
>Nun gilt für $\tilde c=c\circ u$: $$\dot{\tilde c}(s)=\dot c(u(s))\cdot u'(s)=\dot c(u(s))\cdot\frac{1}{l'(u(s))}=\frac{\dot c(u(s))}{\left\lVert\dot c(u(s))\right\rVert}$$was offensichtlich Norm $1$ hat. Außerdem $u'(s)=\frac{1}{l'(u(s))}\gt0\forall s$, d.h. die Umparametrisierung ist orientierungserhaltend. $\square$
## Backlinks
```dataview
TABLE summary AS Zusammenfassung, time AS "Time of Creation"
FROM #mitschrift
WHERE contains(summary, this.file.name)
```