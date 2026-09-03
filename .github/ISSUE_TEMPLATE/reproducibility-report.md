---
name: Something does not reproduce
about: A command, digest, signature, or timestamp did not come out the way the repository says it should
title: ''
labels: reproducibility
assignees: ''
---

<!--
The most useful report this project can receive. Fill in what you can; a partial report with the
exact command is far better than a complete one without it.
-->

## What you ran

```
<the exact command, and the directory you ran it from>
```

## What you expected

<!-- Quote the line from the README, the release notes, or the paper that says what should happen. -->

## What happened

```
<the output, trimmed to the part that differs>
```

## Which chain, if any

<!-- nov08x / jan09x / bitcoin / not chain-specific -->

## Environment

- OS and version:
- Python version (`python -V`):
- Rust toolchain, if the Rust suite is involved (`cargo --version`):
- Repository and commit (`git rev-parse HEAD`):

## Anything already checked

<!--
Optional. For example: whether the release signature verifies, whether the OpenTimestamps proof
upgrades, whether a clean re-clone behaves differently.
-->
