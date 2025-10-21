---
tags:
  - WS2025/26
  - Mechanik
  - TheoMech
---
# Theoretische Physik
# Kapitel 0: Einführung

| physikalische Realität<br>Beobachtungen, Experimente         | $\rightarrow$            | Abstraktion<br>- Idealisierung<br>- math. Beschreibungen |
| ------------------------------------------------------------ | ------------------------ | -------------------------------------------------------- |
| Falsifizierung? $\uparrow\quad\leftarrow$<br>Übereinstimmung | Berechnung<br>Vorhersage | $\hookleftarrow$                                         |
## Kugelkoordinaten
$$\hat\varphi \sim \lim_{\Delta\varphi\to0} \frac1{\Delta\varphi}\cdot\Delta\vec r = \frac{\partial \vec r}{\partial\varphi} $$
$$\hat\vartheta \sim \lim_{\Delta\vartheta\to0} \frac1{\Delta\vartheta}\cdot\Delta\vec r = \frac{\partial \vec r}{\partial\vartheta} $$
---
## Rutherford-Streuung
Hat ein Atom einen Kern?
1) "$+$"  schwammig verteilt
   ![[Pasted image 20251014192852.png]]
2) "$+$" in kleinen Kern konzentriert
   ![[SmartSelect_20251014_191742_Samsung Notes.jpg]]
---
## Variationsrechnung Kettenlinie
![[SmartSelect_20251014_191605_Samsung Notes.jpg]]
1) elementare Betrachtung: *Seil und Gewichtskräfte*
2) Extremalprinzip: Suche $y(x)$ mit geringster potentieller Energie
$$E[y(x)] = \int_{x_1}^{x_2} y\sqrt{1+ y'^2}\qquad E: \text{Funktion} \to \mathbb R $$
Annahme: Minimum bei Funktion $y_0(x)$ 
Betrachte Funktionen "in der Nähe" von $y_0(x)$
$$y(x) = y_0 +\varepsilon \cdot y_1(x)\qquad y_1\text{ ist variabel} $$
$$E[y] = E[y_0] +\varepsilon\int_{x_1}^{x_2}\left(y_1\sqrt{1+y_0'^2} + \frac{y_1'y_0'y_0}{\sqrt{1+y_0'^2}} \right) +O(\varepsilon^2)$$
$$= E[y_0] + \int_{x_1}^{x_2} \left(y_1\sqrt{1+y_0'^2} - \left(\frac{y_0'y_0}{\sqrt{1+y_0'^2}} \right)'\right) +O(\varepsilon^2) $$
$\Rightarrow y''y-y'^2-1 = 0\quad\text{DGL}$ 
---
## Hammilton-Mechanik

![[Notes_251014_191506_18b.jpg]]
# Kapitel 1: Newtonsche Mechanik der Punktmassen
### Grundannahmen über Raum & Zeit
- Raum und Zeit seien **absolut** und unabhängig voneinander beschreibbar (nicht den phys. Gesetzen unterworfen)
- Raum sei euklidisch, 3D, isotrop *(invariant bezgl. Drehungen)*, homogen *(invariant bzgl. Verschiebungen)*
- von der Mechanik zu beschreibende Ereignisse: Ort ($\to$ "Punkt") und Zeit ($\to$ "Zeitpunkt") wohldefiniert
**Beachte:** relativistische Physik und Quantenphysik weichen davon ab!
## 1.1 Vektorrechnung in 3D
### Wh.:
- Vektorraumaxiome
- Betrag und Richtung
### Physik:
Vektoren mit Bezugsobjekt *("Kraft auf $xy$")* oder -punkt *(Vektorfeld: ortsabhängige Größe mit Vektoreigenschaften)*
### Produkte von Vektoren
1) Skalarprodukt $\quad(\vec a, \vec b)\;\leftarrow$ definierende Eigenschaften 
   3D:$$\vec a\cdot\vec b = \|\vec a\| \cdot\|\vec b\|\cos(\angle(\vec a, \vec b)) $$
   Es gilt:$$\begin{align}
   \vec a\cdot\vec b &= \vec b\cdot\vec a&\text{symm.}\\
   (\vec a+\vec b)\cdot\vec c &= \vec a\cdot\vec c +\vec b\cdot\vec c&\text{distr.}\\
   (\lambda\vec a)\cdot\vec b &= \lambda\cdot(\vec a\cdot\vec b) \\
   \|\vec a\| &= \sqrt{\vec a\cdot\vec a}\\
   \vec a\cdot\vec b &= 0 \Leftrightarrow \vec a\perp\vec b&\text{Orthogonalität} \\
   \|\vec a\cdot\vec b\|&\leq|\vec a\|\cdot\|\vec b\|&\text{CSU} \\
   \|\|\vec a\|-\|\vec b\|\|&\leq\|\vec a+\vec b\|\leq\|\vec a\|+\|\vec b\| &\text{Dreiecksug.}
   \end{align} $$
   Einheitsvektoren $\vec n$ zur Charakterisierung einer Richtung$$\|\vec n\| = 1 $$Projektion von $\vec a$ in Richtung $\vec n$:
   [[Graphic]]
   in Richtung $\vec b$:
   [[Graphic]]
   
2) Vektorprodukt (Kreuzprodukt)$$\vec a \times\vec b = \vec c$$
   - $\vec a\perp\vec c$ und $\vec b\perp\vec c$
   - $\|\vec c\| = \|\vec a\|\|\vec b\|\cdot\sin(\angle(\vec a, \vec b))$
   - $\vec a \to\vec b\to\vec c$ rechtshändig
   Es gilt:$$\begin{align}
   \vec a\times\vec b &= -\vec b\times\vec a &\text{auch $\vec a\times\vec a=0$ antikommutativ}\\
   (\vec a+\vec b)\times \vec c &= \vec a \times \vec c +\vec b\times \vec c &\text{distributiv}\\
   (\vec a\times\vec b)\times\vec c &\neq\vec a\times(\vec b\times\vec c) &\text{i.a. nicht assoziativ}
   \end{align} $$
   abweichende Notationen: $[\vec a, \vec b]$, $[\vec a\, \vec b]$, $\vec a\wedge\vec b$
   
3) Produktraum, dyadisches Produkt *(dyad.)*: $\vec a\otimes\vec b$
   Koordinaten bezüglich einer Basis: $a_s\,b_k$ $\stackrel{\wedge}{=}$ Matrix, Rang 1
   Matrix $\Leftrightarrow$ lineare Abbildung
   dyad. Produkt: Abbildung$$\vec x \to (\vec b\cdot\vec x)\,\vec a $$$(\vec a\otimes\vec b)\,\vec x = (\vec b\cdot\vec x)\,\vec a$ 
   weitere Interpretation: quadratische Abbildung Vektor $\to$ Skalar
   Beispiel: Trägheitstensor von Punktmassen wird aus dynamischen Produkten aufgebaut$$\begin{align}
   \vec \omega \underline{\underline{I}}\vec \omega = \vec \omega\cdot\underline{\underline{I}}\vec \omega \to&\text{Frage: Was, wenn die Basis, auf die sich Koord. und Matrixlemente beziehen,}\\
   &\hspace{1.55cm}\text{keine ON-Basis bezüglich "$\cdot$" ist?}\\
   \to&\text{relevante Frage für gekrümmte Räume und manche krummliegenden KOS}
   \end{align}$$
   Es gilt:$$\begin{align}
   \vec a\otimes\vec b&\neq\vec b\otimes\vec a\\
   (\vec a + \vec b)\otimes\vec c &= \vec a\otimes\vec c+\vec b\otimes\vec c \\
   \vec a \otimes (\vec b + \vec c) &= \vec a\otimes\vec b +\vec a\otimes\vec c\\
   (\lambda\vec a)\otimes\vec b &= \vec a\otimes(\lambda\vec b) = \lambda\,\vec a\otimes\vec b
   \end{align} $$
   Für $\|\vec n\| = 1$: $\quad(\vec n\otimes\vec n)\,\vec a = (\vec n\cdot\vec a)\,\vec n$ Projektion, s.o. 
   Verkettung zweier linearer Abbildungen ($\stackrel{\wedge}{=}$ Matrix-Matrix-Multiplikation)$$(\vec a\otimes\vec b)\circ(\vec c\otimes\vec d) = (\vec b\cdot\vec c)\;\vec a\otimes\vec a $$
### Komponentendarstellung
Vektoren $\vec b_3, \vec b_2,  \vec b_3$ heißen linear unabhängig, wenn
$$\lambda_1\vec b_1 + \lambda_2\vec b_2 + \lambda_3\vec b_3 = 0 \Rightarrow \lambda_1 = \lambda_2 = \lambda_3 = 0$$
im 3D euklidischen Raum: "nicht coplanar", bilden Basis
- Vektor $\vec a$ darstellbar in Koordinaten:
  $$\vec a = a_1\vec b_1 + a_2\vec b_2 + a_3\vec b_3 \quad, a_1, a_2, a_3\text{ eindeutig}$$
an Skalarprodukt angepasste Basis: ON-Basis $\vec e_1, \vec e_2, \vec e_3$ mit:
$$\vec e_i \cdot\vec e_j = \delta_{ij} \Rightarrow \vec a\cdot\vec b = \sum_ia_ib_i. $$
Dann gilt $\vec a = \sum_{i = 1}^3 a_i\vec e_i$, bzw. $a_i = \vec e_i\cdot\vec a$. 

Levi-Civita-Symbol
$$\varepsilon_{ijk} = \cases{1 &\text{falls $ijk$ eine gerade Permutation von 123 ist}\\-1 &--------||------  ungerade------||---------------------\\ 0 &sonst } $$
für $i,j,k\in{1,2,3}$. Für rechtshändiges ON-System: $\vec e_i\times\vec e_j = \sum_{k=1}^3\varepsilon_{ijk}\vec e_k$.

Einsteinsche Summenkonvention: über doppelt auftauchende Indizes wird summiert:
$$\begin{align}
\vec a &= a_i\vec e_i\\
\vec a\cdot\vec b &= a_ib_i\\
\vec a\times\vec b &= \varepsilon_{ijk}\,a_i\,b_j\,\vec e_k
\end{align} $$

Spatprodukt $(\vec a\times\vec b)\cdot\vec c$
Eigenschaften: $(\vec a\times\vec b)\cdot\vec c =(\vec c\times\vec a)\cdot \vec b = (\vec b \times\vec c)\cdot\vec a$
$$=\varepsilon_{ijk}\,a_i\,b_j\,c_k\qquad\text{3 Summationen!}$$
Geometrische Interpretation:
![[Drawing 2025-10-21 10.18.38.excalidraw]]
$--\to = \vec a\times\vec b$
Das von $\vec a,\vec b,\vec c$ aufgespannte Parallelepiped hat das Volumen $V =\|(\vec a \times\vec b)\cdot \vec c\|$.

rechtshändige ON-Basis: $\;(\vec e_i\times\vec e_j)\cdot\vec e_k = \varepsilon_{ijk}$
Hilfsformeln für Produkt zweier $\varepsilon_{ijk}$:
1) $1$ Index gemeinsam: $\;\varepsilon_{ijk}\;\varepsilon_{lmk} = \delta_{ie}\delta_{jm} - \delta_{im}\delta_{jl}$
2) $2$ Indizes gemeinsam: $\;\varepsilon_{ijk}\;\varepsilon_{ljk} = 2\delta_{il}$
3) 3 Indizes gemeinsam: $\;\varepsilon_{ijk}\;\varepsilon_{ijk} = 6$

Folgerung für Vektoren
$$\begin{align}
\vec a\times(\vec b\times\vec c) &=\vec b\cdot (\vec a\cdot\vec c)- \vec c\cdot(\vec a\cdot\vec b) &\text{Großmann-Identität}\quad\text{(Grassmann eng.)} \\
(\vec a\times\vec b)\cdot(\vec c\times\vec d) &= (\vec a\cdot\vec c)(\vec b\cdot\vec d) - (\vec a\cdot\vec a)(\vec b\cdot\vec c) & \text{Lagrange-Identität}\\
\vec a\times(\vec b\times\vec c) + \vec b\times(\vec c\times\vec a) &+ \vec c\times(\vec a\times\vec b) = 0 &\text{Jacobi-Identität}
\end{align}$$

---
### Matrix
Komponentendarstellung einer linearen Abbildung $A:\mathbb R^n\to\mathbb R^n$, insbesondere $n = m = 3$

Linearität: $A(\lambda_1\vec x_1+\lambda_2\vec x_2) = \lambda_1 A \vec x_1 + \lambda _2 A\vec x_2$

Matrixelemente: $A_{ij} = \vec e_i\cdot A\vec e_j$ (für eine ON-Basis)
$$A\vec e_j = A_{ij}\cdot\vec e_i\qquad\text{allgemein} $$
Für Koordinaten: $A: \vec x\to\vec y$ entspricht $y_i = A_{ij} x_i$

Verhalten linearer Abbildungen: $C = B\cdot A$
$\qquad\downarrow$
Matrixmultiplikation $\qquad c_{ij} = b_{ik}\cdot a_{kj}$

Konstriktion von $A$ aus $A_{ij}$ und dyadischen Produkten:
$$\begin{align}
A &= A_{ik}\;\vec e_i\otimes\vec e_k &\text{(elemente verifizierbar)}\\
\text{Basisunabhängig} &\;\;| \;\;\text{bezogen auf eine bestimmte Basis}
\end{align}$$
Ziel: Verwende Vektoren, die in einer Problemstellung gegeben  sind, für dyadisches Produkt $\to$ koordinatenunabhängige Beschreibung

Verifiziere: $\quad A \vec e_j = A_{ij} \vec e_i$ für $A = A_{ik}\; \vec e_i\otimes\vec e_k$
$$\begin{align}
A_{ik}\;\vec e_i\otimes\vec e_k\;\vec e_j = A_{ik} (\vec e_k\cdot \vec e_j) \;\vec e_i = A_{ij} \;\delta_{kj}\;\vec e_i = A_{ij}\; \vec e_i \quad\boxed{}
\end{align} $$

---
### 1.1.3 Drehung von (Orts-) Vektoren
1) Drehung um beliebige Achse:
   [[Drawing]]
   $$\begin{align}
   \vec a &= \vec a_{\parallel} + \vec a_{\perp} &\text{parallel und orthogonal zur Drehachse}\\
   \vec a_{\parallel} &= (\vec n\cdot\vec a)\;\vec n &,\|\vec n\| = 1\\
   \vec a_{\perp} &= \vec a-\vec a_{\parallel} = \vec n \times(\vec a\times\vec n) &\text{Großmann, }(\vec n\cdot\vec n) = 1
   \end{align} $$
   In der Ebene orthogonal zu $\vec n$:
   [[Drawing]]
   nach Drehung:
   $$\begin{align}
   \vec a_{\perp}' &= \cos\alpha\cdot\vec a_{\perp} + \sin\alpha \cdot\vec n\times\vec a\\
   \vec a_{\parallel}' &= \vec a_{\parallel}\\
   \vec a' &= \vec a_{\parallel}' +  \vec a_{\perp}'
   \end{align}$$
   Darstellung der Drehung ohne Bezug auf eine Basis
2) Drehung um infinitesimale Winkel $d\alpha$:
   $d\alpha$ infinitesimal $\to$ linearisiere $\sin, \cos$
   $$\begin{align}
   \sin d\alpha &\to d\alpha\\
   \cos d\alpha &\to 1
   \end{align} $$
   Damit
   $$d\vec a = (\vec n\cdot\vec a)\; \vec n +\vec n\times(\vec a\times\vec n) + d\alpha\;\vec n\times\vec a - \vec a $$
   $d\vec a = d\vec \Omega\times\vec a$ mit $d\vec \Omega = d\alpha\vec n$
   $\frac{d\vec a}{dt} = \frac{d\vec\Omega}{dt}\times\vec a$
3) Drehmatrix
   Abbildung $R_{\vec n,\alpha} \;\vec a\to\vec a'$ ist linear $\to$ Matrixdarstellung
   Umformungen $\quad(\vec n\cdot\vec a)\,\vec n = (\vec n\otimes\vec n)\,\vec a$
   $$\begin{align}
   \vec n \times(\vec a\times\vec n) &= a-(\vec n\cdot\vec a)\;\vec n = (\mathbb 1 -\vec n\otimes\vec n)\;\vec a\\
   \vec n\times\vec a &= \vec n\times(\mathbb 1\;\vec a) = \vec n\times\vec e_l\;(\vec e_l\cdot\vec a)
   \end{align}$$
   $\mathbb 1 = \vec e_l \otimes\vec e_l$ : identische Abbildung im $\mathbb R^3$
   Dann gilt $R_{\vec n,\alpha} \;\vec a =\left[(1-\cos\alpha)\;\vec n\otimes\vec n + \cos\alpha \; \mathbb 1 +\sin\alpha\;(\vec n\times\vec e_l) \otimes\vec e_l \right]\vec a$.
   Drehmatrix: $R_{ij} = \vec e_i\cdot R_{\vec n,\alpha}\;\vec e_j = (1-\cos\alpha)\; n_i\,n_j +\cos\alpha\cdot\delta_{ij} - \sin\alpha\,\varepsilon_{ijk}\,n_k$ 
	   da $\;\vec e_i\cdot(\vec n\times\vec e_l)\otimes\vec e_l\cdot\vec e_j = \vec e_i\cdot (\vec n\times\vec e_j) = -\varepsilon_{ijk} \vec n\vec e_k$
   Bemerkung: Vereinfachung zur bekannten Drehmatrix, wenn $\vec n \in \{\vec e_1,\vec e_2,\vec e_3\}$.

Drehungen werden durch **orthogonale Matrizen** beschrieben.
Eigenschaft: $\quad R\vec a\cdot R\vec b = (\vec a\cdot\vec b) \quad [\Rightarrow \|R\vec a\| = \|\vec a\|]$
inverse Matrix = transponierte Matrix

außerdem: $\|R\| = 1$

Aktive und passive Transformationen
- *aktiv:* $\vec a\to\vec b$ Vektor wird gedreht, Basis wird beibehalten
  $$b_i = R_{ij} \,a_j\quad\text{(wie gehabt)} $$
- *passiv*: $\vec a$ ändert sich nicht, Basis wird gedreht. $\;\vec e_j' = R \,\vec e_j\to$ neue Koordinaten?
$$a_i' = \vec a\cdot\vec e_i = \vec a\cdot R\,\vec e_i \stackrel{\vec a = a_j\vec e_j} = \vec e_j\cdot R\,\vec e_i\;\vec a_j = R_{ij}\,a_j \leftarrow \text{transponierte/inverse Rotatiosmatrix} $$
