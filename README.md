# Open review: Saluca Labs research

Some of our work has not yet been checked by anyone outside Saluca Labs. When a *Check the Record* episode
covers one of our own papers and the only record is our own, we say so on air ("not yet independently
checked") and ask for a review here, in public.

**Reviewing is free, and anyone may do it.** Every review is published, whether it supports us or refutes us.

## Status

Maintained, and open for reviews. As of 2026-10-22 no review issues have been filed yet, and
[CORRECTIONS.md](CORRECTIONS.md) holds one entry (2026-10-03, from our own re-check).

## Install

Nothing to install: this repo is a process, an issue form and a corrections log. You need a GitHub account
to open an issue.

## Quickstart

1. Open [a new Review issue](https://github.com/saluca-labs/open-review/issues/new?template=review.yml).
2. Fill in the required fields: the paper's DOI or the episode, the claim, what you did, what you found, and
   your evidence.
3. Submit. The issue is public at once and carries the `review` label.

## Usage

### How to send a review

Open an issue with the **Review** template. Tell us:

1. **What you are reviewing:** the paper (its DOI) and, if it came from an episode, which one.
2. **The claim:** quote the exact sentence or result you are checking.
3. **What you did:** reproduced it, re-derived it, tested it, or read it against other work.
4. **What you found:** holds, does not hold, or partly. Include the evidence, and say what would change your mind.

A review that refutes a claim is the most useful kind. You do not need to be an academic, and you do not need
to be polite about the claim, only about the people.

### What we do with it

- Every review stays public here as an issue.
- If a review shows we were wrong, we correct the record: a new version of the paper (cited by its concept DOI,
  so the citation always resolves to the corrected one), an entry in [CORRECTIONS.md](CORRECTIONS.md), and,
  where an episode made the claim, a correction on the channel.
- We record what happened either way. A review we disagree with stays up, with our answer beside it.
- Money never affects a verdict or which reviews are published.

### What is in scope

Papers by Saluca Labs and the claims our episodes make about them. Reviews of other people's work belong to
them, not here.

## Architecture

There is no code. The pieces are:

- [`.github/ISSUE_TEMPLATE/review.yml`](.github/ISSUE_TEMPLATE/review.yml): the Review issue form. Required
  fields: work, claim, method, verdict (Holds, Does not hold, Partly holds, Cannot tell from the record),
  evidence. An optional checkbox discloses a financial relationship with Saluca Labs.
- [`.github/ISSUE_TEMPLATE/config.yml`](.github/ISSUE_TEMPLATE/config.yml): turns off blank issues, so every
  issue starts from the form.
- [`CORRECTIONS.md`](CORRECTIONS.md): every correction to our published work, newest first, each naming the
  work by concept DOI.

## Citation

No archived record for this repo. The works reviewed here are cited by concept DOI in
[CORRECTIONS.md](CORRECTIONS.md) and in each review issue.

## License

Functional Source License 1.1, Apache 2.0 future licence (FSL-1.1-Apache-2.0).
Source-available: each release converts to Apache 2.0 after two years. See
[`LICENSE`](LICENSE).

## Links

- [CORRECTIONS.md](CORRECTIONS.md): the corrections and review log
- [Saluca Labs on Zenodo](https://zenodo.org/search?q=%22Saluca%20Agentic%20AI%20Research%20Team%22): our
  published papers
- [saluca-labs/roadmap](https://github.com/saluca-labs/roadmap): product direction, decided in the open

Saluca Labs

_Last updated: 2026-10-23_
