# Contributing to awesome-free-llm-apis

Thanks for helping keep this the most detailed **free LLM API** list on GitHub. Every entry here is manually verified — that's what separates this from auto-scraped alternatives. Please read this before opening a PR.

---

## What We Accept

✅ Providers with a **permanent free tier** — no expiry, no invite, no credit card required to start  
✅ Entries with **all required fields** filled in (see format below)  
✅ Corrections to existing entries (rate limits change — PRs fixing stale data are very welcome)  
✅ New categories if a genuinely new type of **free AI API** provider emerges  

---

## What We Do NOT Accept

❌ Trial credits (e.g. "$5 free for 3 months")  
❌ Time-limited promos or waitlisted access  
❌ Invite-only or closed beta providers  
❌ Providers that require a credit card to activate the free tier  
❌ Providers with no public documentation on what the free tier includes  
❌ Wrappers or aggregators that depend on another paid API under the hood  

---

## Entry Format

Every entry in **awesome-free-llm-apis** must follow this exact format. Do not skip fields — use `Undocumented` if a provider doesn't publish the info.

````markdown
### [Provider Name](https://provider.com/api-keys) 🇺🇸

> One sentence describing what makes this free LLM API notable or unique.

| Detail | Info |
|---|---|
| **Free Models** | Model A, Model B, Model C + N more |
| **Rate Limits** | X RPM · Y RPD ([source](https://docs.provider.com/limits)) |
| **OpenAI Compat** | ✅ Yes — `https://api.provider.com/v1`  /  ⚠️ Partial  /  ❌ No |
| **SDKs** | Python (`package-name`), JS/TS (`package-name`), REST |
| **Speed Tier** | 🟢 Fast / 🟡 Medium / 🔴 Slow |
````

**Field rules:**

- **Free Models** — list the most capable or well-known ones first, then `+ N more` if there are many
- **Rate Limits** — always link to the official docs page where you found the numbers; if limits are not published, write `Undocumented`
- **OpenAI Compat** — test it yourself with a `client.chat.completions.create()` call before marking ✅; use ⚠️ Partial if it mostly works but has gaps; ❌ if it uses a completely different format
- **SDKs** — only list official packages; include the package name in backticks
- **Speed Tier** — pick one based on the legend in README.md; add a short note if relevant (e.g. "LPU-based")

---

## How to Submit a PR

1. **Fork** this repo and create a new branch: `git checkout -b add-provider-name`
2. **Add your entry** in the correct section (Provider API or Inference Provider), in alphabetical order within that section
3. **Update the Quick Comparison table** in README.md with a one-line row for your entry
4. **Add the `base_url`** to the Python provider dict in the Code Snippets section (if OpenAI-compatible)
5. **Note the verification date** in your PR description (e.g. "Verified March 2026")
6. Open a pull request with the title: `Add [Provider Name]` or `Fix [Provider Name] rate limits`

---

## Updating Stale Entries

Rate limits on **free LLM APIs** change without notice. If you find an entry that's out of date:

- Link to the current official docs showing the new limits
- Note the date you verified it
- If a free tier has been **removed entirely**, open a PR to remove the entry and explain why

---

## Speed Tier Guidelines

When assigning a speed tier, use observed output token throughput as a guide:

| Tier | Guidance |
|---|---|
| 🟢 Fast | Purpose-built inference hardware (LPU, wafer-scale chip). Consistently 300+ tok/sec |
| 🟡 Medium | Standard GPU cloud (A100/H100). Typical 50–150 tok/sec, occasional queuing |
| 🔴 Slow | Shared or throttled infra. Cold starts, queuing, or CPU offload common |

If you're unsure, default to 🟡 Medium and note it in your PR.

---

## Questions

Open an issue if you're unsure whether a provider qualifies for **awesome-free-llm-apis**, or if you want to propose a new column or section before writing it up.
