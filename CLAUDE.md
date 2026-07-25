# tsv-website — TYPO3 Sitepackages

## Projektuebersicht

TYPO3-Sitepackage fuer die offizielle Vereinswebsite [tsv-wartenberg.de](https://www.tsv-wartenberg.de/). Basiert auf TYPO3 v13 mit Bootstrap Package v15 (Bootstrap 5). Produktiv/live ist das Sitepackage `tsvwartenberg_modern` unter `v2/`.

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
├── v2/   tsvwartenberg_modern    (produktives Sitepackage – live)
│   ├── Classes/
│   ├── Configuration/
│   │   └── Sets/SitePackage/     (Site-Set: config.yaml, settings.yaml, setup.typoscript)
│   ├── Resources/
│   │   ├── Private/              (Layouts, Partials, Templates, Language)
│   │   └── Public/Scss/Theme/    (Vereinsfarben, _navbar/_footer/_frame)
│   ├── composer.json
│   └── ext_emconf.php
├── .github/workflows/           (ProdCI/TestCI: rsync-Deploy)
├── CLAUDE.md
└── README.md
```

Das Sitepackage `tsvwartenberg_modern` hängt nur von `bootstrap-package/full`
ab. Templates/Navigation/Footer stammen aus dem Bootstrap Package; dieses
Repo liefert das SCSS-Theme und die Site-Konfiguration.

## Historie: früheres v1-Sitepackage

Früher lag parallel ein älteres Sitepackage `v1/` (`tsvwartenberg`,
Bootstrap-3-Design) im Repo. Es wurde entfernt, nachdem die Live-Seite
dauerhaft auf `tsvwartenberg_modern` umgestellt wurde. Der alte Stand
bleibt in der Git-Historie erhalten (`git log -- v1/`).

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
