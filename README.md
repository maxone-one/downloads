# downloads

**Hier liegen die fertigen Dateien aller Projekte von maxone.one zum Herunterladen.**
Installer, Pakete, Vorlagen, alles, was ein Mensch anklicken und speichern soll.

Der Quelltext der Projekte liegt nicht hier, sondern in ihren eigenen, privaten
Repositories. Dieses Repository ist öffentlich, damit die Downloads es sein können,
und es enthält deshalb genau nichts außer dieser Datei.

## Warum ein einziges Repository für alles

Ein Downloadkanal statt einer je Projekt. Nur diese eine Stelle muss öffentlich
sein, alle Projekte selbst bleiben privat. Und es gibt nur eine Ordnung zu pflegen
statt einer je Werkzeug.

## Wo die Dateien wirklich liegen

**Nicht im Verzeichnis, sondern in den Releases.** Das ist der ganze Sinn dieser
Ablage. Eine Datei im Git-Verzeichnis lädt jeder Klon in voller Größe mit, für immer
und in jeder je veröffentlichten Fassung. Ein Release-Anhang liegt daneben und
belastet das Repository nicht.

Die Grenzen, die dabei gelten
([GitHub-Doku](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases)):

| | Release-Anhang | Datei im Verzeichnis |
|---|---|---|
| je Datei | 2 GiB | 100 MiB, Warnung ab 50 MiB |
| Anzahl | 1000 je Release | unbegrenzt, aber alles wächst mit |
| Gesamtgröße | unbegrenzt | unter 1 GB empfohlen |
| Bandbreite | unbegrenzt | entfällt |

## Die Ordnung

**Jedes Release trägt sein Projekt im Tag.** Das Schema ist
`<projekt>-v<version>`, also `beo-v0.1.0` oder `vera-v1.2.0`. Ohne dieses Präfix
wäre in einem gemeinsamen Repository nicht erkennbar, wozu ein Release gehört.

**Der Titel des Releases nennt Projekt und Version im Klartext**, also `Beo 0.1.0`.
Er steht in der Übersicht und wird von Menschen gelesen.

**Jeder Anhang trägt Projekt, Version und Plattform im Dateinamen.** Nach dem
Herunterladen liegt er in einem fremden Ordner zwischen hundert anderen Dateien, und
`setup.exe` sagt dort nichts mehr:

```
beo_0.1.0_amd64.deb
beo_0.1.0_x64-setup.exe
beo_0.1.0_aarch64.dmg
```

## Wie ein Download verlinkt wird

**Nicht über `releases/latest`.** Der Dauerlink
`https://github.com/maxone-one/downloads/releases/latest/download/<datei>` zeigt auf
das zuletzt veröffentlichte Release **irgendeines** Projekts in diesem Repository.
Wer ihn heute für Beo einbaut, liefert nach dem nächsten Vera-Release einen 404 aus.
Das ist der eine Preis des gemeinsamen Repositories, und er ist bezahlbar, solange
ihn jeder kennt.

**Der richtige Weg ist die Abfrage nach dem Präfix.** Die Seite holt sich die
Release-Liste und nimmt den ersten Treffer ihres Projekts. Sie bekommt damit im
selben Zug die Versionsnummer und den Dateinamen, kann beides anzeigen und muss
nichts fest verdrahten:

```
https://api.github.com/repos/maxone-one/downloads/releases
```

Ein fest gesetzter Link auf ein bestimmtes Release bleibt dagegen für immer gültig
und ist überall dort richtig, wo eine bestimmte Fassung gemeint ist:

```
https://github.com/maxone-one/downloads/releases/download/beo-v0.1.0/beo_0.1.0_amd64.deb
```

## Was hier nie hineinkommt

Kein Quelltext, keine Schlüssel, keine Zugangsdaten, keine Kundendaten. Dieses
Repository ist öffentlich, und was hier liegt, ist gelesen.
