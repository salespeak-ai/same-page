# Same Page

Same Page checks whether your company says the same thing everywhere. Give it your website. It reads your public pages, shows where two of them disagree (both passages quoted word for word, both linked), asks which version is right, and writes the exact wording to change.

It runs inside the AI assistant you already use: ChatGPT, Claude, Grok, or any agent that can load a skill and fetch web pages.

**Public beta.** Same Page checks the public pages it can access. It can miss issues, and it never changes your website.

## Try it

| Where | How |
|---|---|
| ChatGPT | Open the [Same Page GPT](https://chatgpt.com/g/g-6ad310b0eb848191a8349de53787991b-same-page) and type your website. Needs a ChatGPT account; logged-out visitors cannot chat with GPTs. |
| Grok | Open the [Same Page bot](https://x.ai/bot/BrDgZVp_v3jBEUK7JMzvm), choose **Add to Grok Bot**, and type your website. |
| Claude (claude.ai) | Download [`same-page-claude-skill.zip`](claude/same-page-claude-skill.zip), then in Claude open **Customize > Skills**, choose **Add > Upload skill**, and upload the zip. Start a new chat: "Check my company website: example.com". Claude loads the skill on its own. |
| Claude Code | `/plugin marketplace add salespeak-ai/same-page`, then `/plugin install same-page@same-page`. |
| Any other agent | Load [`same-page.md`](same-page.md) as the agent's instructions. The agent needs a tool that fetches a URL and returns the page text. |

## What it does

1. **Check.** Reads up to 12 pages first: pricing, terms, security and trust center, integrations, product pages, about. Reports within about a minute.
2. **Quote.** Every finding has two exact quotes and two links. A quote that is not in the fetched page text is dropped.
3. **Fix.** Say "fix 1". It shows both passages and asks: A is correct, B is correct, neither, or not sure. It waits for your answer and never picks for you.
4. **Correct.** After you answer, it searches the other pages for the same wrong version and lists every place it found, with the exact current text and the replacement, ready to paste into a ticket. It says how many pages it checked; pages it did not check may hold more.
5. **Not sure.** It writes a short request you can forward to whoever owns the answer, with both quotes and links. No replacement copy.

## What it does not do

- It does not edit your website, contact anyone, or send anything anywhere.
- It does not decide which version is true. Your answer is treated as your proposal, not a verified fact.
- It does not read logged-in pages, files, or internal documents.
- It can miss issues: pages it did not read, text a site builds with JavaScript (trust centers often do), and pages that show AI assistants a different version than people see. Every report lists what was read, partly read, and not read.

## Privacy

Same Page is a set of instructions. The pages are fetched by the AI assistant you run it in, under that assistant's terms. Same Page sends nothing to Salespeak. The only Salespeak link it shows is optional, appears at most once after a completed correction, and carries UTM parameters so we can count clicks.

## Files

| Path | What |
|---|---|
| `same-page.md` | The whole protocol in one file, for any agent |
| `skills/same-page/SKILL.md` | Agent Skill (Claude Code plugin, Claude, other skill-aware agents) |
| `claude/same-page-claude-skill.zip` | The same skill, zipped for claude.ai upload |
| `chatgpt/` | Custom GPT instructions and its knowledge file |
| `grok/` | Grok Bot instructions and skills |

## Feedback

Open an issue, or write to support@salespeak.ai.

Made by [Salespeak](https://salespeak.ai/?utm_source=github&utm_medium=same-page&utm_campaign=same-page-beta). MIT License.
