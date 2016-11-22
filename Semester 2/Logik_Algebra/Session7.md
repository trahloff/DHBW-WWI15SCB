<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Schaltalgebra](#schaltalgebra)
	- [Definition](#definition)
	- [Operationen](#operationen)
		- [AND](#and)
		- [OR](#or)
		- [Komplement](#komplement)
- [Boolsche Funktionen](#boolsche-funktionen)
	- [Definition](#definition)
	- [Einstellige Boolsche Funktionen](#einstellige-boolsche-funktionen)
	- [Zweistellige Boolsche Funktionen](#zweistellige-boolsche-funktionen)
		- [NAND](#nand)
		- [NOR](#nor)
		- [XOR](#xor)
		- [COIN](#coin)
		- [Implikation (f11)](#implikation-f11)
	- [Verknüpfungsbasen](#verknüpfungsbasen)
		- [Beweis](#beweis)
	- [Normalformen in der Schaltalgebra (sehr sehr unvollständig)](#normalformen-in-der-schaltalgebra-sehr-sehr-unvollständig)
	- [Disjunktionsterm](#disjunktionsterm)

<!-- /TOC -->

# Schaltalgebra

1938 SHANNON in Master Thesis gezeigt, dass **Schaltalgebra** Struktur einer Boolschen Algebra hat<br>&rArr; Festlegen: B, &and;, &or;, - und A1 - A4

Die Menge B, die der Schaltalgebra zugrunde liegt, ist die Menge der möglichen Schaltzustände B={0,1}

## Definition

Eine Variable a<sub>i</sub>, die genau zwei Werte 0,1 annehmen kann, nennt man **binäre Schaltvariable** oder **Boolsche Variable**

## Operationen

### AND

**&and;** B x B &rarr; b *Boolsches Produkkt*

| a   | b   | a &and; b   |
| :------------- | :------------- |:------------- |
| 0      | 0       |0      |
| 0      | 1      |0     |
| 1     | 0       |0      |
| 1      | 1       |1      |

&rArr;
  >**AND Funktion** (*Konjunktion*)

### OR

**&or;** B x B &rarr; **Boolsche Summe**

| a   | b   | a &or; b   |
| :------------- | :------------- |:------------- |
| 0      | 0       |0      |
| 0      | 1      |1     |
| 1     | 0       |1      |
| 1      | 1       |1      |

>**Boolsches Summe** = **ODER**

### Komplement

-: B &rarr; B

| a | &macrA;    |
| :------------- | :------------- |
| 0       | 1      |
| 1      | 0      |

wird realisiert durch **Ruhekontaktschaltung**

Müssen zeigen, dass die Axiome einer Boolschen Algebra gelten, d.h.

- Kommutativgesetze
- Komplementgesetze
- Distributivgesetze
- Neutrale Elemente

1. **Kommutativgesetze** <br> a &and; b = b &and; a <br> a &or; b = b &or; a
2. **Komplementgesetze** <br> a &and; &macra; = 0, a &or; &macra; = 1 <br> bei AND mit Komplement is immer  zu weil Komplement von a immer das Gegenteil macht, bei OR immer zu
3. **Distributivgesetze** <br> a &and; (b &or; c) = (a &and; b) &or; (a &and; c)<br> a &or; (b &and; c) = (a &or; b) &and; (a &or; c)<br> ob ich mir den Schalter "a" alleine vor die Schalter b,c packe oder zwei Schalter "a" an b,c ranknubbere is latte
4. **Neutrale Elemente** <br> &forall; a &in; B &exist; 1 &in; B : a &and; 1 = a <br> &forall; a &in; B &exist; 0 &in; B : a &or; 1 = a <br> "0" und "1" stehen für Schalter zu ind AND und Schalter offen in OR. Is halt dann egal &rArr; NEUTRAL

>**( B = { 0, 1 }, AND, OR, NOT )**

# Boolsche Funktionen

## Definition

Seien a1,a2,...an &in; B binäre Schaltvariablen

Eine Abbildung <br> f: B<sup>n</sup> &rarr; B

heißt n-stellige binäre Schaltfunktion oder n-stellige Boolsche Funktion

## Einstellige Boolsche Funktionen

f: B &rarr; B
Es gibt genau 4 einstellige Boolsche Funktionen

| a    | f1(a)    | f2(a)     | f3(a)  **NOT**   | f4(a)     |
| :------------- | :------------- |:------------- |:------------- |:------------- |
| 0     | 0     |0    |1      |1      |
| 1    | 0    |1     |0       |1     |

## Zweistellige Boolsche Funktionen


### NAND

| a b | NAND (a,b)  |
| :------------- | :------------- |
|0 0      | 1    |
|0 1     | 1   |
|1 0      | 1    |
|0 0      | 0    |

**NAND(a,b) = a &uarr; b**

### NOR

| a b | NOR (a,b)  |
| :------------- | :------------- |
|0 0      | 1    |
|0 1     | 0  |
|1 0      | 0    |
|0 0      | 0    |

**NOR(a,b) = a &darr; b**

### XOR

| a b | XOR (a,b)  |
| :------------- | :------------- |
|0 0      | 0    |
|0 1     | 1  |
|1 0      | 1    |
|0 0      | 0    |

**XOR(a,b) = a &oplus; b**

### COIN

| a b | COIN (a,b)  |
| :------------- | :------------- |
|0 0      | 1    |
|0 1     | 0  |
|1 0      | 0    |
|0 0      | 1    |

**COIN(a,b) = NOT XOR(a,b)**

### Implikation (f11)

| a b | Implikation (a,b)  |
| :------------- | :------------- |
|0 0      | 1    |
|0 1     | 1  |
|1 0      | 0    |
|0 0      | 1    |

**Implikation(a,b) = a &rarr; b**

## Verknüpfungsbasen

Ausgangspunkt bei der Konstruktion der Boolschen Algebra sind die beiden 2-stelligen Funktionen AND und OR und NOT (f8: a&and;b, f14: a&or;b, NOT)

&rArr; man kann alle 16 zweistelligen Funktionen durch &and;, &or;, - ausdrücken<br>&rarr; V = {AND, OR, NOT} eine **Verknüpfungsbasis**

Das bedeutet technisch, dass drei elementare Gatter (AND; OR; NOT) ausreichen, alle zweistellige Operationen zu realisieren.

V<sub>1</sub> = {NAND}, V<sub>2</sub> = {NOR} sind **Verknüpfungsbasen**

### Beweis

Jede der zweistelligen Funktionen durch &uarr; und &darr; darstellen.<br>Wir wissen V={&and;,&or,-} ist Verknüpfungsbasis.

- **NOT** = NOR(a,a) = a &darr; a
- **AND** = (a &darr; a) &darr; (b &darr; b)
- **OR** =  (a &darr; b) &darr; (a &darr; b)

## Normalformen in der Schaltalgebra (sehr sehr unvollständig)

Wenn man eine beliebige n-stellige Boolsche Funkrion vorliegen hat (zbsp:<br>f(a,b,c,d) = (a &and; b)&and; &macrc; &and; (d &and; &macra;))<br> dann kann man leicht die Schalttabelle dieser Funktion erstellen.

Oft interessiert aber der umgekehrte weg (von Tabelle zu Boolscher Funktion). Für Beispiel siehe Zettel vom 27.06.16

Zu der Tabelle vom Zettel:

| S1 | S2     |S3    | Lampe    |
| :------------- | :------------- |:------------- |:------------- |
| 0       |0    |0    |0    |
| 0       |0    |1    |1    |
| 0       |1    |0    |1    |
| 0       |1    |1    |0    |
| 1       |0    |0    |1    |
| 1       |0    |1    |0    |
| 1       |1    |0    |0    |
| 1       |1    |1    |1    |

Ein *Konjunktionsterm* einer n-stelligen Funktion ist eine AND-Verknüpfung.<br>

## Disjunktionsterm

Ein **Disjunktionsterm** fpr eine n-stellige Schaltfunktion ist eine OR-Verknüpfung, die alle Schaltvariablen in negierter oder nicht negierter Form enthählt.<br>Ein Disjunktionsterm, der den Wert 0 annimt heißt **Maxterm**. <br>Die AND-Verknüpfung von Maxtermen heißt **Konfunktive-Normalform KNF**

| a b | COIN (a,b)  |
| :------------- | :------------- |
|0 0      | 1    |
|0 1     | 0  | &larr;
|1 0      | 0    | &larr;
|0 0      | 1    |

f<sub>DNF</sub> (a,b) = (a&and;b)&or;(&macra; &and; &macrb;)

f<sub>KNF</sub> (a,b) = (a &or; &macrb;) &and; (&macra; &or; b)


Verwendungszweck KARTENNUMMER 16 Stellig kein text keine Leerzeichen
De18 2219 1405 9198 2000 03
