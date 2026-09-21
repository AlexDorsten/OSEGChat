# Prüfpunkte zum kurzen Datenschutzentwurf

**Stand: 21. September 2026.** Redaktionelle Arbeitsnotizen für [Issue #2](https://github.com/AlexDorsten/OSEGChat/issues/2), kein Bestandteil der späteren Datenschutzerklärung. Der [Entwurf](datenschutzerklaerung-entwurf.md) ist bewusst kurz; fehlende Tatsachen werden durch Kürzen nicht entbehrlich. Die Website wurde nicht verändert.

## Vor Veröffentlichung klären

| Bezug | Erforderlicher Abgleich |
| --- | --- |
| [#2 – Datenschutzhinweise](https://github.com/AlexDorsten/OSEGChat/issues/2) | Verantwortlichen und Kontakt bestätigen; falls benannt, Kontakt des Datenschutzbeauftragten ergänzen. Alle offenen Stellen auflösen, Prüfdatum/Freigabe festhalten. Hinweise spätestens bei der Datenerhebung erreichbar machen; Links auch mobil prüfen. |
| [#3 – Speicherung](https://github.com/AlexDorsten/OSEGChat/issues/3) | Tatsächliche Daten und Fristen für Website, Kontakt, Chatwoot, Anhänge, Protokolle, offene Aufträge, Exporte und Backups festlegen. 15 Minuten betreffen nur den KI-Kontext. |
| [#4 – Browserspeicher](https://github.com/AlexDorsten/OSEGChat/issues/4) | Frisches Browserprofil vor und nach Chatöffnung/Nachricht untersuchen. Speicherzugriffe und § 25 TDDDG prüfen; nötigenfalls Einwilligung vor Zugriff umsetzen. Die bestehende Cookie-Richtlinie nennt `cookieconsent_status` mit einem Jahr; tatsächliches Verhalten noch prüfen. |
| [#5 – Rechtsgrundlagen](https://github.com/AlexDorsten/OSEGChat/issues/5) | Vorgeschlagene Rechtsgrundlagen samt Interessenabwägung bestätigen oder ersetzen. Versand einer Frage ist keine pauschale Einwilligung. Training, Qualitätssicherung, Telemetrie und andere Weiterverwendungen auch außerhalb des Antwortwegs prüfen. |
| [#6 – Betreiber](https://github.com/AlexDorsten/OSEGChat/issues/6) | Infrastrukturbetreiber, Dienstleister, Berechtigungen, Auftragsverarbeitung, Standorte und Drittlandzugriffe klären; auch E-Mail, Plausible, Modellserver, Tunnel und Sicherungen berücksichtigen. |
| [#7 – Rechte und Organisation](https://github.com/AlexDorsten/OSEGChat/issues/7) | Bearbeitung von Auskunft, Löschung, Widerspruch und gegebenenfalls Widerruf praktisch sicherstellen. |

**Weitere Website-Dienste:** Der Bestand enthält Registrierung, Newsletter einschließlich Öffnungsmessung, Kommentare/Abonnements, Bewerbungen sowie AddThis, Facebook, Twitter und YouTube. Vor einem vollständigen Ersatz feststellen, welche Funktionen tatsächlich existieren. Für aktive Verarbeitungen kurze konkrete Angaben ergänzen; nur nachweislich entfallene Verarbeitungen streichen. Normale Links sind von eingebetteten Diensten zu unterscheiden. Der gekürzte Entwurf ist deshalb noch keine vollständige Bestätigung des Website-Inventars.

**Plausible:** Das externe Skript von `plausible.io` ist auf Start-, Kontakt-, Cookie- und Testchat-Seite eingebunden. Datenbeschreibung im Entwurf beruht auf Anbieterangaben, nicht auf einem vollständigen Netzwerk-/Speicheraudit. Betreiber, Vertrag, Konfiguration, Aufbewahrung und rechtliche Einordnung noch bestätigen; „ohne Cookies“ ersetzt keine gesonderte Prüfung.

**KI:** Die Architektur dokumentiert Antwortberechnung, keinen Trainingsschritt. Erst nach betrieblicher Bestätigung kann der offene Satz ersetzt werden durch: „Wir verwenden deine Chatnachrichten nicht zum Trainieren oder Feinabstimmen von KI-Modellen und nicht als Wissensquelle für andere Gespräche.“ Andernfalls tatsächliche Zwecke und Bedingungen beschreiben. Öffentliche Quellenzusammenfassungen sind für sachliche Belege ohne Gesprächsinhalte vorgesehen und höchstens sieben Tage abrufbar; das ist keine bestätigte physische Löschfrist. Weitere Chatwoot-Postfachkanäle benötigen jeweils passende Informationen zum Erhebungszeitpunkt.

## Kurzer Hinweis am Chat

> Hier antwortet dir eine lokale KI zu OSEG. Deine Nachrichten werden in Chatwoot gespeichert und von der KI verarbeitet. Bitte gib keine persönlichen oder vertraulichen Daten ein. Mit „Mensch“ bittest du das Team um Übernahme. [Datenschutz](https://www.ose-germany.de/datenschutz/)

Erst zusammen mit der ergänzten, freigegebenen Erklärung verwenden. Der Link führt derzeit zum alten Bestand. Der Hinweis muss bereits beim Beginn der Datenerhebung zugänglich sein und ersetzt keine erforderliche Einwilligung.

## Quellen und Umfang der Prüfung

- [Veröffentlichte Datenschutzerklärung](https://www.ose-germany.de/datenschutz/), am 21.09.2026 vollständig als [Markdown-Bestand](datenschutzerklaerung-bestand-2026-09-21.md) extrahiert; keine neue rechtliche Bestätigung des Alttexts.
- [Architektur, festgehaltener Repository-Stand](https://github.com/AlexDorsten/OSEGChat/blob/b8cf4d4031743dcd0f1f639c9c421330e6a19f75/ARCHITECTURE.md), dokumentiert am 20.09.2026; keine erneute vollständige Serverprüfung.
- [Testchat](https://www.ose-germany.de/testchat.html), [Startseite](https://www.ose-germany.de/), [Kontakt](https://www.ose-germany.de/kontakt/) und [Cookie-Richtlinie](https://www.ose-germany.de/cookie-richtlinien/), HTML am 21.09.2026 gelesen.
- [Plausible: Data Policy](https://plausible.io/data-policy), Anbieterstand März 2026, abgerufen am 21.09.2026.
- [DSGVO](https://eur-lex.europa.eu/eli/reg/2016/679/oj/deu), insbesondere Art. 6, 12, 13, 15–22, 28 und 44 ff.; [§ 25 TDDDG](https://www.gesetze-im-internet.de/ttdsg/__25.html).
- [DSK: Orientierungshilfe KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf), 06.05.2024; [Berliner Datenschutzaufsicht: Beschwerde](https://www.datenschutz-berlin.de/buergerinnen-und-buerger/beschwerde).
