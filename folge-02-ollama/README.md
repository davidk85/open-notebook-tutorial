# Folge 2: KI lokal anbinden mit Ollama

Chat- und Embedding-Modell kostenlos auf deinem Rechner

▶ Video: folgt

## Was du lernst

- Wofür Open Notebook ein Chat- und ein Embedding-Modell braucht
- Modelle mit Ollama laden
- Ollama in Open Notebook verbinden und testen
- Modelle hinzufügen und als Standard zuweisen
- Wann ein Cloud-Anbieter wie OpenAI sinnvoll ist

## Voraussetzungen

- Ein laufendes Open Notebook: [Open Notebook starten](../README.md#open-notebook-starten)
- Ollama auf deinem Rechner (kostenlos auf ollama.com, für Mac, Windows und Linux)

## Datenschutz

Mit Ollama verarbeitet das Modell deine Quellen auf deinem Rechner, es geht nichts an einen KI-Anbieter. Verbindest du stattdessen OpenAI, Anthropic oder Google, bekommt der Anbieter die Inhalte deiner Quellen und Fragen, bei OpenAI in den USA. Für personenbezogene oder vertrauliche Daten brauchst du dann eine passende Grundlage (Auftragsverarbeitung, Drittlandübermittlung). Keine Rechtsberatung.

## Zum Kopieren

**Chat-Modell laden (3 GB)**

```bash
ollama pull ministral-3:3b
```

**Embedding-Modell laden (274 MB)**

```bash
ollama pull nomic-embed-text
```

**Geladene Modelle anzeigen**

```bash
ollama list
```

**Ollama herunterladen**

```
https://ollama.com/download
```

**Base URL für Ollama auf deinem Rechner (Open Notebook in Docker)**

```
http://host.docker.internal:11434
```

## Quellen und weiterführende Seiten

- [Ollama herunterladen](https://ollama.com/download)
- [Open Notebook: KI-Anbieter verbinden](https://github.com/lfnovo/open-notebook/blob/main/docs/4-AI-PROVIDERS/index.md)
