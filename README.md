# OSEGChat

OSEGChat ist der lokale, quellenbasierte KI-Assistent für **Open Source Ecology Germany (OSEG)**. Er ergänzt die selbst betriebene **Chatwoot Community Edition** und beantwortet sachliche OSEG-Fragen anhand der [OSEG-Wissensdatenbank](https://wissen.oseg.rocks/).

Der Assistent erklärt freundlich in Du-Form und mit der Sachkenntnis eines gut informierten OSEG-Mitglieds. Er bleibt dabei als KI erkennbar und behauptet keine echte Mitgliedschaft oder persönlichen Erlebnisse.

## Inhalt dieses Repositorys

Dieses Repository dokumentiert die bestehende Integration. Es enthält derzeit die README und eine [Architekturbeschreibung](ARCHITECTURE.md). Anwendungscode, Installationspakete und produktive Konfiguration sind hier noch nicht enthalten; ein Klonen dieses Repositorys ergibt deshalb noch keine ausführbare Installation.

Dokumentationsstand: **20. September 2026**. Die Beschreibung basiert auf dem zu diesem Zeitpunkt geprüften Betriebsstand.

## Was der Chat kann

- Fragen zum Verein, zum Mitmachen, zu offener Hardware und dokumentierten OSEG-Projekten beantworten.
- Neue Fragen und neue Antwortformulierungen verarbeiten, ohne Fragen- oder Antworten-Whitelist und ohne manuelle Freigabe jeder Antwort.
- Passende Wissensquellen suchen und jede freigegebene Sachbehauptung mit Belegen verknüpfen.
- Kurze Anschlussfragen anhand eines begrenzten, datenschutzgeprüften Gesprächskontexts verstehen.
- Bei Unklarheit gezielt nachfragen. Fehlen ausreichende Belege, nennt der Bot diese Grenze und bleibt für weitere OSEG-Fragen erreichbar; technische Probleme können eine Team-Übergabe auslösen.
- Auf „Mensch“ eine Übergabe an das OSEG-Team auslösen.

Die bestehende Installation bindet den Bot in alle derzeit konfigurierten Chatwoot-Postfächer ein. Die Verarbeitung unterstützt Text; Anhänge werden nicht als Wissenseingabe ausgewertet.

## Wie eine Antwort entsteht

1. Chatwoot übermittelt eine eingehende Nachricht mit einem signierten Webhook.
2. Der Bot prüft Format, Themenbezug und Datenschutz und löst gegebenenfalls einen Gesprächsbezug auf.
3. Die Wissensplattform liefert passende, zur Modellverarbeitung freigegebene Quellen. Personenangaben werden aus den verwendeten Auszügen entfernt.
4. Das lokale Sprachmodell auf dem GX10 erzeugt eine Antwort mit Quellen-IDs.
5. Programmregeln, lokale Personennamenerkennung und ein separater KI-Prüfaufruf kontrollieren den Entwurf. Vor der Ausgabe wird der verwendete Quellenstand erneut geprüft.
6. Chatwoot erhält die freigegebene Antwort mit datenschutzgeprüften Quellenzusammenfassungen oder eine sichere Ausweichantwort beziehungsweise Team-Übergabe.

Die [Architekturbeschreibung](ARCHITECTURE.md) erläutert Komponenten, Datenfluss, Systemprompts, Speicherung und Fehlerbehandlung.

## Datenschutz und fachliche Grenzen

Der Bot soll keine personenbezogenen Angaben ausgeben, auch keine öffentlich auffindbaren Personennamen. Namenserkennung mit einem lokalen spaCy-Modell, feste Programmregeln und mehrere gezielte Modellaufrufe ergänzen sich. Projekt- und Organisationsnamen bleiben zulässig. Sachliche Ortsangaben zu Organisationen auf Stadt-, Regions- oder Landesebene werden von persönlichen Adressen unterschieden.

**Die Schutzschichten sind keine absolute Garantie gegen jede Datenpreisgabe oder sachliche Fehlaussage.** Generierung und semantische Prüfung laufen in getrennten Aufrufen desselben lokalen Sprachmodells und können gemeinsame Fehler machen. Historische Quellen belegen außerdem keine heutigen Angebote oder Verfügbarkeiten.

Der Ausgabeschutz ist keine vollständige Anonymisierung der Eingaben: Chatwoot speichert Nachrichten weiterhin. Die lokale Frageklassifizierung kann den normalisierten Originaltext erhalten. Kontaktfelder, private Notizen und fremde Gespräche werden nicht als Wissensquelle an das Modell übergeben. Bitte keine persönlichen Daten in den Chat schreiben.

## Betrieb und Kosten

Chatwoot, Bot, Wissensplattform und Modell werden auf vorhandener eigener Infrastruktur betrieben. Das lokale GX10-Modell wird über die vorhandene Tunnelverbindung angebunden. Für die KI-Antworten ist keine kostenpflichtige externe Modell-API vorgesehen; Server-, Energie- und Wartungsaufwand bleiben bestehen.

Betriebliche Voraussetzungen und Prüfungen bei Änderungen stehen in der [Architekturbeschreibung](ARCHITECTURE.md#betrieb-und-verifikation). Zugangsdaten, Tunnelkonfiguration, private Infrastrukturadressen und echte Gesprächsinhalte gehören nicht in dieses öffentliche Repository.

## Öffentliche Angebote

- [OSEG-Website](https://www.ose-germany.de/)
- [OSEG-Wissensdatenbank](https://wissen.oseg.rocks/)
- [OSEG-Blog](https://blog.opensourceecology.de/)
- [OSEG-Testchat](https://ose-germany.de/testchat.html)

## Rückmeldungen

Fehlerberichte sind über die [GitHub-Issues](https://github.com/AlexDorsten/OSEGChat/issues) möglich. Hilfreich sind eine nachgestellte Frage, das erwartete Verhalten und eine bereinigte Beschreibung des beobachteten Fehlers. Bitte keine echten Gesprächsverläufe, Namen, Kontaktangaben oder Zugangsdaten veröffentlichen.
