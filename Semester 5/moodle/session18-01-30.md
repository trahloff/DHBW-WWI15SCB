# Session 30/01/18

- [Ausleihverwaltung](#ausleihverwaltung)
- [Wissenschaftliches Arbeiten](#wissenschaftliches-arbeiten)
- [Summerschool](#summerschool)
- [Bedarfsmeldung](#bedarfsmeldung)
- [Firmenzulassung](#firmenzulassung)
- [Externe Lehrbeauftragte](#externe-lehrbeauftragte)
- [Anmerkungen](#anmerkungen)

## Ausleihverwaltung

(Julius)

### Consumes

- Inventar
- Anfragen 
- Antrag
- Kontaktinfos SGL/LI (Notifications)

### Produces

- Zu-/Absage
- Notification
- Nachfragen (Zweck der Ausleihe)
- RessourcenStatus
- Schaden
- Leihschein (Scan)
- Mahnung
- AbgabeErinnerung

## Wissenschaftliches Arbeiten 

(Sven)

### Consumes

- Betreuerpool
- Kontaktinfos
- Fristverlängerungsantragsantwort (& Gegenvorschlag)
- Anmeldung

### Produces

- Modifikation Betreuerpool
- Modifikation Frist
- Fristverlängerungsantrag
- Notifications
  - Unvollständigkeit
  - Frist(-Verlängerung, etc)
- Abgabe/Thesis
  - Status
  - Bewertung
  - Verlängerung?

## Summerschool

(Jin)

### Consumes

- Anmeldung
- Mietwageninfos (DB?)

### Produces

- Moodle Kurs
- Notifications
  - Zu-/Absagen
  - A Shitton

## Bedarfsmeldung

(Philipp)

### Consumes

- Bedarfsanfragen
- Kapazität

### Produces

- Schätzungen
- Studiengerüste
- Anzahl Studenten
- Bedarf
- Rückmeldung an Unternehmen
- Protokoll (AK)

## Firmenzulassung

(Jin)

### Consumes

- Anfragen/Anträge
- Bestehende Unternehmensprofile

### Produces

- Neue Unternehmensprofile
- Anträge intern

## Externe Lehrbeauftragte

(Jasmin)

### Consumes

### Produces

## Gemeinsamkeiten

- ContactProvider, der MailAdressen etc vorhält
- NotificationService?
- Eine Art von Rollenmodell, dass einen manuellen Override erlaubt
- Gemeinsame Studenten-DB