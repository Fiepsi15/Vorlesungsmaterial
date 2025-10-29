---
tags:
  - HMIII
  - HM
  - WS2025/26
---
Tutorium: [[HM III Tutorium]]
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
Dann löst $y \text{ AWP}\cases{y' = \varphi(x,y)\\ y(\xi) = \eta}\Leftrightarrow y(x) = \eta + \int_\xi^x\varphi(t, y(t))\,dt$ für alle $x\in I$.
Dies ist eine Integralgleichung. $y$ ist auf beigen, aber keine Ableitung möglich
*Interessant:* Differenzieren verschlechtert Regularität, aber Int. verbessert!
### Definition 1.13
$\varphi: M\to \mathbb R,\,M\subset\mathbb R^2$. Dann erfüllt $\varphi$ auf $M$ eine Lipschitz-Bedingung (bezüglich der 2. Variable und mit Lipschitz-konstante $L\geq 0$) (schreibe $\varphi$ erfüllt $(LB)$), wenn 
$$\forall\pmatrix{x\\ y_1},\,\pmatrix{x\\ y_2} \in M: \|\varphi(x,y_1) - \varphi(x, y_2)\| \leq L\cdot\|y_1, y_2\| $$
### Bemerkung
Folgender Weg ist üblich, um eine $(LB)$ zu überprüfen:

Besitzt $\varphi$ (bezgl. der 2. Variablen) eine *beschränkte* partielle Ableitung $\partial_y \varphi$, zum Beispiel $\|\partial_y\varphi(x,y)\|\leq L$ für alle $\pmatrix{x\\ y}\in M$, so folgt für alle $x, y_1, y_2\in \mathbb R$ mit $\pmatrix{x\\ y_1},\,\pmatrix{x\\ y_2}\subset M$, dass die Verbindungsstrecke der beiden Punkte $\|\varphi(x, y_1) -\varphi(x,y_2)\| \stackrel{\text{MWS}}= \|\partial_y \varphi(x, \xi)(y_1-y_2)\|$ $\leq L\cdot \|y_1-y_2\|$ ($\xi$ geeignet zwischen $y_1$ und $y_2$), dh. $\varphi$ erfüllt *(LB)* mit Konstante $L$.
### Satz 1.15 (Existenzsatz von Picard-Lindelöf)
*Gegeben* sei: $r, s> 0,\xi, \eta\in \mathbb R, M =[\xi, \xi + r]\times[\eta-s, \eta+s]$. 
Zudem sei $\varphi: M\to\mathbb R$ stetig mit (LB) zu Konstante $L> 0$.
Außerdem sei $\|\varphi(x,y)\|\leq\frac s r$ für alle $\pmatrix{x\\ y}\in M$ 
(um sicherzustellen, dass nach $r$ Zeit noch nicht $[\eta-s,\,\eta+s]$ verlassen werden könnte).

Dann besitzt das AWP $\cases{y' = \varphi(x,y)\\ y(\xi) = \eta}$ eine Lösung auf dem Intervall $[\xi, \xi + r]$.
### Beweis
Wir definieren eine Folge $(y_n)_{n\in \mathbb N}$ von Funktionen $y_n :[\xi, \xi + r]\to[\eta-s, \eta+s]$ rekursiv durch $y_0(x) \equiv \eta$ *(ein erster aber im Allgemeinen schlechter Lösungskandidat)*
$$y_{n+1}(x) := \eta + \int_\xi^x\varphi(t,y_n(t))\,dt,\text{ für alle }x\in[\xi,\xi+r]$$
(Dieses Verfahren heißt Picard-Iteration und ist konstruktiv!)
Rest des Beweises:
1) $y_n$ sind wohldefiniert, haben also Werte nur in $[\eta-s, \eta+s]$
2) $y_n$ konvergiert gleichmäßig gegen eine Funktion $y$
3) $y$ löst AWP
### Bemerkung
1) Analog gilt dieser Satz auch für Intervalle $[\xi-r,\,\xi]$ oder $[\xi-r,\,\xi+r]$.
2) Es gilt tatsächlich eine Verallgemeinerung dieses Existenzsatzes **ohne** (LB) auf geeignet klein gewähltem Intervall $\to$ Satz von Peano. (Einschränkung: im Allgemeinen keine eindeutige Lösbarkeit. (LB) liefert diese. Ist relevant für die Existenz maximaler Lösungsintervalle,... )
### Beispiel
Picard-Iteration an einfachem Beispiel
$$\cases{y' = x\cdot y \\ y(0) = 1}$$
$$\begin{align}
y_0&:\equiv 1,\quad y_1(x) = 1+\int_0^x t\cdot 1\;dt = 1+\frac {x^2}2\\
y_2(x) &= 1+\int_0^xt\cdot(1+\frac{t^2}2)\;dt = 1+ \frac{x^2}2+\frac{x^4}8
\end{align} $$
Induktion: $y_n (x) = \sum_{k=0}^n \frac{(x^2/2)^k}{k!}$ für alle $x\in\mathbb R$ $\stackrel{n\to\infty}\to \exp(\frac {x^2}2) = y(x)$.
### Proposition 1.16 (Gronwallsches Lemma)
Sei $C\geq 0$ und $f,h:[a,b] \to[0, \infty)$ stetig mit $0\leq f(x) \leq C + \int_a^xh(t)f(t) \,dt$. (Integralungleichung, auf beiden seiten steht $f$ $\to$ Implizit). Dann folgt 
$$0\leq f(x)\leq C\cdot\exp\left(\int_a^xh(t)\;dt\right) \qquad(2)$$
für alle $x\in[a,b]$.
Insbesondere: $C = 0\Rightarrow f\equiv 0$.
**Idee**: $f = \|y_1-y_2\|$ $\leftarrow$ *betrag macht im Allgemeinen die DGL kaputt, aber man bekommt trotzdem noch die Integralgleichung*
**Anschauung:** Die Funktion rechts in $(2)$ als Wahl von $f$ würde die Integralgleichung mit "=" erfüllen
### Satz 1.17 (Existenz- und Eindeutigkeitssatz von Picard-Lindelöf)
Gegeben seien $r,s>0,\, \xi,\eta \in \mathbb R,\, M=[\xi, \xi+r]\times[\eta-s, \eta+s]$ $\varphi: M\to\mathbb R$ sei stetig und erfülle (LB) mit Konstante $L>0$.
Zudem gelte $\| \varphi(x,y)\|\leq \frac s r$ für alle $\pmatrix{x\\  y}\in M.\quad (3)$
Dann hat das AWP $\cases{y' = \varphi(x,y)\\ y(\xi) = \eta}$ existiert eine *eindeutige* Lösung $y:[\xi, \xi +r]\to\mathbb R$.
### Bemerkung
1) Wieder lässt sich $(3)$ auch damit sicherstellen dass man $r>0$ geeignet klein wählt. Wieder funktioniert das entsprechend auf Intervallen der Form $[\xi-r,\xi]$ oder $[\xi-r,\xi+r]$.
2) (LB) ist essentiell für die Eindeutigkeits-Aussage!
### Korollar
Sei $G\subset\mathbb R$ Gebiet, $\varphi: G\to\mathbb R$ stetig und erfülle auf $G$ eine Lokale Lip-Bedingung (LB$_{loc}$),
dh. $\forall \pmatrix{x_0\\y_0}\in G \;\exists\; \varepsilon>0: \varphi$ erfüllt (LB) auf $G \cap B(\pmatrix{x_0\\y_0},\varepsilon)$.
Zudem sei $\pmatrix{\xi\\\eta}\in G$. (Lip-Konstante kann von der Stelle und $\varepsilon$ abhängen).
Dann existieren $a,b$ mit $a<\xi<b$ derart, dass das AWP$\cases{y' = \varphi(x,y)\\ y(\xi) = \eta}$ auf $(a,b)$ eine eindeutige Lösung besitzt.
### Proposition 1.18
(Stetige Abhängigkeit von den gegebenen Daten, dh. insbesondere den AW)

Sei $G\subset \mathbb R^2$ ein Gebiet, $\varphi_1, \varphi_2: G \to \mathbb R$ stetig mit (LB) für Konstante $L>0$. Weiter gelte $\|\varphi_1(x,y)- \varphi_2(x,y)\|\leq C$ für alle $\pmatrix{x\\ y}\in G$ mit festem $C \geq 0$
$y_1: I\to \mathbb R$ sei Lösung des AWP$\cases{y' = \varphi(x,y) \\ y(\xi) = \eta_1}$
$y_2 :I\to \mathbb R$ sei Lösung des AWP$\cases{y' = \varphi(x,y)\\ y(\xi) = \eta_2}$
mit nicht degeneriertem Intervall $I, \xi\in I,\,\eta_1,\eta_2\in \mathbb R$

**Dann** gilt für alle $x\in I$ : $\|y_1(x)-y_2(x)\|\leq (\|\eta_1-\eta_2\|+c\|x-\xi\|)\;e^{L\|x-\xi\|}$

(Diese rechte Seite wird klein, wenn $\eta_1$ nah bei $\eta_2$ und $\varphi_1$ nahe bei $\varphi_2$ ist, womit $c\geq0$ klein gewählt werden kann, wenn $x$ nahe beim Anfangspunkt $\xi$ ist und wenn $L$ klein ist.)
(Beachte, gilt $y_1 = y_2$ und $\varphi_1 = \varphi_2$, dann kann $c=0$ und damit die rechte Seite auch wirklich $\equiv0$ gewählt werden. )
### Beweis
Fall $x>\xi$ (anderer Fall analog)
Dann gilt:
$$\begin{align}
\|y_1(x)-y_2(x)\| &= \left\|\eta_1 + \int_\xi^x \varphi_1(t,y_1(t))dt - \eta_2 - \int_\xi^x \varphi_2(t, y_2(t))dt\right\|\\
&\leq\|\eta_1-\eta_2\| + \int_\xi^x \|\varphi_1(t,y_1(t)) - \varphi_2(t,y_2(t))\|\,dt\\
&\leq\|\eta_1-\eta_2\| + \int_\xi^x \|\varphi_1(t,y_1(t)) - \varphi_2(t,y_1(t))\|\,dt + \int_\xi^x \|\varphi_2(t,y_1(t)) - \varphi_2(t,y_2(t))\|\,dt\\
&\leq \| \eta_1-\eta_2\| + c\cdot\|x-\xi\| + \int_\xi^xL\cdot\|y_1(t)-y_1(t)\|\,dt\\
&\stackrel{\text{Gronwll Lemma}}\Rightarrow \|y_1(x) - y_2(x)\| \leq (\| \eta_1-\eta_2\| + c\cdot\|x-\xi\|) \cdot\exp(L\,\|x-\xi\|)\;\boxed{}
\end{align}$$
### Lemma (Globale Eindeutigkeit bei Lip.-Bed.)
Sei $G \subset \mathbb R^2$ ein Gebiet, $\varphi: G\to\mathbb R$ stetig mit (LB)$_{loc}$. Seien $y_1: I\to\mathbb R$ und $y_2: J\to\mathbb R$ mit $I,J\subset\mathbb R$ nicht degenerierte Intervalle. Lösungen von $y' = \varphi(x,y)$. Gilt dann $y_1(t_0) = y_2(t_0)$ für $t_0\in I\cap J$, do folgt $y_1(t) = y_2(t)$ für alle $t\in I\cap J$.
### Proposition 1.19 (Maximales Lösungsintervall)
Sei $G\subset \mathbb R^2$ ein Gebiet, $\varphi: G \to \mathbb R$ stetig mit (LB)$_{loc}$. Weiter $\pmatrix{\xi\\ \eta}\in G$. Dann existiert ein Intervall $I\subset \mathbb R$ (nicht deg.) und eine Funktion $y_0: I\to \mathbb R$ mit folgenden Eigenschaften:
1) $y_0$ löst AWP
   $$\cases{y' = \varphi(x,y)\\ y(\xi) = \eta} $$
2) Für jede weitere Lösung $\tilde y: J\to \mathbb R$ des AWP gilt $J\subset I$ und $\tilde y = y_0$ auf $J$. In diesem Fall ist $I$ offen, das heißt $s = \inf I, r = \sup I \notin I$.
### Bemerkung
Wenn $G$ in [[#Proposition 1.19]] nicht offen ist existiert immer noch ein maximales Lösungsintervall (in allen vernünftigen Fällen), aber dieses braucht nicht immer offen sein, da die Randpunkte auf $\partial G$ liegen können.

Wir sehen im folgenden wichtigen Resultat, dass eine maximale Lösung insbesondere nicht echt innerhalb von $G$ "versanden" kann (das heißt, die maximale Lösung wird immer nur dadurch beschränkt, dass man sonst "aus $G$ herauslaufen" würde)
### Definition 1.20
Sei $x\in \mathbb R^d$ und $A\subset \mathbb R^d$ mit $A\neq \emptyset$. Dann heißt $d(x, A) := \inf{\{\|y-x\|:y\in A}\}$ der **Abstand** von $x$ zur Menge $A$.
### Proposition 1.21 (Lösungen laufen von Rand zu Rand)
Voraussetzungen wie in [[#Proposition 1.19 (Maximales Lösungsintervall)]]
Für die maximale Lösung $y_0:I\to\mathbb R$ des AWP gilt mindestens eine der folgenden Aussagen:
1) $r=\infty$ (Globale Existenz nach rechts)
2) $\limsup_{t\to r^-}\|y_0(t)\| = 0$ (Blow-up, in endlicher Zeit, falls $r<\infty$)
3) *(falls $\partial G\neq \emptyset$):* $\liminf_{t\to r^-} d(\pmatrix{t\\ y_0(t)}, \partial G) = 0$ (wir laufen also wirklich auf den Rand von $G$)
### Bemerkung
Das Resultat gilt entsprechend natürlich auch für das Verhalten $t\to l^+$ (Zeitliche Entwicklung nach links).

---
Wir haben bereits die folgende Tri... zum Lösen von DGL 1. Ordnung erzielt.
1) Existenz einer (lokalen) Lösung (mit sehr schwachen Anforderungen)
2) Eindeutigkeit dieser (lokalen) Lösung (mit (LB)$_{loc}$)
3) Stetige Abhängigkeit von den Daten
Diese Punkte zusammengenommen ergeben eine Schöne Lösungstheorie. ($\stackrel{1) +2)}\Rightarrow$ Existenz maximaler Lösungsintervalle).

**Übliches Setting:**
$G\subset \mathbb R^2$  ist ein Gebiet und $\varphi: G\to\mathbb R$ ist stetig mit (LB)$_{loc}$.
Wenn $\xi = t_o$ fixiert wird, dann kann man $\eta$ mit $\pmatrix{t_0\\ \eta}\in G$ als Parameter betrachten, wodurch die eindeutige maximale Lösung $y_\eta$ des AWP $\cases{y' = \varphi(x,y)\\ y(t_0) = \eta}$ festgelegt ist, das heißt *allgemeine parametrisierte Lösung* $\eta\to y_\eta$ existiert.

---
## 1.4 Spezielle DGL 1.Ordnung
Wir haben bereits eine abstrakte Lösungstheorie. ($\varphi$ mit (LB)$_{loc}\Rightarrow$ existiert Lösung, ...).
Im folgenden interessieren uns spezieller Konkrete DGL mit konkreten und expliziten Lösungstechniken und Ansätzen (Fast immer ist die abstrakte Lösungstheorie anwendbar, womit wir schon wissen, dass es eine eindeutige Lösung auf einem maximalen Lösungsintervall gibt, aber eben nicht wie diese konkret aussehen und bestimmt werden können).

Ziel: viele verschiedene Beispiele
### 1.4.1 Bernoullische DGL
Gegeben seien $f, g: I\to\mathbb R$ stetig, $\alpha\in\mathbb R$
Dann heißt $y' = f(x) y + g(x) y^\alpha$ 
($\alpha$ legt fest, wo $\varphi(t, z) = f(t) z + g(t)z^\alpha$ definiert ist, zum Beispiel für $\alpha = \frac12$ und $z<0$)

Im allgemeinen für $\alpha\notin\{0, 1\}$ nichtlineare DGL.
#### Anwendung
1) Beispiel eine nichtlineare DGL, wo man allgemeine Lösungen explizit bestimmen kann
2) Beispiel für Lösungstechnik "Reduktion auf bekannten fall durch Substitution"
3) Modell für logistisches Wachstum (zum Beispiel $y' = y(1-y) = y-y^2$)
#### Lösungsansatz
Finde DGL zu $z(x) = (y(x))^{1-\alpha}$ falls $y$ Lösung ist.
$z'(x) = (1-\alpha)(y(x))^{-\alpha}\cdot y'(x)$
$= (1-\alpha)(y(x))^{-\alpha} \; (f(x)y(x)+ g(x)(y(x))^\alpha)=(1-\alpha)\, f(x)\,z(x) + (1-\alpha)\,g(x)$,
das heißt $z$ genügt eine lineare DGL, wofür wir eine explizite Lösung haben.
#### Beispiel
$y' = x\cdot y - 3xy^2\Rightarrow$ Bernoulli mit $f(x) = x, g(x) = -3x, \alpha = 2$.
$y(0) = \frac15$
**Ansatz:** $z(x) = \frac1{y(x)}$
$$\begin{align}
z' = -\frac1{y^2}y' &= -x\cdot z + 3x
\end{align}$$
```
WIP
```
### 1.4.2 Riccatische DGL
Gegeben: $f, g, h \in C(I)$
Dann heißt $y' = f(x) y^2 + g(x) y + h(x)$
Riccatische Differenzialgleichung
#### Anwendung für uns
1) Einfaches Beispiel, für das keine allgemeine Lösungsmethode existiert
2) Ansatz: "Falls man aber eine Lösung kennt, kann man alle bestimmen". beziehungsweise kann in vielen Fällen "äquivalent zu einer ganz anderen DGL umgeschrieben werden"
3) DGL ist ein wichtiger Fall einer DGL in der komplexen Analysis, schwarzsche Transformation
#### Lösungsansatz
Sei $y_1$ eine gegebene/bekannte Lösung von Riccati DGL. Dann gilt für jede weitere Lösung $y_2$ folgendes:
Mit $z:= y_2 - y_1$ gilt
$$\begin{align}
z'(x) = y_2'(x) - y_1'(x) &= f(x)(y_2(x))^2 + g(x)y_2(x) + h(x) - f(x)(y_1(x))^2- g(x) y_1(x) - h(x) \\
&= f(x)\;(y_2(x) + y_1(x))\;(y_2(x)-y_1(x)) + g(x)\;(y_2(x)-y_1(x))\\\\
%&=y_2(x)-y_1(x) +z\,y_1(x)\\
%&= z(x) + z\,y_1(x)
\Rightarrow z'(x)& = f(x)\cdot(z(x))^2 + (g(x) + f(x) \cdot 2y_1(x))z(x)
\end{align}$$
das heißt $z$ erfüllt Bernoullische DGL mit $\alpha = 2$, was wir explizit lösen können.
#### Beispiel
Betrachte Riccatische DGL $y' = y^2 +\frac1{4x^2}, x>0$
Dann ist $y_1: (0, \infty)\to\mathbb R$, $y_1(x) = -\frac 1{2x}$ eine Lösung. Für jede weitere Lösung $y$ gilt mit dem Ansatz $z:= y- y_1 = y +\frac1{2x}$.
$$\begin{align}
z' = y' -\frac1{2x^2} = y^2 + \frac1{4x^2} - \frac1{2x^2} &= (z-\frac1{2x})^2 -\frac1{4x^2}\\
&= z^2-\frac1{x}z
\end{align}$$
Die Bernoulli DLG für $z$ lassen wir mit Ansatz $w = \frac1z$
$$\begin{align}
\Rightarrow w' &= - z^{-2} \cdot z' = \frac{\frac1x z -z^2}{z^2} =\frac1x\frac1z-1\\
&= \frac1xw-1
\end{align}$$
was wine lineare DGL für $w$ ist. Allgemein mit $\eta$ parametrischer Ansatz $w(1) = \eta$:
```
WIP
```

Ansatz: "unter gewissen Anforderungen äquivalent zu ganz anderem Typ von DGL:"
### Lemma 1.22
$I\subset \mathbb R$ offenes nicht degeneriertes Intervall, $\xi\in I,\;g, h: \in C(I)$ und $f\in C^1(I)$.

Dann:
1) Ist $y: I\to \mathbb R$ Lösung von $y' = f(x)y^2 + g(x)y + h(x)$ (Riccati), 
   So ist $u: I\to\mathbb R, \; u(x):= \exp(-\int_\xi^xf(t)y(t) dt)$ eine Lösung von der DGL 2. Ordnung (in nicht kanonischem Raum) "kanonische Transformation von $y$"
   $$f(x)u''-(f'(x) + f(x)g(x))u' + h(x)(f(x))^2u = 0 $$
2) Ist $u: I\to\mathbb R$ Lösung von 
   $$f(x)u''-(f'(x) + f(x)g(x))u' + h(x)(f(x))^2u = 0 $$
   und gilt $f(x)\neq 0$ und $u(x)\neq 0$ auf $I$, so ist $y: I\to\mathbb R,\, y(x) := \frac{-u'(x)}{f(x)u(x)}$ eine Lösung von $y' = f(x)\cdot y^2+ g(x)\cdot y+ h(x)$ (Riccati).
#### Beispiel
$y(x) =-\frac1{2x}$ löst $y'= y^2 + \frac1{4x^2}$ (wie vorher)
Also $f\equiv 1, g\equiv 0, h(x) =\frac1{4x^2}$ auf $(0,\infty)$
$\stackrel{\text{Lemma}}\Rightarrow u(x):= \exp(-\int_1^x-\frac1{2t}\,dt) = \exp(\frac12\log x) = \sqrt{x}$ 
löst die DGL 2. Ordnung
$$u'' - (0 + 1\,0)\cdot u' + \frac1{4x^2}1^2\cdot u = 0 
\Leftrightarrow u'' + \frac1{4x^2} u = 0 $$
### 1.4 3 DGL mit getrennten Veränderlichen
Seien $I, J$ Intervalle, $f: I\to\mathbb R,\,g: J\to\mathbb R$ stetig. Eine DGL der Form
$$y' = f(x)g(y) $$
Produkt, erste Funktion nur von $x$ und zweite Funktion nur von $y$ abhängig.
Eine DGL mit getrennten Veränderlichen.
### Bemerkung
$\varphi(t, z) = f(t)\cdot g(z)$, das heißt bei Differenzierbarkeit $\partial_z\varphi(t, z) \stackrel{\text{?}}= f(t)g'(z)$, wad bedeutet, dass hier im Allgemeinen (LB)$_{loc}$ nicht zu gelten braucht. Trotzdem eine schöne Lösungstechnik und in vielen Fällen auch eindeutige Lösbarkeit.
#### Ansatz
Für eine Lösung $y: I\to\mathbb R$ gilt $\frac{y'(x)}{g(y(x))} = f(x)$ für alle $x\in I$ solange $g(y(x)) \neq 0$ $\int_\xi^x\frac{y'(t)}{g(y(t))}dt := \int_\xi^xf(t)dt = F(x)$ eine (durch $\xi$ festgelegte) SF von $f$.
$G(y(x)) = \int_\eta^{y(x)}\frac1{g(u)}du$, wenn $G(y):= \int_\eta^y\frac1{g(u)}du$ 

**Beachte:** Wenn $g(u) \neq 0$ für alle $u \in J$ ist, ist alles wohldefiniert und $G$ ist stetig differenzierbar mit Ableitung $\frac1{g(y)} \neq 0$, das heißt, die Ableitung hat wegen dem ZWS lokal ein fixiertes Vorzeichen $\Rightarrow G$ ist lokal streng monoton, und damit lokal eindeutig invertierbar mit stetiger Umkehrfunktion, 
**aber** oft nicht möglich lokale Umkehrfunktion von $G$ explizit anzugeben.
### Proposition 1.23 (DGL mit getrennten Variablen)
Seien $f:I\to \mathbb R,\,g:J\to \mathbb R$ stetig, $\xi\in I$ und $\eta\in J$ und $I, J$ offen.

1) Ist $g(y) \neq 0$ ($\to$ gilt lokal um $\eta$ herum), dann existiert eine Umgebung von $\xi$ auf der das AWP $y' = f(x)g(y), \;y(\xi) = \eta$ eine eindeutige Lösung besitzt.
2) Falls $g(\eta) = 0$ und $\delta > 0$ existiert mit $g(y) \neq 0$. für alle $y$ mit $0 < \|y-\eta\|\leq\delta$ und die uneigentlichen Riemann Integrale
   $$\int_\eta^{\eta+\delta}\frac1{g(u)} du\quad\text{und}\quad \int_{\eta-\delta}^\eta \frac1{g(u)}du $$
   beide divergieren.

so hat das AWP $y' = f(x)g(y), \;y(\xi) = \eta$ auf $I$ nur die (offensichtliche) Lösung $y\equiv \eta$.

Nicht anwendbar bei $y' = 1\sqrt{\|y\|},\, g(y) = \sqrt{\|y\|}$
$\int_0^\delta \frac1{\sqrt{1}}du \stackrel{\text{H.S.}} = [2\cdot u^{\frac12}]_0^\delta =2\sqrt\delta \to$ uneigentliches R-int konvergiert
Ind diesem Fall wissen wir ja auch schon, dass man keine eindeutige Lösung für 0 hat!

### Beispiel

1) AWP: $\cases{y' = y(1-y) = y-y^2 \\ y(0) = \frac12}$
   (getrennte Veränderliche, aber auch Bernoulli oder Riccati)
   Einfaches Beispiel zu logistischem Wachstum.
   
   $g(u) = u(1-u) = 0 \Leftrightarrow u\in\{0, 1\}$
   $\eta = \frac12\in(0,1)$
   
   **Autonome** DGL, das heißt rechte Seite hängt nicht direkt von $x$ ab ("die Regeln der Entwicklung sind Zeitunabhängig")
   $$\begin{align}
   F(x) &= \int_0^x1dt = x,\\
   G(y) &= \int_\frac12^y\frac1{u(1-u)} du = \int_\frac12^y\frac1 u+\frac1{1-u} du\\
   &= \left[\log u- \log(u-1)\right]_\frac12^y = \log(\frac y{1-y}) - 0
   \end{align}$$
   $\Rightarrow$ Lösung erfüllt $\log(\frac y{1-y}) = x \Leftrightarrow \frac{y-1+1}{1-y} = e^x \Leftrightarrow -1 + \frac1{1-y} = e^x$ $\Leftrightarrow 1-y = \frac1{e^x + 1} \Leftrightarrow y(x) = \frac{e^x}{e^x + 1} \in (0, 1)$ für alle $x\in \mathbb R$.
2) AWP: $\cases{y' = -\frac x y \\  y(0) = 1}$
   (lokal eindeutig Lösbar wegen (LB)$_{loc}$)
   $$\begin{align} 
   F(x) &= \int_0^x -t \,dt = -\frac{x^2}2\\
   G(y) &= \int_1^y u \, du \stackrel{\text{H.S.}} = \left[\frac12 u^2\right]_1^y = \frac{y^2-1}2
   \end{align}$$
   $G(y(x)) \stackrel!=F(x) \Leftrightarrow y(x = \pm\sqrt{1-x^2})$ und wegen AW ist nur die positive Lösung gültig.
   $\Rightarrow y(x) = \sqrt{1-x^2}$ ist Lösung auf $(-1, 1) \ni 0 = \xi$.
### 1.4.4 Die (Euler-) homogene DGL
Sei $f: I\to\mathbb R$ stetig. Eine DGL der Form
$$y'= f(\frac y x)\quad\leftarrow \text{momentane Änderung nur von $y(x) : x$ abh. ($x\neq 0$)} $$
heißt (Euler-) homogene DGL.
#### Ansatz
$z(x) = \frac{y(x)} x \Leftrightarrow y= x \cdot z$
Also $f(z) = y' \stackrel{\text{P.R.}} = z+ x z'$
$\Rightarrow z' =  \frac{f(z) - z} x$, was eine DGL in getrennten Veränderlichen ist.

#### Beispiel
homogene DGL $y' = \frac y x$ (das heißt $f(u) = u$)
Ansatz: $z =  \frac y x$, das heißt $y = x\,z$
$z = y' = z + xz' \Rightarrow xz' = 0 \stackrel{x\neq 0} \Rightarrow z' \equiv 0$
$\Rightarrow z(x) = c$ für alle $x$
$\Rightarrow y(x) = c\,x$ für $c\in \mathbb R$.
#### Technik/Ansatz
In manchen Beispielen (von homogenen DGL) hilft der Ansatz, dass eine Lösung in Polarkoordinaten nur abhängig zum Beispiel vom Winkel ist.

Wir wollen $y'=f(\frac y x)$ durch diesen Ansatz Lösen:
$$\tilde x(\varphi) = r(\varphi) \cdot \cos\varphi,\quad \tilde y(\varphi) = r(\varphi)\cdot \sin\varphi $$
$$f(\frac{\tilde y}{\tilde x}) = f(\frac{\sin\varphi}{\cos\varphi}) \stackrel{\text{DGL}}= y'(\tilde x(\varphi)) \stackrel{\text{NR.}}=\frac{\tilde y'(\varphi)}{\tilde x'(\varphi)} = \frac{r'(\varphi) \sin\varphi + r(\varphi) \cos\varphi}{r'(\varphi) \cos \varphi - r(\varphi)\sin\varphi}  $$
Nebenrechnung:
$$\begin{align} 
\frac d{d\varphi} \tilde y(\varphi) &= \frac d{d\varphi}(y(\tilde x(\varphi))) = y'(\tilde x(\varphi)) \cdot \tilde x(\varphi) \\
&\Rightarrow y'(\tilde x(\varphi)) = \frac{\tilde y'(\varphi)}{\tilde x'(\varphi)}
\end{align}$$
#### Beispiel
$y' = -\frac y x$
$$\begin{align}
-\frac{\cos \varphi}{\sin\varphi} &=  \frac{r'(\varphi) \sin\varphi + r(\varphi) \cos\varphi}{r'(\varphi) \cos \varphi - r(\varphi)\sin\varphi}\\
\Leftrightarrow r\sin\varphi\cos\varphi - r'(\cos\varphi)^2 &= r'(\sin\varphi)^2 + r\sin\varphi\cos\varphi\\
\Leftrightarrow r' ((\sin\varphi)^2+(\cos\varphi)^2) &= 0\\
\Rightarrow r' &\equiv 0 
\end{align} $$
### 1.4.5 Verallgemeinerte homogene (Jacobi) DGL
$f: I\to\mathbb R$ stetig, $a, b, c, \alpha, \beta, \gamma \in \mathbb R$ gegeben mit $a^2 + b^2 + c^2 >0$ und $\alpha^2 + \beta^2 + \gamma^2 > 0$.
Die DGL
$$y' = f(\frac{ax + bx + c}{\alpha x + \beta y + \gamma}) $$
Lösung durch Fallunterscheidung und Substitution.
Fall 1: $\alpha = \beta = 0$
Fall 2a: $\alpha^2 + \beta^2>0$ und $\pmatrix{a\\ b},\pmatrix{\alpha\\ \beta}$ sind la.
Fall 2b: fast wie 2a, aber linear unabhängig. Dann Löse $a x_0 + by_0 + c = 0$ und $\alpha x_0 + \beta y_0 + \gamma = 0$ für einfache bestimmte $x_0, y_0 \in \mathbb R$. Substituiere dann $z(x) = y(x +x_0) -y_0$
$$\Rightarrow z' = f(\frac{ax +bz}{\alpha x + \beta z}) \stackrel{x \neq 0} = f(\frac{a + b \frac z x}{\alpha + \beta \frac z x}) $$
was rechts es nur von $\frac z x$ abhängt, das heißt eine Euler homogene DGL für $z$ ist.
### Bemerkung
Dieser Lösungsansatz liefert im Allgemeinen (wie schon zum Beispiel bei getrennten Variablen wenn die Umkehrfunktion von $G$ nicht explizit angegeben werden kann) nur eine implizite Beschreibung der Lösung.
### Beispiel
Es sei: $y' = \frac{4x + 3y - 1}{3x + 4y + 1}\quad (f(y) = y,\; a = 4,\; b = 3,\; c = -1,\; ...)$.
Dann ist $\det \pmatrix{4 & 3 \\ 3 & 4} = 16-9 \neq 0 \Rightarrow$ Fall 2b.
Substitution: $z(x) := y(x + 1) - (-1) = y(x+1) + 1$
$$\begin{align}
4x_0 + 3y_0 &= 1\\
3x_0 + 4y_0 &= -1
\end{align}$$
$\Rightarrow x_0 = 1, y_0 = -1$
$$\Rightarrow z'(x) = \frac{4 + 3\frac{z(x)} x}{3 + 4\frac{z(x)} x}$$ 
eine Euler-homogene DGL.
Substitution $w(x) = \frac{z(x)}x \Rightarrow z'(x) = w(x) + xw'(x)$ liefert 
$$w' = - \frac1x\frac{4 + 6 w + 4 w^2}{3 + 4 w + }\quad\text{Ansatz für allg. Lsg AW } w(\xi) = \eta ,$$
eine DLG mit getrennten Variablen
$$\begin{align}
&\Rightarrow \int_\xi^x\frac {3 + 4w(t)}{4 + 6w(t) + 4 w(t)^2} \cdot w'(t) dt \stackrel!= -\int_\xi^x\frac1 tdt = -\log|\frac x\xi|\\
&\Rightarrow \frac{\xi^2}{x^2} = \frac{4 + 6w + 4w^2}{4 + 6\eta + 4\eta^2}\\
&\Rightarrow 4 + 6w + 4w^2 = \frac {2c}{x^2},\;\text{für } c> 0\\
&\Rightarrow 2x^2 + 3 xz + 3z^2 = c\\
&\Rightarrow 2x^3 - x + 3xy + 2y^2 + y = c-1
\end{align}$$
eine Implizite Gleichung für $y$ (ohne Ableitung).
Hier kann man das zu einer expliziten Beschreibung von $y$ umformen, da das eine quadratische Gleichung in $y(x)$ ist. Im allg. kann man hier aber bei einer komplizierteren nicht leicht auflösbaren impliziten Gleichung für die Lösung $y$ landen.
### 1.4.6 Die exakte DGL
Sei $G = (a, b) \times(\alpha,  \beta),\; f,g: G \to \mathbb R$ stetig.
Wir betrachten die DGL
$$f(x, y) + g(x, y)\cdot y' = 0.$$
Diese heißt **exakt**, wenn das Vektorfeld $\pmatrix{f \\ g}: G \to \mathbb R^2$ eine Stammfunktion $F$ besitzt, das heißt $$\nabla F = \pmatrix{\partial_x F \\ \partial_y F} = \pmatrix{f \\ g}$$
mit $F\in C^1: G \to \mathbb R$.
### Lemma 1.24 (exakte DGL)
Wie oben. Sei $C^1\ni y: I \to \mathbb R$ mit $\pmatrix{x\\ y(x)} \in G$ für alle $x\in I$.

Dann Löst $y$ die exakte DGL $f(x, y) + g(x,y) \cdot y' = 0$ genau dann, wenn $\exists\, c\in\mathbb R: F(x, y(x)) = c \;\forall\, x\in I$.
### Beweis
$y$ Lösung $\Leftrightarrow f(x, y(x)) + g(x, y(x)) \cdot y'(x) = 0$ für alle $x\in I$.
$$\begin{align}
&\Leftrightarrow (\partial_x F)(x, y(x)) + (\partial_y F)(x, y(x)) \cdot y'(x)\\
&= \frac d{dx}(F(x, y(x)))\quad\text{nach mehrdim. KR}
\end{align}$$
### Beispiel
#### 1)
DGL: 
$$2 x\log y + \frac{x^2}y \cdot y' = 0\quad(f(x,y) = 2x\log y,\;g(x,y) = \frac {x^2} y) $$
Eine Stammfunktion $F: \mathbb R\times (0, \infty) \to \mathbb R$, ist gegeben durch 
$$F(x, y) = x^2 \log y + h(y)\quad(\text{ok für} h(y) \equiv 0). $$
Damit $y$ Lösung $\Leftrightarrow F(x, y) \equiv C$
$$\begin{align}
&\Leftrightarrow x^2 \log y(x) = c \Leftrightarrow \log y(x) \stackrel{x\neq 0}= \frac c{x^2}\\
&\Leftrightarrow y(x) = \exp(\frac c{x^2})\in(0, \infty).
\end{align}$$
Für jedes $C\in \mathbb R$ ist $y(x) = \exp(\frac c{x^2})$ eine Lösung auf $(0, \infty)$.
#### 2)
Vorher: $y' = - \frac{4x + 3y - 1}{3x + 4y + 1}$
$$\Rightarrow 4x + 3y -1 + (3x + 4y + 1)\cdot y' = 0 $$
Hat Stammfunktion $F: \mathbb R^2 \to \mathbb R,\; F(x,y) = 2x^2 + 3xy - x + h(x)$
$= 2x^2 + 3xy - x + 2y^2 + y$.
$h(y) = 2y^2+y$

Wie vorher: $2x^2 + 3xy - x + 2y^2 + y = C$ ist implizite Beschreibung der Lösung (Hier der viel einfachere Weg)
### Bemerkung
1) $G = (a, b) \times (\alpha, \beta)$ sternförmig (sogar konvex)
   Das heißt nach HM2 gilt: Wenn $f,g\in C^1$ dann besitzt das Vektorfeld $\pmatrix{f\\ g}$ genau dann eine Stammfunktion, wenn die Integrabilitätsbedingung
   $$(\partial_y f)(x,y) = (\partial_x g)(x,y) $$
   gilt. (notwendig wegen Satz von Schwarz + hinreichend mit "Poincare Lemma")
2) Ist $F(x_0, y_0) = C$ und $(\partial_y F)(x_0,y_0) \neq 0$, dann existieren nach dem Satz von der impliziten Funktion offene Intervalle $\tilde I, \tilde J$ mit $x_0\in\tilde I$ und $y_0 \in \tilde J$ sowie (die Implizite Funktion) $y: \tilde I\to\tilde J$ mit $F(x, y(x)) = C$ für alle $x\in\tilde I$.
### Frage
Was, wenn nicht exakt?
**Technik:** Versuch mit einem "integrierbaren Faktor" exakt zu machen.
### Definition 1.25
Seien $f, g\in C((a, b)\times(\alpha,\beta))$.
Dann heißt eine $C^1$ Funktion $\mu: (a, b)\times(\alpha,\beta)\to \mathbb R\backslash\{0\}$ ein *integrierbarer Faktor/Euler Multiplikator* für die DGL $f + g\cdot y' = 0$, wenn die DGL
$$\mu(x,y)f(x,y) + \mu(x,y)g(x,y)\;y' = 0 $$
exakt ist.
### Lemma 1.26
Seien $f, g, \mu\in C^1((a, b)\times(\alpha,\beta))$.
Dann ist $\mu$ integrierbarer Faktor von $f + g\cdot y' = 0$ genau dann wenn
$$f\; \partial_y\mu - g\;\partial_x\mu = (\partial_x g - \partial_y f)\mu $$
(was eine sogar partielle DGL und damit im allgemeinen nicht einfach lösbar ist.
Hoffnung: vielleicht gibt es ja viele taugliche mit Faktoren (dh. Lösungen der partiellen DGL) $\mu$, was diese vielleicht über Zusatzbedingungen einfach auffindbar macht).
