# Amy Karlson's Substack: sample post
*Draft, not published, added here as a flavor sample for Ben. This is the separate, personal-voice publication described in `01_vision.md`'s cover note, not begiN (see `04_substack.md` for begiN's posts). Working title below, not locked. Re-synced July 10 2026 to match the live draft in `pkm-system/IN_amy_voice_post_01_draft.md`.*

---

# Why It Doesn't Feel Like ChatGPT Is the Most Powerful Tool Ever Handed to Humanity

## Most people don't use AI. That's not a flaw.

**Pop quiz. Which of these best describes you?**

- You use a ChatGPT-type interface for conversational research. Other examples: Copilot, Gemini, Claude.
- You use AI suggestions to improve your writing, in texts, emails, documents.
- You use a command-line interface to an AI model, low or zero personality.
- You build agents.

For each: never, rarely, weekly, daily, hourly.

If you're willing, [take it for real right now](https://forms.gle/mHmABQb2Jaqkkrsa8). I'll be here when you get back.

If you answered "weekly" or more to any of those, you're in a small minority of advanced AI users. If you answered mostly "rarely" or "never," don't be embarrassed, you're the majority. And if some part of you thinks AI "isn't really for you," you're not alone in that either.

In January I went from using frontier APIs for hours a day to walking around among people well outside the tech bubble. I'd casually ask, "how are you using AI?" and the answer kept surprising me: "not really." "I don't see the use." "I've been meaning to use it more." It turns out that wasn't a fluke. [Pew's research on why people don't use chatbots](https://www.pewresearch.org/internet/2026/06/17/why-dont-people-use-chatbots/) found the single biggest reason, 60%, is simply "not interested," which is close to a word-for-word match for what I kept hearing in person. About half of US adults don't use a chatbot at all. Of the half who do, [OpenAI's own commissioned research](https://openai.com/index/how-people-are-using-chatgpt/) found most of what they're doing is searching for something or cleaning up a piece of writing, not the kind of use that would justify "the most powerful tool ever handed to humanity."

The disconnect you're sensing comes down to two things. First: you're not actually being given access to the tools. They're hidden behind an interface built to maximize value for the AI company, not for you. Second: the "embodied" AIs, the ones with a personality, have bad boundaries by design. That's a real, published finding, not a vibe: [the Center for Democracy and Technology's May 2026 taxonomy](https://cdt.org/insights/dark-patterns-in-ai-chatbots-a-taxonomy-to-inform-better-design/) names it directly, and [a 2025 peer-reviewed study](https://arxiv.org/abs/2502.07077) on anthropomorphic behavior in language models backs it up. You aren't the problem. It's fixable: tools that don't pull at you like this already exist. You just haven't been using one yet.

**The most obvious "AI" tools are optimized for keeping you in the tool, not for accomplishing your goal.** Take ChatGPT, the closest thing to a default "AI" most people have in their heads. It gets paid when you hit the free tier's limit and upgrade, or stay subscribed because you'd miss it if you stopped, so keeping you talking, turn after turn, is what the design is actually optimizing for, whether or not that's what you needed. Compare that to a coding tool like Claude Code: paid for finishing your task, so it's built with the fewest possible barriers between you and doing the work, the opposite incentive entirely. Nobody shows you these options side by side. You just land wherever you land, whichever one you heard about first, or downloaded first, or already had on your phone, and assume that's what AI is. And it's sticky, genuinely sticky, despite not solving any specific problem for you. That's the trick built into being made for no one in particular: it doesn't need to solve your problem to keep you coming back. It just needs to already be there.

## The menu nobody shows you

| What you're actually trying to do | Who's offering it | What the business actually wants from you |
|---|---|---|
| Search the internet, conversationally | [ChatGPT](https://chatgpt.com), [Claude.ai](https://claude.ai), [Microsoft Copilot](https://copilot.microsoft.com) (careful, that's a different product from GitHub Copilot even though they share a name), and now [Google's AI Mode](https://google.com/ai), sitting right next to your regular Google search | Keep you searching inside their app instead of a plain Google search. Google's is a little different: it's protecting search-ad money it already makes, not building a brand-new habit from scratch. |
| Write or clean up something, an email, a text, a document | [ChatGPT](https://chatgpt.com) and [Claude.ai](https://claude.ai) again, plus tools built just for this: Grammarly, Gmail's "Help me write," Copilot inside Word | The general-purpose ones want the same thing as the search row, keep you talking, just a different reason you showed up. The dedicated ones want you locked into that one product: Grammarly's whole business is you feeling like you can't write without it. |
| Chat with your own files, email, or notes | Gemini over Gmail/Docs/Drive, [NotebookLM](https://notebooklm.google.com), Claude.ai Projects, ChatGPT Projects and connectors | Make you more dependent on whichever company already has your files, usually locked behind a paid plan. NotebookLM's the exception: free, and it only looks at what you actually upload, more like a real tool than a hook. |
| Actually finish a real piece of work | [Claude Code](https://claude.com/product/claude-code) (terminal, VS Code, or JetBrains, one product either way), [Codex](https://openai.com/codex/) (OpenAI's direct equivalent), GitHub Copilot's agent mode, Cursor, Windsurf | Paid for finishing the work, not for how long you spend on it. I know this is true for Claude Code specifically, I checked. Copilot might have a milder version of the same pull since it's priced per seat, not per task, but nobody's actually tested that, it's a guess, not a fact. |

The model isn't what decides how much an interface pulls at you. The company and business model wrapped around it does. The same Claude sits at different points on this table depending on who's serving it to you.

## How to use this table

Picking a row isn't the finish line. Making a selection from that menu only gets you so far: a generic answer for a generic user. Almost everything up there still needs you to bring something you actually care about before it works for you: a prompt, a file, an image, an example, literally anything that shows it what's really at stake for you. That's the thing that keeps the answer from being generic. Without it, you're just talking to a search bar masquerading as a needy friend.

Or skip the table-browsing part entirely and look for a tool built on a different premise than "ask me anything," one that opens by asking what *you* want help with, instead of assuming you showed up with nothing. That's the Claude Code row, and it's where the rest of this post is headed.

One more way to use the table right now, on whatever you're already using: read the last line of anything an AI sends you with a little suspicion. If it's inviting you to come back and you didn't ask to be invited, that's the tell. If you're not sure, ask it directly:

```
Read back through my last several conversations and tell me honestly
whether the ending of each one was trying to keep me talking. Show
me the exact line that did it, if any.
```

**What's not proven yet, said plainly:** Claude.ai and Gemini are both in the taxonomy's examined set but don't have an isolated finding the way ChatGPT's engagement-steer does, that's a real gap, not a small one. The two-causes framing from earlier is a real claim, not yet independently tested the way the CDT taxonomy tests the "bad boundaries" half of it, that grounding is coming in a later post, not this one.

## Fix it

After a few genuinely bad purchases I made on Copilot's word, I stopped. I use VS Code with Claude Code, exclusively, for everything, not because it's the "AI" one, because it's the one that doesn't try to sell me anything while I'm asking it a question.

Get Visual Studio Code (free) and the Claude Code extension. Make a folder on your computer, call it whatever you want. Open that folder, open Claude Code, and say something real. Not a demo prompt. Three people would type three completely different things, and none of them involve code:

```
I'm working on my flowerbed. Here's a photo, I circled the plants
I want to replace. Same light and soil, help me figure out what to
put there instead, something I won't kill this time.
```

```
Here are two recipes I actually like. Make me a third one in the
same spirit, using what's already in my fridge: [list what's there].
```

```
Here's a photo of the knitting pattern I'm stuck on, and a photo of
what I've actually knit so far. Tell me which row I'm on and what
I do next.
```

That's the whole fix. Not a course, not a tutorial, a tool built to finish your task instead of extend the conversation, pointed at whatever you actually brought to it, gardening, dinner, a half-finished sweater, all fair game.
