# Folge 7: Passwort, Backup und Update

Open Notebook absichern, sichern und aktuell halten

▶ Video: folgt

## Was du lernst

- Ein Passwort für Open Notebook setzen
- Ein vollständiges Backup mit tar anlegen
- Prüfen, ob es eine neue Version gibt, und aktualisieren
- Ein Backup wieder einspielen

## Voraussetzungen

- Ein laufendes Open Notebook: [Open Notebook starten](../README.md#open-notebook-starten)
- Open Notebook mit der docker-compose.yml aus dem Begleit-Repo (Folge 1)
- Unter Windows: die Befehle in der WSL-Shell oder Git Bash ausführen, tar gibt es dort

## Datenschutz

Das Backup enthält alles: deine Quellen und Notizen, die gespeicherten API-Schlüssel und die Datei .env mit Schlüssel und Passwort. Bewahre es deshalb verschlüsselt auf, nicht unverschlüsselt in einer Cloud, und lösche alte Backups nach einer festen Frist. Keine Rechtsberatung.

## Zum Kopieren

**Passwort setzen (eigenes Passwort nehmen)**

```
echo "OPEN_NOTEBOOK_PASSWORD=Kaffee-Demo-2026" | tee -a .env
```

**Änderung übernehmen**

```bash
docker compose up -d
```

**Open Notebook anhalten**

```bash
docker compose stop
```

**Backup anlegen**

```
tar czf open-notebook-backup.tar.gz open-notebook-data .env
```

**Wieder starten**

```bash
docker compose start
```

**Befehl aus dem Video**

```
ls -lh open-notebook-backup.tar.gz
```

**Neue Version laden**

```bash
docker compose pull
```

**Neue Version festlegen (Beispiel, Nummer anpassen)**

```
echo "OPEN_NOTEBOOK_VERSION=1.16.0" | tee -a .env
```

**Open Notebook anhalten**

```bash
docker compose down
```

**Datenordner löschen (nur mit Backup!)**

```
rm -rf open-notebook-data
```

**Backup auspacken**

```
tar xzf open-notebook-backup.tar.gz
```

## Quellen und weiterführende Seiten

- [Open Notebook: Docker Compose (Backup, Update)](https://github.com/lfnovo/open-notebook/blob/main/docs/1-INSTALLATION/docker-compose.md)
- [Open Notebook: Releases](https://github.com/lfnovo/open-notebook/releases)
