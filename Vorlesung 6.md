---
tags:
  - Stabilität
---
---
### Asymptotik und Stabilität
---
Wir stellen uns die Frage, ob ein System (eine Differentialgleichung) 
$$y'=Ay$$
unter kleiner Änderung des Anfangswertes
$$y(x_{0})\,\,!= y_{0}$$
eine stark abweichende Lösung erhält. Zum Beispiel hat ein Pendel eine instabile Lösung, wenn es im Hochpunkt steht.

---
>[!info] Grundsituation
>$$y\text{Lsg. von }y'=f(x,y)\qquad y_{0}:=y(x_{0})$$
>$D\subset \mathbb{R}^{n}\times\mathbb{R}^{n} \text{ offen}, \quad f:D\to \mathbb{R}^{n}\in C^{1}$


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

