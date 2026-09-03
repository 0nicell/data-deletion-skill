# Request Templates

Every template uses the same placeholder set. Fill them from `profile.yml` and check
before sending that none survive — a request containing `{{FULL_NAME}}` is a request that
gets deleted unread.

| Placeholder | Example |
|---|---|
| `{{FULL_NAME}}` | Alex Moore |
| `{{PRIMARY_EMAIL}}` | alex.moore@example.com |
| `{{ALL_EMAILS}}` | alex.moore@example.com, a.moore1994@example.com |
| `{{USERNAMES}}` | alexm, moore_a |
| `{{PHONE}}` | +353 XX XXX XXXX |
| `{{COUNTRY}}` | Ireland |
| `{{JURISDICTION_BLOCK}}` | one of the legal-basis paragraphs below |
| `{{DATE}}` | 3 September 2026 |
| `{{DEADLINE_DATE}}` | 3 October 2026 |
| `{{COMPANY}}` | Example Data Ltd |

A note on tone. These read as formal and slightly bureaucratic, and that is deliberate —
they are drafted to be forwarded to a legal or compliance inbox without editing. Warmth
does not improve the reply rate here; a citable article number does.

---

## 1. Master template — single jurisdiction

**Subject:** `Data Subject Erasure Request — {{FULL_NAME}} — {{PRIMARY_EMAIL}}`

```
To Whom It May Concern,

I am writing to formally request the erasure of all personal data your organisation
holds relating to me.

My details:
- Name: {{FULL_NAME}}
- Email address(es): {{ALL_EMAILS}}
- Username(s)/handle(s): {{USERNAMES}}
- Country of residence: {{COUNTRY}}

{{JURISDICTION_BLOCK}}

I request that you permanently delete all records, profiles, data points, and any
derived, inferred or associated information linked to the identifiers above, across all
of your databases, products and services. This includes any indexed, cached or
aggregated data sourced from third-party data breaches, leaks, scraping, public records
or commercial data partners.

I further request that you confirm in writing:
1. That the above data has been deleted, and the date of deletion;
2. Whether you retain any data relating to me for a legal obligation, and if so, the
   specific legal basis and retention period;
3. The identity of any third parties to whom you disclosed my personal data, so that I
   may contact them directly.

Please confirm completion in writing to {{PRIMARY_EMAIL}} by {{DEADLINE_DATE}}.

Yours faithfully,
{{FULL_NAME}}
{{PRIMARY_EMAIL}}
{{COUNTRY}}
```

---

## 2. Jurisdiction blocks

Drop the matching paragraph into `{{JURISDICTION_BLOCK}}`.

**EU — GDPR**
```
As a resident of {{COUNTRY}} in the European Union, I make this request under Article 17
of the General Data Protection Regulation (EU) 2016/679 (the right to erasure). Where the
data you hold originates from data breaches, leaked datasets or unconsented scraping, it
has been processed without a lawful basis under Article 6(1), and Article 17(1)(d)
applies. I also exercise my right under Article 19 to be informed of the recipients of my
personal data.

Under Article 12(3) you are required to respond within one month of receipt. Under
Article 12(5) this request is free of charge. Should you consider that Article 3(2) does
not bring you within scope: the Regulation applies to any controller, wherever
established, that offers services to individuals in the Union or monitors their behaviour.
```

**UK — UK GDPR**
```
As a resident of the United Kingdom, I make this request under Article 17 of the UK GDPR
and the Data Protection Act 2018. Under Article 12(3) you are required to respond within
one month, free of charge. I also exercise my Article 19 right to be told the recipients
of my personal data. If this request is not resolved I will refer the matter to the
Information Commissioner's Office.
```

**Switzerland — FADP**
```
As a resident of Switzerland, I make this request under Article 32 of the revised Federal
Act on Data Protection, requiring the cessation of unlawful processing and the deletion
of the data concerned.
```

**California — CCPA/CPRA**
```
As a resident of California, I make this request under California Civil Code
§1798.105 (right to delete). I additionally direct you, under §1798.120, to cease any
sale or sharing of my personal information, and under §1798.121 to limit the use of any
sensitive personal information. Under §1798.130 you are required to respond within 45
days. Should you deny any part of this request, identify the specific exception in
§1798.105(d) you rely on.
```

**Other US states**
```
As a resident of {{COUNTRY}}, I make this request under [STATE] [ACT NAME], exercising my
right to deletion of personal data, my right to opt out of the sale of personal data, and
my right to opt out of targeted advertising. Please respond within 45 days as the statute
requires, and confirm the process for appealing a refusal.
```

**Canada — PIPEDA + Québec Law 25**
```
As a resident of Canada, I make this request under the Personal Information Protection and
Electronic Documents Act. Under Principle 4.5.3 you must destroy, erase or anonymise
personal information that is no longer required for the purpose for which it was
collected; no such purpose subsists. In the alternative, I request access to all personal
information you hold about me under Principle 4.9, to which the 30-day response
requirement applies. [If in Québec, add: I additionally exercise my rights under Article
28.1 of Law 25 to cessation of dissemination and de-indexing.]
```

**Brazil — LGPD**
```
As a resident of Brazil, I make this request under Article 18(VI) of Law No. 13.709/2018
(LGPD), requesting deletion of personal data, and under Article 18(IV) for the
anonymisation, blocking or deletion of unnecessary or unlawfully processed data. Article
19 requires your response within 15 days.
```

**South Africa — POPIA**
```
As a resident of South Africa, I make this request under Section 24 of the Protection of
Personal Information Act 4 of 2013, requiring the deletion or destruction of personal
information that is inaccurate, irrelevant, excessive, out of date or has been obtained
unlawfully. Data derived from breach corpora or unconsented scraping falls within the
final limb. I am willing to submit a prescribed Form 2 if you require it.
```

**Australia — Privacy Act 1988**
```
As a resident of Australia, I make this request under the Privacy Act 1988. Australian
Privacy Principle 11.2 requires you to destroy or de-identify personal information you no
longer need for any purpose for which it may be used or disclosed. You have no subsisting
purpose for retaining my information, and I request its destruction. To the extent any
information is retained, I exercise my APP 13 right to correction.
```

**Japan — APPI**
```
As a resident of Japan, I make this request under Article 35 of the Act on the Protection
of Personal Information, requesting the cessation of use and the deletion of my personal
data, which was acquired by improper means and is used beyond any purpose notified to me.
```

**South Korea — PIPA**
```
As a resident of the Republic of Korea, I make this request under Article 36 of the
Personal Information Protection Act, requesting the deletion of my personal information.
The Enforcement Decree requires your response within 10 days.
```

**India — DPDP Act**
```
As a resident of India, I make this request under Section 12(3) of the Digital Personal
Data Protection Act 2023, exercising my right to erasure of personal data.
```

**New Zealand — Privacy Act 2020**
```
As a resident of New Zealand, I make this request under the Privacy Act 2020. Information
Privacy Principle 9 prohibits retaining personal information for longer than is required
for the purposes for which it may lawfully be used; no such purpose subsists. I request
deletion, and in the alternative exercise my IPP 6 access right, to which the 20-working-
day requirement applies.
```

**Singapore — PDPA**
```
As a resident of Singapore, I withdraw any and all consent for the collection, use and
disclosure of my personal data under Section 16 of the Personal Data Protection Act 2012,
and require you to cease retention under Section 25, the purpose for collection having
ended.
```

---

## 3. Multi-jurisdiction combined request

Use when the controller's location is unclear, when it plainly operates globally, or when
the subject has lived in more than one country. Costs one paragraph and materially raises
the reply rate.

```
This request is made under every data protection regime applicable to your processing of
my personal data, including but not limited to: Article 17 of the EU General Data
Protection Regulation (2016/679), which applies extraterritorially under Article 3(2) to
any controller offering services to, or monitoring the behaviour of, individuals in the
Union; Article 17 of the UK GDPR; California Civil Code §1798.105 and §1798.120; the
comprehensive consumer privacy statutes of the other US states in which you offer
services; Article 18 of Brazil's LGPD; Section 24 of South Africa's POPIA; Australian
Privacy Principle 11.2; Article 35 of Japan's APPI; and Article 36 of the Republic of
Korea's PIPA.

I am a resident of {{COUNTRY}} and rely primarily on the regime applicable there. Where
your own privacy policy extends any of the above rights to all users regardless of
location, I rely on that undertaking additionally.
```

---

## 4. Breach-search and OSINT services

The important difference: these services often store nothing themselves and simply query
or index other corpora. Deletion alone is therefore worthless — the next crawl reinstates
you. **Ask for suppression as a search selector.** This single change is what produced
durable results in the source campaign.

**Subject:** `Erasure and Search-Suppression Request — {{FULL_NAME}}`

```
To Whom It May Concern,

I am writing to request both erasure and permanent search suppression of my personal data
by {{COMPANY}}.

Identifiers to be suppressed and erased:
- Email: {{ALL_EMAILS}}
- Username: {{USERNAMES}}
- Name: {{FULL_NAME}}

{{JURISDICTION_BLOCK}}

Specifically, I request that you:

1. Delete all records, breach entries, credential pairs, paste captures, index entries and
   derived data associated with the identifiers above;

2. Add each identifier above to a permanent suppression or blacklist, such that any future
   query against your service — by me or by any third party — returns no result for these
   identifiers, and such that future ingestion of new datasets does not reinstate them;

3. Confirm whether your service has ever returned results for these identifiers to third
   parties, and if your logs permit, when;

4. Confirm in writing that no account, billing, correspondence or query-log data relating
   to me is retained.

If your position is that you do not store data but query third-party sources in real time,
points 2 and 4 still apply, and I ask you to answer them directly.

The personal data at issue originates from criminal data breaches and was never
lawfully obtained by the original source. Indexing it and making it searchable is
processing without a lawful basis.

Please confirm by {{DEADLINE_DATE}}.

{{FULL_NAME}}
{{PRIMARY_EMAIL}}
```

---

## 5. People-search sites

These match on name plus location plus age, so a bare email often finds nothing. Include
locations, and expect to be asked for more.

```
To Whom It May Concern,

I am requesting the removal of my personal profile and all associated records from
{{COMPANY}} and any affiliated or white-label sites you operate.

- Full name: {{FULL_NAME}}
- Email: {{ALL_EMAILS}}
- Phone: {{PHONE}}
- Current location: {{COUNTRY}}
- Previous locations: [list]

{{JURISDICTION_BLOCK}}

Please remove my profile from public search, delete the underlying record, and suppress
my details from reinstatement when you next refresh from your upstream sources. Please
also identify those upstream sources so that I may contact them directly.

I am aware that many services in your sector operate multiple consumer-facing brands from
one database. This request extends to every brand you operate.

Please confirm by {{DEADLINE_DATE}}.

{{FULL_NAME}}
```

---

## 6. B2B contact databases and lead-gen platforms

The standard defence here is "legitimate interests" for B2B contact data. Pre-empt it.

```
To Whom It May Concern,

I request the erasure of my personal data from {{COMPANY}}'s contact database and any
products, exports, integrations or customer-facing datasets derived from it.

- Name: {{FULL_NAME}}
- Email: {{ALL_EMAILS}}

{{JURISDICTION_BLOCK}}

I anticipate that you may rely on legitimate interests under Article 6(1)(f) for B2B
contact data. I hereby object to that processing under Article 21(1). Direct-marketing
processing must cease on objection under Article 21(3) without any balancing exercise. To
the extent you rely on legitimate interests for non-marketing purposes, please provide
the legitimate interests assessment you carried out.

Please also confirm which customers of yours received records containing my data, and
whether your contract obliges them to honour a downstream deletion.

Please confirm by {{DEADLINE_DATE}}.

{{FULL_NAME}}
```

---

## 7. Ad-tech and audience data platforms

```
To Whom It May Concern,

I request the erasure of all personal data, identifiers, audience segments, inferred
attributes and hashed identifiers associated with me by {{COMPANY}}.

- Name: {{FULL_NAME}}
- Email: {{ALL_EMAILS}} (please also search hashed forms — MD5 and SHA-256 — of these
  addresses, which is how they are most likely stored in your systems)

{{JURISDICTION_BLOCK}}

I additionally object under Article 21 to all processing for direct marketing purposes,
including profiling, and withdraw any consent previously recorded through a consent
management platform.

Please confirm: the segments I was placed in; the partners with whom my identifiers were
shared or matched; and that deletion has propagated to your identity-resolution graph and
to any downstream partner that received my data.

Please confirm by {{DEADLINE_DATE}}.

{{FULL_NAME}}
```

---

## 8. Short forms

**Live chat / support widget** (agents disengage from long messages):
```
Hi — I need to make a data erasure request under {{LAW}}. Please delete all data held
about {{PRIMARY_EMAIL}} and {{USERNAMES}}, and add both to your permanent search
suppression list. I'm a resident of {{COUNTRY}}. Could you confirm in writing to
{{PRIMARY_EMAIL}}, or give me the correct address for a formal request? Thanks.
```

**Web contact form** (character limits are common):
```
Formal data erasure request under {{LAW}}.
Name: {{FULL_NAME}}
Email(s): {{ALL_EMAILS}}
Username(s): {{USERNAMES}}
Country: {{COUNTRY}}
Please delete all records associated with these identifiers and add them to a permanent
suppression list so future queries return no result. Please confirm in writing to
{{PRIMARY_EMAIL}} within the statutory period.
```

**Social DM** (some smaller breach sites only answer on Telegram/X/Discord):
```
Hi — I'd like to make a formal data removal request. Could you tell me the right address
or process? I need {{PRIMARY_EMAIL}} and the username {{USERNAMES}} removed and
suppressed from search. I'm in {{COUNTRY}} so this is a {{LAW}} request. Happy to send
the full details wherever you prefer.
```

**Registrar / host abuse report** — last resort, where a site has no contact at all and
is publishing breach data:
```
I am reporting a site hosted on your infrastructure that is publishing personal data
obtained from criminal data breaches, including my own, and that provides no functioning
mechanism for data subjects to request removal.

Site: [domain]
My affected identifiers: {{ALL_EMAILS}}
Attempts made to contact the operator: [dates and addresses tried]

I am a resident of {{COUNTRY}} and this processing has no lawful basis under {{LAW}}. I
ask that you forward this to your customer and provide a route for me to reach them.
```

---

## 9. Prompts for driving this skill

Paste-ready prompts for someone using the skill in Claude.

**Start a campaign**
```
Use the data-deletion skill. Build my profile first, then draft erasure requests for the
breach-search and OSINT categories in the registry. I'm in {{COUNTRY}}. Show me every
draft before anything is sent.
```

**Target one category**
```
Use the data-deletion skill. Draft requests to every site in the "People search" category
of the registry, using my profile in profile.yml. Verify each contact address is still
current before drafting, and flag any that look stale.
```

**Handle replies**
```
Here are the replies I've had. Using the data-deletion skill's escalation guidance,
classify each one, draft the right response, and tell me which are past their statutory
deadline.
```

**Escalate**
```
Use the data-deletion skill. These controllers are past deadline with no reply. Draft
final-notice letters, and prepare a regulator complaint for the worst offender — I'm in
{{COUNTRY}}.
```
