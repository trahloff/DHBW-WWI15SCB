<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [KV- Diagramme für unvollständige Boolsche Funktionen](#kv-diagramme-für-unvollständige-boolsche-funktionen)
	- [Beispiel](#beispiel)
- [Schaltnetze](#schaltnetze)
	- [Definition](#definition)
	- [Halbaddierer](#halbaddierer)

<!-- /TOC -->

# KV- Diagramme für unvollständige Boolsche Funktionen

## Beispiel

Konstruiere einen Schaltkreis füreinen Primzahlendetektor für Zahlen &l; 10

Für Zahlen &le; 10 benötigt man 4 Bits a, b, c, d

d > <br>
c > &rArr; f(a,b,c,d)<br>
b > <br>
a > <br>

**Tabelle siehe Blatt (21.07.16)**

f<sub>DNF</sub> (a,b,c,d) = (&amcr; &and; &bmacr; &and; c &and; &dmacr;) &or; (&amcr; &and; &bmacr; &and; c &and; d) &or; (&amcr; &and; b &and; &cmacr; &and; d) &or; (&amcr; &and; b &and; c &and; d)

**KV-Diagramm siehe Blatt (21.07.16)**

# Schaltnetze

## Definition

Ein Schaltnetz F ist die technische Realisierung einer Abbildung <br> f: B<sup>n</sup> &rarr; B<sup>m</sup>

(a<sub>1</sub>,a<sub>n</sub>) &rarr; f(a) = (f<sub>1</sub>(a<sub>1</sub>,a<sub>n</sub>), f<sub>n</sub>(a<sub>1</sub>,a<sub>n</sub>), f<sub>m</sub>(a<sub>1</sub>,a<sub>n</sub>))


## Halbaddierer

Ein Schaltnetz Schaltnetz, das die Addition zweier Bits ohne Berücksichtigung des Übertrags aus einer vorherigen Stelle realisiert.

| a  | b   | sum(a,b)       | cout(a,b)      |
| :------------- | :------------- |:-------------      |:-------------     |
| 0      | 0       |0      |0      |
| 0      | 1     |1      |0      |
| 1      | 0       |1    |0      |
| 1    | 1       |0      |1     |

sum<sub>DNF</sub> (a,b) = (&amacrb; &and; b) &or; (a &and; &bmacr;)<br> = a &oplus; b (XOR)

cout<sub>DNF</sub> (a,b) = a &and; b

**Gatterzeichnung siehe Zettel 4 12.07.16**

In der ALU sind 32 Bit Addierwerke realisiert, die Integer Variablen je 32 addieren

a = (a<sub>31</sub> a<sub>30</sub> ... a<sub>2</sub>a<sub>1</sub>a<sub>0</sub>)<br>
b = (b<sub>31</sub> b<sub>30</sub> ... b<sub>2</sub>b<sub>1</sub>b<sub>0</sub>)



Mengeoperationen

Potenzmenge

Relationen: Equivalenzklassen,...

Kongruenzrelation (modulo)

RSA
