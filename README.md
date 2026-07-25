# TSV Wartenberg – Sitepackage (TYPO3 v13)

Repo für das TYPO3-Sitepackage von [tsv-wartenberg.de](https://www.tsv-wartenberg.de/).

## Struktur

```
v2/   tsvwartenberg_modern    (produktives Sitepackage – live)
```

Das Sitepackage nutzt TYPO3 v13 mit Site Sets und Bootstrap Package v15
(Bootstrap 5). Templates, Navigation und Footer kommen aus dem
Bootstrap Package; `tsvwartenberg_modern` liefert das SCSS-Theme
(Vereinsfarben) und die Site-Konfiguration.

> Historie: Früher existierte parallel ein älteres Sitepackage `v1/`
> (`tsvwartenberg`, Bootstrap-3-Design). Es wurde entfernt, nachdem die
> Live-Seite dauerhaft auf `tsvwartenberg_modern` umgestellt wurde. Der
> alte Stand bleibt in der Git-Historie erhalten.

## Deployment

Das Sitepackage wird automatisch per GitHub Action deployed
(rsync per SSH nach `packages/tsvwartenberg_modern/`):

- Push auf `main` → typo313-prod
- Push auf `test` → typo313-test

Nach dem Deploy im TYPO3-Backend ggf. Cache leeren:

```bash
php vendor/bin/typo3 cache:flush
```
