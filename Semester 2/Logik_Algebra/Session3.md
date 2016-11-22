24.05.2016

<!-- TOC depthFrom:2 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Relationen Allgemein](#relationen-allgemein)
	- [Definition](#definition)
	- [Beispiele](#beispiele)
- [Binäre Relationen](#binäre-relationen)
	- [Definition](#definition)
	- [Beispiele](#beispiele)
- [Symmetrische Relationen](#symmetrische-relationen)
	- [Definition](#definition)
	- [Beispiele](#beispiele)
		- [1.](#1)
		- [2.](#2)
		- [3.](#3)
- [Transitiv](#transitiv)
	- [Definition](#definition)
	- [Beispiel](#beispiel)
- [Äquivalenzrelation](#äquivalenzrelation)
	- [Definition](#definition)
	- [Übung](#übung)
	- [Beispiele](#beispiele)
- [Äquivalenzklasse und Partitionierung](#äquivalenzklasse-und-partitionierung)
	- [Beispiele](#beispiele)
	- [Übung](#übung)
	- [Frage](#frage)

<!-- /TOC -->

## Relationen Allgemein

### Definition

Eine **binäre Relation _R_** zwischen den Mengen M1 und M2 ist eine Teilmenge des Kartesischen Produkts M1 x M2:

> R &sube; M1 x M2

Falls (m,n) &in; R, dann schreibt man:

> m R n

und sagt: m steht in Relation zu n.<br>

Eine n-näre Relation R ist eine Teilmenge des Kartesischen Produkts

> R &sube; M<1< x M2 x ... x Mn
>
> = { (m1, m2, ..., mn) | mi &in; Mi, i=1, ..., n }

### Beispiele

1. R = { (x, y) &in; &#8477;^2 | x &sube; y }

2. Jede Funktion f: &#8477; &rarr; &#8477; ist eine Relation<br> - Merke: umgekehrt gilt das im Allgemeinen nicht, d.h. nicht jeder Graph im &#8477;^2 ist eine Funktion (mehrere y-Werte auf einen x-Wert == keine Funktion)<br>

3. Sei: <br>M<sub>1</sub> = Menge der Städte der Welt<br>M<sub>2</sub> = Menge der Länder der Welt<br>
  M<sub>1</sub> x M<sub>2</sub> = { (Mannheim, Nordkorea), (...) }<br>
  Betrachte:<br>
  R &sube; M1 x M2<br>
  = { (a, b) &in; M1 x M2 | a ist Hauptstadt von b }<br>
  = { (Berlin, Deutschland), (...) }<br>

4. Betrachte die Mengen:<br>
    M<sub>1</sub> = Menge der Kurse der DH<bR>
    M<sub>1</sub> = { WWI15SCB, WWI15SCA, ... }<br>
    M<sub>2</sub> = Menge der Kursräume an der DH<br>
    M<sub>2</sub> = { 041C, ..., 237C } <br>
    Betrachte die Relation:<br>
    > R &sube; M<sub>1</sub> M<sub>2</sub> = { (a, b) &in; M<sub>1</sub> x M<sub>2</sub> | Kurs a findet in Raum b statt }
    >
    > = { (WWI15SCB, 237B),... }

5. Im **allgemeinen** hat man also:<br>
    R &sube; M<sub>1</sub> x ... x M<sub>n</sub><br>
    = { (m<sub>11</sub>, m<sub>12</sub>, ..., m<sub>1n</sub>), ... ()}<br>
    In der Informatik:<br>

|   M<sub>1</sub>    |  M<sub>2</sub>    |
| :------------- | :------------- |
| m<sub>11</sub>    | m<sub>1n</sub>       |
| m<sub>k1</sub>      | m<sub>kn</sub>      |


    - eine n-näre Relation ist eine Tabelle mit n Spalten
    - die k n-Tupel der Relation sind die k Datensätze einer Tabelle
    - die n Mengen M1, ..., Mn sind die Felder/Attribute der Tabelle

## Binäre Relationen

Der begriff der Relation als Teilmenge einer kartesischen Produkts ist sehr weit gefasst. Er ist daher zweckmäßig gewisse Einschränkungen zu betrachten.

### Definition

1. Eine Relation *I* heißt **identische Relation** oder **Identität** auf M x M, falls<br>
 > I = { (x, x) | &forall; x &in; M }

2. Eine Relation R &sube; M x M heißt **reflexiv** genau dann, wenn I &sube; R ist

3. Eine Relation R &sube; M x M heißt **irreflexiv** genau dann, wenn gilt: (x, x) &notin; R für alle x &in; M

### Beispiele

1. R = { (x,y) &in; &#8477;^2 | x &sube; y } &rArr; ist **reflexiv**
2. M = { 1, 2, 3,4 }<br>
   R = { (1, 1), (1, 2), (2, 3), (3, 3), (4, 3) }<br>
   &rArr; **nicht reflexiv** weil (2,2) und (4,4) fehlt. &rarr; es fehlen also Paare. (siehe Adjazenz-Matrix)<br>
   **irreflexiv** wäre es wenn KEIN Zahlenpaar (1,1), ... da wäre

## Symmetrische Relationen

### Definition

Eine binäre Relation R &sube; M x M heißt **symmetrisch**, genau dann, wenn gilt:<br>
> (x, y) &in; R &rArr; (y, x) &in; R

### Beispiele

#### 1.

M = Menge aller Frauen

R &sube; M x M<br>
= { (a, b) &in; M x M | a ist Schwester von b }<br>
&rArr; **symmetrisch**

Beachte: Diese Eigenschaften hängen von M ab!

#### 2.

M = { 1, 2, 3, 4}<br>
R = { (1,1), (2,2), (2,3), (3,2) }<br>
**&rArr; symmetrisch**

#### 3.

M = { 1, 2, 3, 4}

R<sub>1</sub> = { (1,1), (2,2), (3,3), (4,4) } &rArr; reflexiv und symmetrisch<br>
R<sub>2</sub> = { (1,2), (2,1), (1,4), (4,1), (2,3) } &rArr; irreflexiv (beinah symmetrisch)<br>
R<sub>3</sub> = { (1,1), (1,2), (2,4), (1,4) } &rArr; **transitiv**<br>

## Transitiv

### Definition

Eine binäre Relation R &sube; M x M heißt **transitiv**, wenn gilt:<br>
> (x, y) & in; R und (y, z) &in; R &rArr; (x, z) &in; R

(1,2) &in; R, (2,4) &in; R &rarr; (1,4) &in; R

### Beispiel

M = Frauen <br>
R = {(a,b) &in; M x M | a ist Schwester von b } ist transitiv,<br>
(a,b) &in; R **und** (b,c) &in; R &rArr; (a,c) &in; R<br>
 Wenn a Schwester von b und Schwester von c &rArr; a ist auch Schwester von c

## Äquivalenzrelation

### Definition

Eine binäre Relation R &sube; M x M, heißt **Äquivalenzrelation** über M, genau dann, wenn R reflexiv, symmetrisch und transitiv ist.

### Übung

| Relation | Reflexivität, Symmetrie, Transivität     |
| :------------- | :------------- |
| R = { (a,b) &in; &#8484;^2 I a &ne; b}       | irreflexiv weil (a,a) &notin; R; symmetrisch; nicht transitiv weil 4 &ne; 1 und 1 &ne; 4 aber 4=4 &notin; R        |
| R = { (a,b) &in; &#8477;^2 I a + b = 1 }       | nicht reflexiv weil (1,1) &notin; R; symmetrisch weil (a,b) &in; R &rArr; (b,a) &in R; nicht transitiv weil **wenn symmetrisch dann muss es auch reflexiv sein um transitiv zu sein**   |
|  R = { (a,b) &in; &#8477;^2 I a^2 < b^2 }      | nicht reflexiv weil (3,3) &in; R ... 3^2 = 3^2; nicht symmetrisch weil (a,b) &in; R, (b,a) &notin; R;        |
|  R = { (a,b) &in; &#8477;^2 I a - b ist gerade }       | reflexiv weil (a,a) &in; R denn a-a=0, 0 ist gerade; symmetrisch weil a-b = gerade &rarr; b-a = gerade; transitiv? nicht mitbekommen        |
|  R = { &#8469; x &#8469;}      |       |

### Beispiele

Betrachte die Menge: M = Menge aller DH Studenten<br>
Definieren die Relation: R = { (x, y) &in; M x M | x ist im gleichen Kurs wie y}<br>
- reflexiv
- symmetrisch
- transitiv
**&rArr; Äquivalenzrelation**

## Äquivalenzklasse und Partitionierung

[Lode] = Äquivalenzklasse von Fr. Lode under der Relation R<br>
= { x &in; M | (x, Lode) &in; R}<br>
= WWI15SCB

[Gauglitz] = 15SCC

[Lode] ^ [Gauglitz] = &empty;

U [...] = M<br>
U = alle Äquivalenzklassen <br>
dies nennt man eine **Partitionierung** der Menge M

### Beispiele

M = {1, 2, 3, 4, 5, 6 }, R &sube; M x M

R = { (1,1), (2,2), (3,3), (4,4), (5,5), (6,6), (1,2), (2,1),...}

reflexiv? yes!<br>
symmetrisch? jo!<br>
transitiv? **FUCK YEAH !!**

&rArr; Äquivalenzrelation

Äquivalenzklassen:
- [1] = { x &in; M | (x, 1) &in; R} <br>
  = { 1, 2, 3, 4 } c M
- [2] = { 2, 1, 4 } = [1] = [4]
- [3] = {3,6} = [6]
- [5] = {5}

Damit definiert die obige Äquivalenzrelation folgende Äquivalenzklassen:

1. [1] = {1,2,4} &rarr;  [1] &cap; [3] = &empty;
2. [3] = {3,6}&rarr;  [1] &cap; [5] = &empty;
3. [5] = {5}&rarr;  [3] &cap; [5] = &empty;

** &rArr; jede Äquivalenzklasse führt zu einer Partitionierung**

### Übung

M = { 1, 2, 3, 4, 5, 6 }<br>
R = { (1,2), (2,1), (6,1), (3,4), (2,5), ...}

R ergänzen mitmöglichst wenig Elementen zu einer Äquivalenzrelation. Was sind die Klassen?

- Reflexivität
  - (1,1), (2,2), ..., (6,6)
- Symmetrie
  - (1,6), (4,3), (5,2)
- Transivität
  - wg. (6,1) &in; R, (1,2) &in; R &rArr; (6,2) und (2,6)
  - wg. (1,2) &in; R, (2,5) &in; R &rArr; (1,5) und (5,1)
  - wg. (6,2) &in; R, (2,5) &in; R &rArr; (6,5) und (5,6)

Klassen:
- [1] = { 1, 2, 5, 6 } &rArr; [1] &cup; [3] = M
- [2] = { 3, 4 } &rArr; [1] &cap; [3] = &empty;

> Eine Zahl darf **niemals** in mehr als einer Äquivalenzklasse auftauchen

### Frage

`Wie viele verschiedene Äquivalenzklassen können über M = { 1, ..., 6 } gebildet werden?`

Gleichwertig mit: Auf wieviele Art und Weisen kann man die Menge M = { 1, ..., 6 } im disjunkte, nicht leere Teilmengen zerlegen?

Antwort: **BELL-Zahlen**

Und dies ist n = 6 *203*
