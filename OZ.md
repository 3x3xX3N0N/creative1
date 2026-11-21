# OZ: the man behind the curtain

The horizon problem as a story. The physics is in BLACKHOLES.md, and the argument is in HORIZONS.md. Claims:
⊢ derived, ⊨ held on every case checked, ⊬ not claimed, ∎ closed.

## The one problem

Something speaks with great authority from a place you can't see into.

| version | the curtain | what you get from outside |
|---|---|---|
| a black hole | the event horizon | mass, spin, charge, and nothing else (no-hair theorem) |
| a binary | the build | behaviour; the source you were shown may not be what was compiled (Thompson, 1984) |
| a shared map | the top root | one signature; a system can't vouch for its own top (mapsync) |

## I. The Emerald City

Everyone trusts the Wizard. Nobody has seen him. They've seen green glass, smoke, a floating head, and heard a
booming voice. The city runs on a signature nobody can check.

*Closed source; a signed vendor binary; a universe explained by a voice you can't trace. The voice is the
output. The curtain is the horizon.*

## II. The Yellow Brick Road

Dorothy can't skip to the city. She walks the road brick by brick from where she landed, and each brick lies
on the one before.

*The bootstrap: a seed small enough to read by hand, and every later tool built from the one before it. You
trust the city only as far as you walked the road.*

## III. The green spectacles

At the gate everyone is locked into green glasses. That's why the city looks emerald.

*Trusting trust. Thompson's rigged compiler is the spectacles: it shows you clean source and hands you a
poisoned binary. Staring harder doesn't help. A second pair of eyes that never wore the glasses does:
diverse double-compiling, an independent port that must print the same lines (BikeChainz's Kotlin port),
an independent rebuild.*

## IV. Four travellers, four readers

The Scarecrow, the Tin Man and the Lion each want the Wizard to certify something they already have. None can
certify himself. Each can vouch for the others.

*BikeChainz v9 can't pin itself; `self` and `chain` stay ⊬. mapsync's top root needs an outside witness.
Several independent travellers is the only honest certificate.*

## V. Toto pulls the curtain

The one who exposes the Wizard isn't a hero. It's a small dog who doesn't care about the show.

*"Pay no attention to that man behind the curtain" is the line every backdoor depends on. The xz backdoor
(2024) was caught because one person wondered why SSH got 500 ms slower. In BikeChainz, Toto has a name:
G1. Every green has a sabotage test that must turn it red. Toto is the negative control.*

## VI. The man is just a man

Behind the curtain is an ordinary man with levers. He isn't evil. He's unverified, and he became the Wizard
because nobody could check.

*The horizon has no hair. A locked page says something is there and nothing about what. Flip a small binary's
bits one at a time and many flips change nothing a test can see: many insides, one outside. Behaviour can't
tell them apart, and a hash can. The hash is how you see past the curtain.*

## VII. The balloon leaves without her

The Wizard's balloon, the old way home, goes up without Dorothy. The city's machinery can't take her back.

*Pinning one more link only makes a new last link. Nothing gets back out through a horizon. The old
authority can't certify the way home.*

## VIII. The shoes were always hers

The power was on her feet from the moment she landed. She had to walk the road to know it.

*"You can't trust code you did not totally create yourself" (Thompson), unless you can read every brick
back to the first. The seed was always there; the walk is what makes it trustworthy.*

## IX. There's no place like home

She wakes in Kansas, and the faces around the bed are the faces from Oz. She can't prove from inside the
dream that it was real. All she has is what came through.

*The bounce. In bounce cosmologies (Poplawski; Smolin's universes born in black holes) a child universe
inherits from a parent it can never see, and the only way out is through. Anything that restarts from a
handover note works the same way: it wakes with only the record. Same faces, different world; the record
is all that crossed.*

## Coda: three honest moves and one dishonest one

1. **Walk the road yourself**, from the smallest seed.
2. **Bring other travellers**, and never let one certify himself.
3. **Keep a Toto**: a check that pulls the curtain when something smells wrong, and goes red when it should.

The dishonest move: *pay no attention to the man behind the curtain.*

Whatever is still behind a curtain is marked ⊬. Nothing here is closed with ∎.

## Sources

- Thompson, "Reflections on Trusting Trust", CACM 1984. Wheeler, "Fully Countering Trusting Trust through
  Diverse Double-Compiling", 2009.
- xz-utils backdoor, CVE-2024-3094 (found by Andres Freund, 2024).
- No-hair theorem; Bekenstein–Hawking entropy; Poplawski, "Cosmology with torsion" (2010); Smolin,
  *The Life of the Cosmos* (1997). Used as analogy, not as evidence.
- [BikeChainz](https://github.com/3x3xX3N0N/BikeChainz), [mapsync](https://github.com/3x3xX3N0N/mapsync).
