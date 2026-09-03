# Contributing

This is the default for every repository in the
[original-bitcoin-laboratory](https://github.com/original-bitcoin-laboratory) organization.
[`genesis`](https://github.com/original-bitcoin-laboratory/genesis) ships its own, with the build
and test commands specific to that repository; where one exists, it wins.

Thanks for your interest. This laboratory is an **experimental research and teaching artifact —
not money.** Contributions that improve fidelity, reproducibility, tests, or documentation are
welcome.

## The one rule that matters

**A claim about the historical sources must cite a `file:line` witness in a hash-verified archive.**

Everything in this laboratory is supposed to be re-derivable by a stranger. A change that asserts
something about what the November 2008 or January 2009 code does — in prose, in a matrix, in a
test name — needs to point at the line that shows it. A change that cannot cite one is a change to
our commentary, which is fine, but it must not read as a finding.

## Reporting issues and asking questions

Open an issue on the relevant repository. Because nothing of value is at stake, **disclosure can be
public**; see [`SECURITY.md`](SECURITY.md) for the narrow cases where it should not be.

For anything that looks like a correctness or reproducibility problem, include the exact command,
the chain (`nov08x` / `jan09x` / `bitcoin`), and enough detail to reproduce.

## What is deliberately out of scope

**Do not add the 2010-era consensus guardrails** — overflow checks, script size and opcode limits,
and the rest. Their absence in the historical clients is the subject matter, not a bug. The running
nodes add *operational* hardening instead, which is where defensive work belongs.

Fidelity fixes, tests, documentation, and tooling are all in scope.

## Pull requests

1. Branch from `main` and keep changes focused.
2. Add or update tests for any behavior change.
3. A **fidelity** change must cite a `file:line` witness in the primary source or the conformance
   documentation.
4. Run the repository's own reproduce/test command and make sure it stays green. In `genesis` that
   is `python scripts/reproduce.py --rust`.
5. Describe what changed and the evidence for it.

## Scope and framing

This project reconstructs the earliest Bitcoin as a runnable, verifiable artifact, and measures
other chains against it neutrally. It is not a currency, not a wallet for anything of value, and
not a production node. It does not claim that any live chain "is" Bitcoin — that question has no
factual answer, only convention — and contributions should preserve that framing.

## Attribution and licensing

By contributing you agree that your contribution is licensed under the repository's MIT license.
The historical Bitcoin sources retain Satoshi Nakamoto's 2009 MIT notice and are not relicensed.
