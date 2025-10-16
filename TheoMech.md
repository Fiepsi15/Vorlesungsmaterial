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
## Grundannahmen über Raum & Zeit
- Raum und Zeit seien **absolut** und unabhängig voneinander beschreibbar (nicht den phys. Gesetzen unterworfen)
- Raum sei euklidisch, 3D, isotrop *(invariant bezgl. Drehungen)*, homogen *(invariant bzgl. Verschiebungen)*
- von der Mechanik zu beschreibende Ereignisse: Ort ($\to$ "Punkt") und Zeit ($\to$ "Zeitpunkt") wohldefiniert
**Beachte:** relativistische Physik und Quantenphysik weichen davon ab!
## Vektorrechnung in 3D
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
Vektoren $\vec b_3, \vec b_2,  \vec b_3$ heißen linear unabhängig, wenn$$\lambda_1\vec b_1 + \lambda_2\vec b_2 + \lambda_3\vec b_3 = 0 \Rightarrow \lambda_1 = \lambda_2 = \lambda_3 = 0$$ im 3D euklidischen Raum: "nicht coplanar", bilden Basis
- Vektor $\vec a$ darstellbar in Koordinaten:$$\vec a = a_1\vec b_1 + a_2\vec b_2 + a_3\vec b_3 \quad, a_1, a_2, a_3\text{ eindeutig}$$
an Skalarprodukt angepasste Basis: ON-Basis $\vec e_1, \vec e_2, \vec e_3$ mit:$$\vec e_i \cdot\vec e_j = \delta_{ij} \Rightarrow \vec a\cdot\vec b = \sum_ia_ib_i. $$ Dann gilt $\vec a = \sum_{i = 1}^3 a_i\vec e_i$, bzw. $a_i = \vec e_i\cdot\vec a$. 

Levi-Civita-Symbol$$\varepsilon_{ijk} = \cases{1 &\text{falls $ijk$ eine gerade Permutation von 123 ist}\\-1 &--------||------  ungerade------||---------------------\\ 0 &sonst } $$ für $i,j,k\in{1,2,3}$. Für rechtshändiges ON-System: $\vec e_i\times\vec e_j = \sum_{k=1}^3\varepsilon_{ijk}\vec e_k$.
Einsteinsche Summenkonvention: über doppelt auftauchende Indizes wird summiert:$$\begin{align}
\vec a &= a_i\vec e_i\\
\vec a\cdot\vec b &= a_ib_i\\
\vec a\times\vec b &= \varepsilon_{ijk}\,a_i\,b_j\,\vec e_k
\end{align} $$
Spatprodukt $(\vec a\times\vec b)\cdot\vec c$
Eigenschaften: $(\vec a\times\vec b)\cdot\vec c =(\vec c\times\vec a)\cdot \vec b = (\vec b \times\vec c)\cdot\vec a$$$=\varepsilon_{ijk}\,a_i\,b_j\,c_k\qquad\text{3 Summationen!}$$
