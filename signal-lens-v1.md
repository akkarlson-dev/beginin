# Signal Lens v1

The first iN lens/filter/transformer. A standardized prompt that converts any article or podcast transcript into a structured digest — submittable to any AI engine.

## What this is

Not a personal habit. A transformer: input = link or transcript, output = a fixed-shape digest. The point is standardization — every piece run through this comes back in the same shape, so digests are comparable and stackable over time, and a meta-analysis across many of them becomes possible later.

This is lens #1 for iN. Treat the schema below as the interface contract — it should stay stable even as scoring methodology improves underneath it.

Structural note: this has converged, by instinct rather than design, on a CHI-paper shape — Abstract, Mechanism (→ Related Work / Method), Recommendation (→ Results), References. That's not an accident; it's the right shape for archival research digestion, and it's worth keeping explicit. The fields that don't map onto a normal paper (signal-to-noise, % to first actionable content, humanness) are the actual novel contribution here: a meta-layer scoring the source's own rigor and format, which a peer-reviewed paper doesn't need because review already filtered for that. Newsletter/podcast content has no such filter — this lens is standing in for it.

## The prompt (submittable as-is)

You are applying the Signal Lens to the following piece [link or transcript below].

Produce a structured digest with exactly these fields:

1. **ABSTRACT** (~100 words max, no preamble) — Function like a real paper abstract: the claim, the one-sentence basis for it, and the practical upshot. Should be readable as a complete standalone summary even if nothing else in the digest is read.

2. **MECHANISM** (no fixed cap — let density of the source dictate length) — What is claimed to be true, and what evidence is offered for it (named research, data, lived testimony, or pure assertion — say which). If multiple distinct studies/sources/threads of evidence are cited, name each one separately rather than collapsing them. This field is the archival core of the digest — do not compress it just to hit an overall word target. A piece with five cited mechanisms should produce a longer MECHANISM field than a piece with one.

3. **RECOMMENDATION** (no fixed cap) — What the piece says to actually do differently as a result. If there are multiple distinct recommendations or a sequence/hierarchy, list them as such rather than flattening into one sentence.

4. **THE SELL** (1-2 sentences) — Where, if anywhere, the piece routes toward the author's own product, program, platform, or book. State plainly; "none" if absent.

5. **SIGNAL-TO-NOISE SCORE** (1-10, one sentence justification) — Ratio of words that carry the conclusion/mechanism/recommendation vs. words that are narrative padding, preamble unrelated to the claim, or repetition of a point already made. 10 = every part of the piece contributes content captured in fields 1-4 above. 1 = almost none of it does.

6. **% TO FIRST ACTIONABLE CONTENT** (one sentence + the percentage) — What percentage of the way through the piece (by word count or runtime) does the first genuinely useful or actionable point appear — the first point that, on its own, would justify a reader or listener having spent the time up to that point. Distinct from signal-to-noise: a piece can be well-cited throughout and still place that first useful point late in the piece. State the percentage and name the specific sentence or moment.

7. **HUMANNESS** (1-10, one sentence + confidence level, experimental) — Best guess at human-direct-thought vs. AI-mediated-or-templated origin. State reasoning and confidence explicitly; this metric is new and unreliable, treat the score as provisional.

8. **ARCHIVAL SUMMARY** (500-600 characters, plain factual prose) — The single paragraph you'd want to find if you searched your own archive for this topic in two years and had time to read only one thing. Should stand alone without the rest of the digest.

9. **HIGHLIGHT-WORTHY PASSAGES** (1-3 index points) — Best guess at the specific sentence(s) or moments a thoughtful reader would underline or a listener would replay — distinctive phrasing, surprising data, or a moment of original (not formulaic or previously-stated-elsewhere) insight. For each: give its approximate location in the piece (% through, or a nearby paraphrase to locate it — do not reproduce the original wording itself) and one sentence on why it is notable. Omit this field entirely if nothing in the piece meets this standard; do not invent a highlight to fill the slot.

10. **ORIGINALITY** (1-10, one sentence justification) — Separate from signal-to-noise and from the evidence cited in Mechanism: with citations and packaging set aside, is the central idea something genuinely new or a specific original synthesis, or is it established knowledge restated in new language? A piece can score high on signal-to-noise (densely, efficiently written) while scoring low here (efficiently restating something already widely known), and vice versa. State the score and name what the idea would be if reduced to its least dressed-up form.

11. **REFERENCES** — Every named study, dataset, named researcher's work, book, or external source the piece cites or points to — formatted as a simple reference list (author/source — what it's cited for). Include URLs/links if the piece provides them directly. This field is often more reusable later than the rest of the digest, since the underlying sources remain valid even after the surrounding argument is forgotten. Omit entirely if the piece cites nothing.

Produce fields 1-11 above as the digest of the piece itself. Do not summarize the piece's structure or narrative arc as a separate section. Fields 4-7 should stay terse (they are metadata about the piece, not content from it); fields 2, 3, 8, and 11 should be as long as the source's actual density warrants.

After the digest, add one final section, clearly separated, that is about this prompt rather than about the piece:

12. **PROMPT FEEDBACK** (~200 words max) — Reflecting on applying this exact set of instructions to this specific piece: where, if anywhere, did two fields overlap or require an arbitrary choice about which one content belonged in? Where did an instruction require a guess because it was ambiguous for this type of source? Was any field consistently empty or low-value for this kind of piece? This section is for improving the prompt itself in a later revision — it should be specific to what happened on this run, not generic advice about prompts in general.

## Design notes

- Field 1 (Abstract, ~100 words) replaces the original 50-word "Conclusion." A real abstract has to hold claim + basis + upshot, not just the bottom line.
- Fields 4-7 stay terse by design — they're metadata about the piece, not content extracted from it.
- Fields 2, 3, 8, and 11 deliberately have no fixed cap. A padded piece should still compress to a short digest; a dense piece should be allowed to stay long.
- Field 6 (% to first actionable content) may be the single best predictor of reader drop-off — distinct from overall density. **Track this per-author/per-channel over time**: a creator who consistently scores high here (makes you wait) regardless of topic is exhibiting a format choice, not a one-off — that's the data point for the blog post on brand-as-narrative-toll.
- Field 7 (humanness) is the most speculative field. Expect it to be unreliable now; the value is in tracking how it's reasoned about, not trusting the number yet. Note: humanness answers "was this AI-mediated," which is a different question from whether the *authority* behind the content is earned or borrowed — see the Lineage Trace field below, added in v1.1.
- Field 8 (archival summary): fixed 500-600 character target keeps it scannable while still holding the real shape of the argument.
- Field 9 (highlight-worthy passages) is explicitly allowed to be empty.
- Field 10 (originality) answers a different question than signal-to-noise or Mechanism. S/N measures how efficiently the piece is written; Mechanism captures what evidence is cited. Originality asks whether the central idea is genuinely new once citations and packaging are set aside. This came directly out of noticing Brewer's "the body keeps the ledger" — an apparent echo of an established phrase ("the body keeps the score").
- Field 11 (references) is the closest thing to a real bibliography, often more durable than the prose itself.
- Field 12 (prompt feedback) is the model reporting on the prompt's own performance against this specific piece. Intent is to accumulate these across many runs and periodically review as a batch, rather than tweaking reactively.
- Not a personal tool only — meant to be handed to any AI engine, self-contained, no assumed prior context.

## v1.1 addition — Field 10.5: LINEAGE TRACE

Added after recognizing Originality (field 10) can't, by itself, distinguish "restates known material with the source named" (fine — Holiday/Stoicism is the clean case) from "restates known material with the source diluted or unnamed" (the actual problem — see Host Meter v2 for the worked cases).

**10.5. LINEAGE TRACE** (one short paragraph) — Name the most likely upstream tradition, named author, or clinical/research framework the central idea descends from, if one is identifiable. State the hop count if traceable (e.g., "two hops: clinical framework — popularizer — this piece"). Then state plainly whether *this specific piece* names that source, gestures at it without naming, or presents the idea as if it originates here. This is a citation-behavior judgment, not a value judgment about whether popularization itself is legitimate — note in Originality (field 10) separately whether the repackaging adds genuine synthesis value. Omit only if the idea is genuinely first-generation (rare).

This is the field that connects a single-piece digest to the channel-level Host Meter (see companion doc) — repeated Lineage Trace entries for the same author, across pieces, are what let "consistently restates X without naming it" become a defensible claim instead of a one-off impression.

## Open questions for future versions

- Does signal-to-noise need sub-categories (narrative padding vs. credential-establishing vs. emotional pacing) or is one number enough?
- Should humanness eventually be backed by a real classifier/heuristic instead of model judgment alone?
- Worth testing this same prompt across multiple AI engines on the same piece to see how much the digest varies by model.
- At what volume of digests does a meta-analysis layer (patterns across authors, formats, topics) become worth building?
- **Channel-level tracking**: once enough digests exist for a single recurring author/host, plot % to first actionable content over time/episodes. A consistently high (late) number across unrelated topics is evidence of *template*, not content. That's the data point for a future post on narrative-toll-as-brand-strategy.
- Design-session loop: field 12 is meant to accumulate across many digests, then get reviewed as a batch in a dedicated session.
- Originality tracking over time: does a given author's originality score trend down across pieces (running out of original material, recycling under new framing), or stay consistently high?
- **Lineage tracking over time (new)**: same logic as % to first actionable content — across multiple pieces from the same author, does Lineage Trace show a consistent pattern (always cites, sometimes cites, never cites) regardless of topic? That consistency is the actual evidence, not any single piece's score.

---
*v1 — June 2026. First lens built for iN. v1.1 — Lineage Trace field added, same month, after Host Meter v2 work surfaced the need.*

## Worked example: uncapped fields applied to the Brewer GAD article

For comparison, here's what fields 2, 3, and 8 look like with no fixed cap, run against the Substack piece that prompted this revision — vs. the original ~200-word version which couldn't hold all five cited mechanisms.

**MECHANISM (uncapped):**
Five distinct evidence threads, each named separately: (1) JAMA Psychiatry meta-analysis — only 3 of 8 tested psychotherapies beat treatment-as-usual for GAD, 5 including psychodynamic and supportive therapy showed no advantage; (2) a separate meta-analysis putting CBT remission at ~50%; (3) Borkovec's avoidance theory of worry — worry is active avoidance of more visceral distress, not passive symptom; (4) the Contrast Avoidance Model — GAD patients maintain chronic low-grade negative affect to avoid sudden emotional shifts; (5) Ethan Kross's "co-rumination" research — describing distress repeatedly to a sympathetic listener can fuel rather than resolve it; (6) the author's own lab data — 67% symptom reduction in a GAD trial using craving/urge-curiosity training, plus comparable results in smoking and emotional-eating studies.

**ARCHIVAL SUMMARY (~580 characters):**
Brewer (Brown, psychiatrist/neuroscientist) argues GAD resists standard talk therapy because worry functions as active avoidance, not passive symptom — JAMA meta-analysis shows only 3 of 8 therapy types beat doing nothing, CBT remission ~50%. Insight alone fails because understanding the pattern doesn't build distress tolerance; verbal processing can become "co-rumination," a sophisticated avoidance dressed as productive therapy. What works: ACT, enhanced CBT, and mindfulness approaches that build tolerance for raw bodily sensation directly. Access barriers (cost, 3+ month waitlists) are real; his lab reports 67% symptom reduction using curiosity-based urge training.

**REFERENCES (as the piece itself lists them):**
- Borkovec, Alcaine & Behar (2004) — avoidance theory of worry and GAD
- Brewer & Roy (2021), *Am J Lifestyle Medicine* — anxiety-as-habit framework
- Gao et al. (2022), *Psychosomatic Medicine* — app-based mindfulness RCT for sleep/anxiety
- Kross (2021), *Chatter* (book) — co-rumination concept
- Newman & Llera (2011), *Behavior Therapy* — Contrast Avoidance Model
- Papola et al. (2024), *JAMA Psychiatry* — network meta-analysis of GAD psychotherapies, DOI provided in piece
- Roy et al. (2021), *JMIR* — digital therapeutic efficacy trial
- Springer, Levy & Tolin (2018), *Clinical Psychology Review* — CBT remission meta-analysis
- AAMC (2023) — mental health care access barriers, link provided in piece

This is the version worth archiving — it would've been cut by roughly half under the original word cap, and the reference list alone is arguably the most reusable artifact in the whole digest. The full digest with all 12 fields, provenance header, and Lineage Trace is in `digests/brewer-gad-digest.md`.
