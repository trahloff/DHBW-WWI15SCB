# Kongruenzrelationen

<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Kongruenzrelationen](#kongruenzrelationen)
	- [Definition](#definition)
	- [Beispiel](#beispiel)
	- [Beispiel2](#beispiel2)
	- [Add/Mult mod](#addmult-mod)
	- [Addition](#addition)
	- [Multiplikation](#multiplikation)
	- [Intermezzo: Wo geht es hin?](#intermezzo-wo-geht-es-hin)
		- [RSA](#rsa)
			- [Schlüsselgenerierung](#schlüsselgenerierung)
			- [Verschlüsselung](#verschlüsselung)
			- [Entschlüsselung](#entschlüsselung)
	- [Weitere Beispiele](#weitere-beispiele)
	- [Intermezzo: RAID - Systeme](#intermezzo-raid-systeme)
		- [Konfigurationen](#konfigurationen)

<!-- /TOC -->

Wir definieren mit &#8484; die folgende Relation:

>  &equiv; <sub>n</sub> &le; &#8484; * &#8484;

a &equiv; b mod n <=> a-b wird durch n (&in; IN) ohne Rest geteilt

D.h. zwei ganze Zahlen a, b &in; &#8484; stehen in Relation genau dann,
- wenn ihre Differenz ohne Rest durch n geteilt wird

**oder**
- wenn a, b durch n geteilt werden, haben a, b den gleichen Rest (ganzzahlig)

**oder**
- a = Vielfaches von k + r --- k &in; &#8484; <br> und b = Vielfaches von l + r --- l &in; &#8484;

**oder**
- es gibt eine ganze Zahl k &in; &#8484; mit a = b + k * n<br>Bsp: 5 &equiv; 3 mod 2<br>liest sich: "5 kongruent 3 mod 2"<br> Bsp: 178 &equiv; 17 &equiv; 3 mod 7<br>verbose: 178:7 = 25 * 7 Rest 3<br>Bsp: -4 &equiv; 12 &equiv; 0 mod 4<br>Bsp: 19 &equiv; 14 &equiv; 9 &equiv; 4 &equiv; -1 &equiv; -6 mod 5<br>Bsp: 83 = 11 * 7 + 6 <=> 83 &equiv; 6 mod 7

Allgemein:

>a &equiv; b mod n &hArr; a - b durch n ohne Rest geteilt wird<br>&rArr; -1 &equiv; 4 mod 5 &rarr; -1 -4 = -5

## Definition

Die **Kongruenzrelation**
>a &equiv; b mod n

ist eine Äquivalenzrelation

**_Beweis:_**
1. reflexiv
  - a &equiv; a mod n ok, denn a &equiv; a mod n &hArr; a - a ohne Rest durch n geteilt
2. symmetrisch
  - a &equiv; b mod n &rArr; b &equiv; a mod n <br>&hArr; a - b = k * n <br>&hArr; b - a = -k * n
3. transitiv
  - a &equiv; b mod n und b &equiv; c mod n<br>&rArr; a &equiv; c mod n
  - a &equiv; b mod n &hArr; a - b = k * n <br> b &equiv; c mod n &hArr; b - c = l * n<br>________________________________<br>= a &equiv; c mod n

Damit ist a &equiv; b mod n eine Äquivalenzrelation. Was sind die **Äquivalenzklassen**?<br>
> [x] = { y &in; M | (x, y) &in; R}

hier: **[x] = { y &in; &#8484; | x &equiv; y mod n }**

Die Äquivalenzklassen der Kongruenzrelation nennt man Restklassen (mod n)

## Beispiel

n = 5

[0] = { y &in; &#8484; | y &equiv; 0 mod 5 }<br>   =  { y &in; &#8484; | y = k * 5 + 0 k &in; &#8484; }<br>= {..., -15, -10, -5, 0, 5, 10, ...}

[1] = { y &in; &#8484; | y &equiv; 1 mod 5 }<br>   =  { y &in; &#8484; | y = k * 5 + 1 k &in; &#8484; }<br>= {..., -14, -9, -4, 1, 6, 11, ...}

[2] = { y &in; &#8484; | y &equiv; 2 mod 5 }<br>   =  { y &in; &#8484; | y = k * 5 + 2 k &in; &#8484; }<br>= {..., -13, -8, -3, 2, 7, 12, ...}

[3] = ...

[4] = ...

[5] == [0]

> **Demnach**: bei "mod n" gibt es n Äquivalenzklassen

[0] &cap; [1] = &empty; *heißt disjunkt*<br>
[0] &cap; [2] = &empty; <br>
paarweise disjunkt <br>
[0] &cup; [1] &cup; [2]  &cup; [3]  &cup; [4] = &#8484;

## Beispiel2

&#8484;<sub>5</sub> := { [0], [1], [2], [3], [4] }<br>
= Menge der Restklassen mod 5 *Restklassen = Äquivalenzklassen*<br>
= { 0, 1, 2, 3, 4 }

## Add/Mult mod

**Allgemein:**

&#8484;<sub>n</sub> = { 0, 1, ..., n - 1 } &hArr; Menge der Restklassen mod n

Man definiert nun auf &#8484;<sub>n</sub> zwei binäre Operationen:

**Addition mod n:<br>**
&oplus; : &#8484;<sub>n</sub> x &#8484;<sub>n</sub> &rarr; &#8484;<sub>n</sub><br>
a, b &rarr; a &#8853; b = ( a + b ) mod n

**Multiplikation mod n:<br>**
&otimes; : &#8484;<sub>n</sub> x &#8484;<sub>n</sub> &rarr; &#8484;<sub>n</sub><br>
a, b &rarr; a &otimes; b = ( a * b ) mod n

Betrachte R mit<br>
\+ : R x R &rarr; R a,b &rarr; a + b<br>
x : R x R &rarr; R a,b &rarr; a x b<br>

(R, +, x ) hat eine algebraische Struktur eines Körpers ("field"), wenn gilt:<br>

a) <br>
a + b = b + a<br>a x b = b x a

b) <br>
a x (b+c) = a x b + a x c

c) <br>
a + (b+c) = (a+b)+c<br>
a x (b x c) = (a x b) x c

d) <br>
Es existieren neutrale Elemente 0,1 mit<br>
a+0=a<br>a x 1 = a

e)<br>Es entstehen inverse Elemente:

&forall; a &in; R &exist; -a &in; R mit <br>
a + (-a) = 0

&forall; a &in; R &exist; a^-1 &in; R mit <br>
a x a^-1 = 1

---
## Addition

Welche algebraische Struktur hat &#8484;<sub>n</sub>, &oplus;, &otimes;?

&#8484;<sub>5</sub> Addition mod 5

|| 0    | 1    | 2   | 3    |4    |
|:----| :------------- | :------------- |
|**0**|0      | 1      | 2      | 3      | 4      |
|**1**| 1     | 2      | 3      | 4      | 0      |
|**2**| 2      | 3      | 4       | 0      | 1       |
|**3**|3     | 4      | 0      | 1      | 2      |
|**4**| 4   | 0     | 1      | 2       | 3      |

Aus Zeile 1: ( a + 0 ) mod 5 = a mod 5<br>
([0]) = 0 ist neutrales Elemente

0 &oplus; 0 = 0<br>
1 &oplus; 4 = 0<br>
2 &oplus; 3 = 0<br>
3 &oplus; 2 = 0<br>
4 &oplus; 1 = 0<br>

d.h. für jedes aus a &in; &#8484;<sub>5</sub> existiert ein (-a) &in; &#8484;<sub>5</sub> mit a &oplus; (-a) = 0

## Multiplikation

|| 0    | 1    | 2   | 3    |4    |
|:----| :------------- | :------------- |
|**0**|0      | 0      | 0      | 0     | 0     |
|**1**| 0    | 1      | 2     | 3     | 4      |
|**2**| 0     | 2      | 4     | 1      | 3       |
|**3**|0     | 3     | 1     | 4      | 2      |
|**4**| 0   | 4  | 3  |2    | 1    |

1 &otimes; a = a, d.h. [1]<br>
ist neutrales Element der Multiplikation mod 5

1 &otimes; 1 = 1<br>
2 &otimes; 2 = 1<br>
3 &otimes; 3 = 1<br>
4 &otimes; 4 = 1<br>

d.h. &forall; a &in; &#8484;<sub>5</sub> \ [0]<br> &exist; a^-1 &in; &#8484;<sub>5</sub> mit a &otimes; a ^-1 = 1

d.h. für jedes aus a &in; &#8484;<sub>5</sub> existiert ein (-a) &in; &#8484;<sub>5</sub> mit a &oplus; (-a) = 0

3 ist das multiplikative Inverse von 2 <br>
3 = 2^-1, "1/2"

&rArr; &#8484;<sub>5</sub>, &oplus;, &otimes; ist ein **endlicher Körper**

## Intermezzo: Wo geht es hin?

### RSA

#### Schlüsselgenerierung

Diese Art der Mathematik wird u.a. im RSA Algorithmus verwendet. Dieser lautet:<br>
1. Man wähle zwei große, zufällige Primzahlen (p,q) je 512, 1024, 2048, 4096 Bit<br> n = p * q
2. Man berechne die EULER Totientenfunktion<br>
> &phi; (n) = (p-1) * (q-1)

3. Wähle e, 1 < e < &phi;(n) und ggT(e, &phi;(n)) = 1
4. Berechne d mit <br> e * d &equiv; 1 mod &phi;(n)
5. K<sub>pub</sub> = (e,n)<br>K<sub>pub</sub> = (d,n)

#### Verschlüsselung

> C = M^e mod n

#### Entschlüsselung

> M = C^d mod n

## Weitere Beispiele

&#8484;<sub>2</sub> = {0,1}

(a+b) mod 2

> Merke: &oplus; = XOR

**Multiplikation:**<br> (a * b) mod 2 = AND

Auf &#8484;<sub>2</sub> gilt (a+b)^2 = a^2 + b^2

## Intermezzo: RAID - Systeme

### Konfigurationen

- Level 0: *Striping*
  - ich nehme 2+ Platten und verteil meine Daten in Blöcken auf beide, am Ende sieht es für's OS aus als wären alle Platten eine einzige
  - performance RAID, keine Ausfallsicherheit
  <br> <br>
- Level 1: *Mirroring*
    - Datenstrom parallel auf mehrere Platten abgespeichert
    - es wird immer nur 50% der möglichen Kapazität genutzt weil Rest für Backup &rArr; Ausfallsicherheit  <br> <br>
- Level 10: *Striping + Mirroring*
 <br><br>
- Level 2, 3, 4 werden in der Praxis nicht benutzt
<br><br>
- Level 2 benutzt komplexen Hamming-Code<br><br>
- Level 3 Striped die Daten bitweise(!)<br><br>
- Level 4 hat Flaschenhals<br><br>
- Level 5
  - Bei Ausfall kann der RAID-Verbund im laufenden Betrieb die verlorenen Datenblöcke von einer Ersatzplatte (Hot Spare) rekonstruiert
  - berechnet die Parität der verlorenen Datenblöcken
    <br><br>
