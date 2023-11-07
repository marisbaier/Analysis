---
tags:
  - Stabilität
---
---
$$y'=Ay \qquad y(0)=y_0$$
>[!info] Satz 2.8: Stabilität autonomer linearer Systeme
>1. System stabil an jeder Lsg $\quad\Longleftrightarrow\quad Re(\lambda_{i})\leq0\quad\land\quad (Re(\lambda)=0)\Rightarrow (\underbrace{GV(\lambda)=AV(\lambda)}_{\text{"halbeinfach"}})$
>2. asymptotisch stabil $\quad\Longleftrightarrow\quad$ exp stabil $\quad\Longleftrightarrow\quad$ Re($\lambda_{i}$)<0

>[!check] Bestimmung der exp. Abfallsrate
>mit $s:=\text{max}\{Re(\lambda_{i})\}<0$ gilt:
>$$||e^{Ax}y_{0}||\leq M_{\omega}\,\, ||y_{0}||e^{{-\omega x}}\quad\forall\omega\in(s;0)$$
>Falls $\forall \lambda:Re(\lambda)=?\quad\Rightarrow\quad\lambda\text{ halbeinfach}$
>$$\Rightarrow \text{ dann}\quad\exists M:||e^{{Ax}}y_{0}||\leq M||y_{0}||e^{{-sx}}$$

![[Fixed_Points.gif]]
>Schematic visualization of 4 of the most common kinds of fixed points