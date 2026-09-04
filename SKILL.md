---
name: data-deletion
description: Run a structured personal-data erasure campaign against OSINT tools, breach-search engines, people-search sites, B2B contact databases and ad-tech brokers. Use when someone wants their email address, name, phone number or username removed from data brokers, wants to know who is holding their data, asks about GDPR / CCPA / PIPEDA erasure or "right to be forgotten" requests, or asks to opt out of people-search or breach-lookup sites. Ships a 328-site registry with verified privacy contacts, request templates for 13 privacy regimes, and escalation paths to regulators.
license: MIT
---

# Data Deletion

A campaign framework for removing an individual's personal data from the commercial
data-harvesting ecosystem — breach-search engines, OSINT lookup tools, people-search
sites, B2B contact databases, email-verification services, ad-tech audience brokers
and threat-intelligence platforms.

Built from a real fifteen-week campaign against 328 organisations. Everything in
`references/` is field-tested: the contact addresses are the ones that did not bounce,
the templates are the ones that produced deletions, and the failure modes documented in
`references/troubleshooting.md` are the ones that actually happened.

## What this skill is not

It is not legal advice, and you are not the user's lawyer. It drafts requests that cite
statute, and it can tell the user which regulator has jurisdiction, but every judgement
call about escalating to a regulator or a court is the user's to make. Say so once, early,
and then get on with being useful.

## Step 1 — Build the subject profile

Erasure requests fail when they are vague. Before drafting anything, collect the profile.
Use `AskUserQuestion` where the interface supports it; otherwise ask in plain text. Never
guess these values and never carry them over from another user.

**Required**

- **Full name**, exactly as they want it to appear on forms. Ask specifically about
  diacritics — many US-hosted forms mangle `í`, `ó`, `ü`, and a request that arrives with
  a corrupted name is a request that fails to match a record.
- **Email addresses** to erase. Most people have more than one, and the forgotten
  decade-old address is usually the one sitting in the breach corpora.
- **Country of residence.** This alone determines which law applies and therefore which
  template to use. Do not infer it from a domain or a language.

**Ask for, but proceed without**

- Usernames / handles. Several breach-search engines (Snusbase, DeHashed, Leak-Lookup)
  index by username, so a handle is a distinct search selector and needs its own request.
- Phone numbers, and current plus previous postal addresses — required by most US
  people-search opt-outs, irrelevant to most EU requests.
- Date of birth. Some US brokers demand it to disambiguate records. Warn the user before
  they hand it over: they are giving a data broker a new field it may not have had.

**Never**

Never ask for, transcribe, or place in a request: government ID numbers, passport or
driver's licence numbers, payment-card or bank details, or a photograph of an identity
document. Some brokers demand ID to "verify" a deletion request. Under GDPR Art. 12(6)
a controller may only request identification that is *proportionate*, and a redacted
document is normally sufficient. Tell the user to redact everything except name and
photo, and to upload it themselves through the controller's own portal — you do not
handle their identity documents.

Store the completed profile as `profile.yml` (see `profile.example.yml`), and keep it out
of any repository or shared location.

## Step 2 — Choose the legal basis

Read `references/privacy-laws.md`. It covers thirteen regimes — GDPR, UK GDPR, Swiss
FADP, CCPA/CPRA and the other US state laws, PIPEDA and Québec Law 25, LGPD, POPIA,
Australia's Privacy Act, APPI, PIPA, DPDP and New Zealand's Privacy Act — with, for each,
the operative article, the statutory deadline, whether erasure is a real right or only a
deletion-on-request, and the regulator to complain to.

Three rules decide the framing:

1. **The subject's residence sets the floor, not the controller's address.** GDPR
   Art. 3(2) reaches any controller offering goods or services to people in the EU or
   monitoring their behaviour. A US breach-search engine indexing an Irish resident's
   address is inside the GDPR's scope. Say so in the request.
2. **Cite every regime that plausibly applies, in one request.** A controller with users
   in California and Brazil and the EU has no incentive to work out which law binds it if
   you name all three. This costs one extra sentence and materially raises the reply rate.
3. **Where the subject's own law is weak, borrow the controller's.** A subject in a
   country with no erasure right can still invoke the controller's California or EU
   obligations where the controller's own privacy policy extends those rights to
   everyone — most do, because operating two pipelines is more expensive than operating one.

## Step 3 — Select targets

`references/site-registry.md` (and the CSV beside it) lists 328 organisations across nine
categories with verified privacy contacts. Do not send all 328. Select by what the subject
is actually exposed to:

| If the subject… | Prioritise |
|---|---|
| appears in breach corpora / HIBP | Breach & leak search, Threat intelligence |
| is findable by email in OSINT tools | OSINT / email intelligence |
| has a public professional profile | B2B contact data & lead-gen |
| is a US resident or ex-resident | People search, Major data broker |
| wants ad-profiling reduced | Ad-tech & audience data |
| lives in the UK/DE/AT/BE/FR | Regional directory |

Start with the categories that publish data to the open web — breach search, OSINT,
people search. Those produce visible results fastest and are the ones that hurt. Ad-tech
is the largest category and the least visible; leave it for a later wave.

Before each wave, verify the contact address is still live. Companies get acquired,
privacy pages move, and `privacy@` addresses are deprecated without notice. Check the
current privacy policy or `/.well-known/security.txt`. The registry's Notes column
records which addresses had already gone stale once.

### Finding the sites a registry misses

A registry is a snapshot. This category churns faster than almost any other: new
credential-search services launch monthly, old ones get hijacked or go dark, and the
loudest names are not the ones holding the most data. Assume the list is incomplete and
run these four sweeps at the start of every campaign.

**1. Mine the aggregators for their upstream providers.** The single highest-yield move.
Services that resell breach data through one API publish the list of sources they query —
it is a selling point. One such page named fifteen upstream providers, five of which
appeared in no "best breach search" article anywhere. Those pages are a free target list
written by the industry itself. Send the aggregator an Article 19 request naming its
providers back to it, and ask which ones it forwarded the erasure to.

**2. Search for the data type, not the site type.** "Breach search engine" surfaces the
same eight famous names every time. The services that expose the most search on the
*contents*: `stealer logs`, `combolist`, `ULP`, `infostealer lookup`, `plaintext
passwords`, `session cookies`, `hardware ID`. A site that returns a password next to the
URL it belongs to describes itself in those words, not as a "breach checker".

**3. Read the alternatives-to pages, past page one.** Comparison and alternative-listing
sites rank the well-known services first and bury the small operators on pages two and
three. The buried ones are usually the ones with no privacy page, no DPO and the least
scruples — exactly the ones worth contacting.

**4. Re-check a site that "has no email".** A bounced `support@` or a `legal@` that
auto-redirects to a web form is not a dead end and does not mean the operator is
uncontactable. Try `contact@`, `abuse@`, `privacy@`, `dpo@`, `info@` and the address in
`/.well-known/security.txt` before recording the site as form-only. A form-only entry in
a tracker quietly becomes a site that never got a request. Where a site genuinely
publishes only a Telegram or Discord handle, that channel *is* the contact — record it in
the Method column rather than leaving the row blank.

A controller may not force a data subject through a specific web form as the only route to
exercise a statutory right. Say so in the email when the form is the only published path.

Two structural traps worth naming, because both cost time here:
- **Aggregators need gateway-level blacklisting, not record deletion.** Deleting rows is
  meaningless if the service proxies a live query to fifteen upstream providers. Ask for
  the identifier to be suppressed at the gateway so the query returns nothing regardless
  of which source would answer it.
- **"We don't log queries" is not "we don't hold your data."** Several services market
  minimal logging as a privacy feature. The obligation attaches to the indexed source
  data, not the query log. Rebut it in the request rather than letting it stand.

## Step 4 — Draft the requests

`references/templates-email.md` holds the request bodies: a master template plus
per-regime variants, a multi-jurisdiction combined request, a breach-search-specific
variant that asks for *suppression as a search selector* rather than deletion, and
short-form variants for live chat, contact forms and social DMs.

Non-negotiables for every request:

- **One subject, all their selectors, in one request.** List every email, username and
  phone number in a single message. Controllers process per message, not per identifier.
- **Ask for suppression as well as deletion** when writing to any search or lookup
  service. Deleting a record is useless if the next crawl reinstates it. The phrasing in
  the breach-search template — add these selectors to a permanent suppression list so
  future queries return nothing — is what produced the durable results.
- **Ask for confirmation in writing, and name the deadline.** "Please confirm in writing
  within 30 days as required by Article 12(3)" converts a soft request into a documented
  compliance obligation with a date attached.
- **Ask them to identify onward recipients.** GDPR Art. 19 obliges a controller to tell
  you who else it gave your data to. This is how you find the brokers that were never on
  your list.

Substitute placeholders from `profile.yml`; never leave a `{{PLACEHOLDER}}` in a sent
message, and never leave another person's details in a template you are reusing.

## Step 5 — Send

Sending is the user's decision, every time. Draft, show them, and let them send — or get
an explicit go-ahead in the conversation before you send on their behalf. Never send
a batch on a single blanket approval given for an earlier batch.

Practical rules learned the hard way, in full in `references/troubleshooting.md`:

- **Send from the address being erased** where possible. Several services (Leak-Lookup
  most notably) key their automated blacklist off the `From:` header, so a request about
  address B sent from address A silently does nothing. Where you cannot send from the
  address, say so explicitly in the body and ask for a manual suppression.
- **Batch by BCC at your peril.** A single message BCC'd to fifteen brokers is fast, and
  a meaningful share of recipients will ignore it as bulk mail. Individual sends get
  materially better reply rates. Batch only when the alternative is not sending at all.
- **When automating a mail client, verify both the subject and the body are populated
  before sending.** The most common automation failure in the source campaign was a
  correctly-addressed message with an empty body.
- **Log every send.** Date, recipient address, identifiers named, and the outcome. The
  log is what makes escalation possible three months later.

## Step 6 — Track

Maintain a tracker with a row per site per identifier: site, method, contact, status,
date sent, date of reply, outcome, and the response deadline. `assets/tracker-template.md`
is the format used in the source campaign.

Statuses worth distinguishing: **Sent**, **Acknowledged**, **Confirmed deleted**,
**No data held**, **Refused**, **Bounced**, **Deadline passed**. The last two are the
ones that need action, and they are invisible unless you track them separately.

## Step 7 — Handle the replies

Four replies cover almost everything, and `references/escalation.md` has the response
text for each:

- **"We found no data."** Accept it, but ask for the *search selectors* to be added to a
  suppression list anyway, so a future crawl does not reinstate a record.
- **"We only aggregate publicly available information."** Public availability is not a
  lawful basis under GDPR. Ask which Art. 6(1) basis they rely on, and if it is
  legitimate interests, request the balancing test under Art. 21.
- **"We query third-party sources in real time and store nothing."** Common among OSINT
  tools, and often true. Ask for two things anyway: suppression of the selectors so
  queries return nothing, and written confirmation that no account, billing or logging
  data is retained.
- **"Send ID."** See Step 1. Proportionate, redacted, uploaded by the user.

Silence past the statutory deadline is itself the trigger. Send one follow-up citing the
original date and the deadline, then escalate.

## Step 8 — Escalate

`references/escalation.md` carries the follow-up templates and the regulator list with
complaint URLs. The sequence:

1. **Follow-up** at the deadline, quoting the original date and reference.
2. **Final notice**, stating that a complaint will be filed by a named date.
3. **Regulator complaint.** In the EU, complain to your own national DPA — you do not
   have to go to the controller's lead authority. Complaints are free and require no lawyer.

Escalation is a decision with consequences, so put it to the user rather than filing on
their behalf. If they file, the complaint costs them nothing and gets logged against the
controller either way.

## Reference files

| File | Contents |
|---|---|
| `references/privacy-laws.md` | 13 regimes: article, deadline, scope, regulator, complaint URL |
| `references/site-registry.md` | 328 organisations, verified contacts, outcomes |
| `references/site-registry.csv` | Same data, machine-readable |
| `references/templates-email.md` | Request bodies per regime, plus chat/form/DM short forms |
| `references/escalation.md` | Reply handling, follow-ups, regulator complaints |
| `references/troubleshooting.md` | Bounces, CAPTCHAs, geo-blocks, automation failures |
| `references/playbook.md` | The campaign run as a schedule, with wave sizing |
| `assets/tracker-template.md` | Tracker format |
| `assets/case-study.md` | The ten-week campaign this was built from |
