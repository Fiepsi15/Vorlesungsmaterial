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
#### Wh.:
- Vektorraumaxiome
- Betrag und Richtung
#### Physik:
Vektoren mit Bezugsobjekt *("Kraft auf $xy$")* oder -punkt *(Vektorfeld: ortsabhängige Größe mit Vektoreigenschaften)*
### 1.1.1 Produkte von Vektoren
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
### 1.1.2 Komponentendarstellung
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
1) $1$ Index gemeinsam: $\;\varepsilon_{ijk}\;\varepsilon_{lmk} = \delta_{il}\delta_{jm} - \delta_{im}\delta_{jl}$
2) $2$ Indizes gemeinsam: $\;\varepsilon_{ijk}\;\varepsilon_{ljk} = 2\delta_{il}$
3) 3 Indizes gemeinsam: $\;\varepsilon_{ijk}\;\varepsilon_{ijk} = 6$

Folgerung für Vektoren
$$\begin{align}
\vec a\times(\vec b\times\vec c) &=\vec b\cdot (\vec a\cdot\vec c)- \vec c\cdot(\vec a\cdot\vec b) &\text{Graßmann-Identität}\quad\text{(Grassmann eng.)} \\
(\vec a\times\vec b)\cdot(\vec c\times\vec d) &= (\vec a\cdot\vec c)(\vec b\cdot\vec d) - (\vec a\cdot\vec d)(\vec b\cdot\vec c) & \text{Lagrange-Identität}\\
\vec a\times(\vec b\times\vec c) + \vec b\times(\vec c\times\vec a) &+ \vec c\times(\vec a\times\vec b) = 0 &\text{Jacobi-Identität}
\end{align}$$

---
#### Matrix
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
### 1.1.4 Tensoren
Als Tensoren $k$-ter Stufe bezeichnet man ein Objekt mit k Indizes ($3^k$-komponentiges Zahlen-Tupel).
$$T_{i_1, i_2, ..., i_k}\quad i_l\in \{1, 2, 3, ...\} $$
Beispiel $k=2$: Trägheitstensor

Transformationen unter Drehungen: $T'_{i_1, i_2, ..., i_k} = R_{i_1j_1}\, R_{i_2, j_2}\, ... R_{i_k, i_k}\, T_{j_1, j_2, ..., j_k}$
für Fälle wie Trägheitsmomente (Tensor vermittelt eine Abbildung $k$-Tupel von Vektoren $\to$ Skalar)

Fall $k=2$: $\quad T'_{i_1, i_2} = R_{i_1, j_1}\,R_{i_2, j_2}\,T_{j_1, j_2} =  R_{i_1, j_1}\,T_{j_1, j_2}\,R_{i_2, j_2} \stackrel{\wedge}= R\,T\,R^T$

#### Nachtrag zum Kreuzprodukt:
Frage: Wie verhalten sich Vektoren bei Punktspiegelung im Raum?
Eigentlich: $\vec x\to -\vec x$ für alle Vektoren
Konvention in der Physik: Wenn eine Punktspiegelung angewendet wird, behalten die Rechte-Hand-Regeln bei.
Dann müssen wir manche Vektoren von der Spiegelung ausnehmen
$$\vec c = \vec a \times \vec b$$
- spiegele $\vec a, \vec b\quad\;\, \to$ polare Vektoren
- spiegele $\vec c$ *nicht* $\to$ axiale Vektoren, Pseudovektoren
## 1.2 Koordinatensysteme
### 1.2.1 Kartesische Koordinaten
$$\vec e_x, \vec e_y, \vec e_z\quad \to\quad\pmatrix{1\\ 0 \\0}, \pmatrix{0\\ 1 \\0}, \pmatrix{0\\ 0 \\1}, $$
- **dieselbe** Basis für jeden Bezugspunkt im Raum
- Koordinaten sind *Geraden* (zum Beispiel Linie mit $x,y$ konstant und $z$ variable)
### 1.2.2 Krummlinige Koordinaten
$$\begin{align}
&x(q_1, q_2, q_3) &\vec r = x(q_1, q_2, q_3)\;\vec e_x\\
&y(q_1, q_2, q_3) & + y(q_1, q_2, q_3)\;\vec e_y\\
&x(q_1, q_2, q_3) & + z(q_1, q_2, q_3)\;\vec e_z
\end{align}$$
- mehrfach/beliebig oft differenzierbare Funktionen

Gegeben: $\vec r (q_1, q_2, q_3)$, $q_1, q_2, q_3$ abhängig von zum Beispiel verwendeter Zeit. $\rightarrow$ einfache Darstellung / standardisierte Darstellung der äußeren Ableitung
$$\vec e_{q_i} = \frac1{\|\frac{\partial\vec r}{\partial q_{i}}\|}\frac{\partial \vec r}{\partial q_i}\qquad\text{''kovarianter (aus Differentialgeometrie) Einheitsvektor''} $$
$\vec r (q_1 + \Delta q_1, q_2, q_3) = \vec r (q_1 q_1, q_2, q_3) + \frac{\partial \vec r}{\partial q_1}\,\Delta q_1 + \mathcal O((\Delta q_1)^2)$
$\vec e_{q_i}$ ist tangential zur Koordinatenlinie mit variable $q_i$.

allgemein infinitesimale Koordinatenänderungen:
$$d\vec r = \frac{\partial \vec r}{\partial q_1} dq_1 + \frac{\partial \vec r}{\partial q_2} dq_2 + \frac{\partial \vec r}{\partial q_2} dq_2 \quad(*)$$
geometrische Anschauung:
- Linien: alle $q$: hängen von einem Parameter $t$ ab (in der Regel Zeit)
  infinitesimales Element der Länge $ds = \sqrt{d\vec r\cdot d\vec r}$, $(*)$ ist einzusetzen. *(vereinfacht sich für ON-Basis $\vec e_{q_i}$ )*
- infinitesimales Volumen
  ![[Drawing 2025-10-23 09.11.34.excalidraw]]
  Orange: $\frac{\partial \vec r}{\partial q_1} dq_1$
  Blau: $\frac{\partial \vec r}{\partial q_2} dq_2$
  Grün: $\frac{\partial \vec r}{\partial q_3} dq_3$
  $dV = \|(\frac{\partial\vec r}{\partial q_1}\times \frac{\partial \vec r}{\partial q_2})\cdot \frac{\partial \vec r}{\partial q_3}\|\; dq_1\,dq_2\,dq_3 = dx_1 dx_2 dx_3$ 
  Die drei Raumrichtungen sind Richtungen der Koordinatenlinien

### 1.2.3 Zylinderkoordinaten
```
Work in progress, come again later
```
### 1.2.4 Kugelkoordinaten
$$\vec r(r, \vartheta, \varphi) = r\sin\vartheta\cos\varphi\cdot \vec e_x + r\sin\vartheta\sin\varphi\cdot \vec e_y + r\cos\vartheta \cdot\vec e_z $$
$$\begin{align}
r = \sqrt{x^2+y^2+z^2}\quad r&\in \mathbb R_0^+\\
\vartheta & \in [0, \pi]\\
\varphi & \in (-\pi, \pi]
\end{align}$$
$$\begin{align}
\frac{\partial \vec r}{\partial r} &= \pmatrix{\sin \vartheta \cos\varphi\\ \sin\vartheta\sin\varphi\\ \quad\cos\vartheta}, \|\frac{\partial \vec r}{\partial r}\| = 1\\
\frac{\partial \vec r}{\partial \vartheta} &= r\pmatrix{\cos \vartheta \cos\varphi\\ \cos\vartheta\sin\varphi\\ \;-\sin\vartheta}, \|\frac{\partial \vec r}{\partial \vartheta}\| = r\\
\frac{\partial \vec r}{\partial \varphi} &= r \pmatrix{-\sin \vartheta \sin\varphi\\ \;\sin\vartheta\cos\varphi\\ \qquad0}, \|\frac{\partial \vec r}{\partial \varphi}\| = r\sin\vartheta\\
\end{align}$$
Beachte:
- $\vec e_r, \vec e_\vartheta, \vec e_\varphi$ bleiben eine rechtshändige ON-Basis
- Die Einheitsvektoren sind nur von $\vartheta, \varphi$ abhängig
- Ableitungen: $\frac\partial{\partial\vartheta}\vec e_r = \vec e_\vartheta$, $\frac\partial{\partial\varphi}\vec e_r = \sin\vartheta\vec e_\varphi$
- $d\vec r = \vec e_r(\vartheta, \varphi)\,dr+ \vec e_\vartheta(\vartheta,\varphi)\, r\, d\vartheta + \vec e_\varphi(\varphi) \sin\vartheta\, r\,d\varphi$
- $dV = r^2\sin\vartheta\;dr\,d\vartheta\, d\varphi$
## 1.3 Kinematische Größen der Punktteilchens
Kinematik: Beschreibung von Lage und Lageänderung eines Objekts
1) Ortsvektoren 
   $$\vec r = \vec r(t)$$
2) Geschwindigkeit
   $$\vec v = \frac d{dt} \vec r = \dot{\vec r}$$
3) Beschleunigung
   $$\vec a = \frac {d^2}{dt^2} \vec r = \ddot{\vec r}$$
4) Winkelgeschwindigkeit
   $$\vec \omega = \frac{\vec r\times\vec v}{r^2},\quad r = \|r\|$$
5) Flächengeschwindigkeit
   $$\dot A = \frac12|\vec r\times\vec v| $$
   $dA = \dot A\, dt$ ist die Fläche eines infinitesimalen Dreiecks
   $dA = \frac12|\vec r\times d\vec r|$ (halbes Parallelogramm)
## 1.4 Newtonsche Mechanik des Massenpunktes
### 1.4.1 Newtonsche Gesetzte

#### 1687 - "principia"
1) Trägheitsgesetz
2) $\dot{\vec p} = \vec F, \quad \vec p = m\vec v$
3) Reaktionsgesetz
   $$\vec F_{12} = -\vec F_{21} $$
   Kraft von "2" auf "´1".

### 1.4.2 Auszeichnung von Inertialsystemen.
Wechsel zwischen Inertialsystemen: *Galilei-Transformation*. Eine *G-T.* ist eine Koordinatentransformation zwischen Bezugssystemen, die sich durch gleichförmige Bewegung sowie eine feste Rotation und eine Raum-Zeit-Transformation unterscheiden.
![[Drawing 2025-10-28 10.46.03.excalidraw]]
$$\vec r = x_i\vec e_i = \vec s + \vec w t+ x'_j\vec e'_j,\quad \vec e_j' = R\vec e_j\quad\text{(passive Drehung)} $$
Beizung der Koordinaten
$$x_i = \vec s \cdot \vec e_i + \vec w\cdot e_i\cdot t + R_{ij} \,x_j',\quad t= t' + \tau $$
Parameter der G-Tr.: 
```
- Translation (Raum):       3
- Relativgeschwindigkeit:   3
- Rotation:                 3
- Translation (Zeit):       1
```
$\Rightarrow 10$  Parameter

Beachte:
$$\ddot x_1 = R_{ij} - \ddot x_j' \Rightarrow F_j = R_{ij} \; F_j'\quad \text{Transformation von Kräften} $$
$dt = dt' \Rightarrow$ "Punkt" kann $\frac d{dt}$ oder $\frac d{dt'}$ sein.

Zur vollständigen physikalischen Beschreibung müssen die Kräfte spezifiziert werden.
Typischer Fall: Angabe eines Kraftgesetzes, oft in der Form $\vec F(\vec r, \vec v, \vec t)$
$\vec r = \cases{&bezüglich Ursprung/Symetriezentrum\\ &Relativkoordinate}$

Dann ist
$$m \ddot{\vec r} = \vec F(\vec r, \dot{\vec r}, t ) $$
ein System von DGL zur Bestimmung von $x_i(t)$.
Typische Problemstellung: Anfangswertproblem
$$\vec r(t_0), \;\dot{\vec r(t_0)}\quad\text{gegeben} $$
$\Rightarrow$ Lösung ist eindeutig: Determinismus der klassischen Mechanik

Benannte Fälle von Kraftgesetzen:
$$\begin{align}
\vec F &= \vec F(\vec r, t) &\text{Kraftfeld}\\
\vec F &= \vec F(\vec r) &\text{stationäres Kraftfeld}\\
\vec F &= \vec F(t) &\text{homogenes Kraftfeld}\\
\vec F &= f(r) \vec r &\text{Zentralkraftfeld}
\end{align}$$
### 1.4.3 Wichtige Kräfte
1) Gravitation
2) Coulombkraft
3) Lorentzkraft: durch eines $\vec E$ und $\vec B$ bedingt
   $$\vec F (\vec r, \vec v, t) = q\;\vec E(\vec r, t) + q\; \vec v \times\vec B(\vec r, t) $$
4) Effektive Reibungskräfte
   - (a) zwischen festen Oberflächen (Haft, Gleitreibung)
   - (b) zwischen Körpern und Fluid
### 1.4.4 Scheinkräfte
Nicht-Inertialsysteme: $\dot{\vec p} = \vec F$ verletzt, nenne $\dot{\vec p} - \vec F$ "Scheinkraft"
Übergang zu beschleunigten Bezugssystemen:
$$\vec r(t) = \vec s(t) + R(t)\;\vec r'(t) $$
$\vec r(t)$ - Ort im Inertialsystem
$\vec r'(t)$ - Ort aus der Sicht eines Betrachters am Ort $\vec s(t)$, der sich mit $R(t)$ dreht
$$d\vec r = \vec r(t + dt) - \vec r(t) = d\vec s + d(R\vec r') = d\vec s + dR\vec r' + R\,\vec r' $$
$d\vec s$:       $s'$:    Translation
$dR\vec r'$:   $s'$:     Rotation 
$Rd\vec r'$:   Bewegung in $s'$
$$dR\vec r' \stackrel{\text{s. 1.1.3}}= d\vec\Omega\times \vec r' = d\vec \Omega \times R\vec r $$
Geschwindigkeiten: Mit $\vec \omega = \frac{d\vec\Omega}{dt}$
$$\dot{\vec r} = \dot{\vec s} + \vec \omega \times R\vec r' + R\dot{\vec r}'. $$
Infinitesimale Änderungen von $\dot{\vec r}$:
$$\begin{align}
d\dot{\vec r} &= d\dot{\vec s} + \dot{\vec \omega} \times R\vec r' + \vec \omega \times d(R\vec r') + d(R\dot{\vec r'}) \\
&= d\dot{\vec s} + \dot{\vec \omega} \times R\vec r' + \vec \omega \times (d\Omega\times R\vec r') + d\Omega\times R \dot{\vec r'} + R\,d\dot{\vec r'}.
\end{align}$$
Beschleunigung
$$\ddot{\vec r} = \ddot{\vec s} + \dot{\vec \omega} \times R\vec r' + \vec \omega \times (\omega\times R\,\vec r') + 2\vec \omega \times R\dot{\vec r}' + R\ddot{\vec r}'.$$
