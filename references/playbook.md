# Campaign Playbook

The order things happen in, and roughly what each stage costs. Ten weeks of part-time
effort against 329 organisations is the shape this is drawn from; a focused campaign
against the sixty sites that actually publish to the open web is perhaps three weeks.

The single biggest determinant of how long it takes is not drafting. It is finding
working contact addresses, which is why the registry in this repo is the part worth
having.

---

## Week 1 — Reconnaissance

Establish exposure before writing anything. It determines which categories matter and it
gives you the dated evidence you will want if you end up at a regulator.

- Check each address against Have I Been Pwned. The breach list tells you which corpora
  you are in, and therefore which search engines index you.
- Search each address and username on the major OSINT and breach-lookup services. Record
  what is returned, with dated screenshots.
- Search your name on people-search sites, especially if you have ever lived in the US.
- Note which services return a result and which do not. Priority follows the results.

Output: a target list drawn from the registry, ordered by what is actually exposed.

## Week 1 — Profile and infrastructure

- Complete `profile.yml`.
- Decide the legal basis per `references/privacy-laws.md`.
- Set up the tracker from `assets/tracker-template.md`.
- Create a mail label or folder for replies. Volume gets away from you around week three
  otherwise.

## Weeks 2–3 — Wave 1: the sites that publish

Breach & leak search, OSINT / email intelligence, people search. These are the ones
returning your data to anyone who types your address into a box, and they produce the
fastest visible wins.

- 15–20 sites per session; more than that and verification slips.
- Verify every contact address before drafting.
- Send individually, not BCC'd.
- Log every send the same day.

## Weeks 3–5 — Wave 2: B2B and enrichment

The largest category and the one most likely to argue legitimate interests. Use the
Article 21 objection in template 6 from the start rather than waiting for the defence.

Expect a high rate of "we hold no personal Gmail addresses" — several enrichment services
genuinely filter consumer domains. Accept those, request suppression, move on.

## Weeks 4–6 — Wave 3: ad-tech and audience data

Slowest to respond, least visible in effect, and the category where deletion is hardest to
verify. Worth doing, worth doing last. Ask specifically about hashed identifiers — that is
how you exist in these systems.

## Weeks 5–7 — Wave 4: self-service forms and manual work

The forms that need a human: CAPTCHAs, ID uploads, live chat, the sites with no contact
address at all. Batch them into one or two sittings with the inbox open, because of the
expiring-link problem in `troubleshooting.md`.

## Weeks 6–8 — Reply handling

Replies arrive throughout, but the volume peaks a few weeks behind the sends. Classify
each into the six buckets in `references/escalation.md` on arrival, and answer the
deflections promptly — a rebuttal sent two months later reads as an afterthought.

## Weeks 8–10 — Follow-ups and escalation

- Follow-up 1 to everyone past deadline.
- Final notice a week later.
- Regulator complaints for the worst — and choose a small number. A focused complaint
  against a controller that confirmed deletion and then reinstated the data is worth more
  than twenty complaints about silence.

## Ongoing — Re-verification

Every 90 days, re-check the sites that publish. Datasets get re-ingested and suppression
lists get lost in migrations. This is the stage everybody skips, and it is the reason
people conclude that data removal does not work.

---

## Wave sizing

| Sites per session | Outcome |
|---|---|
| 5–10 | Sustainable, thorough, slow |
| 15–20 | The working rate — verification still happens |
| 30+ | Verification gets skipped, bounces go unnoticed, contacts get burned |

## What actually predicts a reply

In rough order, from the source campaign:

1. **A monitored address.** A `dpo@` or `dsars@` address beats a generic `info@` by a wide
   margin, and a support ticket beats an unmonitored `privacy@` alias.
2. **An individual send.** Bulk-BCC'd requests get treated as bulk mail.
3. **A named article and a named date.** "Article 12(3)" and a deadline in the body change
   how the message is routed internally.
4. **EU or UK framing** for any controller with European exposure — the enforcement
   history is real and compliance teams know it.
5. **Brevity in the first message.** The long-form templates work because they are
   structured, not because they are long. Everything past the numbered list is scanned.
