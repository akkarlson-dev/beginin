# Host Meter
*Work in progress. Case study in applied credibility filtering.*

---

## What it is

Signal Lens rates a single piece of content. Host Meter rates the person behind it — a slower-moving instrument that builds over time as individual piece-level digests accumulate.

The instrument has three independent axes. They answer different questions at different timescales and are scored independently on purpose: a creator can pass A and B and still correctly Bounce on C. The goal is not a ranking. It's a regulation system for what reaches you, at what rate, and when.

---

## The three axes

**Axis A — Messenger Credibility.** How honest is this person, structurally? Scored per person, updated periodically, not per piece.

Five dimensions:
1. Authenticity / Intellectual Honesty — updates when shown wrong? genuine uncertainty vs. performed humility?
2. Guest Service — serves the guest's actual expertise, or uses them as a prop?
3. Agenda Transparency — scored on disclosure only, never on approval of the agenda. Open selling = high.
4. Audience Relationship — format invites scrutiny, or cultivates a congregation that polices dissent?
5. Depth / Self-Awareness — has this person's identity and content visibly adapted as they've changed, or are they recirculating a fixed original-era brand unrevised?

Scale: 1–5. 5 = high.

**Axis B — Content Provenance.** Is the content original? Is the lineage acknowledged? This is Signal Lens applied at the piece level, with a Lineage Trace field tracking attribution behavior over time. Not duplicated here — see `signal-lens-v1.md`.

**Axis C — Standing Resonance.** Does this person's work register as nourishing or as static — for this one nervous system, independent of how they score on A and B? Three states: Bounce (durable, trait-like) / Tolerate / Draw. Sparse so far; added as encountered.

---

## Axis A — Current roster

| Person | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| Ira Glass | 5 | 5 | 5 | 5 | 5 |
| Dan Harris | 5 | 4 | 5 | 4 | 5 |
| Sam Harris | 4 | 4 | 5 | 3 | 4 |
| Tim Ferriss | 4 | 4 | 4 | 4 | 4 |
| Rich Roll | 4 | 4 | 4 | 4 | 2 |
| Ryan Holiday | 4 | 4 | 5 | 4 | 2 |
| Mark Manson | 3 | 3 | 4 | 3 | 4 |
| Dax Shepard | 3 | 3 | 3 | 2 | 3 |
| Malcolm Gladwell | 3 | 2 | 3 | 3 | — |
| Michael Pollan | 3 | 3 | 3 | 3 | 5 |
| Glennon Doyle | 3 | 2 | 2 | 1 | 2 |
| Brené Brown | 2 | 2 | 2 | 2 | 1 |
| Dave Asprey | 2 | 2 | 5 | 1 | 1 |
| Andrew Huberman | 1 | 3 | 2 | 2 | 2 |

Notes on a few:
- **Rich Roll** revised down on dimension 5 this pass: brand anchored to a 15-year-old origin story, unrevised despite continuous output.
- **Michael Pollan** revised up on dimension 5: initial read of his AI skepticism as closed-mindedness was wrong — it's a considered argument, and his career shows real sequential evolution.
- **Ryan Holiday** is a positive control on Axis B (clean, constant, explicit citation — it's the entire brand) but flagged on dimension 5: high transparency, low depth.
- **Malcolm Gladwell** genuinely mixed on dimension 5: strong structural evidence of empirical self-correction (built an entire show on it) alongside one credible case of concealment-then-disclosure rather than real change of mind. Not flattened to a single number.
- **Dax Shepard**: unresolved. Treat as unverified.

---

## Axis B — Lineage-failure taxonomy

Four patterns identified so far from the roster:

| Type | Example |
|---|---|
| Dilution-with-citation | Gabby Bernstein — cites sources consistently; density and clinical precision don't survive the compression |
| Contested/thin attribution | Mel Robbins ("Let Them") — two documented public disputes plus a personal unconfirmed pattern match |
| Rebrand-as-science | Judson Brewer — real research, but the contemplative lineage of the core technique is named in his bio, absent from the mechanism |
| Positive control | Ryan Holiday — citation is the brand; low originality score is correct and not a criticism |

Brené Brown has an unverified flag: alleged uncredited use of Black feminist theory. Needs primary-source verification before treated as settled.

---

## Axis C — Standing resonance

| Person | State |
|---|---|
| Gabby Bernstein | Bounce |

Sparse. Added as encountered. Most of the roster hasn't been run through Axis C yet. The Bernstein entry is the worked case that drove the design: she scores acceptable on A and B and still correctly Bounces. That's the system doing its job.

---

## Where this is going

The instrument is designed to accumulate. Each Signal Lens digest of a creator's actual work feeds into a trailing Axis A/B record over time, moving the assessment from gestalt impression toward evidence-based pattern. Axis C stays felt-sense, never inferred.

The Intake Query Layer — a real-time filter ("give me something funny tonight," "something that'll actually teach me something") that runs over the archive without writing back into it — is sketched but untested. Vocabulary and mechanics are in the working doc.

---

*Draft — June 2026. Instrument under active development. Full design rationale, v1 repair history, and per-figure reasoning in `resources/lenses/host-meter-v2-archive.md`.*
