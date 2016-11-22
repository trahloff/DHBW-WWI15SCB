# **Mengenoperationen**
17.05.2016


<!-- TOC depthFrom:2 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Vereinigung von Mengen](#vereinigung-von-mengen)
	- [Definition](#definition)
	- [Beispiel](#beispiel)
	- [Notationen](#notationen)
	- [Rechenregeln](#rechenregeln)
- [Durchschnitt](#durchschnitt)
	- [Definition](#definition)
	- [Notation](#notation)
	- [Rechenregeln](#rechenregeln)
- [Distributivgesetze](#distributivgesetze)
- [Kardinalität](#kardinalität)
	- [Definition](#definition)
	- [Beispiel 1](#beispiel-1)
	- [Beispiel 2](#beispiel-2)
- [Satz von SYLVESTER](#satz-von-sylvester)
	- [Definition](#definition)
	- [Beispiel](#beispiel)
- [Differenz](#differenz)
	- [Definition](#definition)
	- [Beispiele](#beispiele)
	- [Eigenschaften](#eigenschaften)
- [Kartesisches Produkt](#kartesisches-produkt)
	- [Definition](#definition)
	- [Beispiele](#beispiele)
	- [Relation](#relation)
	- [Eigenschaften](#eigenschaften)
- [Komplementmenge](#komplementmenge)
	- [Definition](#definition)
	- [Beispiele](#beispiele)
- [Satz von DeMorgan](#satz-von-demorgan)
	- [Definition](#definition)
	- [Beispiele](#beispiele)
- [Zusammenfassung](#zusammenfassung)
- [Übungen](#übungen)
	- [1](#1)
	- [2](#2)

<!-- /TOC -->

---

## Vereinigung von Mengen

### Definition

Die Vereinigung M1 &cup; M2 zweier Mengen M1, M2 ist die Menge aller Elemente, die zu M1 &or;  M2 gehören.

M1 &cup; M2 = {x | x &isin; M1 oder x &isin; M2}

### Beispiel

{a,b,c} &cup; {a,c,d,e}
= {a,b,c,d,e}

### Notationen

sind M1, M2, ..., Mn endliche Mengen,

n
<br> U  Mi = M1 &cup; M2 &cup; ... U Mn
<br> i=1

### Rechenregeln

1. M &cup; M = M - Idenpotenzgesetz
2. M1 &cup; M2 = M2 &cup; M1 - Kommutativgesetz
3. M &cup; &empty; = M - d.h. &empty; ist das neutrale Element der u-Operation
4. M1 &cup; (M2 &cup; M3) = (M1 &cup; M2) &cup; M3 - Assoziativgesetz

---

## Durchschnitt

### Definition

Der _Durchschnitt_ M1  &cap;  M2 zweier Mengen M1, M2 ist die Menge aller Elemente, die zu M1 **und** M2 gehören.<br>
M1  &cap;  M2 = {x | x &isin; M1 _und_ x &isin; M2}
<br>
<br>
Haben beide Mengen M1 und M2 kein Element gemeinsam, dann ist
<br>M1  &cap;  M2 = &empty;<br>

In diesem Fall heißen M1, M2 **disjunkt** oder elementfremd.
Bsp: {a,b,c,d}  &cap;  {a,c,f} = {a,c}

### Notation

Sind M1, ..., Mn Mengen dann ist

n<br>
 &cap;  Mi = M1  &cap;  M2  &cap;  ...  &cap;  Mn <br>
i=1

### Rechenregeln

1. M  &cap;  M = M - M ist das neutrale Element der  &cap; -Operation
2. M1  &cap;  M2 = M2  &cap;  M1 - Kommutativgesetz
3. M  &cap;  &empty; = &empty;
4. M1  &cap;  (M2  &cap;  M3) = (M1  &cap;  M2)  &cap;  M3 - Assoziativgesetz

## Distributivgesetze

Wir haben also auf Mengen zwei zweistellige Operatoren &cup; und  &cap; . Die **Distributivgesetze** regeln wie sich diese beiden Operationen untereinander Verhalten.

M1 &cup; (M2  &cap;  M3) = (M1 &cup; M2)  &cap;  (M1 &cup; M3)

M1  &cap;  (M2 &cup; M3) = (M1  &cap;  M2) &cup; (M1  &cap;  m3)

## Kardinalität

### Definition

Anzahl der Elemente endlicher Mengen.

Man bezeichnet mit **|M|** die Anzahl der Elemente der Menge M, dies nennt man auch **Kardinalit** (gilt auch für &infin;)

Es gilt die **Siebformel** von _SYLVESTER_:

**|M1 &cup; M2| = |M1| + |M2| - |M1  &cap;  M2|**

### Beispiel 1

M1 = {1,2,3,4,5}; M2 = {3,4,5,6,7}

M1 &cup; M2 = {1,...,7}

M1  &cap;  M2 = {3,4,5}

|M1 &cup; M2| = 7

|M1| = 5 --> 7 = 5+5-3

|M2| = 5

|M1  &cap;  M2| = 3

### Beispiel 2

Man bekommt die Anzahl der durch 2 oder 3 teilbaren natürlichen Zahlen zwischen 1 und 100. <br>

Ak = {n &in; &#8469; | n &in; [1,100] und durch k ohne Rest teilbar}
<br>

Gesucht ist die Kardinalität von A2 &cup; A3

|Ak| = &lfloor; 100/k &rfloor;

&lfloor;x&rfloor; = größte ganze Zahl &le; x <br>
Bsp: &lfloor;pi&rfloor; = 3

|A2| = &lfloor;100/2&rfloor; = 50

|A3| = &lfloor;100/3&rfloor; = 33

Es gibt aber Zahlen wie 6,12,18,... die durch 2 **und** 3 teilbar sind. <br>

A2  &cap;  A3 = A6

|A6| = &lfloor;100/6&rfloor; = 16

--> |A2  &cap;  A3| = |A2| + |A3| - |A2  &cap;  A3|<br>
= 50 + 33 -16 = 67

## Satz von SYLVESTER

### Definition

Seien M1, M2, nnn Mn endliche Mengen dann ist

| n
| U Mi = |M1 &cup; M2 &cup; ... &cup; Mn |
|i=1

  n<br>
= &sum; (-1)^(i-1) * ki<br>
  i=1

Wobei die ki die Summe der Kardinalitäten aller möglichen Schnitte aus i Mengen sind, d.h.

k1 = |M1| + |M2| + ... + |Mn|

n<br>
k2 = &sum; |Mi  &cap;  Mj|<br>
i=1<br>
j=1<br>
i<J<br>


n<br>
k3=&sum; |Mi  &cap;  Mj  &cap;  Mk|<br>
i,j,k<br>
i<j<k

### Beispiel

M1 = {1,2,3,4,5}<br>
M2 = {2,4,6,7,8}<br>
M3 = {2,3,8,9}<br>
M4 = {2,4,5,9,10}<br>

M1 &cup; M2 &cup; M3 &cup; M4 = {1,2,3,4,5,6,7,8,9,10}<br>
|M1 &cup; M2 &cup; M3 &cup; M4| = 10

## Differenz

### Definition

Die Differenz M1 &#8726; M2 zweier Mengen M1, M2 ist die Menge aller Elemente von M1, die nicht in M2 enhalten sind,

M1 &#8726; M2 = {x | x &in; M1 und x &notin; M2}

Man beachte:<br>
M1 &#8726; M2 &ne; M2 &#8726; M1 !!

### Beispiele

M1 {1,2,3,4}, M2 = {3,4,5,6}

M1 &#8726; M2 = {1,2}<br>
M2 &#8726; M1 = {5,6}

### Eigenschaften

1. M &#8726; m = &empty;
2. M &#8726; &empty; = M
3. &empty; &#8726; M = &empty;

## Kartesisches Produkt

### Definition

Seien M1, M2 zwei Mengen. Das **Kartesische Produkt** M1 x M2 dieser Mengen ist die Menge aller geordneten Paare (m1, m2), mit m1 &in; M1 und m2 &in; M2

M1 x M2 = {(m1, m2) | m1 &in; M1, m2 &in; M2}

### Beispiele

1)<br>
&#8477;^2 = &#8477; x &#8477;<br>
= {(x, y) | x &in; &#8477;, y &in; &#8477;}

2)<br>
M1 = {a,b}, M2= {x,y}<br>
M1 x M2 = {(m1, m2) | m1 &in; M1, m2 &in; M2}<br>
={(a,x),(a,y),(b,x),(b,y)}

3)<br>
&#8477;^3 = &#8477; x &#8477; x &#8477;<br>
= {(x,y,z) | x &in; &#8477;, y &in; &#8477;, z &in; &#8477;}

4)<br>
S^1 = {(x,y) &in; &#8477;^2 | x^2+y^ = 1}<br>
= Einheitskreis<br>

### Relation

Eine **Relation** ist eine Teilmenge des Karesischen Produkts M1 x M2<br>

Tabelle &harr; Teilmenge eines Kartesischen Produktes<br>
Datensatz &harr; jeder Datensatz einer Tabelle entspricht einem n-Tupel eines n-fachen Kartesischen Produktes
Feldname (Attribute) &harr; Menge

### Eigenschaften

|M1 x M2| = |M1| &sdot; |M2| (für endliche Mengen)

M1 = {a,b}, M1 = {1,2}<br>
M1 x M2 = {(a,1),(a,2),(b,1),(b,2)}

Für n-Mengen des M1,...,Mn:<br>
n<br>
**X** Mi = M1 x M2 x ... x Mn<br>
i=1<br>
= {(m1,m2,...,mn) | mi &in; M}

Falls alle Mengen gleich sind:<br>
M x M x ... x M = M^n (&#8477;^3)

Es gilt:<br>
**a)** M1 x (M2 &cup; M3) = (M1 x M2) &cup; (M1 x M3)<br>
**b)** M1 x (M2 &cap; M3) = (M1 x M2) &cap; (M1 x M3)

Beispiel zu **b)**:<br>
M1 = { x &in; &#8477; | 1 &le; x &le; 3}<br>
M2 = { y &in; &#8477; | 1 &le; y &le; 4}<br>
M3 = { z &in; &#8477; | 1 &le; z &le; 5}<br>

[hier befindet sich ein wunderschöner Graph]

## Komplementmenge

### Definition

Sei M eine Menge (Obermenge) und M1 Teilmenge von M.<br>
Die **Komplementmenge** CM ist die Menge alle x, mit x &in; M und x &notin; M1.

CM1 = {x &in; M | x &notin; M1}

### Beispiele

M = &#8469; <br>
M1 = {x | x &in; &#8469;, x/2 &in; &#8469;}<br>
CM1 = ungerade natürliche Zahlen<br><br>
Es gilt:<br>
M &cap; CM = &empty;<br>
M &cup; CM = Obermenge<br>
C&empty; = Obermenge<br>
C&empty;(CM) = M

## Satz von DeMorgan

### Definition

Seien M1, M2 zwei Mengen dann gilt:

**C(M1 &cup; M2) = CM1 &cap; CM2<br>
C(M1 &cap; M2) = CM1 &cup; CM2<br>**

### Beispiele

1)<br>
M1 = {x &in; &#8469; | x &le; 3}<br>
M2 = {x &in; &#8469; | x &ge; 3}

M1 &cap; M2 = {[1,3]}

C(M1 &cap; ) = {x &in; &#8469; | x &lt; 1 _und_ x &gt; 3}

2)<br>
>|M = "bezüglich der Menge M"

M = {1,...,5}<br>
M1 = {1,2,3}, M2 = {2,3,4}<br>
M1 &cup; M2 = {1,2,3,4}<br>

C(M1 &cup; ) |M = {5}

CM1|M = {4,5}, CM2 = {1,5}

CM &cup; CM2 = {1,4,5}<br>
CM1 &cap; CM2 = {5}

## Zusammenfassung

Sei M eine endliche Menge M1,...,Mn sind Teilmengen von M, d.h. M1,...Mn &in; p(M).

**Es gelten:**

a) Kommutativgesetz <br>
M1 &cup; M2 = M2 &cup; m1;<br>
M1 &cap; M2 = M2 &cap; m1;

b) Assoziativgesetze <br>
M1 &cup; (M2 &cup; M3) = (M1 &cup; M2) &cup; M3
M1 &cap; (M2 &cap; M3) = (M1 &cap; M2) &cap; M3

c) Distributivgesetze<br>
M1 &cup; (M2 &cap; M3) = (M1 &cup; M2) &cap; (M1 &cup; M3)
M1 &cap; (M2 &cup; M3) = (M1 &cap; M2) &cup; (M1 &cap; M3)

d) Neutrale Elemente<br>
M1 &cup; &empty; = M1<br>
M1 &cap; M = M1

e) Komplementgesetze<br>
M1 &cup; CM1 = M<br>
M1 &cap; CM1 = &empty;

## Übungen

### 1

Sei A={b,c}, B={x}, C={x,z}

Man gebe die folgenden Mengen explizit an:


|  |     |
| :------------- | :------------- |
| A x B      | {(b,x), (c,x)}      |
| B x A      | {(x,b), (x,c)}     |
| A x &empty;      | &empty;       |
| A x B x &empty;      | &empty;      |
| A x (B &cup; C)      | {(b,x), (b,z), (c,x), (c,z)}       |
| A x (B &cap; C)      | A x B       |
| A x B x C      | {(b,x,x), (b,x,z), (c,x,x), (c,x,z)}      |
| A x C x B      | {(b,x,x), (b,z,x), (c,x,x), (c,z,x)}       |

### 2

M1 = {1,2}, M2 = {2,3} &harr; p(M1) = { &empty;, {1}, {2}, {1,2}}, p(M2) = { &empty; , {3}, {3}, {2,3}}

|  |     |
| :------------- | :------------- |
| p(M1) &cap; p(M2)      | {&empty;, {2}}      |
| p(m1 &cap; m2)     | {&empty;, {2}}      |
| A x &empty;      | {&empty;, {1}, {2}, {3}, {1,2}, {2,3}}       |
| A x B x &empty;      | {&empty;, {1}, {2}, ...}      |
| A x (B &cup; C)      |{(&empty;, &empty;), (&empty;, {2}), (&empty;, {3}), (&empty;, {2,3}), ({1}, &empty;), ...}      |
| A x (B &cap; C)      | Item Two       |
