# AGIT — language packs

This repository holds the **translation files for AGIT**, the Annoying Goods local-first
writing app. AGIT itself is closed source; what is published here is only the language data,
so that the community can fix and extend it.

## About AGIT

AGIT is an AI-assisted writing environment for long-form projects — novels, series, scripts,
essays and research. It keeps your text, notes and AI help in one place, with a scene-based
editor, a living story compendium, a project-aware workshop chat, a research binder, and
exports. It runs on your machine: your writing stays yours, and AI models are the ones you
choose and connect yourself.

- **Download and install:** <https://annoyinggoods.com/products/agit/> — AGIT is free to
  install and use. It is **coming soon to the Microsoft Store** as well.
- AGIT is currently a Windows desktop application. See the website for the latest release
  and requirements.

## What is in this repository

```
locales/
  en.yaml    English — the canonical file
  de.yaml    German
  es.yaml    Spanish
  ...        (20 languages in total)
```

Each file is a single YAML document with three parts:

```yaml
language_name: English          # the language's own name, shown in the app
ai_prompt: Always speak to the user using English.   # the line that tells the AI which language to answer in
translations:
  menu.view.toggle_sidebar: "Toggle Sidebar"          # dotted keys mapped to translated strings
  chat.cancelled: "Generation cancelled."
```

Some values contain `{placeholders}` — those must survive translation unchanged.

## Contributing

**English (`locales/en.yaml`) is the canonical file.** Every other language is translated
from it, and it defines the full set of keys. If a key is missing from a translated file, the
app falls back to the English string, so the key sets are expected to match.

Two things worth knowing before you start:

- **Fix a translation** — edit the value in the language's file. Keep the key, the
  `{placeholders}`, and the punctuation structure intact.
- **Add a language** — copy `en.yaml`, set `language_name` and `ai_prompt`, translate the
  values, and open a pull request. Add the file under `locales/`.
- **Machine-seeded files** — `sw.yaml` and `ha.yaml` carry a header noting they are
  machine-seeded and still need a native review. Native corrections are especially welcome.

Translations of the **program itself** (as opposed to its text) are outside the scope of this
licence; see the licence below. This repository is for the language data only.

## Licence

The AGIT application is free to use under the AG Free Use Licence, which includes ethical
use restrictions — see [`LICENSE`](LICENSE). The language files in this repository are
published so that the community can improve them; by contributing you agree that your
contributions may be distributed with AGIT under the same terms.
