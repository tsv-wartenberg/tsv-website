# tsv-website — TYPO3 Sitepackages

## Projektuebersicht

TYPO3-Sitepackages fuer die offizielle Vereinswebsite [tsv-wartenberg.de](https://www.tsv-wartenberg.de/). Enthaelt zwei Design-Varianten (v1 Original, v2 Modern) basierend auf TYPO3 v13 mit Bootstrap Package v15.

**Domain:** tsv-wartenberg.de
**Betreiber:** TSV Wartenberg e.V., 85456 Wartenberg, Bayern

## Tech-Stack

| Schicht | Technologie |
|---------|-------------|
| CMS | TYPO3 v13 |
| Theme-Basis | Bootstrap Package v15 (Bootstrap 5) |
| Sprache | PHP, TypoScript, Fluid Templates |
| Hosting | Strato (Shared Hosting) |

## Projektstruktur

```
tsv-website/
├── v1/   tsvwartenberg           (aktuelles/originales Design)
│   ├── Classes/
│   ├── Configuration/
│   ├── Resources/
│   ├── composer.json
│   └── ext_emconf.php
├── v2/   tsvwartenberg_modern    (modernisiertes Design)
└── README.md
```

## Umschalten zwischen Designs

Siehe `tsv-docs/legacy/ANLEITUNG-v2-UMSCHALTUNG.md` fuer die Anleitung zum Wechsel zwischen v1 und v2 auf dem Server.

## Entwicklungsprozess

Dieses Projekt folgt dem TSV-Standard-Workflow:

**Plan → Todo → Verify → Doku → Commit**

Details: [tsv-docs/prozesse/claude-code-workflow.md](https://github.com/tsv-wartenberg/tsv-docs/blob/main/prozesse/claude-code-workflow.md)

## Architektur-Kontext

Dieses Projekt ist Teil der TSV-Multi-App-Architektur:
- **tsv-website**: Vereinswebsite (dieses Repo)
- **tsv-hub**: Vereinsmanagement (FastAPI + React)
- **tsv-auth**: Zentrale Benutzerverwaltung — geplant
- **tsv-docs**: Zentrale Dokumentation

Zentrale Doku: [github.com/tsv-wartenberg/tsv-docs](https://github.com/tsv-wartenberg/tsv-docs)
