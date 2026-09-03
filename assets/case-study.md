# Case Study — Ten Weeks, 224 Organisations

This skill is a generalisation of one real campaign. The numbers below are what came out
of it. The subject's identifiers are redacted, which is the whole point of the exercise.

**Subject:** one individual, EU resident (Ireland), three email addresses and one
username. **Duration:** ten active weeks. **Organisations contacted:** 224.

---

## What the campaign found

The mental model most people have — "my data is on a few sketchy breach sites" — was
wrong in an instructive way. The breach-search engines were the most *visible* exposure
but the smallest category. The bulk of the data sat with businesses that are entirely
legitimate, well-funded, and mostly unknown to the person whose data they held.

| Category | Organisations | What they hold |
|---|---|---|
| B2B contact data & lead-gen | 69 | Name, email, employer, inferred role — sold per-record |
| Breach & leak search | 35 | Credentials from criminal breaches, searchable by anyone |
| Ad-tech & audience data | 28 | Hashed identifiers, inferred segments, cross-site behaviour |
| OSINT / email intelligence | 27 | Real-time lookups linking an address to accounts |
| People search | 25 | Name, addresses, relatives, age — mostly US-scoped |
| Email verification | 16 | Deliverability checks; several genuinely retain nothing |
| Regional directory | 10 | Electoral roll and directory data, EU/UK |
| Major data broker | 7 | Aggregated profiles sold at scale |
| Threat intelligence | 7 | Infostealer logs and dark-web credential monitoring |

Two-thirds of the target list was discovered *during* the campaign rather than before it,
mostly by asking controllers under Article 19 who they had shared data with, and by
following one service's upstream sources to another.

## Outcomes

Of the organisations that responded within the campaign window:

- **Confirmed deletion or removal** — the largest response group, including several
  breach-search engines and people-search sites.
- **"No data held"** — the second largest, and heavily concentrated in the email-
  verification category, where the claim is credible and in some cases independently
  audited. Each of these was converted into a prospective suppression request.
- **Deflection** — mostly "we only aggregate public data" and "we query in real time and
  store nothing", concentrated among OSINT tools.
- **Silence past deadline** — a persistent minority, and the reason `escalation.md` exists.
- **Bounced** — roughly one in eight published privacy addresses was dead. Working
  replacements were found for almost all of them.

The most instructive single outcome: one major breach-search engine confirmed removal in
writing, and the data was retrievable again nineteen days later. That is the case that
turned "request deletion" into "request deletion **and** permanent suppression as a search
selector", which is now the core of the breach-search template.

## What generalised into the skill

- **Suppression beats deletion.** Deleting a record from a service that re-ingests
  datasets buys you weeks. Suppression of the identifier as a *search selector* is what
  holds.
- **The `From:` address is load-bearing.** Several services key automated removal off the
  sender. A campaign run entirely from one mailbox silently fails for the other addresses.
- **Usernames are separate selectors.** Breach-search engines index by handle as well as
  address, and a request naming only email addresses leaves half the exposure in place.
- **Contact discovery is the real cost.** Drafting is minutes; finding a live address at a
  company whose privacy page is three years stale is the work. That research is now the
  registry in `references/`.
- **One in eight addresses is dead**, and an untracked bounce is how a site stays on your
  "handled" list for months without ever having been contacted.

## What did not work

- Bulk BCC sends. Fast, and ignored at a much higher rate than individual sends.
- Assuming a US company would refuse GDPR. Most did not — naming Article 3(2) explicitly
  ended the argument before it started.
- Treating "we found no data" as a completed item. Without prospective suppression it is
  a snapshot, not an outcome.
- Doing self-service opt-outs across several sittings. Verification links expire in 15
  minutes to 24 hours, and two were lost that way.

## Honest limits

Deletion is not permanent and this is not a solved problem. Datasets resurface under new
operators, acquisitions carry databases across borders, and suppression lists get lost in
migrations. The realistic goal is not disappearance — it is reducing the number of places
your data is trivially retrievable, and having a documented paper trail for the ones that
ignore you.
