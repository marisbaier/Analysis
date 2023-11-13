---
tags:
  - Matrixexponential
---

---
>"Eine Exponentialabbildung ist eine Abbildung der *Lie-Algebra* einer Gruppe auf die Gruppe selbst"
>- Muellerol

Folgendes ist interessant, weil sich der "e-Ansatz" auf Matrix Systeme und später auf allgemeine lineare Operatoren verallgemeinern lässt!

>[!info]- Eigenschaften exp(...)
>1. $\exp(0)=\mathbb{I}$
>   $\exp(A)^{{-1}}=\exp(-A)$
>		$\qquad\quad$insbesondere: $\exp(M_{n\times n},\mathbb{K})\subset GL(n,\mathbb{K})$
>3. $\exp(A+b)=\exp(A)\cdot\exp(B)$
>		$\qquad\quad$wenn $[A,B]=0$, ansonsten [Formel](https://en.wikipedia.org/wiki/Baker%E2%80%93Campbell%E2%80%93Hausdorff_formula)
>4. $\text{det}(\exp(A))=\exp(\text{tr}A)$
>5. $\displaystyle\exp(A)=\lim_{n\to\infty}(\mathbb{I}+\frac{1}{n}A)^{n}$
>6. $\exp(CAC^{-1})=C\exp(A)C^{{-1}}$
>
>BTW ist die Exponentialabbildung glatt:
>$\text{exp: }M_{n\times n}(\mathbb{K})\circlearrowright\quad\in C^\infty$

---
>[!info] 
>$$y'=Ay\quad \Rightarrow\quad y(t)=Ce^{At}$$
