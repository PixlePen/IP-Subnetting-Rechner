# IP-Subnetting-Rechner
Ein simpler Web-Rechner um Subnetting zu betreiben 

# IP-Subnetting-Rechner (Interaktives Web-Tool)

Ein vielseitiger, browserbasierter Rechner zur Berechnung von Netzwerkparametern für **IPv4 und IPv6**. Dieses interaktive Tool wurde entwickelt, um die oft komplexen und fehleranfälligen Subnetting-Berechnungen zu vereinfachen und dient als wertvolle Unterstützung für Fachinformatiker, Studierende und alle, die sich mit Netzwerkplanung und -konfiguration beschäftigen.

## Motivation

Das sichere und effiziente Hantieren mit IP-Adressen und Subnetzen ist eine Kernkompetenz in der Netzwerktechnik. Manuelle Berechnungen sind zeitintensiv und anfällig für Fehler. Mein Ziel war es, ein **zuverlässiges, benutzerfreundliches und direkt im Browser nutzbares Web-Tool** zu entwickeln, das:

* **Komplexe Berechnungen vereinfacht:** Schnelle und präzise Ermittlung aller relevanten Netzwerkparameter.
* **Beide IP-Versionen unterstützt:** Umfassende Funktionalität für IPv4 und IPv6 gleichermaßen.
* **Lernunterstützung bietet:** Hilft, Subnetting-Konzepte zu visualisieren und eigene Berechnungen zu überprüfen.
* **Ohne Installation nutzbar ist:** Direkter Einsatz im Browser ohne Software-Download.

## Funktionen

* **Dual-Stack-Fähigkeit:** Umrechnung und Analyse für **IPv4** (mit Subnetzmaske oder CIDR) und **IPv6** (mit Präfixlänge).
* **Detaillierte Ergebnisse:** Anzeige von:
    * Netz-ID / Netzwerk-Präfix
    * Broadcast-Adresse (nur IPv4)
    * Erste und letzte nutzbare Host-IP
    * Anzahl nutzbarer Hosts / Adressen im Bereich
    * Subnetzmaske in Dezimal- und Binärform (IPv4)
    * CIDR-Notation
    * Standard-Subnetzgröße für IPv6 (/64)
* **Interaktive Oberfläche:** Benutzerfreundliche Eingabe und klare Darstellung der Ergebnisse.
* **Robuste Validierung:** Überprüfung der Eingaben auf Korrektheit und Gültigkeit.

## Technologien und Architektur

Der IP-Subnetting-Rechner ist als reines **Frontend-Projekt** entwickelt und nutzt moderne Webtechnologien:

* **HTML5:** Strukturierung des Formulars und der Ergebnisbereiche.
* **CSS3:** Gestaltung des Designs, das sich nahtlos in das moderne "Nolden.tech"-Theme einfügt. Besonderer Fokus auf Responsivität für die Nutzung auf verschiedenen Geräten.
* **JavaScript:** Die gesamte Berechnungslogik, Validierung und dynamische Anzeige der Ergebnisse ist in JavaScript implementiert.
    * **Bitweise Operationen:** Fundamentale Berechnungen für IPv4-Netzwerke.
    * **`BigInt`:** Nutzung des modernen `BigInt`-Datentyps für die präzise Verarbeitung der 128-Bit-IPv6-Adressen und deren Berechnungen.
    * **Formaterkennung:** Automatische Unterscheidung zwischen IPv4 und IPv6 basierend auf der Eingabe.

## Nutzung

Sie können den IP-Subnetting-Rechner direkt auf meiner Website ausprobieren:

➡️ **[Zum IP-Subnetting-Rechner auf Nolden.tech](https://www.nolden.tech/subnet_calculator.html)**

### Lokale Ausführung

1.  **Herunterladen:** Klonen Sie dieses Repository oder laden Sie die `subnet_calculator.html` Datei herunter.
2.  **Öffnen:** Öffnen Sie die `subnet_calculator.html` in Ihrem Webbrowser.

### Einbindung auf der eigenen Website (Embedding)

Sie können diesen Rechner ganz einfach in Ihre eigene Website integrieren, indem Sie einen `<iframe>` verwenden. Dies bindet das Tool direkt in Ihre Seite ein, ohne dass der Nutzer Ihre Website verlassen muss.

```html
<iframe 
    src="[https://www.nolden.tech/subnet_calculator.html](https://www.nolden.tech/subnet_calculator.html)" 
    width="800" 
    height="600" 
    frameborder="0" 
    allowfullscreen 
    title="IP-Subnetting-Rechner von Nolden.tech">
</iframe>
