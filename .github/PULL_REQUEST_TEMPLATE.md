<!--
Thanks for the change. The checklist below is the one from CONTRIBUTING; it is here so the
evidence arrives with the diff rather than after it.
-->

## What changed

<!-- One or two sentences. -->

## Evidence

<!--
If this changes a claim about the historical sources, cite the `file:line` witness in the primary
source or the conformance documentation. If it does not, say so — "commentary only, no fidelity
claim" is a complete answer.
-->

## Checklist

- [ ] Focused on one thing, branched from `main`.
- [ ] Tests added or updated for any behavior change.
- [ ] A fidelity change cites a `file:line` witness (or this is not a fidelity change).
- [ ] The repository's reproduce/test command is green — in `genesis`,
      `python scripts/reproduce.py --rust`.
- [ ] Does **not** add 2010-era consensus guardrails (overflow, script size, opcode limits). Their
      absence is the subject matter; operational hardening belongs in the running nodes instead.
- [ ] Preserves the framing: experimental artifact, not money, and no claim that any live chain
      "is" Bitcoin.
