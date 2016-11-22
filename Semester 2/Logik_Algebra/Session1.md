# **Mengenlehre**
10.05.2016


<!-- TOC depthFrom:2 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [**Mengenlehre**](#mengenlehre)
	- [Überblick](#überblick)
	- [Allgemein](#allgemein)
		- [Bsp 1](#bsp-1)
		- [Definition](#definition)
		- [Bsp 2 _Keine Mengen im Sinne Canter_](#bsp-2-keine-mengen-im-sinne-canter)
	- [Notationen](#notationen)
	- [Irrationale Zahlen](#irrationale-zahlen)
	- [Antinomie von Russel](#antinomie-von-russel)
	- [Beziehungen zwischen Mengen](#beziehungen-zwischen-mengen)
		- [Definition](#definition)
		- [Bsp 1 _Teilmenge_](#bsp-1-teilmenge)
		- [Bsp 2 _Element/Teilmenge_](#bsp-2-elementteilmenge)
		- [Bsp 3 _Pascal_](#bsp-3-pascal)
	- [Anzahl von Teilmengen](#anzahl-von-teilmengen)
	- [Potenzmenge](#potenzmenge)
		- [Definition](#definition)
		- [Bsp 1 _placeholder_](#bsp-1-placeholder)
		- [Bsp 2 _Denksport_](#bsp-2-denksport)
		- [Übung 1](#übung-1)

<!-- /TOC -->


## Überblick

1. Mengenlehre
2. Relationen
  - Äquivalenzrelationen
3. Kongruenzrelationen
  - modulare Arithmetik
4. Boolesche Algebra
5. Schaltalgebra
6. Assagenlogik

---

## Allgemein

Der Begriff "Menge" bezeichnet eine Gesamtheit konkreter Dinge oder Personen.

### Bsp 1

- Menge der Einwohner von Mannheim
- Menge der Studenten in diesem Raum
- Menge der natürlichen Zahlen
- Menge aller Primzahlen
- Menge der reellen Zahlen
...


### Definition

_Georg Canter (1845 - 1918)_ <br>
Unter einer **Menge M** versteht man eine Zusammenfassung von bestimmten wohlunterschiedenen Objekten der Anschauung oder des Denkens - diese heißen Elemente der Menge **M** - zu einem Ganzen.

### Bsp 2 _Keine Mengen im Sinne Canter_

- eine Menge Butter
- eine Menge Energie

Es gibt endliche Mengen, d.h. Mengen mit einer endlichen Anzahl von Objekten, z.B. Studenten eines Kurses.

Unendliche Mengen haben unendlich viele Elemente, z.B. aller natürlichen Zahlen -> gewohnte Arithmetik geht nicht mehr

Menge der ganzen Zahlen, ist diese Menge "größer" als die Menge der natürlichen Zahlen?

_Canter: Die Menge der Ganzen Zahlen ist genauso mächtig wie die Menge der natürlichen Zahlen_ <br>
 --> Man kann eine umkehrbare Abbildung zwischen diesen beiden Mengen konstruieren.

<br>

| Ganze | Natürliche     |
| :------------- | :------------- |
| 1      | 1      |
| -1 | 2 |
| 2 | 3 |
| -2 | 4 |
| 3 | 5 |
| -3 | 6 |
| ... | ... |
> Abzählbar unendlich

<br>

Rationale Zahlen? ebenfalls abzählbar unendlich

Und reelle Zahlen? auch abzälbar im Intervall {0;1}

Canter (Diagonalisierungsverfahren):
Es gibt keine bijektive Abbildung von {0,1} in die natürlichen Zahlen.
>Reelle Zahlen bilden eine überabzählbare unendliche Menge

---

## Notationen

- Allgemein:
M = {1,4,7,1,4,3,6}
- Unendliche Mengen:
M = {1,4,7,1,4,3,6,...}
- Notation durch definierende Eigenschaft:
  - Allgemein
M = {x | x hat Eigenschaft Q}
  - Formaler:
M = {x | x ∈ &#8469; und x/2 ∈ &#8469;}
- &#8469; = {0,1,2,3,...}
- Z = {...,-2,-1,0,1,2,...}
- Zn = {0,1,...,n-1}
- Menge der Brüche: Q = {p/q | p ∈ Z, q ∈ Z, q != 0}

---

## Irrationale Zahlen

Es gibt Zahlen wie wurzel aus 2, die nicht als Bruch dargestellt werden können (**irrationale Zahlen**)
IR: Menge der reellen Zahlen.
IR ist algebraisch nicht vollständig, d.h. es gibt algebraische Ausdrücke wie x^2+1=0, die in IR keine Lösung haben.

**--> Komplexe Zahlen _C_**

**--> Quaterionen _H_**

---

## Antinomie von Russel

Die von Cantor entwickelte Mengenlehre nennt man heute "naive Mengenlehre", Anfang 1900 hat man entdeckt, dass Cantors Mengenlehre in sich widersprüchlich ist --> **Bertraud RUSSEL**

>Der Barbier von Sevilla rasiert alle Männer von Sevilla, die sich nicht selbst rasieren. <br>
> Rasiert er sich selbst oder nicht?

Problem: Selbstbezug  in der Menge

Etwa 1920 wurde von Ernst **ZERMELO** und **von NEUMANN** u.a. eine konsistente Mengenlehre entwickelt.

Analog: _Lügner-Paradoxon_ in der Logik
>Dieser Satz ist falsch.

---

## Beziehungen zwischen Mengen

### Definition

>Zwei Mengen M1 und M2 heißen gleich, `M1 = M2`, genau dann, wenn jedes Element von M1 auch Element von M2 ist und umgekert.

Hierbei spielt die Reihenfolge der aufgelisteten Elemente keine Rolle, jedes mehrfach vorkommende Element wird nur einfach gezählt.

Eine Menge M1 heißt _Teilmenge_ von M2, wenn jedes Element von jedes Element von M1 auch Element von M2 ist (nicht notwendiger weise auch umgekert). Notation:
>M1 c_ M2

M1 heißt _echte Teilmenge_ von M2, falls M1 Teilemnge von m2 ist und es gibt ein x mit x € M2, x !€ M1.

### Bsp 1 _Teilmenge_
{1,2,3} c_ {1,2,3,4,5}

### Bsp 2 _Element/Teilmenge_

|  X             |   M                            | Beziehung            |  Erklärung    |
| :------------- | :-------------                 |:-------------        |:------------- |
| x = {1}        | M = { 1, 2, 3 }                | c_                   | weil jedes Element von x auch Element von M ist |
| x = {1}        | M = { {1},{2},{3} }            | x &isin; M           | die Elemente von M sind die einelementigen Zahlenmengen. X ist in M enthalten |
| x = {1}        | M = { 1, 2, {1,2} }            | c_                   | enthält x an Position 1 |
| x = {1,2}      | M = { 1, 2, {1,2} }            | beides               | Elemente an Pos 1/2 enthalten, Menge an Pos 3 |
| x = {1}        | M = { {1,2,3} }                | nichts               | Man geht nicht 2 Ebenen in Mengen hinein |
| x = 1          | M = { {1}, {2}, {3} }          | nichts               | ^ |


>'c_' === unterstrichenes c

### Bsp 3 _Pascal_

Sei M = { a, b, c }; Alle Teilmengen auflisten:
- { } _die leere menge ist Teilmenge jeder Menge_  1
- {a}, {b}, {c} 3
- { a, b }, { a, c }, { b, c } 3
- { a, b, c } 1 <br>
--> PascalDreieck

Es gilt: (n über k) gibt an, wie viele verschiedene k-elementige Teilmengen eine n-elementige Menge hat.

(n über k) = n!/k!(n-k)!

n! = n * (n-1) * (n-2) * ...
0! = 1

---

## Anzahl von Teilmengen

Wenn M n(<unendlich) Elemente hat, wieviele verschiedene Teilmengen gibt es?

Es gibt <br>
(n über 0 ) 0-elementige TM,<br>
(n über 1 ) 1-elementige TM,<br>
(n über 2 ) 2-elementige TM,<br>
(n über 3 ) 3-elementige TM,<br>
(n über 4 ) 4-elementige TM,<br>
...

Man muss jetzt alle Zeilen des PascalDreieck zusammenrechnen:<br>

1<br>
1 1<br>
1 2 1<br>
1 3 3 1<br>
...<br>

= 1 + 1+1 + 1+2+1 + 1+3+3+1 ...<br>

**_M_ mit _n_ Elementen: Anzahl der Teilmengen = 2^n**

---

## Potenzmenge

### Definition

Die Potenzmenge P(M) ist die Menge aller Teilmengen der Menge M.

### Bsp 1 _placeholder_

M = { 1, 2 }

P(M) = { &empty;, {1}, {2}, {1,2} }

P( P(M) ) = {&empty;, {&empty;}, {{1}}, {{2}}, {{1,2}} }

{&empty;, {1}}
{&empty;, {1}, {2}}
{&empty;, {1}, {2}, {{1,2}}}

### Bsp 2 _Denksport_

P(&empty;) = {&empty;}

P(P(&empty;)) = { &empty;, {&empty;} }

P(P(P(&empty;))) = { &empty;, {&empty;}, {{&empty;}}, {&empty;, {&empty;}} }

### Übung 1

Sei M1 = {1,2,3}, M2 = {1,2}

|Nummer| Aussage | Wahr/Falsch     |
| :------------- |:------------- |:------------- |
|1| M2 &isin; P(M1)       | Wahr      |
|2| M2 &isin; M1      | Falsch    |
|3| M1 &isin; P(M1)       | Wahr     |
|4| M1 c_ P(M1)     | Falsch       |
|5| M2 c_ P(M1)       | Falsch       |
|6| {{1},M2} c_ P(M1)      | Wahr      |
|7| &empty; &isin; P(M1)       | Wahr      |
|8|  &empty; c_ P(M1)       | Wahr     |
