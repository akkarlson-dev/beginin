# How the iN Lenses Got Built

**Status:** June 2026. Process account and design rationale for Signal Lens and the Content Filter System.
**Companion docs:** `resources/lenses/signal-lens-v1.md`, `resources/lenses/iN-content-filter-system.md`, `resources/lenses/iN-voice-authority-framework.md`

---

## The Problem

Not "too much content." Everyone has too much content. The actual problem: I had no principled way to decide what deserved my time.

The algorithm decides what reaches most people. My alternative was my own gut, which can't scale, can't accumulate, and can't explain itself. What I wanted was something I could look at and say: here is why this piece is worth reading. Here is what it claims. Here is where the idea came from. Here is whether I personally respond to this voice. Four different questions. Each one answerable. None of them requiring me to trust a platform's engagement model.

---

## The First Move: Standardizing the Digest

The first design question: what shape should the output take?

Summaries already exist. What I wanted wasn't a shorter version of a piece. It was a consistent structure that made any piece comparable to any other piece, regardless of format, length, or topic. Comparable and stackable over time. A digest I'd want to find two years later.

Signal Lens v1 is a 12-field prompt, submittable to any AI engine with no assumed context:

1. **Abstract** (~100 words, standalone) — the claim, the basis, the practical upshot
2. **Mechanism** — what is claimed true, and what evidence supports it; named sources listed separately
3. **Recommendation** — what to do differently
4. **The Sell** — where the piece routes toward the author's own product
5. **Signal-to-Noise** (1-10) — ratio of words that carry the conclusion vs. padding and repetition
6. **% to First Actionable Content** — when does the piece start earning the reader's time?
7. **Templated vs. Responsive** — does the structure change when the topic changes, or is the same move recurring?
8. **Archival Summary** (~500 characters) — the paragraph worth finding two years later
9. **Highlight-Worthy Passages** — specific sentences; omit entirely if nothing qualifies
10. **Originality** (1-10) — is the central idea genuinely new, or established knowledge restated?
11. **Lineage Trace** — the upstream tradition; hop count; whether this piece names its source
12. **Prompt Feedback** — how the prompt performed on this specific run

Fields 4-7 are metadata about the piece, not content from it. That distinction matters. Most AI summaries blur what a piece says with how well it says it. Signal Lens separates those into different slots.

The fields with no fixed length cap — Mechanism, Recommendation, Archival Summary, References — are deliberately uncapped. A padded piece compresses to a short digest. A dense piece is allowed to stay long. Compressing everything to a fixed word count creates false equivalence between a newsletter and a well-cited research summary.

---

## The Architecture That Emerged

Once there were per-piece digests, the question became: how do you use them?

That required thinking about what question each field answered, and for whom. A credibility rating on the person is a different question from a quality rating on the piece. Both are different from whether I personally want to engage with this voice right now. Three questions. Three layers.

The architecture:

- **Credibility** (per-person, slow-changing): Is this person honest? Do they update when wrong? Are they transparent about what they're selling?
- **Content Provenance** (per-piece, Signal Lens): Is the idea original? Where did it come from? Does this piece name its sources?
- **Personal Fit** (per-person, durable): Do I respond to this voice? Not today's mood. A standing verdict, like a food allergy.
- **Right-Now Filter** (per session, never archived): Given all of the above, what should surface tonight, with 20 minutes and no interest in hard skills?

The standing rule: none of these layers can edit the others after the fact. A personal allergy is not a credibility verdict. A mood is not a trait. The Right-Now Filter reads everything but writes back to nothing. Mixing these layers is how a recommendation engine ends up suggesting things you've already seen, or surfacing things you've explicitly decided not to engage with.

The full credibility layer (called the Voice and Authority Framework in the spec) has five dimensions, each scored independently: intellectual honesty, how they treat guests in interview format, agenda transparency, the relationship structure with the audience, and whether their perspective has visibly evolved or is running original-era framing unrevised.

---

## The Constant-Finder

Field 7 was originally "Humanness" — a guess at whether a piece was AI-mediated. It became more interesting when pointed at a different question: across 5-10 pieces from the same person, what stays constant regardless of topic?

A human running a fixed formula produces the same diagnostic signature as a template. That's structural, not a moral claim. What stays constant lives at different levels:

**Rhetorical move** (Ryan Holiday): name a historical figure, one-line gloss, pivot to the Stoic productivity point. The slot fills differently each time. Aurelius, a battle, Anne Frank. The move and its depth of treatment never change regardless of what's plugged in.

**Business model** (Laura McKowen): a new personal pathology surfaces, gets narrated well, gets monetized, on a roughly continuous publishing cycle. Sobriety, then love addiction, then Ambien, then fawning. Not visible from inside any single book. Only visible when several are stacked side by side.

**Product format** (Dan Harris): whatever the question — anxiety, parenting, grief, work stress — the resolution is a guided meditation. Because that's what the platform can produce at scale. Not a credibility failure. A format collapse.

The finding that felt most like a real result: the Constant-Finder fired on a low-credibility case (Holiday), a high-credibility case (McKowen), and the highest-credibility case in the original 13-person set (Harris). Sincerity and structural creativity are orthogonal. A person can be completely honest and still be running a fixed structure that no longer responds to its actual input.

---

## The Live Run

Signal Lens was run against a Judson Brewer Substack piece on generalized anxiety disorder (June 2026).

Results: Signal-to-Noise 4/10. The mechanism section is dense and well-cited. The surrounding ~2,000 words largely repeat the same point addressed to three different audiences in sequence. Originality 4/10. The core claim (worry as active avoidance, exposure over insight) is established clinical consensus from Borkovec's work in the 1990s and 2000s. The genuine contribution is a narrower reframe in reward-learning language.

Lineage Trace: Borkovec two to three hops out, named in the mechanism but not in the framing. The contemplative origin of the core technique is in the author's bio, absent from the stated framing of the mechanism itself. "The body keeps the ledger" appears without citation and closely echoes van der Kolk's "The Body Keeps the Score."

This confirmed a read I already had on Brewer from the architecture's worked example — not from a vibe, from a live digest run against an actual piece.

---

## Why This Matters for iN

The design thesis for iN is that a person's own captured signal should become the filter through which external content is evaluated. Not an algorithm. Not engagement optimization. The user's own record of what they found useful, what registered, what they returned to.

Signal Lens is the first operational version of that. It gives users a principled method for evaluating incoming content: evidence-based criteria, lineage tracking, and a clean separation between "is this any good" and "is this good for me right now." Applied to the same person's output across enough pieces, it builds a per-person record. That's when the Constant-Finder becomes legible — when there's enough data to see the pattern, not just the piece.

The lenses are working hypotheses. The schema is stable enough to be version-controlled. The methodology will improve as more digests accumulate and prompt feedback (field 12) is reviewed in batch. The Constant-Finder is still theoretical — all three cases were reasoned from prior knowledge, not from running actual digests. That's the next real test.

---

*June 2026. Amy K. Karlson / Smith-Karlson LLC.*
