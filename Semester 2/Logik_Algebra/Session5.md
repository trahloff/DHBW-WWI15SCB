<!-- TOC depthFrom:2 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Zusammenfassung](#zusammenfassung)
- [Coprim](#coprim)
	- [Definition:](#definition)
	- [Berechnung](#berechnung)
		- [Erweiterter EUKLIDISCHER Algorithmus](#erweiterter-euklidischer-algorithmus)
	- [Beispiel](#beispiel)
	- [Algorithmus](#algorithmus)
	- [Beispiel2](#beispiel2)
	- [Übung](#übung)
- [Euler - Totientenfunktion &phi;(n)](#euler-totientenfunktion-phin)
	- [Übung](#übung)
	- [Satz](#satz)

<!-- /TOC -->

## Zusammenfassung

Auf &#8484; Kongruenzrelation

a &equiv; b mod n &hArr; a - b wird durch n ohne Rest geteilt

&rarr; Äquivalenzrelation<br>
&rarr; es gibt Äquivalenzklassen, diese heißen **Restklassen**

&#8484;<sub>n</sub> = Menge der Restklasse mod n<br>={ 0, ..., n-1 }

Addition und Multiplikation mod n

a,b &rarr; (a+b) mod n<br>a,b &rarr; (axb) mod n

## Coprim

>Wenn n=p eine Primzahl ist, dann existiert in &#8484;<sub>p</sub> für jedes a &ne; 0 ein a<sup>-1</sup> mit a x a<sup>-1</sup> &equiv; 1 mod p.<br>Wenn n zusammengesetzte ist, dann existiert a<sup>-1</sup> genau dann, wenn ggT(a,n) = 1.

### Definition:

>Zwei Zahlen a,n heißen **coprim** &hArr; ggT(a,n) = 1

Beachte: a,n müssen keine Primzahlen sein, z.B. a = 8, n = 15

### Berechnung

Wie kann man das a<sup>-1</sup> mod n berechnen (für beliebiges n)?

1. Multiplikationstabelle erstellen<br>&rarr;ist nicht toll
2. Ein systemisches Verfahren, wie man a<sup>-1</sup> mod n berechnen kann<br>&rArr; **Erweiterter EUKLIDISCHER Algorithmus**

#### Erweiterter EUKLIDISCHER Algorithmus

### Beispiel

Wir berechnen das multiplikative Inverse von 510 mod 1001, d.h. <br> gesucht ist die Zahl d &in; &#8484;<sub>1001</sub> mit<br>510 x d &equiv; 1 mod 1001

Divisionsverfahren anwenden:

1. 1001 = 1 x 510 + 591<br>man drückt den Rest immer als Vielfaches von 1001 und 510 aus. <br> 491 = 1 x 1001 - 1 x 510
2. 510 = 1 x 491 + 19<br>19 = 510 - 1 x 491<br>19 = 510 - 1 x 1001 + 1x 510<br>19 = 2 x 510 - 1 x 1001
3. 491 = 25x 19 + 16<br>18 = 491 - 25 x 19<br>16 = 1 x 1001 - 51 x 510
4. 19 = 1 x 16 + 3 &rArr; 3 = 53 x510 - 27 x 1001
5. 16 = 5 x 3 + 1<br>1 = 16 - 5 x 3<br>1 = 26 x 1001 -51 x 510 - 5 x (53 x 510 - 27 x 1001)

also:

**1 = 161 x 1001 - 316 x 510**

oder

**-316 x 510 = -161 x 1001 + 1**

oder

**-316 x 510 &equiv; 1 mod 1001**

>a &equiv; b mod n<br>
>a = k x n + b



Damit:

d = -316 mod 1001

d &equiv; 685 mod 1001

Check:

685 x 510 = 349350 = 349 x 1001 + 1

### Algorithmus

Der folgende Algorithmus berechnet

- ggT(a,n) falls a,n nicht coprim sind
- a<sup>-1</sup> mod n falls a,n coprim sind

**Input:** <br>zwei natürliche Zahlen a,n, o.B.d.A. n>a<br>Hilfsvariablen:<br>X1, X2, X3<br>Y1, Y2, Y3<br>T1, T2, T3, Q

**Initialisierung:**<br>setze:<br>X1&larr;1 Y1 &larr; 0<br>X2&larr;0 Y1 &larr; 1<br>X3&larr;n Y3 &larr; a

**Iterationen:**<br>Falls Y3 = 0 STOP &rarr; Return X3 = ggT(a,n) &rArr; "kein Inverses"<br>Falls Y3 = 1 STOP &rarr; Return Y2 = a<sup>-1</sup> mod n <br> Q = &rfloor; X3/Y3 &lfloor;<br>T1 = X1 - QY1<br>T2 = X2 - QY2<br>T3 = X3 - QY3<br>&rArr;setze:<br>X1&larr;Y1 Y1 &larr; T1<br>X2&larr;Y2 Y1 &larr; T2<br>X3&larr;Y3 Y3 &larr; T3

### Beispiel2

a = 510; n = 1001

X1&larr;1 Y1 &larr; 0<br>X2&larr;0 Y1 &larr; 1<br>X3&larr;510 Y3 &larr; 1001

Y3 = 0? Y3 = 1? Nein

Q = &rfloor; X3/Y3 &lfloor; ? &rfloor; 1001/510 &lfloor; = 1

T1 = X1 - QY1 = 1<br>
T2 = X2 - QY2 = -1<br>
T3 = X3 - QY3 = 1001 - 510 = 491

X1&larr;0 Y1 &larr; 1<br>X2&larr;1 Y1 &larr; -1<br>X3&larr;510 Y3 &larr; 491

Y3 = 0? Y3 = 1? Nein

Q = &rfloor; X3/Y3 &lfloor; ? &rfloor; 510/491 &lfloor; = 1

T1 = X1 - QY1 = -1<br>
T2 = X2 - QY2 = 2<br>
T3 = X3 - QY3 = 510 - 491 = 19

X1&larr;1 Y1 &larr; -1<br>X2&larr;-1 Y1 &larr; 2<br>X3&larr;419 Y3 &larr; 19

Y3 = 0? Y3 = 1? Nein

Q = &rfloor; X3/Y3 &lfloor; ? &rfloor; 419/19 &lfloor; = 25

T1 = X1 - QY1 = 20<br>
T2 = X2 - QY2 = -1 -25 x 2 = -51<br>
T3 = X3 - QY3 = 510 - 491 = 16

X1&larr;-1 Y1 &larr; 26<br>X2&larr;2 Y1 &larr; -51<br>X3&larr;19 Y3 &larr; 16

Y3 = 0? Y3 = 1? Nein

Q = &rfloor; X3/Y3 &lfloor; ? &rfloor; 419/19 &lfloor; = 25

T1 = X1 - QY1 = -1 - 25 = -26 <br>
T2 = X2 - QY2 = 2 - (-51) = 53<br>
T3 = X3 - QY3 = 19 - 16 = 3

X1&larr;25 Y1 &larr; -26<br>X2&larr;-51 Y1 &larr; 53<br>X3&larr;16 Y3 &larr; 3

Q = &rfloor; 16/3 &lfloor; = 5

T1 = X1 - QY1 = 25 + 5 x 27 = 161 <br>
T2 = X2 - QY2 = -51 - 5 x 53 = -316<br>
T3 = X3 - QY3 = 16 - 15 = 1

X1&larr;-27 Y1 &larr; 161<br>X2&larr;53 Y1 &larr; -316<br>X3&larr;3 Y3 &larr; 1

&rArr; Y3 = 1 STOP return <br>Y2 = -316 = 510<sup>-1</sup> mod 1001

### Übung

Berechnen sie 19<sup>-1</sup> mod 251

Ergebnis:<br> Y2 = -66 &equiv; 185 mod 251

Test:<br> Es muss gelten 185 x 19 = k x 251 + 1<br>185 x 19 = 3514 + 1 = 14 x 251 + 1

## Euler - Totientenfunktion &phi;(n)

Diese Funktion gibt Anzahl der positiven Zahlen an, die kleiner sind als n und coprim zu n

n = 9, Teiler: 1,2,4,5,7,8 &rArr; &phi;(9)=6

>Bei n = Primzahl: &phi;(n) = n - 1

Insbesondere: Sind p,q Primzahlen und n=p x q<br>&phi;(n)=(p-q)(q-1)

Das heißt: von den n = p x q Zahlen 0, ..., n-1 haben (p-q) x (q-1) die Eigenschaft, dass ggT(a,n) = 1 gilt

### Übung

1. **2<sup>6</sup> mod 7**<br>= 2<sup>2</sup> x 2<sup>2</sup> x 2<sup>2</sup> mod 7<br>= 4 x 4 x 4 mod 7<br>=((16 mod 7) x (4 mod 7)) mod 7<br>= 2 x 4 = 8 mod 7 =1
2. **3<sup>10</sup> mod 11**<br>= 3<sup>3</sup> x 3<sup>3</sup> x 3<sup>3</sup> x 3 mod 11<br>= 5 x 5 x 5 x 3 mod 11<br>= 3 x 4 mod 11<br>= 1 mod 1 = 1
3. **4<sup>12</sup> mod 13**<br>= (16 x 16 x 16 x 16  x 16 x 16) mod 13<br>= 3x3x3x3x3x3<br>= 1

### Satz

"kleiner Satz von Fermat"

Falls p (in &phi;(p)) eine Primzahl ist, dann ist

>a<sup>p-a</sup> &equiv; 1 mod p

512 Bit
