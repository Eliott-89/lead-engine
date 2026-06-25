# Lead Engine — Claude Skill

> Automated LinkedIn prospecting pipeline powered by **DataForB2B** and **LinkupAPI**.

From a website URL or an ICP, find your ideal B2B leads and send LinkedIn connection requests — all from Claude, in minutes.

---

## What it does

1. **Builds your ICP** from a website URL, an existing ICP, or both combined
2. **Finds leads** via DataForB2B (800M+ profiles, 75M+ companies)
3. **Shows you the list** for validation before anything is sent
4. **Sends LinkedIn connection requests** via LinkupAPI (capped at 15/day for safety)
5. **Saves everything** to a Google Sheet for tracking *(optional)*
6. **Sends prospecting messages** to accepted connections *(coming in Phase 2)*

---

## Install

```bash
npx skills add YOUR_GITHUB_USERNAME/lead-engine
```

Then in Claude:

```
/lead-engine
```

---

## Requirements

You need accounts on both platforms:

| Tool | Purpose | Link |
|------|---------|------|
| DataForB2B | Lead search & enrichment | [dataforb2b.ai](https://dataforb2b.ai) |
| LinkupAPI | LinkedIn connection requests | [linkupapi.com](https://linkupapi.com) |
| Google Sheets | Lead tracking *(optional)* | Built into Claude connectors |

The skill will walk you through setup if you don't have these yet.

---

## How to use

**Option 1 — From a website:**
```
/lead-engine https://yourcompany.com
```

**Option 2 — From an existing ICP:**
```
/lead-engine [paste your ICP here]
```

**Option 3 — Mix both:**
```
/lead-engine https://yourcompany.com + [paste your ICP]
```

---

## Daily routine

Once set up, your daily prospecting takes **~5 minutes**:

1. Run `/lead-engine`
2. Review the lead list
3. Approve → 15 connection requests sent automatically
4. Check your Google Sheet for accepted connections → send messages

---

## Safety

- Daily cap: **20 requests/day** (LinkedIn's safe limit)
- Connection requests sent **without a note** — message goes out only after the connection is accepted
- Always validates leads with you before sending
- Stops immediately if LinkedIn checkpoint is detected
- Never sends twice to the same profile

---

## Powered by

- [DataForB2B](https://dataforb2b.ai) — B2B data API with 800M+ profiles
- [LinkupAPI](https://linkupapi.com) — LinkedIn automation API

---

## License

MIT
