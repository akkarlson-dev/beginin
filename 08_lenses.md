# iN Lenses: Signal Lens & Content Filter System

**Status:** v1, live. June 2026.
**Files:** `resources/lenses/signal-lens-v1.md` (prompt), `resources/lenses/iN-content-filter-system.md` (master spec), `resources/lenses/digests/` (archive of live runs).

---

## What a Lens Is

A lens is a prompt built on a validated framework. The spreadsheet is the substrate. The lens is what you apply to a slice of the data to get something out. The user's data never leaves. Only the prompt travels.

Most lenses operate on personal captures. Signal Lens is different: it applies the same logic to incoming content. Articles. Podcast transcripts. Any piece of text. One lens. Same 12-field output shape every run. Digests are comparable and stackable over time. A meta-analysis across many of them becomes possible later.

---

## Signal Lens v1

A standardized digest prompt. Twelve fields:

1. **Abstract** (~100 words) — claim, basis, practical upshot. Standalone.
2. **Mechanism** — what is claimed true, and what evidence supports it; named separately if multiple.
3. **Recommendation** — what to do differently.
4. **The Sell** — where the piece routes toward the author's own product.
5. **Signal-to-Noise Score** (1–10) — ratio of content to padding.
6. **% to First Actionable Content** — when the piece starts earning the reader's time.
7. **Templated vs. Responsive** — does the output shape change when the input changes, or does the same structure recur regardless of topic?
8. **Archival Summary** (~500 characters) — the paragraph you'd want to find two years later.
9. **Highlight-Worthy Passages** — specific sentences worth noting; omitted if nothing qualifies.
10. **Originality** (1–10) — is the central idea genuinely new, or established knowledge restated?
11. **Lineage Trace** — the most likely upstream source; how many hops; whether this piece names it.
12. **Prompt Feedback** — how the prompt performed on this specific run.

The full prompt text is in `resources/lenses/signal-lens-v1.md`. Submittable as-is to any AI engine, no assumed context.

Structural note: fields 1, 2, 3, 8, and 11 have no fixed cap — let the source's density dictate length. Fields 4–7 stay terse — they're metadata about the piece, not content from it. Field 9 is explicitly allowed to be empty.

---

## The Content Filter Architecture

Signal Lens is the per-piece instrument. The content filter is what tells you whether to run it at all, and what to do with the results over time.

Four layers, each answering a different question:

| Layer | Question | Timescale | Archival? |
|---|---|---|---|
| **Axis A: Messenger Credibility** | Is this person honest? | Per-person, slow-changing | Yes |
| **Axis B: Content Provenance** | Is this idea original and honestly sourced? | Per-piece | Yes |
| **Axis C: Standing Resonance** | Does this register as nourishing for this specific reader? | Per-person, durable like an allergy | Yes |
| **Intake Query Layer** | Given everything above, what should surface right now? | Per-session, per-mood | No |

**The one rule:** these four layers must be scored independently and never allowed to edit each other after the fact. A personal allergy (Axis C) is not a credibility verdict (Axis A). A mood is not a trait. The Intake Query Layer reads all three but writes back to none of them.

### Axis A: Messenger Credibility (four dimensions, repaired from v1)

1. **Authenticity / Intellectual Honesty** — does this person update when shown they're wrong?
2. **Guest Service** — in interview format, does the host serve the guest's expertise or use them as a prop?
3. **Agenda Transparency** — scored on *disclosure*, not approval. Openly selling = HIGH.
4. **Audience Relationship** — does the format invite scrutiny, or cultivate a congregation that polices dissent?

### Axis B: Content Provenance (Signal Lens fields 10, 10.5, 6)

The three load-bearing fields for the credibility-filter use case:
- **Originality (field 10):** is the central idea genuinely new once citations and packaging are set aside?
- **Lineage Trace (field 10.5):** the upstream tradition or framework; hop count; whether this piece names it, gestures at it, or presents the idea as its own.
- **% to First Actionable Content (field 6):** track per-author over time. A creator who consistently makes you wait regardless of topic is running a format, not responding to content.

### Axis C: Standing Resonance

Three states: **Bounce** / **Tolerate** / **Draw**. Self-reported only — never inferred by an AI pass on the text. Durable, like a food allergy. Does not depend on mood.

Record the threshold if known for a Bounce ("5 min / ~10% in"). This is directly comparable to Signal Lens field 6, measuring rejection instead of payoff.

### The Intake Query Layer (not archival)

Query-time only. Never written back into any creator's or piece's record. Vocabulary: humor/levity, intellectual provocation, comfort/soothing, hard skills/how-to, short-and-light vs. long-and-immersive, save-for-later. Same archive, different surface depending on the question.

The full architecture, standing rules, and known gaps are in `resources/lenses/iN-content-filter-system.md`.

---

## The Constant-Finder

Field 7 (originally "Humanness") was retargeted to ask a more useful question: across 5–10 pieces from the same person, what stays constant regardless of topic?

This fires at three different layers:

- **Rhetorical move** (Holiday): name a historical figure, one-line gloss, pivot to the productivity point. The slot fills differently each time. The move and its depth never change.
- **Business model** (McKowen): a new personal pathology surfaced, narrated beautifully, monetized, on a publishing cycle. Not visible from inside any single book.
- **Product format** (Harris): every question resolves to a guided meditation, regardless of topic. Not a credibility failure. A format collapse.

The Constant-Finder is explicitly orthogonal to Axis A trust. It fired on a low-trust case (Holiday), a high-trust case (McKowen), and the highest-trust case in the original roster (Harris). A person can be completely sincere and still be running a fixed structure that no longer responds to its actual input.

The field is currently theoretical — all three cases were reasoned from memory, not from running actual digests. Needs a real corpus run before it's trusted as more than a hypothesis.

---

## Proof of Concept: Brewer Digest (June 20, 2026)

Signal Lens was run live on a Judson Brewer piece ("Why psychotherapy may not be the best way to treat anxiety," Substack, June 20, 2026). Key findings:

- **Signal-to-Noise: 4/10** — the mechanism section is dense and well-cited; the surrounding ~2,000 words largely repeat the same point to three audiences.
- **Originality: 4/10** — core claim (GAD as active avoidance, exposure beats insight) is established clinical consensus; the genuine contribution is a narrower reframe in reward-learning language.
- **Lineage Trace:** Borkovec's avoidance theory (1990s–2000s); Buddhist equanimity recoded as reward-based learning; the contemplative origin is in the author's bio but absent from the mechanism's stated framing.
- **"The body keeps the ledger"** appears without citation and closely echoes van der Kolk's "The Body Keeps the Score."
- **Field 12 (Prompt Feedback)** produced two immediately actionable v1.2 improvements: Mechanism/References redundancy; Originality edge-case scoring rule needed for "mostly synthesis + one original layer" pieces.

This confirms the content filter's §6.3 read on Brewer ("rebrand-as-science") from a live digest, not a vibe. Full digest: `resources/lenses/digests/brewer-gad-digest.md`.

---

## Why This Matters for iN

The user-owned OUT thesis: the user's own captured signal becomes the filter through which external content is evaluated. Not algorithmic engagement bait. Personal truth as personal lens.

Signal Lens is the first operational version of that. It gives iN users a principled method for evaluating incoming content — one that scores each piece against evidence-based criteria, tracks lineage, and separates "is this any good" (Axis A/B) from "is this good for me right now" (Axis C / Intake Query). The same lens applied to the same creator across five to ten pieces builds a per-person record. That's when the Constant-Finder becomes legible.

iN is primarily a capture system. The downstream question — what should reach you, at what rate, with what provenance — is the natural next layer. Signal Lens is the answer to that question, operational as of June 2026.
