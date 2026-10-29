# Folge 1: Open Notebook installieren

Die freie NotebookLM-Alternative mit Docker auf deinem Rechner

▶ Video: folgt

## Was du lernst

- Was Open Notebook ist und wofür du es nutzt
- Das Begleit-Repo mit der docker-compose.yml herunterladen
- Einen eigenen Schlüssel für gespeicherte API-Schlüssel erzeugen
- Open Notebook mit docker compose starten
- Die Oberfläche im Überblick

## Voraussetzungen

- Docker Desktop (Windows, Mac) oder Docker Engine mit Compose (Linux), siehe [n8n-Reihe, Folge 0](https://github.com/davidk85/n8n-tutorial/tree/main/folge-00-docker-start)
- Docker läuft (docker compose version zeigt eine Version an)

## Zum Kopieren

**Begleit-Repo herunterladen**

```bash
git clone https://github.com/davidk85/open-notebook-tutorial.git
```

**In den Ordner wechseln**

```bash
cd open-notebook-tutorial
```

**Begleit-Repo auf GitHub**

```
https://github.com/davidk85/open-notebook-tutorial
```

**Eigenen Schlüssel erzeugen (Mac und Linux)**

```
echo "OPEN_NOTEBOOK_ENCRYPTION_KEY=$(openssl rand -hex 32)" | tee .env
```

**Open Notebook starten**

```bash
docker compose up -d
```

**Open Notebook im Browser öffnen**

```
http://localhost:8502
```

**Open Notebook stoppen (die Daten bleiben erhalten)**

```bash
docker compose down
```

**Befehl aus dem Video**

```
ls
```

## Quellen und weiterführende Seiten

- [Open Notebook auf GitHub](https://github.com/lfnovo/open-notebook)
- [Open Notebook: Installation mit Docker Compose](https://github.com/lfnovo/open-notebook/blob/main/docs/1-INSTALLATION/docker-compose.md)
