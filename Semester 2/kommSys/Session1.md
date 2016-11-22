# Session 1

<!-- TOC depthFrom:2 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Warum Netzwerke?](#warum-netzwerke)
- [Topologien](#topologien)
- [Weltweise Normierungsverfahren](#weltweise-normierungsverfahren)
	- [ISO](#iso)
	- [ITU](#itu)
	- [RFC](#rfc)
- [OSI](#osi)
- [TCP/IP](#tcpip)
	- [Protokollhierarchien](#protokollhierarchien)
	- [Vgl OSI - TCP/IP](#vgl-osi-tcpip)

<!-- /TOC -->

## Warum Netzwerke?

- Nutzung gemeinsamer Ressourcen
- Flexibilität
- Zuverlässigkeit
- Austausch der Systeme

## Topologien

1. Stern
  - physikalisch:
    - Verbindung von jeder Node zu Zentralnode
  - logisch:
    - ausgezeichneter Knoten im Mittelpunkt des Sterns mit Kenntnis des gesamten Netzes

2. Ring
  - physikalisch:
    - Verbindung von jeder Node zu Nachbarnode
  - logisch:
    - nur Beziehung zwischen Partnern
    - logisches Netz nicht vorher definiert

3. Komplett/Mesh
  - physikalisch:
    - Verbindung von jeder Node zu jeder Node
  - logisch:
    - Kenntnis des gesamten Netzes in jeder Node vorhanden

4. Baum
  - physikalisch:
    - Kabel in definierter hierarchischer Struktur
  - logisch:
    - Kenntnis des gesamten Netzes in der definierten Baumstruktur

5. Bussystem
  - physikalisch:
    - Ein Kabel mit Stichleitungen zu jedem Knoten
  - logisch:
    - keine vorherige Definition des gesamten Netzes in den Knoten erforderlich
    - logisches Netz Stern, Ring oder Baum möglich

## Weltweise Normierungsverfahren

### ISO

- Hersteller machen proposal
- ISO richtet Gremium ein, vergibt Nummer
- nach 5 Jahren eventuell aufnehmen
- &rArr; EN &rArr; DIN

### ITU

- Alles was mit Telefonie zu tun hat
- Spricht nur Empfehlungen aus

### RFC

- Internet-Draft (I-D) online &rArr; RFC

## OSI

<h4><b>People Don't Need Those Stupid Packets Anyway <br><br>
Please Do Not Teach Students Pointless Acronyms </b> </h4>

Aufbau:
- Nachrichten des Senders werden mit **Header** (ICI) versehen
- Nächst tiefere Schicht betrachten Block aus **Nachricht \& Header** der darüberliegenden Schicht als neue Nachricht und bappt eigenen Header vorne ran

## TCP/IP

- Nahtlose Koppelung vorhandener \& neuer Netze
- Kann Zerstörung einzelner Netzwerkkomponenten aushalten
- Flexibel
- State of the Art

### Protokollhierarchien

1. **Host-an-Netz**: IMP's im ARPANET
<br>
3. **Internet-Schicht (IP)**:
  - Routing (Paket wird richtig zugestellt)
  - Vermeidung von Überlastung
  - Quasi Layer 3 in OSI
<br>
3. **Transport-Schicht (TCP/UDP)**:
  - zuverlässiger Aufbau von Datenstrom (TCP)
  - UDP schneller/unsicherer
  <br>
7. **Anwendungsschicht**:

### Vgl OSI - TCP/IP

OSI:
- Klare Trennung von Dienst, Schnittstelle, Protokoll
- Entwurf & Realisierung zeitlich getrennt
- Kapselung aller Schichten
- Sehr aufwendige Implementierung kann Einführung verhindern

TCP/IP:
- Trennung von Dienst, Schnittstelle, Protokoll erst nachträglich eingeführt
- Implementierung und Spezifikation nicht getrennt
- Schichten kennen Nachbarn, verlassen sich auf deren Implementierungsdetails
- Schnelle Implementierung

Ähnlichkeiten:
- Stapel unabhängiger Protokolle mit definierten Schnittstellen
- Funktionalität des Network(3) und Transport (4) Layers ähnlich
