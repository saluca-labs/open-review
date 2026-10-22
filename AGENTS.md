# AGENTS.md

Instructions for AI coding agents working in this repository.

## What this is

A public review process for Saluca Labs papers: a GitHub issue form, and a log of every correction made.
There is no code.

## Read in this order

1. `README.md`: how a review is sent, what happens to it, what is in scope.
2. `CORRECTIONS.md`: the log, and the format a new row must follow.
3. `.github/ISSUE_TEMPLATE/review.yml`: the fields a reviewer fills.

## What you can and cannot see

- You can see the form, the config and the log.
- Reviews themselves are GitHub issues labelled `review`, not files. Read them with
  `gh issue list --repo saluca-labs/open-review --label review --state all`.
- The papers are on Zenodo, not here. Cite them by concept DOI.

## The only numbers to trust

- How many corrections exist: the table rows in `CORRECTIONS.md`.
- How many reviews exist: the `gh issue list` command above. Any count written in prose (including
  the README's Status line) is a snapshot with a date.

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
- When README.md, CORRECTIONS.md or AGENTS.md changes, regenerate `llms-full.txt` in the same PR: the `llms.txt`
  header, then README.md, CORRECTIONS.md and AGENTS.md, each under its path.
- No em-dashes.

## Do not

- Edit or delete an existing `CORRECTIONS.md` row. If one is wrong, add a new row that corrects it.
- Close, edit or hide a review issue, or answer one on Saluca Labs' behalf.
- Commit secrets, hostnames, internal paths or personal emails.

## Done means

The YAML parses, links in README.md and llms.txt resolve, and `llms-full.txt` matches the docs.
