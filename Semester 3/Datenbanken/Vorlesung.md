# SQL - NoSQL

- eher bei Banken
- skaliert gut vertikal
- stark bei Transaktionen, viel lesen, viel schreiben
- immer die gleichen daten

# NoSQL

- nicht standard daten
- unstrukturiert
- konsistent nicht so wichtig
- eher für social media etc


# Datawarehouse

- bei normalen datenbanken: man schaut sich einzelnen eintrag ein
- datawarehouse: man schaut sich alle in relation an

# Unterschied: Dateisystem/Datenbank

- DS speichert Bytes, Struktur is egal. "SPeicher keine Daten sondern Bytes -> keine Datenbanl". Integrität wird nicht gewahrt.


- Ein DBMS managed EINE DB. Darin können mehrere Namespaces sein. Im normalen Sprachgebrauch werden diese namespaces als "Datenbank" bezeichnet

- Isolation = welche Art von Abschottung möchte ich haben
- Bei verteilten Datenbanken Probleme:
  - Man hat ein Netzwerk dazwischen -->
    - Ausfall
    - Performance
    - Delay/Jitter

> In verteilten System kann nie ein konsistenter Zustand erreicht werden. Es ist nie sicher ob die letzte Nachricht angekommen ist

- CAP / ACID:
  - das C in ACID = keine Inkonsitenz auf einem Systemn, C in CAP meint globale Konsistenz auf allen Systemen
  - AP --> meist NoSQL



  # Entitäten für Beziehungen (Slide 25)

  - Erst wenn die Beziehung von Kunde/Artikel/Kaufhaus besteht existiert Kauf
