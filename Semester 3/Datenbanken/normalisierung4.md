# Schlüsselkandidaten

- **Vereinsbezeichnung** => {Gründungsjahr}
- **Vereinsbezeichnung, Spielernummer** => {Gründungsjahr, Spielername, Geburtsdatum}

> Primärschlüssel = {Vereinsbezeichnung, Spielernummer}

# 1NF

Nach seiner Ansicht nach wahrscheinlich vorhanden oder er will Namen -> Vor/NachN. haben. Nach **allen** anderen Quellen müsste man Geburtsdatum in GJahr, GMonat, GTag aufsplitten.<br>
Wenn man wie hier Name aufteilt wäre das machbar/richtig aber mit den Datensätzen völliger Schwachsinn weil damit Nachname funktional abhängig von Vorname wäre. Ungünstiger Datensatz.

Vereinsbezeichnung | Gründungsjahr | Spielernummer | SpielerVorName | SpielerNachName | Geburtsdatum
:----------------- | :------------ | :------------ | :------------- | :-------------- | :-----------
Muster             | 1921          | 2             | Karl           | Bein            | 1980-09-02
Fritz              | 1949          | 11            | Fritz          | Wurf            | 1980-09-02
Muster             | 1921          | 7             | Hans           | Mehner          | 1986-12-31
Muster             | 1921          | 11            | Kurt           | Bebel           | 1975-06-16
Hehner             | 1971          | 2             | Franz          | Bein            | 1971-11-30
Hehner             | 1971          | 3             | Hubertus       | Klein           | 1983-08-09
Hehner             | 1971          | 1             | Franz          | Bein            | 1982-06-26

# 2NF

Vereinsbezeichnung | Gründungsjahr
:----------------- | :------------
Muster             | 1921
Fritz              | 1949
Hehner             | 1971

> Primärschlüssel = {Vereinsbezeichnung}

<br>

Spielernummer | Vereinsbezeichnung | SpielerVorName | SpielerNachName | Geburtsdatum
:------------ | :----------------- | :------------- | :-------------- | :-----------
2             | Muster             | Karl           | Bein            | 1980-09-02
11            | Fritz              | Fritz          | Wurf            | 1980-09-02
7             | Muster             | Hans           | Mehner          | 1986-12-31
11            | Muster             | Kurt           | Bebel           | 1975-06-16
2             | Hehner             | Franz          | Bein            | 1971-11-30
3             | Hehner             | Hubertus       | Klein           | 1983-08-09
1             | Hehner             | Franz          | Bein            | 1982-06-26

> Primärschlüssel = {Spielernummer, Vereinsbezeichnung(FS)}

# 3NF

Siehe Kommentar 1NF. Abgesehen von den Namen. Gibt es keine funktionale Abhängigkeiten zwischen Nichtschlüssel-Attributen:<br>
Name &ne; {Datum}
