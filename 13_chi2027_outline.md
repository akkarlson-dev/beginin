> *Working research proposal, May 2026. Shared as a record of independent research direction.*

# CHI 2027: Working Paper Outline
*IN. Formative Study: Personal Micro-Capture as Scaffold for LLM Literacy*
*Draft: May 2026 | Authors: Amy K. Karlson, Missie Smith*

---

## Working Title

**"Is It Higher Friction to Enter or Forget? A Formative Study of Personal Micro-Capture as Scaffold for LLM Literacy"**

---

## Abstract
*[Draft after study completes. Key elements: the empty box problem, the PhyDigit connection, the IN. scaffold, 25-person cohort, 4-week course, RQs, findings on LLM literacy stages, contributions.]*

---

## 1. Introduction

### The Problem: The Empty Prompt
Today's default AI interface is a blank prompt field. No directive, no context, no personal grounding. The user is expected to arrive with a question: but most people don't know what to ask. Without a personal data substrate, the most powerful reasoning tool in history produces generic outputs for generic inputs. This is not a UI problem. It is a scaffolding problem.

The promise of LLMs is radical personalization. The reality for most users is a blank field that returns the same answer to everyone. The gap between promise and reality is not compute or capability: it is the absence of anything personal to put in.

**IN. as directive.** IN. is not a product name: it is a verb. A command. A stance. *In.* Put the thing in. Be present. Turn inward. The brand is the directive: the single act the system asks of you. This framing is intentional and load-bearing: it removes the decision overhead that kills capture habits. You don't decide what to do with a thought. You go IN.

### The Friction Question
Karlson, Smith & Madinei [under review] modeled device engagement as a continuous cost optimization: the cost of engaging with a device at any moment vs. the cost of refraining. Their PhyDigit framework identified seven cost categories (Social, Cognitive, Physical, Productivity, Opportunity, Health, Safety) operating simultaneously on both sides of the decision threshold.

Applied to self-capture, this framework asks a specific question: is it higher friction to enter a thought, or to forget it?

Earlier work (Karlson, Andrew & Brush, CHI 2009) studied the input side of this question for micronotes. Even natural modalities: voice and digital ink: failed to displace paper. The paper concluded that demonstrating the value of accumulated digital captures (searching, sharing, reflecting) would be necessary to shift adoption. That value demonstration had to wait for LLMs.

**The hypothesis this paper tests**: when the cost of engaging (entering a thought) approaches zero AND the accumulated data produces value through AI conversation, the optimization tips decisively toward capture: and this creates a new kind of literacy.

The tagline and research provocation: *Is it higher friction to enter or forget?*

### The Organization Graveyard
Capture without reciprocal value is unsustainable. Every organization system that has failed has failed for the same reason: the user puts something in, and nothing meaningful comes back. Without return, the exchange is asymmetric: and asymmetric exchanges extinguish.

For two decades, people have been told to organize themselves digitally. The tools have multiplied: task managers, PKM systems, journaling apps, note-taking platforms. Each promises to be the place where the thought goes. Most become graveyards within weeks: abandoned apps, half-finished Notion workspaces, notebooks that captured three days of ideas and then went dark.

The pattern is consistent and predictable: organization systems extract structure-labor from the user at entry time, when it is most costly. Choose a category. Pick a project. Apply a tag. When the accumulated taxonomy no longer fits the user's current concerns, maintenance cost exceeds perceived return. Entropy wins. The system fails not from lack of motivation, but because the design requires sustained structural upkeep in exchange for deferred and uncertain value. The user learns to experience organization systems as a source of guilt rather than relief.

This failure mode is not incidental: it is how most capture systems are built, because imposed structure is what makes retrieval possible. IN. makes a different bet: zero structure at entry, with AI conversation as the retrospective sense-making layer. The user does not need to anticipate what the data will be *for*. That question is asked later, when there is something to look at. The relationship is symmetrical: you ↔ your data, no taxonomy in between.

The prevailing paradigm of AI interaction shares a version of this failure mode at scale. Even with powerful, capable tools widely available, most users engage with them as a glorified search bar or writing coach: the two dominant use patterns for a tool capable of dramatically more. The cause is not lack of capability; it is the absence of anything personal to bring. OpenAI's own analysis of 1.1 million ChatGPT conversations found that approximately 24% of use falls under "Seeking Information," which the study explicitly calls a very close substitute for web search, and that personal reflection constitutes under 2% of usage (Chatterji et al., 2025). The blank box is not neutral: it actively forecloses the personal. Generic inputs produce generic outputs, regardless of the capability of the model receiving them.

This is not a capability gap: and it is also not a curiosity gap. Users do have questions they are genuinely, passionately curious about. Those questions are about themselves: their patterns, their relationships, their choices, their futures. The failure is one of subject matter. Nobody is particularly curious about querying the encyclopedia. People are acutely curious about themselves: they simply have never had a tool that made their own experience the subject of inquiry rather than a footnote.

LLMs change this, but not through retrieval. Retrieval is still asymmetric: you ask, it returns, the exchange ends. What LLMs make possible: given a personal data substrate: is *conversation*. Conversation requires reciprocal energy: each turn responds to the specific content the user brought. The accumulated data is not merely searchable; it is a conversational partner. For the first time, putting something in generates a return proportional to what you've accumulated and how honestly you've captured it. This is the mechanism that makes capture sustainable.

**Truth in, AI literacy out.** The thesis of this paper is that personal micro-capture is the missing substrate: the onramp between the empty box and the personally meaningful AI conversation. Zero-friction capture is the precondition for building it. When the cost of entering approaches zero, and the accumulated data produces value through AI conversation, the PhyDigit optimization tips decisively toward capture. This paper asks what follows.

### The Intervention: IN.
IN. (intoyourspace.com) is a personal micro-capture platform built on three principles:
1. **Zero decisions on the way in**: the only act is capture; no category, no tag, no priority
2. **Your data stays yours**: Google Form → Sheet → personal archive you can see and query
3. **The value is in the return**: accumulated captures become a personal AI conversation partner

This paper presents a formative study of IN. with a first cohort: 25 people, 4 weeks, structured as a micro-capture course, with pre/post measurement and optional semi-structured interviews.

### Contributions
1. **LLM literacy as construct**: a framework distinguishing LLM literacy (personal meaning-making through AI conversation grounded in one's own data) from existing AI literacy frameworks focused on tool understanding
2. **The scaffold model**: personal micro-capture as the zero-friction onramp that makes AI conversation personally meaningful
3. **Stage taxonomy**: an empirically grounded characterization of LLM literacy development stages observable over 4 weeks
4. **The friction answer**: empirical data on whether lowering CostEngaging tips the PhyDigit optimization toward capture: and what changes as a result
5. **Design implications**: for AI onboarding, personal informatics, and community-based learning around LLM tools

---

## 2. Related Work

### 2.1 The Micronote Lifecycle
Lin et al. (2004) identified the lifecycle of a micronote: trigger, record, transfer, maintain, refer, complete, discard, archive. Their work, and the body that followed it, focused primarily on the *record* stage: how to get things in. The consistent finding: digital capture lags paper.

Karlson, Andrew & Brush (CHI 2009) conducted a controlled study of input modality (voice, ink, keyboard) for micronotes. Even with near-perfect transcription quality, paper remained the preferred modality for nearly half of participants. The paper concluded that transcription quality alone would not drive digital adoption; the value of what happens *after* capture would need to be demonstrated. That paper studied the cost of engaging. This paper studies what happens when the value of engaging compounds.

### 2.2 The PhyDigit Framework
Karlson, Smith & Madinei [arxiv, under review for CHI] developed the PhyDigit Framework for understanding mobile device use friction. The framework models device engagement as an informal cost minimization: Cost(engaging) vs. Cost(refraining), across seven constituent costs: Social, Cognitive, Physical, Productivity, Opportunity, Health, Safety: modulated by context.

The framework established that friction is not a single barrier but a multivariate optimization, and that users perform this calculation instantaneously and continuously. We apply this framework to self-capture: entering a thought into your personal space vs. letting it dissipate. IN. is designed to minimize CostEngaging to near zero. This study observes what follows.

### 2.3 Personal Informatics & Self-Tracking
The personal informatics literature (Li et al. 2010; Choe et al.; Epstein et al.) documents a five-stage model: prepare, collect, integrate, reflect, act. Most work in this space has focused on quantified, sensor-derived metrics: steps, sleep, heart rate, mood ratings.

IN. is qualitative and interpretive. The captured signal is meaning, not measure. The "integrate/reflect" stages are powered by LLM conversation rather than algorithmic dashboards. The gap in the literature: what happens to the lifecycle when the reflection stage is a conversation with your own data?

### 2.4 AI Literacy & LLM Fluency
Existing AI literacy frameworks (Ng et al. 2021; Long & Magerko 2020) address what people should know *about* AI systems: how they work, how to evaluate their outputs, their ethical implications. These are important but insufficient for our purposes. A user can pass an AI literacy test and still stare blankly at a prompt field.

We propose **LLM literacy** as a distinct construct: the ability to formulate personally meaningful questions to an AI system, grounded in one's own data, and to interpret and act on the outputs. This is not knowledge about AI: it is fluency *with* AI, developed through practice. The distinction matters: it shifts the design question from "what should users understand?" to "what conditions allow fluency to develop?"

*[This section warrants further development in dialogue with a learning sciences collaborator. Potential framework: Collins (Ontario Tech) on skill acquisition and AI tool fluency as a candidate theoretical lens: see Section 10.]*

### 2.5 Skill Acquisition & Language Learning as Analogues
The development of LLM literacy bears structural resemblance to both skill acquisition and language learning: two bodies of theory that offer useful scaffolding for this paper's claims.

**Skill acquisition**: Dreyfus & Dreyfus (1980) proposed a five-stage model of expertise development: novice, advanced beginner, competent, proficient, expert: in which learners move from rule-following toward intuitive, contextually sensitive judgment. Applied here: IN. participants begin as novices (what do I capture? what do I ask?) and, over four weeks, we observe whether and how they progress. The markers of stage transition are an empirical contribution of this study.

**Language acquisition**: Krashen's Input Hypothesis (1982) proposes that acquisition occurs when learners receive *comprehensible input*: material slightly above their current level, grounded in context they already understand. Personal data is exactly this: comprehensible, personal, inherently meaningful input. The LLM conversation partner operates on material the user already knows, making the exchange immediately interpretable. This may be why personal data is a more effective onramp than generic AI prompting: the content is already *in* the user's Zone of Proximal Development (Vygotsky 1978).

**Learning curves**: The power law of practice (Newell & Rosenbloom 1981) predicts that performance improves rapidly at first and then flattens. Capture behavior, query sophistication, and vocabulary development in this study may follow this pattern: or may show discontinuous jumps (insight events) characteristic of restructuring learning. Both are interesting findings.

The common thread: literacy is not transmitted, it is developed through repeated, contextually grounded practice. IN. is designed to provide exactly this: low-friction, high-frequency, personally meaningful practice: and this study asks what that produces.

### 2.6 Reflective Practice & Learning Theory
Kolb (1984) proposed the Learning Cycle: concrete experience → reflective observation → abstract conceptualization → active experimentation. Schön (1983) described Reflective Practice as knowing-in-action and reflection-in-action: the practitioner's ongoing dialogue with their own experience.

IN. operationalizes the Kolb cycle on personal data: capture (experience) → query (reflection) → insight (conceptualization) → behavior change (experimentation). The 4-week course is designed to move participants through this cycle deliberately, with the course structure aligned to the cycle's stages.

---

## 3. System: IN.: Your Space

*IN. is a personal micro-capture platform developed and deployed by the first author. This paper presents a formative study of its first public cohort. Following standard CHI practice for practitioner research, this conflict of interest is disclosed explicitly: the first author designed the system, ran the course, and conducted the research. Independence is maintained through independent measurement framework and survey validation (Smith) and a grounded theory analysis approach that does not presuppose findings. The goal of the study is to understand how people engage with personal micro-capture and LLM conversation: not to validate IN. as a product.*

### 3.1 Design Principles
- **Zero decisions on the way in**: the only question is whether to capture; no category, tag, or priority required
- **No categorization at entry**: classification happens downstream (Claude Haiku, asynchronously), not at capture time
- **Your data stays yours**: Google ecosystem throughout; participant owns the Sheet
- **Emergent lenses**: what the data is *for* is discovered through use, not prescribed by the system or researchers. Lenses are named after participants discover them, not before.

### 3.2 The Capture Interface
- **Google Form** (mobile-first, single field): submit anything; nothing is wrong to capture
- **Google Sheet**: personal archive, always visible, always inspectable by the participant
- **Just Landed** (Apps Script web app): lightweight view of recent captures; simple, fast, theirs
- **Experimental views**: introduced in working calls based on participant-expressed interests; not predetermined

### 3.3 The Conversation Interface
- **Gemini / Google AI in Sheets**: participants query their own data in natural language
- No custom AI interface is required for the study; the Sheet is the interface
- The act of forming a question to one's own accumulated data is the primary literacy event we study
- Participants are shown how to query in Week 1; what they ask, and how that evolves, is observed

### 3.4 The LLM Literacy Progression: A Working Framework
*Working draft, May 2026. To be refined against empirical findings from the study.*

The IN. system is designed to scaffold users through a developmental progression toward LLM fluency. This progression is not prescribed to participants: it is a theoretical model against which observed behavior will be coded. The stages connect directly to the skill acquisition literature (Dreyfus & Dreyfus 1980; §2.5) and the Kolb learning cycle (§2.6).

The core design claim: **the blank box is not the onramp. The capture habit is the onramp.** Each stage unlocks the next; no stage can be skipped.

| Stage | Name | What the user does | Input | Output |
|---|---|---|---|---|
| 1 | **Vote** | Capture. Say yes. Binary act: nothing more required. | Anything. Stream of consciousness. | Nothing yet. The friction of a lost thought is removed. |
| 2 | **View** | Look at their space. Read what they captured. | Same data. | A view. No query skill required. Recognition that the data has value. |
| 3 | **Tweak** | Modify a prompt, adjust phrasing, observe that output changes. | Same data + a small prompt modification. | Noticeably different result. The feedback loop between input and output becomes legible. |
| 4 | **Expand** | Bring new classes of data in; discover new classes of question. | New input types: documents, images, exports, message threads, health data, financial data. | New question categories emerge that were not previously possible. *"Never buy another insight app."* |
| 5 | **Formulate** | Intentional, composed query. | `[personal data] + [context] + [question] + [lens] + [output format]` | Genuinely personal, unrepeatable output. The answer is only possible because it is theirs. This is LLM literacy. |
| 6 | **Extend** | Design lightweight agents or pipelines that automate stages 2–4. | Intent + data sources + permission grants. | Goals accomplished rather than questions answered. System acts on behalf of user's stated values. |

**Design notes:**
- Stage 1 is the entire ask for Week 1 of the course. No query instruction yet.
- The transition from Stage 2 → 3 is the first literacy event: the user discovers they can change the output by changing the input. This is the moment to observe. *Behavioral marker:* the user spontaneously questions the system's boundaries: *"but what about my email?"* or *"could it look at my calendar?"*: without being prompted. This indicates Stage 3 reasoning beginning to form: the user is already thinking in terms of expanding the data substrate. The course is designed to both elicit and answer this question. Participants are assigned to ask something that seems like it probably won't work; the course session ensures the answer is delivered concretely and cleanly, not theoretically. The "stunned YES" is the designed moment.
- Stage 4 is enabled by the current multimodal capabilities of LLMs (documents, images, spreadsheet exports, health exports, financial data). The same interface that answers generic questions can analyze a bank statement, a text thread, a step-count export, or a genealogy database export. No specialized app required.
- Stage 5 is the research target: the full query formulation pattern `[data]+[context]+[question]+[lens]+[output format]`. The CHI paper asks: does IN. scaffold users to Stage 5, and what does the developmental arc look like?
- Stage 6 is horizon/post-study. Not measured in this study but observed qualitatively if it emerges.

**Relationship to the OpenAI ChatGPT usage data (Chatterji et al. 2025):**
OpenAI's own analysis of 1.1M ChatGPT conversations finds that ~24% of usage is "Seeking Information": which the paper explicitly calls "a very close substitute for web search." Only 1.9% of conversations involve personal reflection or relationships. The vast majority of use sits at Stage 2 or below in the above framework: users receive outputs but are not bringing personal data or formulating personally meaningful questions. This is not a capability gap: the tools are capable of Stage 5 interactions. It is a scaffolding gap. IN. is designed to close it.

### 3.5 The Lens Architecture: A Three-Stage Transformation Model

A lens is not a single prompt. It is a three-stage transformation pipeline, each stage independently parameterizable. Formalizing this structure is a design contribution of this paper; it provides the vocabulary for how the IN. community creates, shares, and characterizes analytical lenses.

**The pipeline:**

```
[Input bundle]        : which data, scoped how (time range, data type, relationship, topic)
        ↓
[Framework]           : what analytical vocabulary is applied to the input
        ↓
[Intermediate result] : the analytical reading: framework-complete, format-free
        ↓
[Output rendering]    : score / narrative / clinical / humorous / post / visualization
```

**The intermediate representation.** The key architectural insight is that the framework is applied to the data *once*, producing a format-free analytical result. Output rendering is a separate pass on that result. Applied to a conversation thread, a Gottman framework produces an intermediate result of the form: *instances of the Four Horsemen, bids for connection and responses, positive-to-negative exchange ratio*. From that single analytical result, the system can generate a clinical score, a plain-language narrative, a humorous verdict, or a shareable post. The analytical work is decoupled from the presentation choice.

This decoupling has two important consequences. First, framework and output format are orthogonal: a lens can be research-rigorous and delivered humorously: the evidence basis of the framework is not diminished by a playful rendering. Second, the intermediate result is potentially inspectable: users can see the analytical layer before the output rendering, which supports the transparency-over-magic design principle (§3.1) and is itself a literacy event.

**The lens template.** A well-formed lens specifies all three stages:
- *Input view*: which subset of the user's data is relevant, how scoped
- *Framework*: what analytical vocabulary is applied, and at what evidence-base level
- *Output format*: how the result is rendered (score, narrative, verdict, post, visualization)

A prompt that underspecifies these stages produces less personally precise output. The LLM literacy progression (§3.4) can be understood as the development of the user's ability to fully specify all three stages: Stage 5 (*Formulate*) is precisely the capacity to compose a complete lens rather than a generic query.

**Framework evidence-base axis.** Lenses differ meaningfully in the research grounding of their framework stage. At one end: clinically validated frameworks with longitudinal research support (Gottman Method, CBT, DBT). In the middle: practitioner frameworks with moderate evidence bases (NVC, Motivational Interviewing, Attachment Theory). At the other end: editorial or artistic lenses with no research claim ("what would your 90-year-old self say?", "roast this"). This axis characterizes the framework stage only: it is orthogonal to output format. A rigorous framework can produce a humorous output; an editorial lens can produce a clinical-sounding report. The evidence axis does not determine quality or user value; it determines what claim the lens is making.

*Note: the system design questions: whether the intermediate result is a computed artifact, how output rendering is implemented, lens composability: are deferred to a dedicated design session. What is documented here is the conceptual architecture, not the implementation.*

---

## 4. Study Design

### 4.1 The Micro-Capture Course
A structured 4-week course, modeled on community-based learning cohorts (e.g., McCowen 2026; Atthey 2025), with:

| Week | Event | Duration | Purpose |
|------|-------|----------|---------|
| 0 | Pre-survey + setup | Async | Baseline; set up your space |
| 1 | Kickoff call | 1 hr | What IN. is; first capture; homework assigned |
| 2 | Working call | 1 hr | What did you capture? First queries; what surprised you? |
| 3 | Working call | 1 hr | Evolving use; emerging patterns; what do you want to know? |
| 4 | Wrap-up call | 1 hr | What changed? What would you keep? |
| 5 | Post-survey | Async | Post-measurement; reflection |

- Async community channel active throughout (optional; behavior observed, not required)
- Homework after Weeks 1–2: structured capture prompts + open capture
- Optional paid semi-structured interview (~1 hr) within 2 weeks of course end

### 4.2 Participants
- Up to 25 adults, 18+
- Recruited through Amy Karlson's personal network, Substack, and community partners
- No prior AI tool experience required; diversity in AI familiarity is methodologically desirable
- Incentive: free course participation; interview participants compensated at market rate
- Research intent disclosed at enrollment: "I am a researcher studying how people learn to use AI through personal data"

### 4.3 Ethics
- REB approval through institutional affiliate (Auburn University, Smith; or alternative IRB pathway)
- Informed consent at enrollment: captures analyzed in aggregate; individual data never published without explicit permission
- Community chat: participants informed it may be analyzed as research data; opt-out available
- Interview data: recorded and transcribed with explicit consent; identifiable details anonymized in publication

---

## 5. Research Questions

### On Entry Behavior (the capture side)
- **RQ1**: What do people capture in Week 1: what categories emerge, what length, what tone?
- **RQ2**: How do capture patterns evolve over 4 weeks: frequency, length, category breadth, vocabulary?
- **RQ3**: What does entry timing reveal: when do people capture, and does the pattern shift?
- **RQ4**: Is there a critical mass before the system feels alive? What does the drop-off pattern look like, and what happened just before?
- **RQ4b**: Does input modality (voice vs. typing) correlate with entry length? Does that relationship shift as the capture habit matures? *(Ascertainable from logs + one survey question; connects to Karlson, Andrew & Brush 2009 on modality and capture behavior.)*

### On Query Formation (the conversation side)
- **RQ5**: What is the first question people ask their own data: and what prompted it?
- **RQ6**: How does query sophistication evolve: from specific to abstract, from fact-finding to insight-seeking?
- **RQ7**: Do people begin generating their own query templates? When does this appear?
- **RQ8**: What is the first moment a user feels surprised or "seen" by their own data?

### On LLM Literacy Development
- **RQ9**: What stages of LLM literacy are observable across the cohort? What are the behavioral and linguistic markers of each stage?
- **RQ10**: How does language around AI and self-knowledge evolve over 4 weeks: in calls, in the community channel, in interviews?
- **RQ11**: What accelerates or delays literacy development: prior AI experience, capture volume, social sharing?
- **RQ12**: Is there a "teach yourself to fish" moment: when does self-directed, generative query formation begin?

### On Community & Social Dynamics
- **RQ13**: What do people share in the community channel: insights, how-to, emotional resonance, data?
- **RQ14**: Does the cohort naturally become a maker space: do people co-create queries, share templates, build on each other's frameworks?
- **RQ15**: Does observing others' queries (never their data) change how a participant crafts their own?

### On the Friction Question (connecting to PhyDigit)
- **RQ16**: As perceived value of accumulated data grows, does capture frequency increase?
- **RQ17**: What are the stated barriers to capture: and do they map to PhyDigit cost categories?
- **RQ18**: At what point, if any, does entering feel like lower friction than not entering?

---

## 6. Data Collection

| Source | What It Captures | Timing |
|--------|-----------------|--------|
| Google Form + Sheet logs | Capture frequency, timing, length, vocabulary evolution | Continuous (4 wks) |
| Pre-survey | AI familiarity, self-reflection habits, baseline attitudes | Week 0 |
| Post-survey | Same measures + system attitudes, habit formation, literacy self-report | Week 5 |
| Community channel | Sharing behavior, language evolution, peer influence, query sharing | Ongoing |
| Homework responses | Directed capture behavior; first query attempts | Weeks 1–2 |
| Call recordings / notes | Real-time reactions, breakthrough moments, questions asked | Weeks 1–4 |
| Semi-structured interviews | Deep retrospective: vocabulary, insight moments, behavior change, literacy arc | Post-course |

---

## 7. Analysis Plan

- **Behavioral analysis**: Google Sheet logs → frequency curves, vocabulary evolution over time, category broadening, timing patterns
- **Survey analysis**: pre/post delta on AI familiarity, self-reflection confidence, capture habit formation; Missie Smith leads measurement framework and instrument validation
- **Qualitative coding**: grounded theory approach (consistent with PhyDigit paper methodology) applied to community chat, interview transcripts, call notes → emergent LLM literacy stage taxonomy
- **Discourse analysis**: language evolution around AI and self-capture across calls and community channel over 4 weeks
- **Friction mapping**: participant-reported barriers coded against PhyDigit cost categories; capture frequency plotted against self-reported value accumulation

---

## 8. Anticipated Contributions

1. **LLM literacy as construct**: a framework distinguishing LLM literacy from AI literacy; applicable beyond IN. to any personal-data-grounded AI interface
2. **The scaffold model**: personal micro-capture as the zero-friction onramp: a replicable design pattern for AI onboarding
3. **Stage taxonomy**: empirically grounded stages of LLM literacy development in first-time users, with behavioral markers for each stage
4. **The friction answer**: data on whether PhyDigit CostEngaging reduction tips behavior toward capture, and the downstream effects
5. **Design implications**: for AI interface designers, personal informatics researchers, and community learning practitioners

---

## 9. Timeline

| Milestone | Target |
|-----------|--------|
| Reach out to Missie Smith re: survey design and co-authorship | May 2026 |
| Arxiv submission: PhyDigit / subtlety paper | June 2026 |
| REB submission (Auburn University, or alternative) | June 2026 |
| REB approval | July 2026 |
| Participant recruitment | July–August 2026 |
| Course runs | August–September 2026 |
| Interviews | September 2026 |
| Data analysis | September–October 2026 |
| Paper draft | October–November 2026 |
| CHI 2027 submission | ~November 2026 |

*Note: CHI 2027 deadline TBC: verify at chi2027.acm.org when announced.*

---

## 10. Team & Roles

This is Amy Karlson's research program. The study design, the platform, the course, and the paper are hers. Collaborators are invited because they bring specific expertise that strengthens the work: not because the work depends on them.

| Person | Role | Institution | Status |
|--------|------|-------------|--------|
| Amy K. Karlson | PI; study design; IN. platform; community layer; paper lead | Independent / intoyourspace.com | Confirmed |
| Missie Smith | Measurement framework; pre/post survey design and validation; PhyDigit connection | Auburn University | Proposed |

**If Smith confirms:** Survey instruments are formally validated. PhyDigit lineage is explicitly co-claimed. REB filed through Auburn University.

**If Smith does not confirm:** Alternative REB paths exist (commercial IRB; other institutional affiliate). The study proceeds. The paper proceeds solo-authored. The research questions, the platform, and the findings stand on their own.

**Potential additional collaborator:** Christopher Collins (Ontario Tech, CS): learning sciences and AI literacy framework development. Would strengthen Section 2.4–2.5 and could serve as secondary REB affiliate. Bring in only if Smith sees benefit; not on the critical path.

---

## 11. Prior Work Lineage

This paper is the third in a line, all authored or co-authored by Karlson:

1. **Karlson, Andrew & Brush (CHI 2009)**: studied the INPUT side of micronote capture: input modality friction, why paper persists. Concluded: demonstrating the value of accumulated digital captures (search, share, reflect) will be necessary for adoption.
2. **Karlson, Smith & Madinei (arxiv, under review)**: the PhyDigit framework: cost optimization model for mobile device engagement. Established that friction is a multivariate optimization, and modeled the simultaneous costs of engaging and refraining.
3. **This paper**: operationalizes the output-value hypothesis from 2009, using PhyDigit to understand the friction question, and proposes a scaffold model for a new literacy: the ability to have a meaningful AI conversation grounded in one's own data.

---

## 12. Why Now: A Note on Research Trajectory

*(Parenthetical framing for collaborators, readers, and the record.)*

This paper arrives at a specific moment: and that moment is not accidental.

In 2009, the first author studied why people wouldn't put their thoughts into a phone. The answer was friction: the cost of entering was higher than the cost of forgetting. The paper concluded that demonstrating downstream value would be necessary to change that calculus. It didn't predict what form that value would take.

In the years between, the same author studied the physics of living simultaneously in digital and physical worlds: the invisible optimization every device user performs dozens of times a day, the cost function nobody had named. That framework now has a name: PhyDigit.

Then LLMs arrived. And with them, something the field had not quite anticipated: the empty box as the dominant interface paradigm. The blank text field. The cursor. The implicit demand: *tell me what you want.* For most people, that demand is paralyzing. Not because they lack curiosity: but because they have never been given a substrate, a directive, or a scaffold.

The research agenda that began with a study of micronote capture on a Windows Mobile phone has arrived, naturally and without forcing, at the central design question of the current moment in HCI: **how do ordinary people learn to have a meaningful conversation with AI?**

The answer this paper proposes is not a better interface. It is a better onramp. Give people a box. Tell them to put things in it. Ask no questions on the way in. Then, when the box is full enough to hold a conversation: ask them what they want to know.

LLM conversation is becoming the new universal language of HCI. The keyboard replaced the command line. The touchscreen replaced the keyboard. The conversation interface is replacing the touchscreen: not for everyone, not yet, but directionally and irreversibly. The question the field must now answer is the same question it has always answered at each transition: *who gets left behind, and how do we bring them with us?*

IN. is an answer to that question. This paper is the first empirical test of whether it works.

---

*Working document. Not for distribution without author permission.*
*Last updated: May 2026*
