# Privacy Laws — Erasure Rights by Jurisdiction

Thirteen regimes, with the operative provision, the statutory clock, how strong the
erasure right actually is, and where to complain when it is ignored.

Two things are true of every entry below and worth saying once: this is a working
reference for drafting requests, not legal advice; and the strength of a right on paper
is a poor predictor of how a given controller responds. The regimes with real
enforcement history — the EU, the UK, California, Brazil — get replies. The ones without
mostly get replies because the controller cannot be bothered to work out whether they are
obliged to.

**Verify before you rely.** Privacy law moves faster than documentation. Check the current
text before citing a deadline in a formal complaint.

---

## Quick comparison

| Regime | Erasure provision | Deadline | Right strength | Regulator |
|---|---|---|---|---|
| **EU GDPR** | Art. 17 | 1 month (+2 ext.) | Strong, broad extraterritorial reach | National DPA |
| **UK GDPR / DPA 2018** | Art. 17 | 1 month (+2 ext.) | Strong | ICO |
| **Swiss FADP** | Art. 32 | "Reasonable", ~30 days | Strong | FDPIC |
| **CCPA / CPRA (California)** | §1798.105 | 45 days (+45 ext.) | Strong for CA residents | CPPA / CA AG |
| **Other US states (19 more)** | Varies | 45 days typical | Moderate, resident-scoped | State AG |
| **PIPEDA (Canada)** | Principle 4.9 / s.8 | 30 days | Weak — access strong, erasure limited | OPC |
| **Québec Law 25** | Art. 28.1 | 30 days | Strong — includes de-indexing | CAI |
| **LGPD (Brazil)** | Art. 18(VI) | 15 days | Strong | ANPD |
| **POPIA (South Africa)** | s.24 | "Reasonable time" | Moderate | Information Regulator |
| **Privacy Act 1988 (Australia)** | APP 11.2 / 13 | 30 days | Weak — destruction duty, not a right | OAIC |
| **APPI (Japan)** | Art. 35 | "Without delay" | Moderate — conditional | PPC |
| **PIPA (South Korea)** | Art. 36 | 10 days | Strong | PIPC |
| **DPDP Act (India)** | s.12(3) | Per Rules | Strong on paper, phasing in | Data Protection Board |
| **Privacy Act 2020 (NZ)** | IPP 6/7 | 20 working days | Weak — correction, not erasure | OPC NZ |
| **PDPA (Singapore)** | s.16 / s.25 | 30 days | Weak — withdrawal of consent | PDPC |

---

## EU — GDPR

**Art. 17 (right to erasure / "right to be forgotten").** Ground yourself in 17(1)(a) —
data no longer necessary for the purpose collected — and 17(1)(c) where you object under
Art. 21 and the controller has no overriding legitimate grounds. For data scraped from
breach corpora, 17(1)(d) — unlawfully processed — is the strongest ground available and
the one most breach-search engines cannot answer.

- **Deadline:** one month from receipt (Art. 12(3)), extendable by two months for complex
  requests, but the controller must *tell you* it is extending, within the first month.
- **Free:** Art. 12(5). A controller charging a fee for a first request is in breach.
- **Onward recipients:** Art. 19 obliges the controller to notify every recipient it
  disclosed your data to, and to tell you who they are if you ask. Always ask.
- **Reach:** Art. 3(2) — applies to any controller anywhere offering goods or services to
  people in the EU, or monitoring their behaviour. Indexing an EU resident's leaked
  credentials and serving them to searchers is monitoring. Say this explicitly to
  US-hosted services that claim GDPR does not apply to them.
- **Refusal must be reasoned**, and must tell you about your right to complain to a DPA
  and to a judicial remedy (Art. 12(4)).
- **Regulator:** your own national DPA — you do not have to approach the controller's lead
  authority. Full list: https://edpb.europa.eu/about-edpb/about-edpb/members_en
- **Ireland (DPC):** https://forms.dataprotection.ie/contact
- **France (CNIL):** https://www.cnil.fr/en/plaintes
- **Germany:** federal-state DPAs, https://www.bfdi.bund.de
- **Netherlands (AP):** https://autoriteitpersoonsgegevens.nl/en

## UK — UK GDPR + Data Protection Act 2018

Substantively identical to Art. 17 post-Brexit, with the same one-month clock. The ICO is
markedly more responsive to individual complaints than most EU DPAs, and its
`Report a concern` route is the single most effective escalation in this document for
UK-facing controllers.

- **Regulator:** ICO — https://ico.org.uk/make-a-complaint/

## Switzerland — revised FADP (2023)

**Art. 32** gives a right to have unlawful processing stopped and data deleted. Not an EU
member, so cite the FADP directly rather than assuming GDPR carries.

- **Regulator:** FDPIC — https://www.edoeb.admin.ch

## California — CCPA as amended by CPRA

**§1798.105** — right to delete personal information collected from the consumer, with a
list of exceptions in 1798.105(d) that data brokers reach for constantly. §1798.120 gives
the separate right to opt out of sale or sharing, which is often the more useful lever
against ad-tech.

- **Deadline:** 45 days, extendable once by 45 more with notice.
- **Data broker registry:** California requires data brokers to register. The registry at
  https://cppa.ca.gov/data_broker_registry/ is a target list you did not have to research.
- **DELETE Act:** California's DROP mechanism lets a resident submit one deletion request
  that registered data brokers must honour — check its current operational status before
  telling anyone to rely on it.
- **Regulator:** CPPA — https://cppa.ca.gov/webapplications/complaint

## Other US states

Twenty states had comprehensive consumer privacy laws on the books as of 2026 — among
them Virginia, Colorado, Connecticut, Utah, Texas, Oregon, Montana, Delaware, Iowa,
Nebraska, New Hampshire, New Jersey, Tennessee, Minnesota, Maryland, Indiana, Kentucky and
Rhode Island. They converge on a similar shape: a deletion right for residents, a 45-day
clock, an appeal mechanism, and enforcement by the state Attorney General with no private
right of action.

Practically: name the subject's state law if they are a US resident, and otherwise skip
the state layer and lead with whichever of GDPR or CCPA the controller is likelier to
recognise.

## Canada — PIPEDA and Québec Law 25

**PIPEDA** is the weak one. It gives a strong right of *access* (Principle 4.9, 30 days)
and a duty to destroy data no longer needed for the stated purpose (Principle 4.5.3), but
no free-standing erasure right. The workable move is to request access first, then argue
the purpose has expired.

**Québec Law 25** is much stronger: Art. 28.1 gives a genuine de-indexing and cessation
right, closer to Art. 17 than to PIPEDA.

- **Regulators:** OPC — https://www.priv.gc.ca/en/report-a-concern/ ; CAI (Québec) —
  https://www.cai.gouv.qc.ca

## Brazil — LGPD

**Art. 18(VI)** — deletion of personal data processed with consent. Art. 18(IV) covers
anonymisation, blocking or deletion of unnecessary or unlawfully processed data, which is
the ground that fits scraped and breached data. The 15-day response window in Art. 19 is
the shortest of any major regime — use it, and cite it.

- **Regulator:** ANPD — https://www.gov.br/anpd/pt-br/canais_atendimento/cidadao-titular

## South Africa — POPIA

**s.24** — right to correction or deletion of personal information that is inaccurate,
irrelevant, excessive, out of date, incomplete, misleading, or obtained unlawfully. The
"obtained unlawfully" limb applies cleanly to breach-sourced data. Requests use the
prescribed **Form 2**.

- **Regulator:** Information Regulator — https://inforegulator.org.za

## Australia — Privacy Act 1988

No general erasure right. **APP 11.2** requires an entity to destroy or de-identify
personal information it no longer needs, and **APP 13** gives a correction right. The
argument that works: assert the entity has no lawful purpose for retaining the data and
is therefore obliged under APP 11.2 to destroy it.

- **Regulator:** OAIC — https://www.oaic.gov.au/privacy/privacy-complaints

## Japan — APPI

**Art. 35** — cessation of use or deletion, available where data was obtained improperly,
used beyond the notified purpose, or where retention creates a risk of harm to the
individual's rights. Breach-sourced data fits the first limb.

- **Regulator:** PPC — https://www.ppc.go.jp

## South Korea — PIPA

**Art. 36** — correction and deletion, with a 10-day response window under the Enforcement
Decree. One of the shortest clocks in the world and the reason PIPA is worth naming even
for controllers with a small Korean footprint.

- **Regulator:** PIPC — https://www.pipc.go.kr

## India — DPDP Act 2023

**s.12(3)** gives data principals a right to erasure. The Digital Personal Data
Protection Rules were notified in November 2025 with phased implementation, so procedural
detail — including the response window — comes from the Rules rather than the Act. Check
current status before citing a specific deadline in a formal complaint.

- **Regulator:** Data Protection Board of India.

## New Zealand — Privacy Act 2020

IPP 6 (access) and IPP 7 (correction); no erasure right. Principle 9 — do not keep
information longer than required for the purpose — is the retention argument. 20 working
days for access requests.

- **Regulator:** OPC — https://privacy.org.nz/tools/complaint-form/

## Singapore — PDPA

No erasure right as such. **s.16** gives withdrawal of consent, which triggers a duty to
cease collection, use and disclosure, and s.25 requires ceasing retention when the
purpose has ended. Frame the request as withdrawal of consent plus a s.25 retention
challenge, not as erasure.

- **Regulator:** PDPC — https://www.pdpc.gov.sg
