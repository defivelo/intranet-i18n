# AGENTS

See [README.md](README.md) for what this repository is, the Weblate
integration, and the CI / submodule propagation.

## Guidance for agents

- This repo contains only gettext translation catalogs (`de/`, `fr/`).
  Keep changes scoped to translations.
- French is the source language: `fr/` should contain no translations
  (every entry mirrors its `msgid`); only `de/` (German) is translated.
- Do not hand-edit source (`msgid`) strings — they are extracted from the
  parent `intranet` application.
- Prefer letting Weblate push translation changes rather than editing by
  hand, to avoid conflicting with Weblate's own commits.
- A push to `master` propagates to the intranet application via CI. Treat
  `master` changes as production-affecting, and make sure `.po` files still
  compile (`msgfmt --check`) before committing.
