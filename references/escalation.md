# Handling Replies and Escalating

## Classifying what comes back

Sort every reply into one of six buckets on arrival. The bucket determines the response,
and sorting on arrival is what stops a campaign silting up.

| Bucket | Signal | Action |
|---|---|---|
| **Confirmed deleted** | Explicit confirmation with or without a date | Log, close, re-verify in 90 days |
| **No data held** | "We found no records" | Request prospective suppression (below) |
| **Deflection** | "Public data" / "real-time only" / "not in scope" | Rebut (below) |
| **ID demanded** | Asks for identity documents | Proportionality reply (below) |
| **Silence** | Nothing past the statutory deadline | Follow-up, then final notice |
| **Bounce** | Delivery failure | Find the live address — see `troubleshooting.md` |

---

## Rebuttals

### "We found no data relating to you."

Accept it, then close the door for next time. This is a two-line reply and it is the most
valuable one in the document, because the record that does not exist today gets created by
the next dataset ingest.

```
Thank you for confirming. As you hold no data currently, adding these identifiers to a
permanent suppression list creates no burden and no conflict with any retention
obligation. I ask that you do so, so that any future ingest, crawl or dataset acquisition
does not create a record for me. Please confirm the suppression has been applied.
```

### "We only aggregate publicly available information."

```
Public availability is not itself a lawful basis for processing. Article 6(1) requires you
to identify a specific basis, and the exemption for personal data manifestly made public
by the data subject in Article 9(2)(e) applies to special-category data and to data made
public by me — not to data made public by a criminal breach or by a third party.

Please identify the Article 6(1) basis on which you rely. If it is legitimate interests
under 6(1)(f), please provide the balancing assessment you carried out, as I have
objected under Article 21.
```

### "We query third-party sources in real time; we store nothing."

Common among OSINT tools, and often literally true. It is also not an answer to the
request.

```
I accept that you may not retain a persistent copy. My request is not limited to stored
records. Where your service accepts an identifier as a query and returns personal data
about the individual behind it, you are determining the purposes and means of that
processing and you are a controller in respect of it.

I therefore ask you to:
1. Add my identifiers to a suppression list, so that queries against them return no
   result regardless of what the upstream source holds;
2. Confirm in writing that no query logs, cached results, account or billing data relating
   to me are retained;
3. Identify the upstream sources you query, so that I may exercise my rights against them.
```

### "Send us a copy of your ID."

```
I am willing to verify my identity proportionately. Under Article 12(6) you may request
only the additional information necessary to confirm my identity, and that request must be
proportionate to the sensitivity of the data and the risk of misidentification.

You hold my email address; I am writing from that address, which is itself strong
evidence of control. If you require more, I will provide a copy of an identity document
with all fields other than my name and photograph redacted, uploaded through a secure
channel you nominate. I will not send an unredacted identity document, and I will not send
identity documents by email.
```

### "Deletion would break our product / we have a legal obligation to retain."

```
Please identify the specific legal obligation, the jurisdiction it arises in, and the
retention period it prescribes. A commercial or contractual interest in retaining the data
is not a legal obligation within the meaning of Article 17(3)(b).

Where a genuine obligation applies to part of the data, Article 18 entitles me to
restriction of processing for the remainder: retain what you must, and cease all other
processing including publication, search indexing and disclosure.
```

---

## Follow-up sequence

### Follow-up 1 — at the deadline

**Subject:** `Follow-up: Data Erasure Request — {{FULL_NAME}} — sent {{ORIGINAL_DATE}}`

```
I wrote to you on {{ORIGINAL_DATE}} requesting the erasure of my personal data under
{{LAW}}. The statutory response period has now expired and I have had no substantive
response.

Original request details:
- Name: {{FULL_NAME}}
- Identifiers: {{ALL_EMAILS}}, {{USERNAMES}}
- Date sent: {{ORIGINAL_DATE}}
- Reference (if issued): {{REFERENCE}}

Please confirm within 7 days that the data has been erased. If you have decided to refuse
the request in whole or in part, you are required to tell me so, with reasons, and to
inform me of my right to complain to a supervisory authority.

{{FULL_NAME}}
```

### Follow-up 2 — final notice

```
This is a final notice before I refer this matter to {{REGULATOR}}.

My erasure request of {{ORIGINAL_DATE}} remains unanswered {{DAYS}} days later. The
statutory deadline under {{LAW}} was {{DEADLINE_DATE}}.

Unless I receive written confirmation of erasure by {{FINAL_DATE}}, I will file a
complaint with {{REGULATOR}} setting out the dates above.

I would prefer to resolve this directly and will withdraw nothing that has already been
actioned. Please treat this as a final opportunity to respond.

{{FULL_NAME}}
```

### Where a confirmed deletion did not hold

The single most useful escalation letter in the set, because it converts a soft dispute
into a documented misstatement.

```
On {{CONFIRMATION_DATE}} you confirmed in writing (reference {{REFERENCE}}) that my
personal data had been erased. As of {{TODAY}}, data relating to {{IDENTIFIER}} remains
retrievable through your service. I have retained evidence.

This means either that the erasure was not carried out, or that it was reversed by a
subsequent ingest without any suppression being applied. Either way your confirmation was
inaccurate.

Please confirm within 7 days: what happened; whether the identifiers have now been added
to a permanent suppression list; and what change prevents recurrence. Absent a
satisfactory response I will file a complaint with {{REGULATOR}} citing your written
confirmation and the current state of your service.
```

---

## Regulator complaints

Complaints are free, need no lawyer, and are decided on the documents. What they need:

1. The controller's name and website.
2. Your original request, in full, with the date sent.
3. Proof of delivery — the sent message, or a delivery receipt.
4. Every reply received, in full.
5. A one-paragraph statement of what you want: erasure, and a finding that the deadline
   was breached.
6. Evidence the data is still live, if it is — a dated screenshot.

In the EU, complain to **your own** national authority. It will liaise with the lead
authority under the one-stop-shop mechanism; that is its job, not yours.

| Jurisdiction | Regulator | Complaint route |
|---|---|---|
| Ireland | Data Protection Commission | https://forms.dataprotection.ie/contact |
| UK | ICO | https://ico.org.uk/make-a-complaint/ |
| France | CNIL | https://www.cnil.fr/en/plaintes |
| Germany | Federal & state DPAs | https://www.bfdi.bund.de |
| Netherlands | Autoriteit Persoonsgegevens | https://autoriteitpersoonsgegevens.nl/en |
| Spain | AEPD | https://www.aepd.es |
| Italy | Garante | https://www.garanteprivacy.it |
| EU (other) | Find your DPA | https://edpb.europa.eu/about-edpb/about-edpb/members_en |
| Switzerland | FDPIC | https://www.edoeb.admin.ch |
| California | CPPA | https://cppa.ca.gov/webapplications/complaint |
| US (other states) | State Attorney General | State AG consumer protection portal |
| Canada | OPC | https://www.priv.gc.ca/en/report-a-concern/ |
| Québec | CAI | https://www.cai.gouv.qc.ca |
| Brazil | ANPD | https://www.gov.br/anpd |
| South Africa | Information Regulator | https://inforegulator.org.za |
| Australia | OAIC | https://www.oaic.gov.au/privacy/privacy-complaints |
| New Zealand | OPC | https://privacy.org.nz/tools/complaint-form/ |
| Japan | PPC | https://www.ppc.go.jp |
| South Korea | PIPC | https://www.pipc.go.kr |
| Singapore | PDPC | https://www.pdpc.gov.sg |
| India | Data Protection Board | Per DPDP Rules |

## Re-verification

Deletion is not permanent. Datasets get re-ingested, companies get acquired with their
databases, and suppression lists get lost in migrations. Re-check the sites that mattered
— the ones that publish to the open web — every 90 days. A confirmed deletion that
silently reversed is a stronger complaint than one that never happened, so keep the
confirmation emails.
