# Site Registry

Every organisation contacted during the ten-week campaign this skill was built from, grouped by what
they actually do with your data. **224 entries.** Machine-readable copy: [`site-registry.csv`](site-registry.csv).

Contact addresses are the ones that were *verified working* — where an obvious address bounced, the
replacement is recorded and the bounce noted. That column is the single most valuable thing in this
repo: finding it is the slow part of the job, and it is already done.

**Outcome** records what came back during the campaign. Treat it as evidence that the address is live,
not as a promise about your own request — a broker holding nothing on one person may hold plenty on another.

| Category | Entries |
|---|---|
| [Breach & leak search](#breach--leak-search) | 35 |
| [OSINT / email intelligence](#osint--email-intelligence) | 27 |
| [People search](#people-search) | 25 |
| [Major data broker](#major-data-broker) | 7 |
| [B2B contact data & lead-gen](#b2b-contact-data--lead-gen) | 69 |
| [Email verification](#email-verification) | 16 |
| [Ad-tech & audience data](#ad-tech--audience-data) | 28 |
| [Threat intelligence](#threat-intelligence) | 7 |
| [Regional directory](#regional-directory) | 10 |
| **Total** | **224** |


## Breach & leak search

| Site | Jurisdiction | Method | Verified contact | Outcome | Notes |
|---|---|---|---|---|---|
| BreachDirectory | US / intl | Email | `contact@breachdirectory.org` | Request sent — awaiting reply |  |
| BreachForums | Intl | N/A | `(seized 2024)` | Defunct — seized |  |
| BreachSense | US / intl | Email | `info@breachsense.com` | Request sent — awaiting reply |  |
| CheckLeaked.cc | US / intl | Email | `privacy@checkleaked.cc` | Request sent — awaiting reply | JS-only contact page |
| Cracked.io | Intl | N/A | `(seized)` | Defunct — seized |  |
| CyberNews Breach Checker | LT / EU | Self-service | `cybernews.com/data-leak-check-opt-out/` | Submitted |  |
| DataBreach.com | US / intl | Self-service + Email | `contact@databreach.com` | Submitted |  |
| DeHashed | US / intl | Web form | `dehashed.com/support` | Request sent — awaiting reply |  |
| Digital Footprint Check | US / intl | Email | `info@digitalfootprintcheck.com` | Request sent — awaiting reply |  |
| Exposed.vc | Intl | N/A | `(domain for sale)` | Defunct — no action |  |
| GhostProject | FR / EU | Social media | `ghostproject.fr` | Contacted via social |  |
| HackCheck.io | US / intl | Email | `hackcheck@hackcheck.io` | Request sent — awaiting reply | 16B+ records; address decoded from Cloudflare obfuscation |
| Hashes.org | Intl | Manual | `hashes.org` | Needs manual visit | Hash-cracking community |
| HashKiller | UK | Manual | `hashkiller.io` | Needs manual visit | Hash-cracking community forum |
| Have I Been Pwned | AU | Web form | `haveibeenpwned.com/OptOut` | Opt-out completed | Per-address email verification; choose public-search removal + breach deletion |
| HaveIBeenBreached / Cloaked | US / intl | Email | `privacy@cloaked.id` | No data |  |
| IntelFetch | SE / EU | Email | `dpo@intelfetch.net` | Confirmed removed |  |
| IntelX | CZ / EU | Web form | `intelx.io/abuse` | Confirmed removed (follow-up filed) |  |
| Leak-Lookup | US / intl | Email | `(previous session)` | Request sent — awaiting reply |  |
| LeakCheck | US / intl | Email | `(previous session)` | Removal approved |  |
| LeakedSource | Intl | N/A | `(shut down)` | Defunct — shut down |  |
| LeakNix | US / intl | Email | `info@leaknix.com` | Request sent — awaiting reply | support@ bounced |
| LeakPeek | UK | Live chat | `leakpeek.com/contact` | Contacted via live chat |  |
| LeakRadar | US / intl | Email | `contact@leakradar.io` | Request sent — awaiting reply | privacy@ bounced |
| Logoutify / BreachDirectory.com | US / intl | Email | `info@breachdirectory.com` | No records found |  |
| OffSeq Breach | US / intl | Email | `breach@offseq.com` | Request sent — awaiting reply |  |
| OSINTLeak | US / intl | Self-service | `osintleak.com` | Submitted |  |
| ProxyNova | US / intl | Email | `admin@proxynova.com` | Request sent — awaiting reply | Hosts the COMB credential dataset |
| PSBDMP | US / intl | Email | `support@psbdmp.ws` | Request sent — awaiting reply |  |
| RaidForums | Intl | N/A | `(seized 2022)` | Defunct — seized by FBI |  |
| ScatteredSecrets | US / intl | Email | `legal@scatteredsecrets.com` | Request sent — awaiting reply |  |
| Snusbase | US / intl | Email | `support@snusbase.com` | Request sent — awaiting reply |  |
| Snusbase | US / intl | Email | `help@snusbase.com` | Request sent — awaiting reply | Supports username search |
| WeLeakInfo | Intl | N/A | `(seized 2021)` | Defunct — seized by FBI/DOJ |  |
| XposedOrNot | US / intl | Email | `deva@xposedornot.com` | Request sent — awaiting reply |  |

## OSINT / email intelligence

| Site | Jurisdiction | Method | Verified contact | Outcome | Notes |
|---|---|---|---|---|---|
| AbstractAPI | US / intl | Email | `team@abstractapi.com` | Request sent — awaiting reply |  |
| AccuSights | US / intl | Email | `support@accusights.com` | Request sent — awaiting reply | privacy@ bounced |
| Analyst Research Tools | US / intl | N/A | `analystresearchtools.com` | No action — link aggregator only |  |
| BehindTheEmail | US / intl | Email | `contact@behindtheemail.com` | Request sent — awaiting reply |  |
| Castrick Clues | US / intl | N/A | `(closed Feb 2026)` | Defunct — service closed |  |
| ClarityCheck | US / intl | Email | `privacy@claritycheck.com` | Request sent — awaiting reply |  |
| CloudSint | US / intl | Email | `privacy@cloudsint.net` | Request sent — awaiting reply |  |
| EmailOSINT | US / intl | N/A | `(parked domain)` | Skipped — parked domain |  |
| EmailOSINT.org | US / intl | Email | `privacy@emailosint.org` | Confirmed processed |  |
| EmailRep.io | US / intl | Email | `privacy@sublimesecurity.com` | No PII identified |  |
| EmailSearch.io | US / intl | Email | `hi@emailsearch.io` | Request sent — awaiting reply |  |
| EmailSherlock | US / intl | Web form | `emailsherlock.com/optout` | Submitted |  |
| Epieos | FR / EU | Email | `contact@epieos.com` | Request sent — awaiting reply |  |
| FootprintIQ | US / intl | N/A | `footprintiq.app` | No action — client-side only | Ephemeral scans, no server storage |
| Forensic OSINT | US / intl | N/A | `forensicosint.com` | No action — client-side only | 100% client-side |
| IntelBase | US / intl | Email | `support@intelbase.is` | Request sent — awaiting reply |  |
| Intelligence Security | US / intl | N/A | `intelligencesecurity.io` | Skipped — site defunct |  |
| Mailboxlayer | AT / EU | Email | `support@mailboxlayer.com` | Request sent — awaiting reply |  |
| Minelead.io | US / intl | Email | `support@minelead.io` | Request sent — awaiting reply |  |
| Opsis OSINT | US / intl | Email | `privacy@useopsis.com` | Request sent — awaiting reply |  |
| OSINT Industries | UK | Web form | `osint.industries/contact-us` | No storage; suppression requested |  |
| Osintly | US / intl | N/A | `(parked domain)` | Skipped — parked domain |  |
| SEON | HU / EU | Email | `dpo@seon.io` | Request sent — awaiting reply |  |
| Skymem | US / intl | Email | `info@skymem.com` | No record |  |
| Social Searcher | US / intl | Email | `info@social-searcher.com` | No personal data stored |  |
| TraceFind | US / intl | Email | `contact@tracefind.info` | Request sent — awaiting reply |  |
| UserSearch | US / intl | Email | `hello@usersearch.com` | Request sent — awaiting reply |  |

## People search

| Site | Jurisdiction | Method | Verified contact | Outcome | Notes |
|---|---|---|---|---|---|
| BeenVerified | US / intl | Email | `privacy@beenverified.com` | No record |  |
| CheckPeople | US / intl | Email | `privacy@checkpeople.com` | Request sent — awaiting reply |  |
| ClustrMaps | US / intl | Email | `support@clustrmaps.com` | Request sent — awaiting reply | remove@ DNS failure |
| FamilyTreeNow | US / intl | Email | `privacy@familytreenow.com` | Request sent — awaiting reply |  |
| FastPeopleSearch | US / intl | Email | `support@fastpeoplesearch.zendesk.com` | Request sent — awaiting reply |  |
| IDCrawl | US / intl | Web form | `idcrawl.com/remove-my-information` | Form — user action required |  |
| InfoTracer | US / intl | Email | `privacy@infotracer.com` | Confirmed removed |  |
| Instant Checkmate | US / intl | Email | `privacy@instantcheckmate.com` | Confirmed deleted |  |
| Intelius | US / intl | Email | `privacy@intelius.com` | Confirmed deleted |  |
| Lullar | EU | Manual | `lullar.com` | Needs manual visit | Profile aggregator |
| MyLife | US / intl | Email | `privacy@mylife.com` | No record |  |
| Nuwber | US / intl | Email | `privacy@nuwber.com` | Request sent — awaiting reply |  |
| PeekYou | US / intl | Email | `info@peekyou.com` | Request sent — awaiting reply |  |
| Pentester.com | US | Web form | `forms.gle (opt-out form)` | Skipped — low relevance | support@ bounced; form is name/address oriented |
| PeopleFinders | US / intl | Email | `customercare@peoplefinders.com` | Request sent — awaiting reply |  |
| PeopleLooker | US / intl | Email | `privacy@peoplelooker.com` | No record |  |
| Pipl | US / intl | Web form | `pipl.com/personal-information-removal-request` | Submitted |  |
| Radaris | US / intl | Email | `removal@radaris.com` | Request sent — awaiting reply |  |
| Spokeo | US / intl | Email | `privacy@spokeo.com` | Request sent — awaiting reply |  |
| Spytox | US / intl | Email | `hello@spytox.com` | Site shut down |  |
| That'sThem | US / intl | Email | `optout@thatsthem.com` | Request sent — awaiting reply | privacy@ bounced |
| TruePeopleSearch | US / intl | Email | `support@truepeoplesearch.com` | Request sent — awaiting reply |  |
| Truthfinder | US / intl | Email | `privacy@truthfinder.com` | Request sent — awaiting reply |  |
| USPhoneBook | US / intl | Email | `privacy@usphonebook.com` | Request sent — awaiting reply |  |
| WhitePages | US / intl | Email | `privacy@whitepages.com` | Request sent — awaiting reply |  |

## Major data broker

| Site | Jurisdiction | Method | Verified contact | Outcome | Notes |
|---|---|---|---|---|---|
| Acxiom | US / intl | OneTrust portal | `privacyportal.onetrust.com` | No PII held (EU portal) |  |
| CoreLogic / Cotality | US / intl | Email | `privacy@corelogic.com` | Request sent — awaiting reply |  |
| Dun & Bradstreet | US / intl | Email | `eudpo@dnb.com` | Request sent — awaiting reply |  |
| Experian Marketing Services | US / intl | Email | `eu.data.privacy@experian.com` | No data held |  |
| LexisNexis | US / intl | Email | `privacy.information.mgr@lexisnexis.com` | Request sent — awaiting reply |  |
| Melissa Data | US / intl | Email | `optout@melissa.com` | Request sent — awaiting reply |  |
| Neustar / TransUnion | US / intl | Email | `ns_privacy@transunion.com` | Request sent — awaiting reply |  |

## B2B contact data & lead-gen

| Site | Jurisdiction | Method | Verified contact | Outcome | Notes |
|---|---|---|---|---|---|
| 6sense | US / intl | Email | `DataSubjectRequests@6sense.com` | Submitted via Ketch |  |
| Adapt.io | US / intl | Email | `support@adapt.io` | Request sent — awaiting reply |  |
| AeroLeads | US / intl | Email | `hello@aeroleads.com` | Request sent — awaiting reply |  |
| Albacross | SE / EU | Email | `support@albacross.com` | Request sent — awaiting reply |  |
| Amplemarket | US / intl | Email | `privacy@amplemarket.com` | Request sent — awaiting reply |  |
| AnymailFinder | UK | Email | `legal@anymailfinder.com` | Request sent — awaiting reply |  |
| Apollo.io | US / intl | Email | `(previous session)` | No data |  |
| Bombora | US / intl | Email | `dsars@bombora.com` | Request sent — awaiting reply |  |
| BookYourData | US / intl | Email | `gdpr@bookyourdata.com` | Request sent — awaiting reply | privacy@ bounced |
| BuiltWith | US / intl | Email | `support@builtwith.com` | Request sent — awaiting reply |  |
| Clay.com | US / intl | Email | `privacy@clay.com` | Request sent — awaiting reply |  |
| Clearbit | US / intl | Email | `privacy@clearbit.com` | Request sent — awaiting reply |  |
| Cognism | UK | Email | `privacy@cognism.com` | Request sent — awaiting reply |  |
| Coldlytics | US / intl | Email | `support@coldlytics.com` | Request sent — awaiting reply |  |
| ContactOut | US / intl | Email | `support@contactout.com` | Request sent — awaiting reply |  |
| CuFinder | US / intl | Email | `support@cufinder.io` | Request sent — awaiting reply | privacy@ bounced |
| Datagma | FR / EU | Email | `gdpr@datagma.com` | Request sent — awaiting reply |  |
| Dealfront / Leadfeeder | US / intl | Email | `dpo@dealfront.com` | Request sent — awaiting reply |  |
| Demandbase | US (EU rep) | Email | `GDPRrepresentative@demandbase.com` | Request sent — awaiting reply |  |
| Enrich.so | US / intl | Email | `team@enrich.so` | Request sent — awaiting reply |  |
| Evaboot | FR / EU | Email | `privacy@evaboot.com` | Request sent — awaiting reply |  |
| FindThatLead | US / intl | Email | `dpo@findthatlead.com` | Request sent — awaiting reply |  |
| Findymail | FR / EU | Email | `privacy@findymail.com` | Does not process personal Gmail |  |
| FullContact | US / intl | Email | `privacy@fullcontact.com` | Request sent — awaiting reply |  |
| FullEnrich | FR / EU | Email | `support@fullenrich.com` | No data |  |
| GetEmail.io | US / intl | Email | `support@getemail.io` | Request sent — awaiting reply | contact@ bounced |
| GetProspect | US / intl | Email | `support@getprospect.com` | Does not store personal Gmail |  |
| Groove | US / intl | Email | `support@groove.co` | Request sent — awaiting reply |  |
| HG Insights | US / intl | Email | `legal@hginsights.com` | Request sent — awaiting reply |  |
| HireEZ | US / intl | Email | `privacy@hireez.com` | No data |  |
| Hunter.io | US / intl | Email | `(previous session)` | Does not collect personal email |  |
| Interseller | US / intl | Email | `privacy@interseller.io` | Request sent — awaiting reply |  |
| Kaspr | FR / EU | Email | `privacy@kaspr.io` | Request sent — awaiting reply |  |
| Kendo | US / intl | Email | `support@kendoemailapp.com` | Request sent — awaiting reply |  |
| Lead Forensics | UK | Email | `data-compliance@leadforensics.com` | No data held |  |
| LeadGenius | US / intl | Email | `optout@leadgenius.com` | Request sent — awaiting reply |  |
| LeadIQ | US / intl | Email | `support@leadiq.com` | Confirmed removed |  |
| LeadLeaper | US / intl | Email | `contact@leadleaper.com` | Confirmed deleted |  |
| Lemlist | FR / EU | Email | `privacy@lemlist.com` | Request sent — awaiting reply | dpo@ bounced |
| Lusha | US / intl | Email | `privacy@lusha.com` | Request sent — awaiting reply |  |
| Mailshake | US / intl | Email | `hello@mailshake.com` | Request sent — awaiting reply |  |
| Mixmax | US / intl | Email | `privacy@mixmax.com` | Request sent — awaiting reply |  |
| Nymeria.io | US / intl | Email | `contact@nymeria.io` | Request sent — awaiting reply |  |
| Outreach.io | US / intl | Email | `support@outreach.io` | Request sent — awaiting reply |  |
| Overloop | US / intl | Email | `support@overloop.ai` | Already removed |  |
| People Data Labs | US / intl | Email | `privacy@peopledatalabs.com` | Request sent — awaiting reply |  |
| PhantomBuster | FR / EU | Email | `dpo@thephantomcompany.com` | Request sent — awaiting reply |  |
| Prospeo | US / intl | Self-service | `prospeo.io/optout` | Added to suppression list |  |
| ProxyCurl / Nubela | US / intl | Email | `hello@nubela.co` | Request sent — awaiting reply | privacy@ bounced |
| ReachStream | US / intl | Email | `support@reachstream.net` | Request sent — awaiting reply | privacy@ bounced |
| Reply.io | US / intl | Email | `dpo@reply.io` | No data |  |
| RocketReach | US / intl | Email | `(previous session)` | No profile found |  |
| SalesIntel | US / intl | Email | `support@salesintel.io` | Confirmed removed |  |
| Salesloft | US / intl | Email | `privacy@salesloft.com` | Request sent — awaiting reply |  |
| SalesQL | US / intl | Email | `privacy@salesql.com` | Request sent — awaiting reply |  |
| Seamless.ai | US (EU rep: IT Governance) | Email | `eurep@itgovernance.eu` | Processing |  |
| SignalHire | US / intl | Email | `support@signalhire.com` | Request sent — awaiting reply |  |
| Skrapp.io | US / intl | Email | `support@skrapp.io` | Request sent — awaiting reply |  |
| Snov.io | US / intl | Email | `snovio_dpo@snov.io` | No data held |  |
| Surfe (ex-Leadjet) | DE / EU | Email | `dpo@surfe.com` | Request sent — awaiting reply |  |
| Swordfish.ai | US / intl | Email | `contact@swordfish.ai` | Request sent — awaiting reply |  |
| Tomba.io | US / intl | Email | `support@tomba.io` | Request sent — awaiting reply |  |
| UpLead | US / intl | Email | `support@uplead.com` | Request sent — awaiting reply |  |
| Vainu | US / intl | Email | `support@vainu.com` | No data |  |
| VoilaNorbert | US / intl | Email | `support@voilanorbert.com` | Request sent — awaiting reply |  |
| Wiza | US / intl | Email | `optout@wiza.com` | Request sent — awaiting reply |  |
| Woodpecker.co | PL / EU | Email | `legal@woodpecker.co` | Request sent — awaiting reply |  |
| Yesware | US / intl | Email | `support@yesware.com` | Request sent — awaiting reply |  |
| ZoomInfo | US / intl | Email | `privacy@zoominfo.com` | Request sent — awaiting reply |  |

## Email verification

| Site | Jurisdiction | Method | Verified contact | Outcome | Notes |
|---|---|---|---|---|---|
| Bouncer | US / intl | Email | `hello@usebouncer.com` | Request sent — awaiting reply |  |
| BriteVerify / Validity | US / intl | Email | `privacy@validity.com` | Request sent — awaiting reply |  |
| Clearout | US / intl | Email | `us@clearout.io` | Request sent — awaiting reply |  |
| DeBounce | EU | N/A | `debounce.com/contact (form only)` | ⚠️ Needs action |  |
| Dropcontact | FR / EU | N/A | `(CNIL-audited, no personal DB)` | Skipped — CNIL-audited, no personal DB |  |
| EmailHippo | UK | Email | `dpo@emailhippo.com` | No records |  |
| EmailListVerify | US / intl | Email | `privacy@emaillistverify.com` | Request sent — awaiting reply |  |
| Kickbox | US / intl | Email | `help@kickbox.com` | Actioned |  |
| MillionVerifier | HU / EU | Email | `support@millionverifier.com` | No personal data processed |  |
| MyEmailVerifier | US / intl | Email | `support@myemailverifier.com` | Request sent — awaiting reply |  |
| NeverBounce | US / intl | Email | `privacy@neverbounce.com` | Request sent — awaiting reply |  |
| Proofy | US / intl | Email | `support@proofy.io` | Request sent — awaiting reply |  |
| QuickEmailVerification | US / intl | Email | `support@quickemailverification.com` | No account |  |
| Validity / BriteVerify portal | US | Web form | `privacyportal.onetrust.com` | Form — user action required | OneTrust webform |
| Verifalia | IT / EU | Email | `support@verifalia.com` | Does not retain personal data |  |
| ZeroBounce | US / intl | Email | `support@zerobounce.net` | Request sent — awaiting reply |  |

## Ad-tech & audience data

| Site | Jurisdiction | Method | Verified contact | Outcome | Notes |
|---|---|---|---|---|---|
| ActiveCampaign | US / intl | Email | `privacy@activecampaign.com` | Request sent — awaiting reply |  |
| Adform | DK / EU | Email | `privacy@adform.com` | Request sent — awaiting reply |  |
| Criteo | FR / EU | Email | `dpo@criteo.com` | Request sent — awaiting reply |  |
| DoubleVerify | US / intl | Email | `privacy@doubleverify.com` | Request sent — awaiting reply |  |
| Emarsys / SAP | AT / EU | Email | `dataprotection@emarsys.com` | Request sent — awaiting reply |  |
| Epsilon | US / intl | Email | `privacy@epsilon.com` | Request sent — awaiting reply |  |
| Eyeota | US / intl | Email | `privacy@eyeota.com` | Request sent — awaiting reply |  |
| Index Exchange | DE / EU | Email | `privacy@indexexchange.com` | Request sent — awaiting reply |  |
| Integral Ad Science (IAS) | US / intl | Email | `privacy@integralads.com` | Processing |  |
| LiveIntent | US / intl | Email | `privacy@liveintent.com` | Request sent — awaiting reply |  |
| LiveRamp | UK / US | Email | `ukprivacy@liveramp.com` | Request sent — awaiting reply |  |
| Lotame | US / intl | Email | `privacy@lotame.com` | Request sent — awaiting reply |  |
| Magnite / Rubicon Project | US (EU rep: Dublin) | Email | `privacy@magnite.com` | Request sent — awaiting reply |  |
| OpenX | US / intl | Email | `dpo@openx.com` | Acknowledged |  |
| Oracle Data Cloud / BlueKai | US / intl | Email | `privacy_ww@oracle.com` | Processing |  |
| Outbrain | UK / IL | Email | `privacy@outbrain.com` | Request sent — awaiting reply |  |
| PubMatic | US (EU rep: Amsterdam) | Email | `pubmaticprivacy@pubmatic.com` | Request sent — awaiting reply |  |
| Quantcast | US / intl | Email | `privacy@quantcast.com` | Request sent — awaiting reply |  |
| Seedtag | ES / EU | Email | `gdpr@seedtag.com` | Request sent — awaiting reply |  |
| Sharethrough | US / intl | Email | `support@sharethrough.com` | Request sent — awaiting reply |  |
| Smart AdServer | FR / EU | Email | `privacy@smartadserver.com` | Request sent — awaiting reply |  |
| Stirista | US / intl | Email | `privacy@stirista.com` | No record; opt-out list |  |
| Taboola | US / intl | Email | `dpo@taboola.com` | Request sent — awaiting reply |  |
| Teads | US / intl | Email | `dpo@teads.com` | Request sent — awaiting reply |  |
| The Trade Desk | US / intl | Email | `dpo@thetradedesk.com` | Request sent — awaiting reply |  |
| Xandr / Microsoft Advertising | UK / US | Web form | `aka.ms/privacyresponse` | ⚠️ Needs action | privacy@microsoft.com bounced — use aka.ms/privacyresponse |
| Zeotap | DE / EU | Email | `privacy@zeotap.com` | Request sent — awaiting reply |  |
| Zeta Global | US / intl | Email | `privacy@zetaglobal.com` | Request sent — awaiting reply |  |

## Threat intelligence

| Site | Jurisdiction | Method | Verified contact | Outcome | Notes |
|---|---|---|---|---|---|
| Bitsight / Cybersixgill | US / intl | Email | `privacy@bitsight.com` | Request sent — awaiting reply |  |
| Constella Intelligence | ES / EU | Email | `privacy@constellaintelligence.com` | Request sent — awaiting reply |  |
| Cyble | US / intl | Email | `dpo@cyble.com` | Request sent — awaiting reply |  |
| Flashpoint | US / intl | Email | `privacy@flashpoint.io` | Request sent — awaiting reply |  |
| Hudson Rock | US / intl | Email | `hello@hudsonrock.com` | Request sent — awaiting reply |  |
| SpyCloud | US / intl | Email | `privacy@spycloud.com` | Request sent — awaiting reply |  |
| ThreatMon | US / intl | Email | `info@threatmonit.io` | Request sent — awaiting reply | dpo@ bounced |

## Regional directory

| Site | Jurisdiction | Method | Verified contact | Outcome | Notes |
|---|---|---|---|---|---|
| 118118.com | UK | Email | `privacy@118118.com` | Request sent — awaiting reply | UK directory enquiries, Cardiff |
| 192.com | UK | Email | `privacy@192.com` | Request sent — awaiting reply | Electoral-roll people search; JS-heavy, contact unverified |
| Cylex UK | UK / DE | Manual | `uk.cylex.co.uk` | Needs manual visit | No contact exposed |
| Das Telefonbuch | DE / EU | Manual | `dastelefonbuch.de` | Needs manual visit | German phone directory |
| Herold.at | AT / EU | Manual | `herold.at` | Needs manual visit | Austrian phone/business directory |
| Infobel | BE / EU | Manual | `infobel.com` | Needs manual visit | Pan-European business directory |
| Scoot.co.uk | UK | Manual | `scoot.co.uk` | Needs manual visit | No contact exposed |
| Whitepages UK | UK | Email | `privacy@whitepages.co.uk` | Request sent — awaiting reply | Contact unverified |
| Yasni.de | DE / EU | Email | `datenschutz@yasni.de` | Request sent — awaiting reply | German people-search |
| Yell.com | UK | Email | `dpo@yell.com` | Request sent — awaiting reply | UK business/people directory, Reg. 4205228 |
