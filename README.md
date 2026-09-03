# Data Deletion Skill

**A Claude skill for running a structured personal-data erasure campaign against the
commercial data-harvesting ecosystem.** Ships a registry of 224 organisations with
verified privacy contacts, request templates for 13 privacy regimes, and escalation paths
to 21 regulators.

Built from a real ten-week campaign, not from a blog post about one.

<p>
<img alt="Skill" src="https://img.shields.io/badge/Claude-Skill-8A63D2">
<img alt="Sites" src="https://img.shields.io/badge/sites%20covered-224-1f6feb">
<img alt="Regimes" src="https://img.shields.io/badge/privacy%20regimes-13-2da44e">
<img alt="Regulators" src="https://img.shields.io/badge/regulators-21-e3b341">
<img alt="Development" src="https://img.shields.io/badge/built%20over-10%20active%20weeks-6e7781">
<img alt="License" src="https://img.shields.io/badge/license-MIT-24292f">
</p>

---

## The problem

Ask someone where their personal data is and they will name a breach site or two. In the
campaign this skill was built from, breach-search engines turned out to be the most
*visible* exposure and one of the smallest categories. Sixty-nine organisations were B2B
contact databases — legitimate, well-funded companies selling the subject's name and
address per record. Twenty-eight were ad-tech platforms holding hashed identifiers and
inferred segments. Most of the target list was discovered mid-campaign by asking one
controller who it had shared data with, then following that thread.

Removing yourself is not hard because the law is weak. It is hard because it is 224
separate pieces of admin, each requiring a working contact address that is probably not
the one on the privacy page, a legal basis matched to your jurisdiction, and a follow-up
thirty days later that nobody remembers to send.

This skill is that admin, packaged.

## What's in it

| | |
|---|---|
| [`SKILL.md`](SKILL.md) | The skill: an eight-step campaign process Claude follows |
| [`references/site-registry.md`](references/site-registry.md) | **224 organisations**, nine categories, verified privacy contacts and recorded outcomes |
| [`references/site-registry.csv`](references/site-registry.csv) | Same data, machine-readable |
| [`references/privacy-laws.md`](references/privacy-laws.md) | **13 regimes** — article, deadline, right strength, regulator |
| [`references/templates-email.md`](references/templates-email.md) | Request bodies per regime, per site-category, plus chat / form / DM short forms |
| [`references/escalation.md`](references/escalation.md) | Reply classification, rebuttals, follow-ups, **21 regulator complaint routes** |
| [`references/troubleshooting.md`](references/troubleshooting.md) | Bounces, CAPTCHAs, geo-blocks, the `From:`-address trap, automation failures |
| [`references/playbook.md`](references/playbook.md) | The campaign as a ten-week schedule with wave sizing |
| [`assets/tracker-template.md`](assets/tracker-template.md) | Tracker format |
| [`assets/case-study.md`](assets/case-study.md) | The campaign it was built from, redacted |

## Coverage

**224 organisations across nine categories**

| Category | Count | Examples of what they do |
|---|---:|---|
| B2B contact data & lead-gen | 69 | Sell name/email/employer records per lookup |
| Breach & leak search | 35 | Make credentials from criminal breaches publicly searchable |
| Ad-tech & audience data | 28 | Hold hashed identifiers and inferred behavioural segments |
| OSINT / email intelligence | 27 | Turn an email address into a map of your accounts |
| People search | 25 | Publish addresses, relatives, age — mostly US-scoped |
| Email verification | 16 | Deliverability checking; several retain nothing |
| Regional directory | 10 | Electoral roll and directory data across the UK, DE, AT, BE |
| Major data broker | 7 | Aggregate and resell profiles at scale |
| Threat intelligence | 7 | Index infostealer logs and dark-web credential dumps |

**13 privacy regimes** — EU GDPR · UK GDPR · Swiss FADP · CCPA/CPRA · 19 other US state
laws · PIPEDA · Québec Law 25 · LGPD · POPIA · Australia's Privacy Act · APPI · PIPA ·
India's DPDP Act · NZ Privacy Act · Singapore's PDPA

Each with the operative article, the statutory clock, an honest assessment of how strong
the right actually is, and the regulator to complain to when it is ignored.

## Install

Clone into your Claude skills directory:

```bash
git clone https://github.com/OWNER/data-deletion-skill.git ~/.claude/skills/data-deletion
```

Or add it to a project as `.claude/skills/data-deletion/`.

Then set up your profile:

```bash
cp profile.example.yml profile.yml
$EDITOR profile.yml     # profile.yml is gitignored — keep it that way
```

## Use

```
Use the data-deletion skill. Build my profile first, then draft erasure requests for the
breach-search and OSINT categories in the registry. I'm in Ireland. Show me every draft
before anything is sent.
```

More prompts in [`references/templates-email.md`](references/templates-email.md#9-prompts-for-driving-this-skill).

The skill drafts, tracks and escalates. **It does not send anything without you seeing it
first**, and it will not touch your identity documents — if a broker demands ID, it tells
you how to push back on the scope and you upload a redacted copy yourself.

## Four things that came out of doing this for real

**Suppression beats deletion.** One major breach-search engine confirmed removal in
writing; the data was retrievable again nineteen days later, reinstated by the next
dataset ingest. Every template now asks for the identifier to be added to a permanent
*search-selector suppression list*, not just for the record to be deleted. That one change
is the difference between a result that holds and a result that lasts three weeks.

**The `From:` address is load-bearing.** Several services key their automated removal off
the sender header — request removal of address B from address A and precisely nothing
happens, silently. Run the campaign one address at a time, from that address.

**One in eight published privacy addresses is dead.** `privacy@` aliases rot. `support@`
and `legal@` are monitored; a support ticket reaches a compliance team that an
unmonitored alias never will. Every bounce and its working replacement is recorded in the
registry, which is the part of this repo that took the ten weeks.

**Naming Article 3(2) ends the argument.** US-hosted services that assumed GDPR did not
reach them mostly stopped assuming it once the extraterritorial provision was quoted at
them. It costs one sentence.

## Scope and honesty

This is not legal advice, and it does not promise disappearance. Datasets resurface under
new operators, acquisitions carry databases across borders, and suppression lists get lost
in migrations. What it offers is a much smaller number of places your data is trivially
retrievable, and a documented paper trail against the ones that ignore you — which is what
a regulator complaint is made of.

The registry's **Outcome** column records what came back during the source campaign. Read
it as evidence that an address is live, not as a prediction about your own request: a
broker holding nothing on one person may hold a great deal on another.

## Contributing

The registry is the part that decays. Pull requests welcome for:

- Contact addresses that have changed or started bouncing
- Organisations not yet covered, with a verified privacy contact
- Jurisdictions not yet covered, with the operative provision and regulator
- Corrections to any legal citation

Please do not open issues containing anyone's personal data, including your own.

## License

MIT — see [LICENSE](LICENSE).
