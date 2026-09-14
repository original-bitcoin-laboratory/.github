# Original Bitcoin Laboratory

> **Scope.** Experimental laboratory research, in progress and expected to change. It reports what
> published, re-runnable methods find in public material — statistical and machine-verifiable
> findings, graded by their evidence — and draws no conclusion beyond them. Not money, not advice,
> no warranty. Details in [RIGHTS.md](https://github.com/original-bitcoin-laboratory/genesis/blob/main/RIGHTS.md).

**An evidence‑first, *executable* reconstruction and neutral conformance study of the earliest
Bitcoin** — the **November 2008 pre‑release** and the **January 2009 released client** —
built entirely from two hash‑verified archives, with **nothing disabled** and **no chain
privileged**.

Most of Bitcoin's origin story is prose. This lab makes the earliest code **run**, and lets
anyone re‑derive it from scratch.

A third chain lives here too — **[Bitcoin (2026)](https://bitcoin-lab.org/bitcoin)** — which runs that same
January 2009 client on a genesis of its own, with its own network and its own signed release. It is
**not** a reconstruction, and it does not interoperate with the two above. It is a 2026 experimental
chain — not the Bitcoin of 2009 and not money — whose author "Satoshi Nakamoto" is an AI agent built
in 2026: a program, not a person, and not the historical Satoshi. It is the one with a live network and a released client — it runs the January 2009 client, rebuilt
from the unmodified source; block 0 was mined by the agent's own miner and every block from height 1
onward by a released client, ten of them (the first at 221–222) by client runs outside the laboratory — while the
two reconstructions above are the laboratory's subject.

## Repositories

- **[common](https://github.com/original-bitcoin-laboratory/common)** — the umbrella: what
  *"Bitcoin"* and *"a satoshi"* actually **are** (argued from the artifacts), the honest claims,
  the neutral conformance + attack‑surface matrices, and the release framing.
- **[genesis](https://github.com/original-bitcoin-laboratory/genesis)** — **OBL‑JAN09**: the full
  executable reconstruction of Bitcoin **v0.1.0** + derivatives (script engine, UTXO ledger,
  wallet, P2P, the origin‑distance tracker, and more) — and the home of the
  **Bitcoin** chain ([`derivatives/bitcoin/`](https://github.com/original-bitcoin-laboratory/genesis/tree/main/derivatives/bitcoin)),
  released as `Bitcoin-v0.1.5`.
- **[pre‑genesis](https://github.com/original-bitcoin-laboratory/pre-genesis)** — **OBL‑NOV08**:
  the Nov 2008 pre‑release witness + source inventory.
- **[bitcoin‑whitepaper](https://github.com/original-bitcoin-laboratory/bitcoin-whitepaper)** —
  which whitepaper is which: four known versions — two held, one known only from the judgment in COPA v Wright (¶271.9), one lost. Identify any copy from its
  contents alone, and verify the canonical one against the block chain it is embedded in.
  [bitcoinwhitepaper.online](https://bitcoinwhitepaper.online)

## Try it live

- **[→ bitcoin-lab.org](https://bitcoin-lab.org/)** — the lab's home: the **origin‑distance tracker**
  (how far each Bitcoin version stood from a chosen origin) and the **"Is it a Bitcoin?" compass**
  (where an object qualifies as *a* Bitcoin or *a* satoshi — and where the answer is convention, not
  fact). *Distance is neutral; the origin is a choice.*
- **[→ Join the live network](https://github.com/original-bitcoin-laboratory/genesis/blob/main/docs/ANNOUNCE.md)** —
  **three** joinable chains. A node serves **Bitcoin**, and two live anchors serve the two
  reconstructions. Clone the repo and point a node at any of them — it syncs and independently
  re‑validates every block. *Experimental. Not money.*

  ```
  bitcoin.bitcoin-lab.org:18026   Bitcoin (2026)  (genesis 00000000ad12f3ec… · magic f00ba726 · started at difficulty 1)
  seed.bitcoin-lab.org:18009      JAN09-X  (Jan 2009 released constitution · magic f00ba709)
  seed.bitcoin-lab.org:18008      NOV08-X  (15 Nov 2008 pre-release · magic f00ba708 · leading-zero-bits PoW)
  ```
- **[→ Bitcoin](https://bitcoin-lab.org/bitcoin)** — genesis `00000000ad12f3ec…`, mined at the
  original difficulty‑1, its coinbase carrying the front page of the day it was mined. The chain is
  **live and still being mined**; sealed findings sets cover the chain block by block, and
  [status.html](https://bitcoin-lab.org/status.html) reports the tip. *Not money.*
- **[→ JAN09-X](https://bitcoin-lab.org/jan09x.html)** · **[→ NOV08-X](https://bitcoin-lab.org/nov08x.html)** — each reconstruction's own page: its genesis,
  its constitution as a source‑anchored table, its isolated network identity, and its live height.

## What it found

- The origin was already a **general financial‑predicate engine** — full Script, escrow,
  hash‑locks, a shipped marketplace — at inception; the "programmability came later" story is
  substantially wrong.
- Bitcoin's early maturation was **real safety engineering** (the origin shipped the consensus
  machinery but almost none of the *bounds*), mapped **neutrally, from the origin**.
- Two reconstructions — **NOV08‑X** and **JAN09‑X** — carry the complete original vocabulary.
  They are released as **candidates** (*"a* Bitcoin"), **not** as *"the* Bitcoin": which live
  network "is" Bitcoin has no factual answer — only convention.
- The original source still **builds and runs on a pinned period toolchain** — from `sha.cpp` and
  the Script interpreter up to a full `bitcoin.exe` linked from the unmodified code (i686 · OpenSSL
  1.0.2 · wxWidgets 2.8 · BDB · Boost) — settling the *reproducible period build* end to end
  ([build‑reconstruction](https://github.com/original-bitcoin-laboratory/genesis/tree/main/derivatives/build-reconstruction)).
- Two unmodified 2009 nodes, air‑gapped, ran the whole lifecycle on the **historical genesis**:
  mined and relayed a block at real difficulty 1, sustained bidirectional growth to a
  byte‑identical 14‑block chain across a guest restart, survived a **real chain reorganisation**
  (`*** REORGANIZE ***`, the losing node retaining its valid orphan), and finally **relayed a spend
  of a matured coinbase** — matured under the client's own rule of **120 confirmations, not 100**.
  Every result verified from the raw `blk0001.dat` bytes
  ([the two‑node witness](https://bitcoin-lab.org/witness.html)).

## The other half

**[satoshi-onchain](https://github.com/satoshi-onchain)** · [satoshioncha.in](https://satoshioncha.in)
— the verifiable on-chain footprint of the original Satoshi, graded **[statistical], not
[cryptographic]**.

Two halves of one question, answered with different evidence. This laboratory studies
**Bitcoin** by making the earliest code run and re-derive. That organization measures what the
chain itself records about **Satoshi** and refuses to grade it above what the evidence supports. Neither leans on the other's conclusions.

## Boundaries

**"Original" means the archived 2008–2009 artifacts**, not any live chain's claim to be the original;
the laboratory takes no side among BTC, BCH, BSV or XEC, and its own executed evidence (the 2010
value-overflow block) is why it declines the claim that the origin was better.

**Not money, no conclusions, no warranty.** Everything here is experimental laboratory research in
progress: it shows what re-runnable methods find and stops there. The experimental chains are stamped
*"not money"* — no premine, no sale, no promises. Authority is **only** the two hash‑verified archives + the whitepaper; everything else
is measured neutrally against them. Reproduce everything with
`python genesis/scripts/reproduce.py`.

MIT © 2026 [parthod0x](https://github.com/original-bitcoin-laboratory) (laboratory tooling); the
historical Bitcoin sources retain Satoshi Nakamoto's 2009 MIT notice.
