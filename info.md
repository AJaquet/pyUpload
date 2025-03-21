## pyUpload - Sicherer Datei-Upload-Server für eine einfache und sichere Dateiübertragung

### Beschreibung

pyUpload ist eine leistungsstarke und dennoch einfache Lösung für den sicheren Datei-Upload über HTTPS. Dieses Programm eignet sich ideal, um Dateien schnell und unkompliziert von einem Smartphone oder einem anderen Gerät auf einen Computer zu übertragen. 

Anstatt zusätzliche Apps oder USB-Kabel zu nutzen, kann der Benutzer den Server starten, den automatisch generierten QR-Code mit dem Smartphone scannen und die Dateien direkt über die Weboberfläche hochladen. Der Computer speichert die hochgeladenen Dateien strukturiert in individuellen Verzeichnissen für jedes Gerät.

Zusätzlich erstellt pyUpload bei Bedarf automatisch ein selbstsigniertes SSL-Zertifikat, um eine verschlüsselte Verbindung sicherzustellen. Damit bleibt die Dateiübertragung geschützt und zuverlässig.

### Download
- **Portabel für Windows als .zip**
[download id="2323"]

> Aktuell ist der Download der portablen und Compilierten Version gesperrt da es von diversen Virenscannern als Bedrohung eingestuft wird. Bei Interesse ist das Programm aktuell nur auf Anfrage per eMail erhältlich. In Kürze erfolgt eine Veröffentlichung inklusive Code auf GitHub.


### Features – Die Vorteile von pyUpload auf einen Blick

- **Sichere Dateiübertragung per HTTPS** – Alle Daten werden verschlüsselt übertragen.
- **Automatische Erstellung eines selbstsignierten SSL-Zertifikats** – Keine zusätzliche Konfiguration notwendig.
- **Intuitive, webbasierte Benutzeroberfläche** – Einfach zu bedienen, keine Installation erforderlich.
- **Strukturierte Speicherung** – Dateien werden in client-spezifischen Verzeichnissen gespeichert.
- **Zentralisierte und client-spezifische Logging-Funktion** – Detaillierte Nachverfolgung aller Uploads.
- **Flexible Nutzung mit oder ohne GUI** – Start als Desktop-Anwendung oder reine Konsolen-Version möglich.
- **Schnelle Einrichtung** – Download, Entpacken und sofort loslegen!

### Installationsanleitung – So startest du pyUpload

Es gibt zwei Möglichkeiten, pyUpload zu nutzen: Entweder die manuelle Installation oder die Nutzung einer vorgefertigten, ausführbaren Version.

#### 1. Nutzung der fertigen Download-Version

Falls du keine Python-Installation benötigst, kannst du die vorgefertigte **ZIP-Version** von pyUpload herunterladen. Diese enthält bereits alle notwendigen Dateien und ist sofort einsatzbereit.

1. Lade die neueste **pyUpload.zip** von der offiziellen Website herunter.
2. Entpacke die ZIP-Datei in einen beliebigen Ordner.
3. Starte die enthaltene `pyUpload.exe`.
4. Falls die grafische Benutzeroberfläche nicht benötigt wird, kann die `pyUpload.exe` direkt in der Konsole mit `--nogui` gestartet werden:
   ```sh
   pyUpload.exe --nogui
   ```
5. Eine Übersicht aller verfügbaren Befehle und Optionen erhältst du mit:
   ```sh
   pyUpload.exe --help
   ```

#### 2. Manuelle Installation für Python-Nutzer

1. Stelle sicher, dass **Python 3** auf deinem System installiert ist.
2. Installiere alle benötigten Abhängigkeiten mit folgendem Befehl:
   ```sh
   pip install -r requirements.txt
   ```
3. Starte den Server mit:
   ```sh
   python pyUpload.py
   ```
4. Falls du keine grafische Benutzeroberfläche benötigst, kannst du den Server im Konsolenmodus starten:
   ```sh
   python pyUpload.py --nogui
   ```

### Zugriff auf die Weboberfläche

- Sobald der Server läuft, kann er über die lokale IP-Adresse aufgerufen werden:
  ```
  https://<server-ip>:4443
  ```
- Falls die GUI-Version gestartet wurde, erscheint ein **QR-Code**, der die Verbindungsadresse enthält. Dies ermöglicht eine einfache Verbindung mit Smartphones und Tablets.

### Datei-Upload leicht gemacht – So funktioniert es

1. Öffne die **Weboberfläche** im Browser.
2. Wähle die gewünschte **Datei aus** und klicke auf **„Hochladen“**.
3. Nach erfolgreichem Upload erscheint eine **Bestätigungsseite**, die den Abschluss der Übertragung bestätigt.

### SSL-Zertifikatswarnung in Browsern umgehen

Da pyUpload ein **selbstsigniertes SSL-Zertifikat** nutzt, kann es beim ersten Zugriff zu einer Warnung des Browsers kommen. Um die verschlüsselte Verbindung zu akzeptieren, gibt es zwei Möglichkeiten:

- In den meisten Browsern gibt es eine Option wie **„Erweitert“** oder **„Trotzdem fortfahren“**, um die Warnung zu übergehen.
- Alternativ kann das Zertifikat **manuell importiert und als vertrauenswürdig markiert** werden, um künftige Warnmeldungen zu vermeiden.

### Logging und Fehlerbehandlung – Transparenz und Kontrolle

- Alle **Uploads und Anfragen** werden in **zentralen sowie client-spezifischen Logdateien** gespeichert. Diese befinden sich im `logs/`-Verzeichnis.
- Falls während der Nutzung von pyUpload **Probleme auftreten**, bietet ein Blick in diese Logdateien wertvolle Hinweise zur Fehlerbehebung.

### Lizenz und Autor

- **Entwickelt von Adam Skotarczak (C) 2025**.

