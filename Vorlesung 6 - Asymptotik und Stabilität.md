---
tags:
  - Stabilität
---

---
Wir stellen uns die Frage, ob ein System (eine Differentialgleichung) unter kleiner Änderung des Anfangswertes
$$y(x_{0}):= y_{0}$$
eine stark abweichende Lösung erhält. Zum Beispiel hat ein Pendel eine instabile Lösung, wenn es im Hochpunkt steht (es erreicht bei kleiner Änderung von $y_{0}$ starke Änderung der Lösung - gemessen in der $d_{sup}$-Norm).
hallo

---
>[!info]- Grundsituation
>$$y:[x_{0};\infty)\to \mathbb{R}^{n}\quad\text{Lsg. von}\quad y'=f(x,y)\qquad y_{0}:=y(x_{0})$$
>$D\subset \mathbb{R}^{n}\times\mathbb{R}^{n} \text{ offen}, \quad f:D\to \mathbb{R}^{n}\in C^{1}$

Die Lösung y "heißt":

>[!check]- Def: "stabil"
>Wir gucken, ob in einem kleinen Bereich ($z_{0}$ nah an $y_{0}$) die Lösung plötzlich extrem anders wird.
>$$\forall \epsilon>0\quad\exists\delta>0:\quad\forall z_{0}\in \mathbb{R}^{n}:$$
>$$||y_{0}-z_{0}||<\delta\quad\Rightarrow\quad||y_{x_{0}y_{0}}(x)-y_{x_{0}z_{0}}||<\epsilon\quad\forall x\geq x_{0}$$
>A.k.a. die Stetigkeit des _Lösungsoperators_ bzgl. $d_{sup}$

>[!check]- Def: "attraktiv"

>[!check]- Def: "asymptotisch stabil"

>[!check]- Def: "exponentiell stabil"

---

![alt text](Bilder/poincare_diagram.png)
>Stabilitätsdiagramm von #LAS (y'=Ay)
>[Youtube-Video "Sketching phase portraits"](https://youtu.be/dpbRUQ-5YWc?si=RUVXktmzVDl8H8ZY)

---
$D\subset \mathbb{R}^{n+1}$ offen, $f:D\to \mathbb{R}^{n} \in C^{1},x_{0}\in \mathbb{R}$
$y:[x_{0};\infty)\to \mathbb{R}^{n}$ Lsg. von $y'=f(x,y) \quad y_{0}:=y(x_{0})$
$y$ heißt
- (f-) stabil (auf $[x_{0};\infty)$)
$$\forall\epsilon>0\quad\exists\delta>0:\quad||y_{0}-z_{0}||<\delta\Rightarrow||y_{x_{0}y_{0}}(t)-y_{x_{0}z_{0}}(t)||_\text{sup}<\epsilon$$
- (f-) attraktiv (auf $[x_{0};\infty)$)
$$\exists\delta>0:\quad||y_{0}-z_{0}||\Rightarrow y_{x_{0}z_{0}}\text{ ex auf }I$$
- (f-) asymptotisch stabil $\Leftrightarrow$ stabil und attraktiv

