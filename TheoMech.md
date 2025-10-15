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
