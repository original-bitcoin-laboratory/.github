# `.github` — organization defaults

This repository holds no laboratory code. It carries the files GitHub serves as the
**default for every repository in
[original-bitcoin-laboratory](https://github.com/original-bitcoin-laboratory)** that does not
ship its own. If you arrived here from a policy link on another repository, this is why.

| File | What it says |
| --- | --- |
| [`SECURITY.md`](SECURITY.md) | The 2008/2009 clients are missing the guardrails added from 2010 onward **on purpose**. Reproducing those absences faithfully is the subject matter, not a vulnerability. What *is* in scope, and how to report it. |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | How to send a change, and the one rule that surprises people: do not "fix" the historical client. |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Contributor Covenant, plus what counts as evidence here. |
| [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE) | The two reports worth structuring: a reproduction that diverges, and a fidelity finding against a cited source line. |
| [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) | Asks a changed claim to arrive with its re-derivation. |
| [`profile/README.md`](profile/README.md) | The organization landing page. |

A repository that ships its own copy of any of these overrides the default. That is the intended
way to specialize: override the file, do not weaken the default.

## The laboratory itself

- **[`common`](https://github.com/original-bitcoin-laboratory/common)** — umbrella: roadmap and
  cross-edition conformance.
- **[`pre-genesis`](https://github.com/original-bitcoin-laboratory/pre-genesis)** — OBL-NOV08, the
  November 2008 pre-release, its constitution executed as the NOV08-X network.
- **[`genesis`](https://github.com/original-bitcoin-laboratory/genesis)** — OBL-JAN09, the January
  2009 released client.
- **[`bitcoin-whitepaper`](https://github.com/original-bitcoin-laboratory/bitcoin-whitepaper)** —
  which whitepaper is which: four known versions, two held, one lost.

Site: <https://bitcoin-lab.org> · Not money.
