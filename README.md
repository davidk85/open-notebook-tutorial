# Open-Notebook-Tutorials von ToolVibes

Begleitmaterial zur Reihe über [Open Notebook](https://github.com/lfnovo/open-notebook) auf dem YouTube-Kanal
**ToolVibes**: eine fertige docker-compose.yml, Beispieldateien und alle Befehle aus den Videos zum Kopieren.
Open Notebook ist eine selbst gehostete Alternative zu Googles NotebookLM. Jede Folge hat einen eigenen Ordner mit Anleitung.

## Folgen

| Folge | Thema | Level |
|---|---|---|

## Open Notebook starten

Du brauchst Docker Desktop (Windows, Mac) oder Docker Engine mit Compose (Linux). Dann im Ordner dieses Repos
einmal einen eigenen Schlüssel erzeugen und starten:

```bash
echo "OPEN_NOTEBOOK_ENCRYPTION_KEY=$(openssl rand -hex 32)" | tee .env
docker compose up -d
```

Danach http://localhost:8502 öffnen. Der Schlüssel in `.env` verschlüsselt die API-Schlüssel, die du in Open Notebook
speicherst: aufheben und nicht ändern, sonst sind sie nicht mehr lesbar. Unter Windows (PowerShell) legst du die
Datei `.env` mit einem Editor an und trägst dort `OPEN_NOTEBOOK_ENCRYPTION_KEY=` und eine lange, zufällige Zeichenfolge ein.

Die Videos nutzen Open Notebook 1.15.0. Eine andere Version stellst du in `docker-compose.yml` ein.
Stoppen mit `docker compose down`. Deine Notebooks bleiben im Ordner `open-notebook-data` erhalten.

## Hinweise

- Open Notebook ist nur auf deinem Rechner erreichbar (Ports an 127.0.0.1 gebunden) und hat ohne Passwort keinen Login.
  Bevor andere Geräte darauf zugreifen, ein Passwort setzen (Folge 7).
- Mit Ollama bleiben Quellen und Fragen auf deinem Rechner. Cloud-Anbieter wie OpenAI bekommen die Inhalte deiner Quellen.
- Beispieldaten in den Videos sind erfunden, zum Beispiel die „Kaffeerösterei Morgenrot“.
