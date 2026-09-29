# DÉFI VÉLO intranet — translations

This repository holds the translation files (`.po`) for the
[swing/defivelo/intranet](https://gitlab.liip.ch/swing/defivelo/intranet)
project. It is mounted as a git submodule under `locale` in that project.

## Weblate integration

Translations are managed through Weblate:
<https://translate.liip.ch/projects/defivelo/intranet/>

Weblate reads from and pushes to the `master` branch of this repository.

Since 2026-09-28, the source language is **French**. The `fr/` catalog is
therefore the source and should contain no translations — only `de/`
(German) is translated.

## CI / submodule propagation

A push to the `master` branch triggers the CI, which updates the `locale`
submodule pointer on the `intranet` project (branch `main`) to the new
commit, so the translations flow back into the intranet application
automatically.

See `.gitlab-ci.yml` for the details.
