# AI Endpoint Lens

**Status:** v1, July 8 2026. A lens for choosing where to do your thinking, not for judging anyone who's using the wrong one, they didn't know there was a choice.

---

## What This Is

Every AI product is a different endpoint into the same underlying capability, and every endpoint is designed for a specific customer with a specific incentive shaping it. Nobody tells you this. You just end up wherever you first landed, usually the one that was first to market, and assume that's what AI is.

This lens exists so a reader can look at the actual menu, real customer, real features, real and imagined barriers, and the actual steer built into the design, and choose on purpose instead of by default.

**Honesty rule, load-bearing:** no one is an expert at this, the interfaces themselves are barely a few years old and keep changing. This lens is a snapshot, not a verdict, and it should be revised as products change rather than treated as settled.

---

## The Framework

For each endpoint:

| Dimension | Question it answers |
|---|---|
| Target customer | Who was this actually built for? |
| Core features | What does it actually do well? |
| Real barriers to entry | Cost, technical setup, what genuinely stands between a new user and using it |
| Imagined barriers to entry | What people assume stops them that doesn't actually |
| The steer | What direction does the design nudge the interaction toward? (verified against real research where possible, flagged as unverified where not) |

---

## The Endpoints

| Endpoint | Target customer | Core features | Real barriers | Imagined barriers | The steer |
|---|---|---|---|---|---|
| ChatGPT (consumer, web/app) | Mass market, first-to-market default | General chat, image gen, voice mode, memory | None, free tier exists | None, it's the one people think requires no barrier at all | **Verified:** continued engagement. CDT taxonomy (May 2026) names "user autonomy compromised for engagement" and "false social and emotional connection" as documented categories; Sarah's transcript (`claude_convos/sarah_chatgpt_relationship_pull.md`) is a live example. |
| Claude.ai (consumer chat/app) | Similar mass-market surface to ChatGPT | General chat, artifacts, projects, memory | None, free tier exists | Same as ChatGPT, people don't know it's different underneath | **Not yet independently verified.** Included in the CDT taxonomy's product set but no confirmed finding here distinguishing it from ChatGPT's specific pattern. Don't assert a steer that hasn't been checked. |
| Claude Code (VS Code extension / CLI) | Developers, technical workflows | Full filesystem access, tool use, multi-step agentic work, runs your own scripts | Real: requires comfort in a terminal or code editor, no polished onboarding for non-technical users | Perceived-but-often-false: "I'm not a developer, this isn't for me." The actual bar is lower than the interface implies, see Post 4 ("All iN," parked, `IN_post_arc.md`) | Built to get out of your way and work your agenda. Task-completion pricing model, not engagement-optimized. Structural contrast with the row above, not incidental. |
| Gemini / Google surfaces (chatbar, sidebar) | Existing Google ecosystem users | Integrated into Search, Docs, Workspace | Low, most people already have a Google account | Unclear, not yet researched | **Not yet researched. Do not publish a claim here until it's checked with the same rigor ChatGPT got.** |
| Copilot / other assistants | Not yet researched | — | — | — | **Not yet researched.** |

---

## How To Use This

Ask yourself one question: what do I actually want out of this interaction, a finished answer and nothing else, or company along the way? Neither is wrong. The failure mode isn't picking the wrong one, it's not knowing there was a choice, and getting steered somewhere by default that doesn't match what you actually needed.

**Rows with a real, verified steer can be stated as fact. Rows marked unresearched should stay marked that way until someone actually checks**, same discipline the rest of this project's research has held to (see `IN_research.md`'s interface-surface tracking).

---

*v1, July 8 2026. Two rows verified, three flagged honestly as not yet researched. Revise as products change and as the unresearched rows get real attention, don't let this go stale and get cited as settled.*
