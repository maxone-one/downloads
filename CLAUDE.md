# downloads

Die globalen Regeln gelten zusätzlich und gehen vor: `~/.claude/CLAUDE.md` und `~/.claude/rules/`. Hier steht nur, was an diesem Repo anders ist.

## Was dieses Repo ist

Der gemeinsame, öffentliche Downloadkanal aller maxone.one-Projekte auf GitHub: Installer, Pakete und Vorlagen liegen als Anhänge an Releases (veröffentlichte Fassungen bei GitHub), nicht im Git-Verzeichnis. Im Repo selbst liegt nur die `README.md`, es gibt keinen Quelltext und keinen Build. Der einzige Commit ist vom 25.08.2026, das Repo ist nach seiner `README.md` ein reiner Träger für Release-Anhänge und kein Projekt mit Entwicklung.

## Der Startablauf

In diesem Repo gibt es noch keine der Akten für Stand, Übergabe, `BUGS.md` oder `IRRTUEMER.md`.

Fehlt eine dieser Akten, wird sie beim nächsten Anfassen angelegt (Vorlage für die Übergabe: `~/Projekte/m1-standards/templates/HANDOFF.md`), und den Sinn jeder Datei pflegt die Datei selbst in ihrem Kopf. Max' Zettel `~/.claude/NOTIZEN.md` wird bei jedem Start gelesen.

## Eigenheiten und Grenzen

**Das Repo ist öffentlich, und alles darin ist für jeden lesbar.** Nie hinein: Quelltext, Schlüssel, Zugangsdaten, Kundendaten (so steht es in `README.md`). Auch diese `CLAUDE.md` ist öffentlich lesbar und enthält deshalb nur, was ohnehin in `README.md` steht. Dass `README.md` sagt, das Repo enthalte nichts außer ihr, stimmt seit dieser Datei nicht mehr wörtlich.

Jedes Release trägt sein Projekt im Tag nach dem Schema `<projekt>-v<version>`, zum Beispiel `beo-v0.1.0`. Der Titel nennt Projekt und Version im Klartext. Jeder Anhang trägt Projekt, Version und Plattform im Dateinamen, zum Beispiel `beo_0.1.0_amd64.deb`. Verlinkt wird nie über `releases/latest`, denn dieser Link zeigt auf das neueste Release irgendeines Projekts. Die Seiten fragen stattdessen die Release-Liste ab und nehmen den ersten Treffer ihres Projekts. Es gibt keinen Ordner `.github/workflows/`. Der Remote ist `maxone-one/downloads` auf GitHub.

## Wo was liegt

| Pfad | Inhalt |
|---|---|
| `README.md` | die gesamte Ordnung des Kanals: Zweck, Grenzen von GitHub, Benennung, Verlinkung |

## Rollen: Maker und Enabler (Max, 13.10.2026)

Max wörtlich: „Du bist Maker und Executor, ich bin Enabler.“ **Claude führt jeden Handgriff selbst aus** (aufladen, einrichten, anmelden, klicken, einspielen), Max ermöglicht ihn mit Freigabe, Zugang und Budget. Zurück an Max geht nur, was kein Werkzeug von Claude erreicht, mit dem Beleg des Versuchs. Freigabepflichten bleiben, die Ausführung gehört Claude. Ergänzt Punkt 2 und 3 der globalen CLAUDE.md.

## Fenster nie in den Vordergrund (Max, 26.10.2026)

Kein Fenster, kein Tab und kein Dialog wird in den Vordergrund geholt. Gearbeitet wird im Hintergrund, damit Max ungestört arbeiten kann. Globale Regel: `~/.claude/rules/fenster-nie-in-den-vordergrund.md`, CLAUDE.md Punkt 2i.

## Rollen: Maker, Executor, Approver (Max, 30.10.2026)

Du bist Maker und Executor. Max ist Approver. Claude führt jeden Handgriff selbst aus, Max gibt frei. Was nach außen wirkt (Senden, Veröffentlichen, Löschen, Kosten), bleibt an seine Freigabe gebunden. Globale Regel: Punkt 2 und 3 der globalen CLAUDE.md.
