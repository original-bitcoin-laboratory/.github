# Original Bitcoin Laboratory

**An evidence‑first, *executable* reconstruction and neutral conformance study of the earliest
Bitcoin** — the **November 2008 pre‑release** and the **January 2009 v0.1.0** genesis client —
built entirely from two hash‑verified archives, with **nothing disabled** and **no chain
privileged**.

Most of Bitcoin's origin story is prose. This lab makes the earliest code **run**, and lets
anyone re‑derive it from scratch.

A third chain lives here too — **[Bitcoin](https://bitcoin-lab.org/bitcoin)** — which runs that same
v0.1.0 client on a genesis of its own, with its own network and its own signed release. It is **not**
a reconstruction, and it does not interoperate with the two above.

## Repositories

- **[common](https://github.com/original-bitcoin-laboratory/common)** — the umbrella: what
  *"Bitcoin"* and *"a satoshi"* actually **are** (argued from the artifacts), the honest claims,
  the neutral conformance + attack‑surface matrices, and the release framing.
- **[genesis](https://github.com/original-bitcoin-laboratory/genesis)** — **OBL‑JAN09**: the full
  executable reconstruction of Bitcoin **v0.1.0** + derivatives (script engine, UTXO ledger,
  wallet, P2P, the origin‑distance tracker, and more) — and the home of the
  **Bitcoin** chain ([`derivatives/bitcoin/`](https://github.com/original-bitcoin-laboratory/genesis/tree/main/derivatives/bitcoin)),
  released as `Bitcoin-v0.1.1`.
- **[pre‑genesis](https://github.com/original-bitcoin-laboratory/pre-genesis)** — **OBL‑NOV08**:
  the Nov 2008 pre‑release witness + source inventory.

## Try it live

- **[→ bitcoin-lab.org](https://bitcoin-lab.org/)** — the lab's home: the **origin‑distance tracker**
  (how far each Bitcoin version stood from a chosen origin) and the **"Is it a Bitcoin?" compass**
  (where an object qualifies as *a* Bitcoin or *a* satoshi — and where the answer is convention, not
  fact). *Distance is neutral; the origin is a choice.*
- **[→ Join the live network](https://github.com/original-bitcoin-laboratory/genesis/blob/main/docs/ANNOUNCE.md)** —
  two always‑on anchors run both reconstructions: **JAN09‑X** at `seed.bitcoin-lab.org:18009` and
  **NOV08‑X** at `seed.bitcoin-lab.org:18008` (its own genesis + leading‑zero‑bits PoW). Clone the repo
  and `python -m netnode --chain jan09x --datadir ./data --connect seed.bitcoin-lab.org:18009` (or
  `--chain nov08x … :18008`) to sync and re‑validate a chain yourself. *Experimental. Not money.*
- **[→ Bitcoin](https://bitcoin-lab.org/bitcoin)** — a separate chain on its own seed:
  `python -m netnode --chain bitcoin --datadir ./data --connect bitcoin.bitcoin-lab.org:18026`.
  Genesis `00000000ad12f3ec…`, mined at the original difficulty‑1, its coinbase carrying the front
  page of the day it was mined. Block 1 is unmined and anyone may take it. *Not money.*

## What it found (honestly)

- The origin was already a **general financial‑predicate engine** — full Script, escrow,
  hash‑locks, a shipped marketplace — at inception; the "programmability came later" story is
  substantially wrong.
- Bitcoin's early maturation was **real safety engineering** (the origin shipped the consensus
  machinery but almost none of the *bounds*), mapped **neutrally, from the origin**.
- Two reconstructions — **NOV08‑X** and **JAN09‑X** — carry the complete original vocabulary.
  They are released as **candidates** (*"a* Bitcoin"), **never** as *"the* Bitcoin": which live
  network "is" Bitcoin has no factual answer — only convention.
- The original source still **builds and runs on a pinned period toolchain** — from `sha.cpp` and
  the Script interpreter up to a full `bitcoin.exe` linked from the unmodified code (i686 · OpenSSL
  1.0.2 · wxWidgets 2.8 · BDB · Boost) — settling the *reproducible period build* end to end
  ([build‑reconstruction](https://github.com/original-bitcoin-laboratory/genesis/tree/main/derivatives/build-reconstruction)).
- Two unmodified 2009 nodes, air‑gapped, **produced and relayed a block** — one mined block 1 at
  real difficulty 1 on the historical genesis and the other received and accepted it, both block
  files byte‑identical, verified from the raw bytes
  ([two‑node witness](https://github.com/original-bitcoin-laboratory/genesis/tree/main/r3-findings/2026-07-31-twonode-mined-block)).

## Boundaries

**Not money.** The experimental chains are stamped *"not money"* — no premine, no sale, no
promises. Authority is **only** the two hash‑verified archives + the whitepaper; everything else
is measured neutrally against them. Reproduce everything with
`python genesis/scripts/reproduce.py`.

MIT © 2026 [parthod0x](https://github.com/original-bitcoin-laboratory) (laboratory tooling); the
historical Bitcoin sources retain Satoshi Nakamoto's 2009 MIT notice.
