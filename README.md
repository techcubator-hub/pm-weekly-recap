# What this tool does

This is a senior product lead's weekly update generator. You fill in your week once — progress, blockers, and next steps — and it automatically produces three tailored versions ready to send:

- **VP** — concise, outcome-focused, 3–5 bullets
- **GM** — business impact and risk framing
- **Internal team** — detailed, with action items and emoji sections

Each output has a "Copy for Slack" button (Slack-formatted) and a "Copy" button (plain text for email). All three versions can be saved back to Notion in one click.

---

# How to use it

## Step 1 — Open the app

Open the `weekly-recap.html` file in any browser. No installation needed.

First time only: click **⚙ API key** in the bottom corner and paste your Anthropic API key (`sk-ant-…`). It saves to your browser's local storage and never leaves your device.

> Get your key at [console.anthropic.com](http://console.anthropic.com) → API Keys
> 

## Step 2 — Pull from Notion (optional)

Paste any Notion page URL into the source field and hit **Pull from Notion**. The app reads the page and pre-fills the form fields automatically.

Or skip this step and type your updates directly.

## Step 3 — Fill in your updates

Four fields:

- **Progress** — key milestones, decisions made, things shipped
- **Blockers & risks** — dependencies, open decisions, anything slowing you down
- **Next steps** — what's planned for next week
- **Extras** (optional) — wins, shoutouts, context for specific audiences

## Step 4 — Generate

Hit **Generate updates →**. Three tailored versions appear within seconds.

## Step 5 — Send

- Click **Copy for Slack** on any card to copy Slack-formatted text
- Click **Copy** for plain text (email-ready)
- Click **Save to Notion** to write all three versions as a new child page in this Notion project

---

# Setup requirements

| What | Where to get it |
| --- | --- |
| Anthropic API key | [console.anthropic.com](http://console.anthropic.com) → API Keys |
| Notion connected to Claude | [claude.ai](http://claude.ai) → Integrations → Notion |
| The HTML file | Exported from Claude — see `/weekly-recap.html` |

---

# Audience templates

## VP — High-level summary

Executive-ready. Leads with outcomes and impact. 3–5 bullets max. Only flags high-priority risks. No activities, no jargon.

## GM — Business focus

Three sections: Progress, Risks, Next steps. Written in short prose. Frames everything in terms of business impact, revenue implications, and customer outcomes.

## Internal team — Detailed

Four sections with emoji anchors: ✅ Done, ⚠️ Blockers, 🔜 Next week, and Action items. Specific about owners and deadlines. Direct and transparent.

---

# Project context

This tool is part of **Project 1000** — the goal of reaching 1,000 paid subscribers in one year. It was built to reduce the time spent writing weekly stakeholder updates from ~30 minutes to under 5 minutes, while improving consistency and audience-appropriateness across VP, GM, and team communications.

---

# File structure

```
weekly-recap.html    — standalone app, open in any browser
README               — this page
Weekly recap archive — saved outputs, one page per week
```

---

# Troubleshooting

**"Couldn't read that page"** — Check that the Notion page is shared with your Claude integration. In Notion: open the page → Share → confirm Claude has access.

**"Something went wrong" on generate** — Your API key may be missing or expired. Click ⚙ API key and re-enter it.

**Save to Notion fails** — Same as above — check API key and Notion connection.

**Outputs look off** — Edit the input fields and hit Generate again. The more specific your inputs, the better the outputs.

---

# Weekly routine

Every Friday (or your preferred day):

1. Open `weekly-recap.html`
2. Paste your Notion notes page URL → pull content
3. Review and edit the pre-filled fields
4. Generate → copy to Slack/email
5. Save to Notion for your archive
