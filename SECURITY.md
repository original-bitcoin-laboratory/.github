# Security policy

This policy is the default for every repository in the
[original-bitcoin-laboratory](https://github.com/original-bitcoin-laboratory) organization. A
repository that ships its own `SECURITY.md` overrides it.

## What this software is

An **experimental research and teaching artifact — not money.** The chains this laboratory runs
carry no premine, no sale, and no promise of value, and they are stamped *"not money"* precisely so
that nothing is at stake in them. That framing is what makes the rest of this policy possible.

## The report that is worth the most

**"An artifact you published does not verify."**

Every release is signed and OpenTimestamps-anchored, and the instructions for checking that are
published beside it. If a signature, a digest, or a timestamp does not check out — or if a claim in
the documentation is not supported by the source line it cites — that is a defect. It is
corrected in the open rather than argued about, and the correction says what was wrong.

That is the highest-value report this project can receive, and it is not a conventional
vulnerability. It is treated as one here.

## What is *not* a vulnerability

**The historical clients are missing bounds on purpose, and that is the finding.** The November
2008 and January 2009 sources shipped the consensus machinery with almost none of the guardrails
added from 2010 onward — no overflow check on output values, no script size or opcode limits, no
`nLockTime` handling as later understood. Reconstructing them faithfully means reproducing those
absences.

Reports of the form *"the script engine has no opcode limit"* or *"outputs can overflow"* are
therefore **expected, documented, and out of scope as vulnerabilities.** They are the subject matter.
The neutral conformance and attack-surface matrices in
[`common`](https://github.com/original-bitcoin-laboratory/common) enumerate them deliberately, and
[`CONTRIBUTING`](CONTRIBUTING.md) asks contributors not to "fix" them.

What *is* in scope, in the derivatives and tooling that are ours rather than historical:

- a defect in the **operational** hardening added around the historical core (the running nodes,
  the P2P layer, the build and release tooling);
- anything that could harm a person who runs this software as documented — arbitrary file writes,
  code execution from untrusted input, credential or key exposure;
- a defect in the signing, timestamping, or verification path, since those are what the evidence
  claims rest on.

## How to report

**Public is fine, and usually better.** Because nothing of value is at stake, an issue on the
relevant repository is the normal route, and a public report can be checked by anyone:

<https://github.com/original-bitcoin-laboratory>

Please include the exact command, the chain (`nov08x` / `jan09x` / `bitcoin`), and enough detail to
reproduce.

**Report privately** only if you believe a report would put someone at risk before it can be fixed —
for example a defect that affects anyone already running a node, or one that touches key handling:

- Email `parthms.id@gmail.com`
- Or see <https://bitcoin-lab.org/.well-known/security.txt>

The maintainer's OpenPGP release-signing key is
`B128 526A F85A E4A8 F22B  949F B014 5F74 B78C F1DA`.

## What to expect

One maintainer, no service-level agreement, and no bounty. Reports are acknowledged when read and
fixed in the open. A report that changes a published claim is recorded as having done so,
with attribution if you want it and without if you do not.

## Supported versions

The latest release of each repository. Historical releases are kept and remain verifiable — their
signatures and timestamps continue to check — but they are not patched; a defect found in one is
fixed forward.
