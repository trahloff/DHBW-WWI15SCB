<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [RSA](#rsa)
	- [Keygenerierung](#keygenerierung)
	- [Encryption](#encryption)
	- [Decryption](#decryption)
	- [Beispiel](#beispiel)
- [Wie rechnet man Modulo ohne Taschenrechner?](#wie-rechnet-man-modulo-ohne-taschenrechner)
- [Boolsche Algebra](#boolsche-algebra)
	- [Definition](#definition)
	- [Beispiele](#beispiele)

<!-- /TOC -->

# RSA

## Keygenerierung

1. Man erzeugt zwei zufällige Primzahlen p,q<br>berechnet n = p x q (&#8469;<sub>n</sub>)
2. Berechne die die EULER-Totientenfunktion<br>&phi;(n) = (p-1)(q-1)
3. Wähle eine Zahl e, mit 1<e<&phi;(n), ggT(e, &phi;(n) | = 1)
4. Bestimme d mit 1<d<&phi;(n)<br> e x d &equiv; 1 mod &phi;(n)<br>(also: e und d sind multiplikativ Invers)

>K<sub>pub</sub> = (e, n)<br>K<sub>priv</sub> = (d, n)

## Encryption

> Klartext **M** wird geeignet als Zahl codiert, so dass 1<M<n <br> &rArr; C = M<sup>e</sup> mod n <br> K<sub>pub</sub> = (e, n)

## Decryption

> M = C<sup>d</sup> mod n

## Beispiel

**Keygenerierung:**
1. p = 17 <br> q = 23 <br> n = 17 x 23 = 391 (&#8484;<sub>391</sub>)
2. &phi;(391) = (17-1)(23-1) = 16 x 22 = 352
3.
4.  Wähle eine Zahl e, mit 1<e<&phi;(n), ggT(e, &phi;(n) | = 1)<br> e = 5 <br> **e = 5**
5. Berechne d mit 5 x d &equiv; 1 mod 352 <br> &rArr; ERWEITERTER EUKLID <br> **= 141** <br> d.h. : 5 x 141 = 705 = 704 +1 = 2 x 352 + 1<br> **also** 5 x 141 &equiv; 1 mod 352 <br> **K<sub>pub</sub> = (5, 391) <br> K<sub>priv</sub> = (141, 391)**

**Encryption**

1. M = 'a' &rarr; ASCII = 97
2. C = 97<sup>5</sup> mod 391 <br>= (97<sup>2</sup> x 97<sup>2</sup> x 97) mod 391<br>= [(97<sup>2</sup> mod 391) (97<sup>2</sup> mod 391) (97 mod 391)] mod 391 <br>  **= 20**

**Decryption**

1. M = 20<sup>141</sup> mod 391
2. 141 = 128 + 8 + 4 <br> = 20 <sup>128 + 8 + 4</sup> mod 391 <br> = (20<sup>128</sup> x 20<sup>8</sup> x 20<sup>4</sup> x 20) mod 391 <br> = [(20<sup>128</sup> mod 391) (20<sup>8</sup> mod 391)(20<sup>4</sup> mod 391) (20mod 391)] mod 391 <br> **= 97**

# Wie rechnet man Modulo ohne Taschenrechner?

1.  253 x 64 mod 391 &rarr; 16192 mod 391
2. 16192 / 391 = **41,411...**
3. Subtrahiere ganzzahligen rest -41
4. hier fehlt noch was :) **schickt PULLREQUESTS**

# Boolsche Algebra

## Definition

Eine Boolsche Algebra ist eine algebraische Struktur (B, &cup;, &cap;)

- B ist eine Menge mit |B| &ge; 2 (mehr als 2 Elemente)
- zwei zweistellige Operationen auf B:<br> &and;: B x B &rarr; B **Boolsches Produkt**<br>&or;: B x B &rarr; B **Boolsches Summe**
- eine einstellige operation auf B<br>-: B &rarr; B **Boolsches Komplement**<br> a &rarr; ā

Es gelten die folgenden Axiome

**1. Kommutativgesetze** <br> a &and; b = b &and; a <br> a &or; b = b &or; a
**2. Distributivgesetze**<br> a &or; (b &and; c) = (a &or; b) &and; (a &or; c)
**3. Neutrale Elemente** <br> &exist; 0 &in; B mit a &and; 0 = a &forall; a &in; B <br> &exist; 1 &in; B mit a &and; 1 = a &forall; a &in; B
**4. Komplementgesetze** <br> &forall; a &in; B &exist; ā &in; B mit a &or; ā = 1 <br> &forall; a &in; B &exist; ā &in; B mit a &and; ā = 0

Das 6-Tupel (B, &or;, &and;, -, 0, 1) heißt **Boolsche Algebra**

## Beispiele

Um konkrete Realisierungen von Boolschen Algebraen zu finden muss man B, &and;, &or;, ... konkret belegen.

**1.**<br> Sei M eine Menge; setze B = p(M) "Potenzmenge"

 &cup;:<br> p(M) x p(m) &rarr; p(M)<br>(A, B) &rarr; A &cup; B &cup; &harr; &or;

&cap;:<br> p(M) x p(m) &rarr; p(M)<br>(A, B) &rarr; A &cap; B &cap; &harr; &and;

-:<br> p(M) x p(m) &rarr; p(M)<br>A &rarr; &Amacr;

Neutrale Elemente:<br>&forall; A &in; p(M): A &cup; &empty; = A &empty; &in; p(M)<br>&forall; A &in; p(M): A &cap; M = A &empty; &in; p(M)

Komplementgesetze:<br> A &cup; &Amacr; = M<br> A &cap; &Amacr; = &empty; <br> &rArr; (p(M), &cup;, &cap;, -, &empty;, M)

**2.** *Abgefahren*<br> B = T<sub>30</sub> = {1,2,3,5,6,10,15,30} (*Teiler von 30*)

definiere:<br> a &and; = ggT(a,b)<br>a &or; b = kgV(a,b)<br>&amacr; = 30/a
