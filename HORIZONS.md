# Horizons: nothing certifies itself

The thread that ties this repo to BLACKHOLES.md, OZ.md and the owner's public repos. Claims: ⊢ derived,
⊨ held on every case checked, ⊬ not claimed, ∎ closed (vocabulary from BikeChainz). The analogies are
analogies: physics is not evidence for software, or the other way round.

## The pattern

| system | the inside | the horizon | what gets out | the outside reader |
|---|---|---|---|---|
| a black hole | whatever fell in | event horizon | mass, spin, charge (no hair) | nobody, from our side; in bounce models, only a parent universe sees both |
| our universe | everything we can observe | cosmic horizon | nothing from beyond it | ⊬ |
| [BikeChainz](https://github.com/3x3xX3N0N/BikeChainz) | v1 … v9, each pinning the last | the head of the chain (v9's `self` and `chain` print ⊬ forever) | a sha256 | `g1_review.py`, git history, the independent Kotlin port |
| [mapsync](https://github.com/3x3xX3N0N/mapsync) | each person's own signed map | `top_root` | one root | a public timestamp, kept outside the system |
| a compiler | the binary | the build | behaviour | a second, independent compiler (diverse double-compiling) |
| a private share | the documents | a password (HTTP 401) | "something is here" | whoever holds the key |

In every row: **the inside can't vouch for its own top, and adding one more layer only moves the top.**
BikeChainz says it directly. Pinning the last link only makes a new last link, so the chain stops at v9 on
purpose. A universe explained by a parent universe has the same problem one level up.

## The no-hair rule for software

A black hole shows mass, spin and charge and hides everything else. A program shows behaviour and hides how
it was built. If you flip bits in a small binary one at a time, many flips change nothing any test can see:
many insides, one outside. **No behaviour test can tell them all apart, and a hash can.** That's why
BikeChainz pins bytes rather than trusting output, and why every green check there needs a negative control
that turns it red (G1).

## Trusting trust: open source vs protected source

**The problem (Thompson, 1984).** A compiler can be rigged to backdoor what it compiles and to re-insert the
rigging whenever it compiles a clean copy of itself. The source is clean and the binary is poisoned. *"You
can't trust code that you did not totally create yourself."*

**Protected (closed) source** asks you to trust the vendor's word and build system. SolarWinds (2020): a
compromised build server shipped signed malware to about 18,000 customers. Nobody outside could check.

**Open source** gives you many readers, but Thompson's attack lives in the toolchain and the binary, not in the
source. xz-utils (CVE-2024-3094): the backdoor hid in test files and release tarballs that didn't match the
repository. The code was open, and almost nobody compared what shipped with what was published. It was
caught by accident, by one person curious about a 500 ms delay.

So open source is **necessary but not sufficient**. What has advanced since 1984 is checking the path from
source to binary:

1. **Diverse double-compiling** (Wheeler, 2005; PhD 2009). Rebuild the compiler with an independent compiler
   and compare bytes. "Trust one" becomes "two independent ones weren't both rigged the same way."
2. **Reproducible builds** (Debian, Tor, Bitcoin Core, NixOS). The same source gives the same bytes, so
   anyone can rebuild and compare.
3. **Bootstrappable builds** (stage0, GNU Mes, live-bootstrap). Start from a seed small enough for a person
   to read completely, and build everything else from source. GNU Guix reached a full-source bootstrap in 2023
   from a seed of a few hundred bytes. It's the most direct answer to Thompson: shrink "code you didn't create"
   until one person can read all of it.
4. **Transparency logs and provenance** (Certificate Transparency, Sigstore, SLSA, in-toto). Public
   append-only logs, so a quiet swap leaves evidence.
5. **Hardware** is the open frontier: a CPU can lie below all of the above. Partial answers are open hardware
   (RISC-V, OpenTitan) and checking on more than one architecture. ⊬

Every one of these adds **an independent outside reader**. None of them makes the inside vouch for itself.

## How the owner's repos sit in that lineage

| idea | where |
|---|---|
| independent implementation must agree | BikeChainz's Kotlin port prints the same lines from independent code |
| bytes are load-bearing | BikeChainz v7–v9 pin sha256 prefixes; `.gitattributes` keeps line endings exact |
| every green needs a red | BikeChainz G1: each check must fail under sabotage, and says so |
| an index of signed roots, not one merged truth | mapsync: each owner signs only their own map; `index.json` rolls up roots |
| names are labels, keys are identities | mapsync's "two Codys": sameness only by explicit signed `same_as` |
| the top needs an outside witness | mapsync says so in its README rather than claiming otherwise |
| honest labels | ⊢ ⊨ ⊬ ∎: never close an open case |

## A map of maps

The owner keeps a private **map of maps**: one index page over every project's own map. Each project keeps its
own map, and the index only points at them. That's mapsync's shape in practice. Behind the password it shows
everything; outside, it returns a 401, which says something is there and nothing about what. It's a
horizon with a door, and the key is what makes the reader an insider.

## Strong, medium, weak

The parallels on this page aren't equal, so here they're ranked:

- **Strong** (the same structure): chain head ⊬ ↔ the observer can't see the parent; no-hair ↔ behaviour hides
  the build, so pin the hash; entropy counts indistinguishable insides ↔ silent mutants; Bekenstein bound and
  the information paradox ↔ compression and lossless round trips.
- **Medium** (the same rule, different stuff): trust boundaries in security designs ↔ horizons; ledgers whose
  shares must sum to the cost (BikeChainz's Shapley split) ↔ conservation.
- **Weak** (metaphor only): the busiest project as the "central mass" everything else orbits. Nice imagery, and
  nothing more.

## The one line

**No system can certify itself from inside. Trust comes from walking the road from the smallest seed, from
independent travellers who check each other, and from a check that goes red when something is wrong.
Anything still behind a curtain is marked ⊬.**

Told as a story: OZ.md. Told as a job: LAMP-LIGHTER.md.
