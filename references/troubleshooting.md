# Troubleshooting

Everything here happened during the ten-week campaign. The pattern is more useful than
the individual case: assume roughly a fifth of your carefully-researched contact addresses
will fail, and build the campaign so that finding out costs you a day rather than a month.

---

## Bounced addresses

**Roughly one in eight verified privacy addresses bounced.** The address on a privacy
policy is often years stale. Observed failures and their working replacements:

| Failed | Working replacement |
|---|---|
| `privacy@` at several people-search sites | `optout@`, `removal@`, `customercare@` |
| `dpo@` at mid-size SaaS | `privacy@`, `legal@`, `support@` |
| `privacy@microsoft.com` | the web form at `aka.ms/privacyresponse` |
| `remove@` (DNS failure) | `support@` |
| `contact@` | `support@` |

The order that works, cheapest first:

1. Re-read the current privacy policy — the address in your notes may be from a cached
   version.
2. Check `https://domain/.well-known/security.txt` — often carries a live contact when the
   privacy page does not.
3. Try `support@` and `legal@`. Support tickets get routed to compliance; unmonitored
   `privacy@` aliases do not.
4. Check the WHOIS abuse contact.
5. For EU-facing companies, look for a named Article 27 representative — those addresses
   are monitored precisely because they exist for this purpose.
6. Live chat. Ask for the right address rather than making the request; agents will give
   you one.
7. Social DM. Smaller breach-search operators frequently answer on Telegram or X and
   nowhere else.

**Log every bounce.** A bounce is not a completed contact, and an untracked bounce is the
most common way a site quietly stays on the list of things you think you handled.

---

## CAPTCHAs and reCAPTCHA

Opt-out forms are heavily protected, and rightly so. Do not attempt to solve or bypass
them — leave the CAPTCHA to the person whose data it is. The practical arrangement is to
fill everything else in, then hand over for the final click.

Where a form is truly inaccessible, email is nearly always an acceptable alternative
channel: no regime requires a data subject to use a specific form, and a request sent to
a monitored address starts the statutory clock just as a form submission does. Say so if
challenged.

---

## Geo-blocking

Several US people-search sites Cloudflare-block or outright refuse EU and UK traffic —
sometimes as a deliberate GDPR-avoidance measure. Their opt-out form is then unreachable
by exactly the people with the strongest right to use it.

Email instead, and name the problem in the request. "Your opt-out form is not accessible
from my country, so I am making this request by email" is both a fact and a useful thing
to have in writing if you end up complaining.

---

## The `From:` address problem

**Several services key their automated removal off the sender address.** Leak-Lookup is
the clearest example: mail its removal address from account A and account A gets
blacklisted, regardless of what the body asks for.

Consequences:

- Send each address's request **from that address** where you can still access it.
- Where the mailbox is gone, say so explicitly and ask for a manual suppression:
  *"I no longer have access to this mailbox and cannot write from it. Please apply the
  suppression manually and confirm to this address."*
- Where a service verifies by emailing a link to the address being removed — Have I Been
  Pwned's opt-out works this way — the request can only be completed from that inbox.
  Nobody can do it for you.

Plan the campaign around this. Do one address at a time, from that address, rather than
running everything from a primary account and discovering at the end that two thirds of
the automated paths ignored you.

---

## Expiring verification links

Self-service opt-outs commonly send a confirmation link valid for **15 minutes to 24
hours**. Two of them expired unused during the source campaign and had to be restarted
weeks later.

Do the self-service opt-outs in a single sitting with the inbox already open, and treat
them as a separate work session from the email drafting.

---

## Automating a mail client

The single most common failure mode when driving Gmail through browser automation: **the
message sends with a correct subject and an empty body.** The compose body is a
`contenteditable` div rather than a textarea, and setting `.value` on it silently does
nothing.

What works:

```js
document.execCommand('insertText', false, subjectText);  // focus input[name="subjectbox"] first
document.execCommand('insertText', false, bodyText);     // focus div[aria-label="Message Body"] first
```

And then, before every send, read both fields back and confirm they are non-empty. A
blank message to a compliance inbox is worse than no message: it burns the contact and
you will believe the site is handled.

---

## JavaScript-only contact pages

A meaningful number of breach-search and directory sites render their contact details
only after JS execution, or obfuscate the address through Cloudflare's email protection.
Fetching the HTML returns nothing useful.

- Cloudflare-obfuscated addresses can be decoded from the `data-cfemail` attribute.
- Otherwise, load the page in a real browser and read it.
- Failing that, the registry marks these as **Needs manual visit** — they are a short list
  and worth an hour with a browser open.

---

## Sites that are gone

Several notorious breach-search services have been seized by law enforcement or shut
down: WeLeakInfo (2021), RaidForums (2022), BreachForums (2024), LeakedSource, Cracked.io.

Nothing to do, and nothing to worry about from those specific domains — but the datasets
they hosted did not disappear with them. They resurface under new operators, which is the
argument for suppression lists over one-time deletions.

---

## Sites that genuinely hold nothing

A large share of email-verification services do not retain personal data at all: they
check deliverability in real time and discard. Several replied to that effect and the
claim is plausible and, in some cases, independently audited.

Do not treat these as evasions. Ask for prospective suppression, accept the answer, log
it, and spend the effort on the categories that publish.
