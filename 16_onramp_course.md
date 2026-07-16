# The On-Ramp: A 5-Week Course

**Status:** July 2026. First full curriculum draft, written in direct response to a portfolio-feedback exchange with Merrie Morris (full exchange: `claude_convos/merrie_morris_feedback_exchange.md`). Pairs with the pricing shape sketched in `01_vision.md` §6 and the sandbox-not-movement framing in §2.5.

---

## The Idea in One Line

People don't need prettier interfaces to start using AI well. They need something of their own to bring to it first. This course builds that, one week at a time, starting with zero AI.

## What You're Actually Building

Google Sheets as a personal database, with views that can be raw (just the spreadsheet), programmatically generated (scripted dashboards, filtered displays), or skinned as custom forms by topic. A step-count input and a to-do list input could be two separate forms, one conditional form, or auto-imported from an adjacent app like Apple Health. The user decides, with scaffolding. This is not a fixed product they adapt to. They are learning to tune the interface to themselves, not waiting for someone to tell them what they should want to track.

## The Curriculum

| Week | Theme | What you do | What you gain | Tech |
|---|---|---|---|---|
| 1 | The Sandbox | Capture anything you will want to return to. No filter, no category. Raw list. | The habit of noticing and recording. Return as the reward. | Google Form + Sheets. Zero AI. Raw view only. |
| 2 | The Refinement | Use Gemini to build and iterate on custom forms and views. To-do view with followable links, keyword search, simple chart. Rebuild the form to fit your own workflow. | First AI touch: but for building the tool, not querying personal data. Customization as skill. | Apps Script for views. Gemini to generate and iterate on forms. No triggers yet. |
| 3 | The View | Build views that reflect your data back to you: word cloud, calendar or time series of entries, theme clusters. Apps Script digests screenshots from your captures folder. Nothing flashy: practical, occasionally surprising. | Reading your own signal. Seeing patterns you didn't consciously track. | Apps Script for screenshot digestion. Sheets infoviz. Gemini for simple queries over captures, within Google ecosystem only. |
| 4 | The Engine | Practice asking questions over your behavioral data. Free tier: iOS Shortcut logs daily steps to Google Sheets automatically; ask Gemini "what's my average this month?" Advanced: Gemini Advanced queries your inbox ("what are the themes of my last 5 todos?") and sets up a scheduled digest. | AI as presentation layer over your own material. Prompt-as-recipe. First automation trigger. | Free: iOS Shortcuts + Sheets + Gemini free tier. Advanced: Gemini Advanced ($20/month). Apps Script triggers. Data stays in Google. |
| 5 | The Lens | Build a custom lens for something you care about. AI-ify your hobby. Share the method, not the data. | Generalizable prompt design. Domain transfer. The skill is yours to apply anywhere. | Apps Script Web App (`doGet()`): a real front-end UI over your own data. Shareable lens prompt. |

**Design note on ordering:** AI shows up nowhere in Week 1. That's deliberate, not an oversight. The sandbox has to hold something real before AI is useful for anything, otherwise the course repeats the exact blank-box problem it's trying to solve, one week later and with extra steps.

## What People Trade and What They Keep

By the end of the on-ramp, they've traded almost nothing in privacy for a skill they can generalize to their own lives, automate things, and play with to their heart's content. A new hobby in itself, perhaps. No week requires sensitive data (financial records, health data) to work. Five items in a spreadsheet carries a different privacy weight than a bank statement, and the course doesn't need the second kind to teach the skill.

No one exits with a finished product. They exit with a method: bring a question, bring some material, see what comes back, iterate. And with a working example of it, built on their own data, in their own words.

## Pricing and Cadence

Wraps the graduated pricing shape in `01_vision.md` §6, front-loaded then tapering, not finalized. Weekly live call plus office hours during the 5 weeks (mirrors the community's existing live-session cadence, §6 of `01_vision.md`). Whether a second cohort of "material" gets added past week 5, or the steady state is closer to "find an interest, dig in for a bit, then leave," is genuinely open, including the ~250-400 price-point and call-cadence for what that second cohort would look like. Both outcomes are fine. That's not a hedge, it's the actual design position: some people stay, most pass through, same as any real space.

---

*July 2026. Amy K. Karlson / Smith-Karlson LLC.*
