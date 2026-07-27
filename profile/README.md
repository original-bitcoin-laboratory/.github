# Original Bitcoin Laboratory

**An evidence‑first, *executable* reconstruction and neutral conformance study of the earliest
Bitcoin** — the **November 2008 pre‑release** and the **January 2009 v0.1.0** genesis client —
built entirely from two hash‑verified archives, with **nothing disabled** and **no chain
privileged**.

Most of Bitcoin's origin story is prose. This lab makes the earliest code **run**, and lets
anyone re‑derive it from scratch.

## Repositories

- **[common](https://github.com/original-bitcoin-laboratory/common)** — the umbrella: what
  *"Bitcoin"* and *"a satoshi"* actually **are** (argued from the artifacts), the honest claims,
  the neutral conformance + attack‑surface matrices, and the release framing.
- **[genesis](https://github.com/original-bitcoin-laboratory/genesis)** — **OBL‑JAN09**: the full
  executable reconstruction of Bitcoin **v0.1.0** + derivatives (script engine, UTXO ledger,
  wallet, P2P, the origin‑distance tracker, and more).
- **[pre‑genesis](https://github.com/original-bitcoin-laboratory/pre-genesis)** — **OBL‑NOV08**:
  the Nov 2008 pre‑release witness + source inventory.

## Try it live

- **[→ The origin‑distance tracker](https://original-bitcoin-laboratory.github.io/genesis/)** — pick
  an origin, pick a moment in history, and see how far each Bitcoin version stood from it.
  *Distance is neutral; the origin is a choice.*
- **[→ Is it a Bitcoin?](https://original-bitcoin-laboratory.github.io/genesis/is-it-bitcoin.html)** — a
  reasoning compass: state a few facts about any object (a paper, a chain, a token, an amount) and see
  where it qualifies as *a* Bitcoin or *a* satoshi — and where the answer is convention, not fact.
- **[→ Join the live network](https://github.com/original-bitcoin-laboratory/genesis/blob/main/docs/ANNOUNCE.md)** —
  two always‑on anchors run both reconstructions: **JAN09‑X** at `seed.bitcoin-lab.org:18009` and
  **NOV08‑X** at `seed.bitcoin-lab.org:18008` (its own genesis + leading‑zero‑bits PoW). Clone the repo
  and `python -m netnode --chain jan09x --datadir ./data --connect seed.bitcoin-lab.org:18009` (or
  `--chain nov08x … :18008`) to sync and re‑validate a chain yourself. *Experimental. Not money.*

## What it found (honestly)

- The origin was already a **general financial‑predicate engine** — full Script, escrow,
  hash‑locks, a shipped marketplace — at inception; the "programmability came later" story is
  substantially wrong.
- Bitcoin's early maturation was **real safety engineering** (the origin shipped the consensus
  machinery but almost none of the *bounds*), mapped **neutrally, from the origin**.
- Two reconstructions — **NOV08‑X** and **JAN09‑X** — carry the complete original vocabulary.
  They are released as **candidates** (*"a* Bitcoin"), **never** as *"the* Bitcoin": which live
  network "is" Bitcoin has no factual answer — only convention.

## Boundaries

**Not money.** The experimental chains are stamped *"not money"* — no premine, no sale, no
promises. Authority is **only** the two hash‑verified archives + the whitepaper; everything else
is measured neutrally against them. Reproduce everything with
`python genesis/scripts/reproduce.py`.

MIT © 2026 Parth Mauria Saxena (laboratory tooling); the historical Bitcoin sources retain
Satoshi Nakamoto's 2009 MIT notice.
