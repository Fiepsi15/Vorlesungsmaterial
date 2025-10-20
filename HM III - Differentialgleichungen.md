---
tags:
  - HMIII
  - HM
  - WS2025/26
---
# Kapitel 1 DGL 1. Ordnung
## 1 Gleichmäßige Konvergenz
[[Graph]]
Sei $x\in (0,1)$ fest. Dann $\lim_{n\to\infty} f_n(x) = 0 =:f$ 
Also $f_n(x) \to f(x)\;\forall\, x\in(0,1)$, aber $\int_0^1 f_n(t)dt = 1\neq 0 = \int_0^1 f(t)dt$
$$\lim_{n\to\infty} \int_0^1f_n(t)dt\neq \int_0^1\left(\lim_{n\to\infty}f(t)\right)dt.$$
Das Integral vertauscht (hier) nicht mit dem Limes!

### Ähnlich:
$$\lim_{x\to1}\lim_{n\to\infty}x^n = \lim_{x\to1} 0=0$$
$$\lim_{n\to\infty}\lim_{x\to1}x^n = \lim_{n\to\infty} 1=1$$
### Potenz-Reihe:
$\sum_{n=0}^\infty a_n(x-x_0)^n$ definiert eine Funktion auf einem offenen Kurvenbereich $B(x_0, R) = \{y\in\mathbb C :\|y-x\|<\mathbb R\}$  wobei $R$ der Konvergenzradius der PR ist, dh.
$$R = \frac1{\limsup_{n\to\infty}\sqrt[n]{\|a\|}}\qquad\left(\text{bzw.}\cases{0,\; \text{falls }\limsup_{n\to\infty} = \infty \\ \infty\; \text{falls } \limsup_{n\to\infty} = 0}\right) $$
PR definieren schöne Funktionen auf dem (offenen) = KB. Hoffentlich immer differenzierbar, dass man die Ableitung durch gliedweise Differenzieren bekommt.
### Frage:
Gilt $\frac d{dx}\left(\sum_{n=0}^\infty a_n(x-x_0)^n\right) = \sum_{n=1}^\infty na_n(x-x_0)^{n-1}$ ? $(\forall x\in B(x_0, R))$ 
Kernfrage der Analysis, of Grenzprozesse (z.B. limes, Reihen, Integration, differentiation) vertauscht werden können.
### Definition 1.1
Geg. Folge von Funktionen $(f_n)_{n\in\mathbb N}$ mit $f_n: D \to \mathbb R^m.$ Dann heißt die Folge $(f_n)_{n\in\mathbb N}$ $\underline{\text{gleichmäßig Konvergent}}$ gegen die Funktion $f:D\to \mathbb R^m$$\Leftrightarrow\,\forall\,\epsilon>0\,\exists\, n_0 \in \mathbb N : \,\forall\, n\geq n_0:\forall x\in D: \|f_n(x)-f(x)\|<\epsilon$ 
Insbesondere konvergiert $\sum_{n=1}^\infty$ gleichmäßig, wenn die Folge der Partialsummen $\left(\sum_{n = 1}^N\right)_{N\in \mathbb N}$ gleichmäßig konvergiert.
### Bemerkung:
Gleichmäßig bedeutet hier, dass der Index $n_0(\epsilon)$ für ein gegebenes $\epsilon>0$ unabhängig von $x\in D$ gewählt werden kann, dh. $n_0$ macht den Job $\forall x$ gleichzeitig.

---
### Satz 1.2 (Stetigkeit der Grenzfunktion)
Sei $(f_n)_{n\in \mathbb N}$ gleichmäßig Konvergent gegen $f: D\to \mathbb R^m$ und $f_n: D\to \mathbb R^m$ alle stetig, dann ist auch $f$ stetig.
### Folgerung:
Sind alle $f_n: D\to \mathbb R ^m$ stetig und ist $\sum_{n=1}^\infty f_n$ gleichmäßig Konvergent, dann ist auch $\sum_{n=1}^\infty f_n$ stetig.

---
### Proposition 1.3 (Cauchy-Kriterium für gleichmäßige Konvergenz)
Eine Folge $(f_n)_{n\in \mathbb N}$ von Funktionen $f_n : D\to \mathbb R^m$ konvergiert genau dann gleichmäßig (auf D), wenn gilt:
$$\forall\,\epsilon>0 \,\exists\, n_0\in\mathbb N: \,\forall\,n,m\geq n_0 :\,\forall\,x\in D:\quad\|f_n(x)-f_m(x)\|<\epsilon $$
### Folgerung:
$\sum_{k = 1}^\infty f_k$ konvergiert gleichmäßig genau dann wenn gilt:
$$\forall\, \varepsilon>0\;\exists\; n_0 \in \mathbb N: \;\forall\;n\geq m\geq n_0:\;\forall\; x\in D:\quad \left\|\sum_{k = m}^n f_k(x)\right\|<\varepsilon$$
---
### Proposition 1.4 (Weierstraß'sches Majorantenkriterium)
Sei $\sum_{k=1}^\infty f_k$ eine Reihe von Funktionen $f_k:D\to \mathbb R^m$. 
Wenn eine Zahlenfolge $(a_n)_{n\in \mathbb N}$ mit $\|f_k(x)\|\leq a_k\;\forall\;x\in D$ existiert und $\sum_{k=1}^\infty a_k$  (absolut) konvergiert, dann konvergiert $\sum_{k=1}^\infty f_k$ gleichmäßig.
### Bemerkung
$$\forall\,\epsilon>0 \,\exists\, n_0\in\mathbb N: \,\forall\,n\geq n_0 :\,\underline{\forall x\in D: \|f_n(x)-f(x)\|\leq\varepsilon}$$
$:=\sup_{x\in D}\|f_n(x)-f(x)\|\leq\varepsilon$ definiert eine Norm auf dem VR der Funktionen auf D, welche als ==Konv:== die gleichmäßig konvergieren induziert!

Wenn $D\subset\mathbb R^p$  kompakt ist, ist jedes $f\in C(D)$ beschränkt $\Rightarrow (C(D),\|\cdot\|_\infty)$ ist normierter VR der wegen dem Resultaten aus letzter VL $\underline{\text{vollständig}}$ _(Cauchyfolgen sind konvergent)_ ist. 

Wenn $f_n\to f$ gleichmäßig, dann existiert $n_0 \in \mathbb N$ mit $\forall n\geq n_0: f_n$ liegt komplett im $\varepsilon$-Schlauch.

$\underline{\text{W-krit: }}$ Wenn Zahlenfolge $(a_n)_{n\in \mathbb N}$ mit $\forall x\in D: \|f_n(x)\|\leq a_n$ für alle $n\in N$ $\underline{\text{und}}$ $\sum_{n=1}^\infty a_n<\infty$ dann konvergiert $\sum _{n=1}^\infty f_n$ gleichmäßig auf D.
### Beispiel
$\sum_{n=1}^\infty\frac{\sin\left({e^{kx}+\log\sqrt{1+kx^2}}\right)}{k^2}$ konvergiert gleichmäßig, denn $\|\frac{\sin\left({e^{kx}+\log\sqrt{1+kx^2}}\right)}{k^2}\|\leq \frac1{k^2}$ und $\sum_{k=1}^\infty\frac1{k^2}<\infty$ 
### Folgerung
Sei $\sum_{k=0}^\infty a_k(x-x_0)^k$ eine PR mit KR $R> 0\;(R=\infty ok)$. Dann ist die PR gleichmäßig konvergent auf $B(x_0,R)$. 
### Bemerkung
Die gliedweise differenzierte (nur reell auf $(x_0-R, x_0+R)$) PR $\sum_{k=1}^\infty a_k k\cdot(x-x_0)^k = \sum_{k=0}^\infty a_{k+1} (k + 1) (x-x_0)^k$ hat ebenfalls KR R (konvergier also ebenfalls gleichmäßig auf jedem $B(x_0,r)$ mit $r\in (0,R)$).

---
### Satz 1.5 (Differenzierbarkeit der Grenzfunktion)
Sei $(f_n)_{n\in N}$ eine Folge von Funktionen $f_n:[a,b]\to \mathbb R$. Es gelte:
1) $(f'_n)_{n\in N}$ konvergiert gleichmäßig gegen eine Funktion $g:[a,b]\to\mathbb R$
2) $(f_n(x_1))_{n\in \mathbb N}$ konvergiert (in $\mathbb R$) für ein festes $x_1\in [a,b]$.
#### Dann:
1) $(f_n)_{n\in \mathbb N}$ konvergiert gleichmäßig gegen eine Funktion $f:[a,b]\to\mathbb R$
2) $f$ ist auf $[a,b]$ differenzierbar mit $f' = g$
### Bemerkung
$((\lim f_n)' = \lim(f_n'))$ Es gibt einen einfachen Beweis über [[Hauptsatz der DI]] falls $f_n'$ Riemann integrierbar.
### Bemerkung
Wenn $f_n: I\to \mathbb R$ auf einem beliebigen nicht degenerierten _(dh. nicht Ein-Punktintervall)_ Intervall $I$ differenzierbar sind, und $(f_n')_{n\in\mathbb N}$ auf jedem Kompakten Teilintervall von $I$ gleichmäßig konvergiert und $(f_n(x_1))_{n\in\mathbb N}$ an jeder Stelle $x_1 \in I$ konvergiert, gilt weiterhin, dass $f_n$ auf jedem kompakten Teilintervall von $I$ (und damit auf ganz $I$ punktweise) gegen ein auf ganz $I$ differenzierbare Funktion $f$ konvergiert, und es gilt $\lim_{n\to\infty}f'_n(x)=f'(x)$ für alle $x\in I$.
### Folgerung:
Seien $(f_n)$ differenzierbare Funktionen, $f_n:I\to\mathbb R,\,I\subset \mathbb R$ nicht degeneriert.
Wenn $\sum_{k = 1}^\infty f_k'$ auf jedem $[a,b]\subset I$ gleichmäßig konvergiert, und $\sum_{k = 1}^\infty f_k(x_1)$ konvegiert für ein $x_1\in[a,b]$, dann ist $\sum_{k=1}^\infty f_k$ gleichmäßig konvergent auf jedem $[a,b]\subset I$ und definiert auf $I$ eine differenzierbare Funktion mit $\left(\sum_{k=1}^\infty f_k\right)' = \sum_{k=1}^\infty f_k'$. Speziell im Fall reeller PR haben wir also, dass eine PR mit KR $R>0$ auf $(x_0-R, x_0+R)$ eine unendlich oft differenzierbare Funktion definiert, wobei man die Ableitung durch gliedweise Differenzieren berechnen kann.
### Beispiel
$\sum_{n=0}^\infty \frac{\sin(\frac x n)}n$ ist differenzierbar auf $\mathbb R$ mit Ableitung $\sum_{n=1}^\infty\frac{\cos(\frac x n)}{n^2}$, denn die ursprüngliche Reihe konvergiert für $x = 0$ und die abgeleitete Reihe konvergiert gleichmäßig mit der gleichen Begründung wie im Beispiel zu [[#Proposition 1.4 (Weierstraß'sches Majorantenkriterium)]].

---
### Satz 1.6 (Integration der Grenzfunktion)
Sei $(f_n)_{n\in\mathbb N}$ eine Folge stetiger Funktionen $f_n:[a, b]\to\mathbb R$ die auf $[a,b]$ gleichmäßig gegen eine (stetige) Funktion $f:[a,b]\to \mathbb R$ konvergiert. Dann:
$$\lim_{n\to\infty}\int_a^bf_n(x)dx = \int_a^bf(x)dx $$
### Folgerung
$\sum_{n=1}^\infty f_n$ gleichmäßig konvergente Reihe stetiger Funktionen $f_n:I\to \mathbb R$, dann $\int_a^b\left(\sum_{n=1}^\infty f_n(x)\right)dx =\sum_{n=1}^\infty\left(\int_a^bf_n(x)dx\right)$ für alle $[a,b]\subset I$.
### Bemerkung
Die Voraussetzungen von Satz 1.6 sind eigentlich zu stark, dh. der Satz gilt mit dem leistungsfähigeren Lebesgue Integral viel allgemeiner. Als Spezialfall erhalten wir für das R-Int:
### Satz 1.7 (Satz von Arzelà)
$(f_n)$ Folge von auf $[a,b]$ R-int Funktionen die auf $[a,b]$ punktweise gegen eine R-int. Funktion. Gilt dann zudem dass $C>0$ existiert mit $f:[a,b]$ konvergiert $\|f_n(x)\|\leq C$ für alle $n\in\mathbb N$ und $x\in [a,b]$, so gilt
$$\lim_{n\to\infty}\int_a^b f_n(x)dx = \int_a^b f(x)dx.$$
---
### Bonus (Anwendung für Konvergenzresultat von Fourier-Reihen)
Sei $f\in C^2(\mathbb R)$ $2\pi$-periodisch. Die Fourie-Partialsummen (in der komplexen Form) sind dann $S_n[f](x) =\sum_{k = -n}^n c_k e^{ikx}$, wobei $c_k = \frac1{2\pi}\int_{-\pi}^\pi f(t) e^{ikt} dt$ für alle $k\in \mathbb Z$.
#### Übungsaufgabe
Es gilt $c_k[f'] = ikc_k[f'] = -k^2 c_k[f]$ für alle $k\in \mathbb Z$ 
$\Rightarrow c_k[f''] = ikc_k[f'] = -k^2c_k[f]$. Mit $M:= max_{x\in[-\pi,\pi]} \|f''(x)\|<\infty$ gilt also $\|c_k[f]\|\leq\frac M{k^2}$. 
Da $\|e^{ikx}\| = 1$ konvergiert $S_n[f]$ gleichmäßig für $n\to\infty$ wegen des Weierstraß Majoranten-Kriteriums, den$$\|c_k e^{ikx}\| = \|c_k\|\leq\frac M{k^2},\,\text{und} \,\sum_{k=1}^\infty\frac M{k^2}<\infty.$$(Natürlich konvergiert $S_n[f]$ dann auch gegen f, aber das erfordert zusätzlich zum Beispiel ein einfaches pw. Konvergenzresultat)

---
## Kapitel 1.2 Die Lineare Differenzialgleichung
### Definition 1.8
1) Eine Menge $M\subset \mathbb R$ heißt **wegzusammenhängend**, wenn zu beliebigen Punkten $x,y\in M$ ein (stetiger) Weg $\gamma:[0,1]\to M$ mit $\gamma(0) = x$ und $\gamma(1) = y$ existiert ("bel. Paare von Punkten in $M$, können ohne $M$ zu verlassen durch einen Weg verbunden werden")
2) $G\subset \mathbb R^d$ heißt **Gebiet**, falls $G$ offen und wegzusammenänngend ist.
### Bemerkung
1) Tatsächlich kann man sich überlegen, dass in einem Gebiet alle zwei Punkte sogar über einen polygonalen Streckenzug verbunden werden können
2) Sternförmige und insbesondere Konvexe Teilmengen von $\mathbb R^d$ sind automatisch wegzusammenhängend.
Warum? DGL Zustandsraum Gebiet
### Lemma 1.9
Eine offene Menge $G$ ist genau dann ein Gebiet, wenn aus $G = O_1\cup O_2$ mit $O_1, O_2$ offen und disjunkt stets $O_1 = \varnothing$ oder $O_2 = \varnothing$ folgt. (das heißt, man kann $G$ mit offenen Mengen nicht auf interessant Art in zwei Teile zerlegen.)$$\begin{align}\tilde O_1 \cap G &\neq\varnothing\\
\tilde O_2 \cap G &\neq\varnothing\\
\tilde O_1 \cap \tilde O_2 \cap G &\neq\varnothing\\
G \subset\tilde O_1 &\cup \tilde O_2\end{align}$$
### Definition 1.10
$G\subset \mathbb R^2$ ein Gebiet (ohne eine andere vernünftige Menge wie zum Beispiel ein Rechteck $[a,b]\times[L,H]$ mit $a<b$ und $L<H$) und $\varphi: G\to \mathbb R$ stetig.
1) Eine Funktion $y:I\to \mathbb R$ (mit $I\subset \mathbb R$ nicht-deg. Intervall) heißt *Lösung der DGL 1. Ordnung*$$y'(x) = \varphi(x,y(x)) \qquad(\text{oder kurz } y' = \varphi(x,y)) $$wenn $y$ stetig differenzierbar ist mit $\pmatrix{x\\y(x)}\in G \;\forall\; x\in I$ und $y'(x) = \varphi(x, y(x)) \;\forall\; x\in I.$
2) $y: I\to\mathbb R$ heißt *Lösung des Anfangswertproblems* (AWP)$$\cases{y' = \varphi(x,y)\\y(\xi) = \eta}$$wenn $\pmatrix{\xi\\\eta}\in G$ und $y$ eine Lösung der DGL $y' = \varphi(x,y)$ mit $\xi\in I$ und $y(\xi) = \eta$.
3) Seien $f,g: I\to\mathbb R$ stetig. Dann heißt eine DGL der Form$$y' = f(x)\cdot y +g(x)$$*lineare Differentialgleichung 1. Ordnung*.
   Im Fall $g\equiv 0$ heißt diese DGL *homogen*, sonst *inhomogen*. Schon im Vorkurs der HM1 haben wir insbesondere solche linearen DGL 1. Ordnung gelöst.
### Satz 1.11
Sei $I$ nicht deg. Intervall, $f,g: I\to\mathbb R$ stetig. Definiere $y_\gamma :I\to\mathbb R, y_0(x) = exp\left(\int_\xi^x f(t)dt\right)$ und $y_1(x) = y_0(x)\cdot\left(\eta + \int_\xi^x \frac{g(t)}{y_0(t)}dt\right)\;(\xi\in I)$.
#### Dann
1) $y_0$ ist eindeutige Lösung des AWP auf $I$$$\cases{y' = f(x)y\\y(\xi) = 1} $$
2) $y_1$ ist eindeutige Lösung des AWP auf $I$$$\cases{y' = f(x)y+g(x)\\y(\xi) = \eta}$$
### Bemerkung 
zur Herleitung mit dem Ansatz "Variation der Konstanten" für inhomogene Lösung bei Kenntnis der zugehörigen homogenen Lösung.
Sei $F$ Stammfunktion von $f$ mit $F(\xi) = 0\quad (\Rightarrow F(x)= \int_\xi ^x f(t)dt)$. Dann sind alle Lösungen der homogenen DGL $y' = f(x)y$ von der Form $y(x) = c\cdot e^{F(x)}$ für geeignete Konstante $c$. Voraussetzung der Konstanten ist der Ansatz$$y(x) := c(x)e^{F(X)}$$für die Lösung der inhomogenen DGL$$\begin{align}
&\Rightarrow \underline{f(x)\,y(x)} +g(x) \stackrel!= y'(x) = c'(x)\,e^{F(x)}+ \underline{c(x)\,e^{F(x)}\,f(x)}\\
&\Rightarrow c'(x) = \frac{g(x)}{e^{F(x)}}
\end{align} $$
Lösung mit HDI legt $c$ fest $\to$ Formel wie bey $y_1$.
### Beispiel
(zu lin. DGL 1.)
1) *(unvollständig)* $$\text{AWP}\cases{y' = \frac y x-x &dh. $\varphi(t,z) = \frac z t -t$ nach def. für $t=0$\\y(1) = 2} $$
2) $$\cases{y' = y\sin x + \sin x\\y(0) = 0&$[\varphi(t,z) = f(t)z+g(t),\, f(t) = g(t) = \sin(t)]$}$$
   Lösung $y_0(x) = exp \int_0^x\sin t\;dt = e^{1-\cos x}$$$\begin{align}
   y_1(x) &= e^{1-\cos x}\cdot\left(0 + \int_0^x(\sin t)e^{\cos t -1}dt \right) \\
   &= e^{-\cos t} \cdot(-1) \int_0^x (-\sin t) e^{\cos t}dt \\
   &= e^{-\cos x}(-1)[e^{\cos t}]_0^x = e^{\cos x}\cdot(e-e^{\cos x})\\
   &= e^{1-\cos x}-1
   \end{align}$$
   Dann ist $y_1$ Lösung von AWP auf Intervall $\mathbb R$ 
## Existenz und Eindeutigkeitsaussagen
Solche Resultate sind wichtig schon allein für sich genommen, aus theoretischem und angewandten gründen.

Weitere Aspekte im folgenden:
1) DGL kann äquivalent als Integralgleichung geschrieben werden
2) Die Beweistechniken sind konstruktiv und können zur Approximation von Lösungen verwendet werden
3) In der Regel gibt es "maximale Lösungsintervalle" (angeben), die daher kommen, dass die Lösung gegen den Rand vom Def-Bereich von $\varphi$ läuft und deshalb nicht weiter fortsetzbar ist.
### Proposition 1.12 (Volterra Integralgleichung)
$G\subset\mathbb R^2$ sein ein Gebiet $\varphi : G\to\mathbb R$ stetig, $\pmatrix{\xi\\\eta}\in G$. Weiter sei $y: I\to\mathbb R$ mit $I$ nicht deg. Intervall
Dann löst $y \text{ AWP}\cases{y' = \varphi(x,y)\\y(\xi) = \eta}\Leftrightarrow y(x) = \eta + \int_\xi^x\varphi(t, y(t))\,dt$ für alle $x\in I$.
Dies ist eine Integralgleichung. $y$ ist auf beigen, aber keine Ableitung möglich
*Interessant:* Differenzieren verschlechtert Regularität, aber Int. verbessert!
### Definition 1.13
$\varphi: M\to \mathbb R,\,M\subset\mathbb R^2$. Dann erfüllt $\varphi$ auf $M$ eine Lipschitz-Bedingung (bezüglich der 2. Variable und mit Lipschitz-konstante $L\geq 0$) (schreibe $\varphi$ erfüllt $(LB)$), wenn $$\forall\pmatrix{x\\y_1},\,\pmatrix{x\\y_2} \in M: \|\varphi(x,y_1) - \varphi(x, y_2)\| \leq L\cdot\|y_1, y_2\| $$
### Bemerkung
Folgender Weg ist üblich, um eine $(LB)$ zu überprüfen:

Besitzt $\varphi$ (bezgl. der 2. Variablen) eine *beschränkte* partielle Ableitung $\partial_y \varphi$, zum Beispiel $\|\partial_y\varphi(x,y)\|\leq L$ für alle $\pmatrix{x\\ y}\in M$, so folgt für alle $x, y_1, y_2\in \mathbb R$ mit $\pmatrix{x\\ y_1},\,\pmatrix{x\\ y_2}\subset M$, dass die Verbindungsstrecke der beiden Punkte $\|\varphi(x, y_1) -\varphi(x,y_2)\| \stackrel{\text{MWS}}= \|\partial_y \varphi(x, \xi)(y_1-y_2)\|$ $\leq L\cdot \|y_1-y_2\|$ ($\xi$ geeignet zwischen $y_1$ und $y_2$), dh. $\varphi$ erfüllt *(LB)* mit Konstante $L$.
### Satz 1.15 (Existenzsatz von Picard-Lindelöf)
*Gegeben* sei: $r, s> 0,\xi, \eta\in \mathbb R, M =[\xi, \xi + r]\times[\eta-s, \eta+s]$. 
Zudem sei $\varphi: M\to\mathbb R$ stetig mit (LB) zu Konstante $L> 0$.
Außerdem sei $\|\varphi(x,y)\|\leq\frac s r$ für alle $\pmatrix{x\\y}\in M$ 
(um sicherzustellen, dass nach $r$ Zeit noch nicht $[\eta-s,\,\eta+s]$ verlassen werden könnte).

Dann besitzt das AWP $\cases{y' = \varphi(x,y)\\y(\xi) = \eta}$ eine Lösung auf dem Intervall $[\xi, \xi + r]$.
### Beweis
Wir definieren eine Folge $(y_n)_{n\in \mathbb N}$ von Funktionen $y_n :[\xi, \xi + r]\to[\eta-s, \eta+s]$ rekursiv durch $y_0(x) \equiv \eta$ *(ein erster aber im Allgemeinen schlechter Lösungskandidat)*
$$y_{n+1}(x) := \eta + \int_\xi^x\varphi(t,y_n(t))\,dt,\text{ für alle }x\in[\xi,\xi+r]$$
(Dieses Verfahren heißt Picard-Iteration und ist konstruktiv!)
Rest des Beweises:
1) $y_n$ sind wohldefiniert, haben also Werte nur in $[\eta-s, \eta+s]$
2) $y_n$ konvergiert gleichmäßig gegen eine Funktion $y$
3) $y$ löst AWP

