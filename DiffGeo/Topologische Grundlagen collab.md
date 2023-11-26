---
time: 26.11.2023 23:26
tags:
  - concept
  - status/todo
module: M18
aliases:
---
modul: [[M13 Differentialgeometrie]]
# Topologische Grundlagen

>[!def] Def. 6.1: [[Topological spaces|Topologische Räume]]
>Sei $X$ eine Menge.
>1. Eine Teilmenge $\mathcal{O}$ der Potenzmenge $\mathcal{P}(X)$ heißt **Topologie auf $X¥$** falls
>    - $\emptyset,X\in\mathcal{O}$
>    - $U,V\in\mathcal{O}\Rightarrow U\cap V\in\mathcal{O}$
>    - $U_{i}\in\mathcal{O}$ für alle $i\in I$ (Indexmenge) $\Rightarrow\bigcup\limits_{i\in I}U_i\in\mathcal{O}$.
>2. Das Tupel $(X,\mathcal{O})$ heißt dann **topologischer Raum**.
>3. Eine Menge $M\subseteq X$ heißt **offen**, falls $M\in\mathcal{O}$ und **abgeschlossen**, falls $M^{c}:=X\setminus M\in\mathcal{O}$

>[!bem] Bemerkung 6.2
>Sei $(X,\mathcal{O})$ top. Raum.
>1. Wenn $A_{1},...,A_{k}\subset X$ abg. sind, ist auch $\bigcup_{i=1}^{k}A_{i}$ abg.
>2. Wenn $A_{1},...,A_{k}\subset X$ abg. sind, ist auch $\bigcap_{i=1}^{k}A_{i}$ abg.

>[!exp] Beispiele 6.3
>1. Die **diskrete Topologie** $\mathcal{T}=\mathcal{P}(X)$
>2. $\mathcal\{\emptyset,X\}$, die triviale Topologie auf $X$.
>3. Sei $X=\mathbb{R}^{n}$. The **Standardtopologie auf $\mathbb{R}^{n}$** ist definiert als $$\textcolor{Aquamarine}{U\in\mathcal{T}\Leftrightarrow\forall x\in U:\exists\varepsilon\gt0:B_{\varepsilon}(x)\subseteq U}$$

>[!def] Def. 6.4: Umgebungen
>Sei $(X,\mathcal{O})$ top. Raum. Sei $x\in X$. Eine Teilmenge $U\subset X$ heißt eine Umgebung von $x$, wenn gilt: $$\exists\Omega\in\mathcal{O}:x\in\Omega\subset U$$

>[!bem] Bemerkung 6.5
>1. Wenn $U$ Umgebung von $x$ und $V\supset U$, dann ist auch $V$ eine Umgebung von $x$.
>2. Wenn $U_{1},...,U_{k}$ Umgebungen von $x$ sind, dann ist auch $\bigcap_{i=1}^{k}U_{i}$ eine Umgebung von $X$
>3. $$\Omega\subset X\text{ offen}\Leftrightarrow\Omega\text{ Umg. }\forall x\in\Omega\Leftrightarrow\forall x\in\Omega:\exists\text{ Umg. }U:U\subset\Omega$$

>[!def] Def. 6.6: Induzierte Topologie
>Sei $(X,\mathcal{O})$ top. Raum. Sei $M\subset X$. Dann heißt $$\mathcal{O}_{M}:=\{\Omega\cap M\vert\Omega\in\mathcal{O}\}\subset\mathcal{P}(M)$$
>die von $\mathcal{O}$ **induzierte Topologie** auf $M$. $(M,\mathcal{O}_{M})$ ist wieder top. Raum.

>[!def] Def. 6.7: [[Metrische Räume|Stetigkeit]]
>$X,Y$ top. Räume, $f:X\rightarrow Y$ eine Abbildung, $x\in X$.
>- $f$ **stetig in $x$** $$:\Leftrightarrow\forall\text{ Umg. }V\text{ von }f(x):\exists\text{ Umg. }U\text{ von }x:f(U)\subset V$$
>- $f$ **stetig** $$:\Leftrightarrow\forall x\in X:f\text{ stetig in }x$$

>[!bem] Bemerkung 6.8
>$X,Y$ top. Räume, $f:X\rightarrow Y$ eine Abbildung.
>1. $f$ stetig $\Leftrightarrow$ Urbilder offener Mengen sind offen. 
>2. Stetigkeit ist lokal (bzgl. der induzierten Topologie): $X'\subset X$, $Y'\subset Y$ mit $f(X')\subset Y'$, $x\in X'$ und $f$ stetig in $x$, dann auch $f\vert_{X'}:X'\rightarrow Y'$ stetig in $x$.
>3. Wenn $Z$ noch ein top. Raum, $g:Y\rightarrow Z$, $f$ stetig in $x$, $g$ stetig in $f(x)$, dann auch $g\circ f:X\rightarrow Z$ stetig in $x$.

>[!def] Def. 6.9
>Sei $X$ ein top. Raum, $x\in X$.
>1. Eine Folge $(x_{k})_{k}\in X^{\mathbb{N}}$ in $X$ **konvergiert** gegen $x$, geschrieben $x_{k}\xrightarrow[\,k_{\infty}\,]{}x$ $$:\Leftrightarrow\forall\text{ Umg. }U\text{ von }x:\exists k_{0}\in\mathbb{N}:\forall k\ge k_{0}:x_{k}\in U$$In diesem Fall heißt $x$ **Grenzwert** von $(x_{k})_{k}$.
>2. Eine Folge $(x_{k})_{k}$ in $X$ heißt **konvergent** $:\Leftrightarrow\exists x\in X:x_{k}\xrightarrow[\,k_{\infty}\,]{}x$.

>[!def] Def. 6.10: [[Convergence of sequences & Hausdorff property|Hausdorff-Räume]]
>Ein top. Raum $(X,\mathcal{O})$ heißt ein **Hausdorff-Raum** oder **Hausdorff** $$:\Leftrightarrow\forall x_{1},x_{2}\in X\text{ mit }x_{1}\ne x_{2}:\exists\text{ Umg. }U_{1},U_{2}\text{ von }x_{1},x_{2}\text{ mit }U_{1}\cap U_{2}=\emptyset$$

>[!bem] Bemerkung 6.11
>Wenn $(X,\mathcal{O})$ ein Hausdorff-Raum ist, dann hat jede konvergente Folge in $X$ genau einen Grenzwert.

>[!def] Def. 6.12
>Sei $(X,\mathcal{O})$ top. Raum.
>1. Eine Menge $\mathcal{B}\subset\mathcal{O}$ heißt eine **[[Basis]]** für die Topologie von $(X,\mathcal{O})$ $$:\Leftrightarrow\forall\Omega\in\mathcal{O}:\Omega=\bigcup_{U\in\mathcal{B},U\subset\Omega}U$$
>2. $(X,\mathcal{O})$ **hat abzählbare Topologie**, wenn eine abzählbare Basis für die Topologie von $(X,\mathcal{O})$ existiert.

>[!exp] Beispiel 6.13
>$\mathbb{R}^{n}$ mit der Standard-Topologie hat abzählbare Topologie: Eine abzählbare Basis ist z.B. $$\{B_{\varepsilon}(x)\vert\varepsilon\gt0,\varepsilon\in\mathbb{Q},x\in\mathbb{Q}^{n}\}$$
