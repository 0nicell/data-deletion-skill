# Data Deletion Skill

**A Claude skill that runs your personal-data deletion campaign for you.**

Getting your data deleted isn't hard because the law is weak. It's hard because it's hundreds of separate pieces of admin — each one needing the right contact address, the right law for your country, and a follow-up 30 days later that nobody remembers to send.

This skill is that admin, packaged.

<p>
<img alt="Skill" src="https://img.shields.io/badge/Claude-Skill-8A63D2">
<img alt="Sites" src="https://img.shields.io/badge/sites%20covered-314-1f6feb">
<img alt="Regimes" src="https://img.shields.io/badge/privacy%20regimes-13-2da44e">
<img alt="Regulators" src="https://img.shields.io/badge/regulators-21-e3b341">
<img alt="License" src="https://img.shields.io/badge/license-MIT-24292f">
</p>

It comes from a real ten-week campaign, not from reading about one.

---

## What you get

- **314 companies** that hold personal data, with privacy contacts that were checked and actually work
- **Request templates** for 13 different privacy laws, written for each type of company
- **21 regulators** to complain to, with the route for each, when a company ignores you
- **A week-by-week plan** so you're not doing all 314 at once
- **A tracker** for what you sent, what came back, and what needs chasing

Claude drafts, tracks and escalates. **It never sends anything without showing you first**, and it won't touch your ID documents — if a company demands ID, it tells you how to push back, and you upload a redacted copy yourself.

---

## Setup

### 1. Install the skill

```bash
git clone https://github.com/0nicell/data-deletion-skill.git ~/.claude/skills/data-deletion
```

Or drop it into a project as `.claude/skills/data-deletion/`.

### 2. Add your details

```bash
cp profile.example.yml profile.yml
$EDITOR profile.yml
```

`profile.yml` is gitignored. Keep it that way — it has your personal details in it.

### 3. Ask Claude to start

```
Use the data-deletion skill. Build my profile first, then draft erasure requests for the
breach-search and OSINT categories in the registry. I'm in Ireland. Show me every draft
before anything is sent.
```

More prompts are in [`references/templates-email.md`](references/templates-email.md#9-prompts-for-driving-this-skill).

---

## What's in the repo

| File | What it's for |
|---|---|
| [`SKILL.md`](SKILL.md) | The skill itself — the eight-step process Claude follows |
| [`references/site-registry.md`](references/site-registry.md) | **314 companies**, nine categories, working contacts, and what happened when they were contacted |
| [`references/site-registry.csv`](references/site-registry.csv) | The same list, as a spreadsheet |
| [`references/privacy-laws.md`](references/privacy-laws.md) | **13 privacy laws** — which article to cite, the deadline, how strong the right is, who regulates it |
| [`references/templates-email.md`](references/templates-email.md) | The emails to send, plus short versions for chat, web forms and DMs |
| [`references/escalation.md`](references/escalation.md) | What their reply means, how to answer it, and how to complain to a regulator |
| [`references/troubleshooting.md`](references/troubleshooting.md) | Bounces, CAPTCHAs, geo-blocks, and the `From:` address trap |
| [`references/playbook.md`](references/playbook.md) | The whole campaign as a ten-week schedule |
| [`assets/tracker-template.md`](assets/tracker-template.md) | The tracker format |
| [`assets/case-study.md`](assets/case-study.md) | The original campaign, with personal details removed |

---

## Who's on the list

Most people assume their data sits on one or two breach-search sites. In the campaign this was built from, those sites were the most *visible* problem and one of the smallest categories.

| Type of company | How many | What they actually do |
|---|---:|---|
| B2B contact data & lead-gen | 75 | Sell your name, email and employer, per lookup |
| Breach & leak search | 54 | Make passwords from criminal breaches publicly searchable |
| People search | 41 | Publish addresses, relatives and age — mostly US |
| OSINT / email intelligence | 36 | Turn an email address into a map of your accounts |
| Ad-tech & audience data | 32 | Hold your ad IDs and guesses about your behaviour |
| Threat intelligence | 29 | Index malware logs and dark-web password dumps |
| Regional directories | 18 | Electoral roll and directory data — UK, DE, AT, BE |
| Email verification | 17 | Check whether addresses are real; several keep nothing |
| Major data brokers | 12 | Collect and resell full profiles at scale |

Most of that list was found *during* the campaign, by asking one company who it had shared data with and then following the trail.

**The 13 laws covered:** EU GDPR · UK GDPR · Swiss FADP · CCPA/CPRA (plus 19 other US state laws) · PIPEDA · Québec Law 25 · LGPD · POPIA · Australia's Privacy Act · APPI · PIPA · India's DPDP Act · NZ Privacy Act · Singapore's PDPA

Each one comes with the exact article to quote, the legal deadline, an honest read on how much the right is really worth, and the regulator to go to when it's ignored.

---

## Four things learned the hard way

**Ask them to blacklist your email as a search term, not just delete the record.** One big breach-search site confirmed deletion in writing. The data was searchable again 19 days later, put back by the next data import. Every template now asks for your email to be added to a permanent *search suppression list*. That single change is the difference between a result that lasts and one that lasts three weeks.

**Send it from the address you want removed.** Several services match removal requests to the sender's email. Ask from address A to remove address B and nothing happens at all, silently. Run one address at a time, from that address.

**One in eight published privacy addresses is dead.** `privacy@` aliases rot. `support@` and `legal@` are actually monitored, and a support ticket reaches a compliance team that an unread alias never will. Every bounce and its working replacement is recorded in the registry — that's the part of this repo that took ten weeks.

**Quoting Article 3(2) ends the argument.** US companies that assumed GDPR didn't apply to them mostly stopped assuming it once the article that says it does was quoted at them. It costs one sentence.

---

## What this won't do

It's not legal advice, and it doesn't promise you'll disappear. Datasets come back under new owners, acquisitions move databases across borders, and suppression lists get lost in migrations.

What it does give you is far fewer places where your data is easy to find, plus a paper trail against the companies that ignore you — which is exactly what a regulator complaint is made of.

The **Outcome** column in the registry records what came back during the original campaign. Read it as proof that an address works, not as a prediction about your request. A company holding nothing on one person may hold plenty on another.

---

## Contributing

The registry is the part that goes stale. Pull requests welcome for:

- Contact addresses that have changed or started bouncing
- Companies not covered yet, with a verified privacy contact
- Countries not covered yet, with the law and regulator
- Corrections to any legal citation

Please don't open issues containing anyone's personal data, including your own.

## Licence

MIT — see [LICENSE](LICENSE).
