# AGENTS.md

Instructions for AI coding agents working in this repository.

## Setup

Nothing to install. The repo is Markdown and two GitHub issue-template YAML files.

## Test

```sh
python -c "import yaml; [yaml.safe_load(open(f, encoding='utf-8')) for f in ('.github/ISSUE_TEMPLATE/review.yml', '.github/ISSUE_TEMPLATE/config.yml')]"
```

Passing: no output, exit 0. GitHub renders issue forms from the default branch only, so after a
change to `review.yml` is merged, open the new-issue page and check the form renders.

## Conventions

- `CORRECTIONS.md` is newest first, one table row per correction. Name the work by its Zenodo concept
  DOI, never a version DOI. Say what was claimed, what was found, the source, and what changed.
- A correction row is added only when the correction itself has been made (for example the new paper
  version is published). Do not add rows for planned corrections.
- When README.md or CORRECTIONS.md changes, regenerate `llms-full.txt` in the same PR: the `llms.txt`
  header, then `## README.md` and its text, then `## CORRECTIONS.md` and its text.
- No em-dashes.

## Do not

- Edit or delete an existing `CORRECTIONS.md` row. If one is wrong, add a new row that corrects it.
- Close, edit or hide a review issue, or answer one on Saluca Labs' behalf.
- Commit secrets, hostnames, internal paths or personal emails.

## Done means

The YAML parses, links in README.md and llms.txt resolve, and `llms-full.txt` matches the docs.
