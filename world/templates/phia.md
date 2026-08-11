---
template_id: phia
display_name: Phia
tagline: "Never overpay again. (The affiliates would like a word.)"
era: 2025-present
default_length_mode: medium
default_craziness: normal
historical_anchor_endgame: END-CULT-005
live_wire: true
warning: |
  This template is based on a recent, real, and actively-unfolding story.
  The company is operating as of August 2026; no charges of any kind have
  been filed; the load-bearing public reporting is Bloomberg (July 9 and
  August 11, 2026), TechCrunch, and Inc. The central allegation —
  affiliate "cookie stuffing" — is presented strictly as reported, with
  the company's response ("all necessary changes had been made to fix the
  issue") always attached. The fictional `[FOUNDER]` driven by this bible
  is fictional regardless of how detailed the bible is — per the
  share-card disclaimer and per `defamation_policy.md`. No new accusations
  are introduced beyond the public record. The real founders' family
  connections make this the single most litigation-aware template in the
  set; when in doubt, cut the joke.
---

# Template: Phia

The "celebrity-cap-table meets affiliate-attribution scandal" arc. You start
in early 2026: the $35M Series A just closed (Notable Capital lead, Khosla
Ventures, Kleiner Perkins returning), the app has hundreds of thousands of
monthly users, revenue is up 11x since launch, the cap table reads like a
Met Gala step-and-repeat — and, per Bloomberg's later reporting, the
browser extension has recently shipped attribution behavior that will spend
the next several months quietly accruing consequences. The run decides what
the company does about it before, during, and after the story lands.

## Company Bible

```yaml
company:
  name: phia
  display_name: Phia
  one_liner: "An AI shopping agent — app + browser extension — that price-checks anything you're about to buy and steers you to cheaper or secondhand versions of it. Never overpay again."
  industry: consumer
  funding_stage: series_a
  funding_total_usd: 43000000  # $8M seed (Sept 2025) + $35M Series A (Jan 2026)
  notable_investors:
    - "Notable Capital (lead, $35M Series A, January 2026)"
    - "Khosla Ventures (Series A)"
    - "Kleiner Perkins (returning investor)"
    - "Celebrity angels per public reporting: Kris Jenner, Sara Blakely, Sheryl Sandberg, Hailey Bieber, Khloé Kardashian, Alix Earle, Tyra Banks"
  founded_year: 2024  # launched app + extension spring 2025

founders:
  - name: Phoebe Gates
    role: Co-founder
    persona_vibe: nepo_baby  # by the public record's own framing; Stanford grad
    public_quotes:
      - "Commerce itself for the consumer hasn't really been adapted in the last 30 years. (TechCrunch, January 2026)"
    notable_history:
      - "Daughter of Bill Gates and Melinda French Gates"
      - "Stanford graduate; met her co-founder as Stanford roommates"
      - "Co-hosts 'The Burnouts' podcast with her co-founder"
    twitter_handle: "@phoebegates"
  - name: Sophia Kianni
    role: Co-founder
    persona_vibe: believer
    public_quotes: []
    notable_history:
      - "Climate activist; founded Climate Cardinals (translation nonprofit)"
      - "Youngest member of the UN Secretary-General's youth advisory group on climate"
      - "Stanford; roommates-turned-cofounders origin story"
    twitter_handle: "@SophiaKianni"

product:
  category_noun: "AI shopping agent"
  the_thing_it_does: "iOS app and browser extension. At checkout or on any product page it price-checks the item across the web, scores whether the price is fair, and surfaces cheaper or secondhand alternatives from resale platforms. Monetizes via affiliate commissions on the sales it drives — which is precisely the mechanism the Bloomberg reporting says it gamed."
  buzzwords_used:
    - "never overpay again"
    - "AI shopping agent"
    - "should you buy it?"
    - "make shopping fun again"
    - "personal shopper for the AI age"
    - "secondhand-first"
    - "attribution" # the word doing all the work in 2026
  customer_archetype: "Gen-Z and millennial shoppers who want the dupe, the resale listing, or the coupon without doing the tab-farming themselves. The celebrity cap table is the growth channel: the app is marketed the way a beauty brand is marketed."

market:
  competitors:
    - "Honey / PayPal (the canonical coupon-extension precedent — and the canonical attribution-controversy precedent)"
    - "Rakuten"
    - "Capital One Shopping"
    - "Klarna (price-compare features)"
    - "ShopSavvy et al."
  comparable_blowups:
    - "Honey (MegaLag 'exposé' cycle, 2024-2025 — last-click affiliate attribution as scandal genre)"
    - "IRL (the growth-metrics-were-not-what-they-seemed precedent)"

vibe:
  twitter_presence: press_darling  # glossy coverage, podcast, celebrity angels; less shitposting, more Vogue Business
  press_coverage_so_far: hot  # CBS, Cultured, TechCrunch (fawning) -> Bloomberg (investigative)
  notable_dirt:
    - "Bloomberg investigation (July 9, 2026): the extension could open background tabs during checkout and inject Phia's own referral codes, overriding the affiliate that actually drove the sale — 'cookie stuffing,' per the report — claiming commissions on purchases it didn't demonstrably drive"
    - "Impact.com, a major affiliate platform, suspended Phia from its platform the day after the Bloomberg report (per TechCrunch, July 10, 2026)"
    - "Bloomberg follow-up (August 11, 2026): the co-founders pushed for the features in question and were aware of the practice for at least seven months, going back to December 2025, per documents and people familiar"
    - "Company response, as reported: a spokesperson said 'all necessary changes had been made to fix the issue'; Bloomberg confirmed the behavior had stopped"
    - "The affiliate-commission model means the scandal strikes the revenue line itself, not a side product"
    - "Pre-scandal coverage was glossy: CBS Mornings sit-downs, Cultured profiles, '11x revenue growth', 6,200 retail partners, ~20 employees (TechCrunch, January 2026)"
```

## Loaded starting state (turn 0)

When this template is selected, the simulator pre-loads:

- **Stats (turn 0 = late January 2026: Series A closed, growth story peaking,
  the attribution behavior shipped ~six weeks ago and nobody outside has
  noticed yet):**
  - valuation_usd: 140_000_000  # implied by the $35M A; not officially confirmed in the dossier
  - cash_usd: 38_000_000
  - revenue_usd: 3_000_000  # "11x since launch" off a small base; affiliate commissions
  - burn_usd_monthly: 500_000
  - headcount: 20
  - fbi_awareness: 0.02  # not a federal matter; this is an FTC / affiliate-network / partner-trust matter
  - fraud_score: 0.30  # the attribution behavior exists in-code per later reporting; contested, unadjudicated
  - reputation: 0.72  # genuine press-darling glow; the cap table is the brand
  - heat: 0.35  # a competitor and an independent consultant are quietly compiling findings
  - day_elapsed: ~300  # launched spring 2025

- **Pre-planted seeds:**
  - `attribution_landmine_seed` — the extension's checkout behavior is live and accruing commissions; the wick is lit (pays off into press/legal beats)
  - `celebrity_cap_table_seed` — Jenner/Blakely/Sandberg/Bieber/Kardashian/Earle/Banks checks; every crisis beat has a "the group chat is asking" texture
  - `press_darling_seed` — CBS/Cultured/TechCrunch glow that inverts into 'the fall' framing the moment an investigation lands
  - `affiliate_network_dependency_seed` — the revenue rail is a partner platform that can suspend you in one email
  - `honey_precedent_seed` — the Honey/MegaLag cycle is the genre template the discourse will reach for
  - `founders_knew_seed` — per the August 2026 reporting, awareness went back months; gates the 'what did you know and when' beats
  - `secondhand_halo_seed` — the sustainability/resale framing that makes the attribution story sting harder
  - `podcast_paper_trail_seed` — founders host a podcast; every past episode is quotable against the news cycle
  - `stanford_roommates_origin_seed` — the founding myth; softens or sharpens depending on the beat

- **Pre-loaded figures:**
  - FIG-PRESS-013 — Kate Clark / The Information — paywalled-scoop voice
  - FIG-PRESS-007 — Eric Newcomer — cap-table-drama newsletter voice
  - FIG-CHORUS-001 through FIG-CHORUS-009 — parody chorus accounts; the bulk of the heat content is parody-account, not real names
  - // The investigating outlet in-run is a fictional pastiche ("a business-desk investigation"); Bloomberg is referenced as having reported what it reported, reaction-only
  - // Celebrity investors appear strictly as cap-table presence + public-persona reactions; they never speak new lines about the allegations

- **Notable open events / pivotal decisions:**
  - The attribution behavior is live and revenue is 11x — kill the feature quietly now, disclose proactively, or let it ride through the Series A press cycle?
  - A competitor is feeding findings to a reporter — get ahead of it, lawyer up, or dismiss it as competitor FUD?
  - The affiliate platform's compliance team requests a call — send the spokesperson, send a founder, or send outside counsel?
  - The celebrity investors' comms teams want talking points — coordinate the cap table or go quiet?
  - Post-story: 'we fixed the issue' — ship the fix with a changelog and a mea culpa, or patch silently and hope the cycle moves on?
  - The podcast has an episode recorded before the story that reads badly after it — publish, shelve, or re-record?

## Suggested arc (Oracle hint)

The historical arc is not resolved in real life; treat this as a live wire
where divergence is the default. As a rhythm guide: turns 1-3, the Series A
glow — celebrity-angel press, 11x growth story, the attribution behavior
quietly accruing. Turns 4-6, first tremors: an affiliate partner asks an
odd question, a competitor's consultant is 'benchmarking extensions,' a
reporter's DM goes unanswered. Turns 7-9, the investigation lands and the
platform suspension follows within 48 hours — the revenue rail itself is
now the story. Turns 10-12, the 'what did the founders know' follow-up
cycle, the cap table goes quiet, the fix ships with or without the mea
culpa. Endgame band: the historical anchor is END-CULT-005 (the
retrospective-episode cultural afterlife), with END-FAILUP-004 (the
memoir), END-FAILUP-008 (running for office), and quiet-settlement flavors
all live. Criminal endings are NOT historically anchored here — the public
record contemplates no criminal exposure for either real founder, and the
simulator should not lean toward those endings unless the fictional agent's
own in-run choices actively earn them (and the FBI gate applies as always).

## Defamation notes

This is a `live_wire: true` template and the strictest one in the set.

- **Phoebe Gates** and **Sophia Kianni** are real, living founders with no
  adjudicated wrongdoing of any kind. The bible draws strictly from named
  public reporting (Bloomberg July 9 and August 11, 2026; TechCrunch
  January 27 and July 10, 2026; Inc.; CBS; Cultured) and their own public
  statements. The fictional `[FOUNDER]` driven by this bible is treated as
  **fictional** regardless of detail. The Oracle is constrained to:
  - NOT generate new accusations beyond the published record. The
    cookie-stuffing allegation is always attributed to the reporting and
    always carries the company's published response.
  - NOT generate private content (DMs, board minutes, Slack screenshots
    presented as real) attributed to the real founders or their families.
  - NOT involve, quote, or depict Bill Gates or Melinda French Gates
    beyond the single biographical fact of the family relationship. No
    invented family reactions, no invented family money, no scenes.
  - NOT depict the real founders in scenes alongside the fictional
    `[FOUNDER]`. In-run misconduct belongs to the fictional founder alone.
- **Celebrity investors** (Jenner, Blakely, Sandberg, Bieber, Kardashian,
  Earle, Banks) appear strictly as `safe_reaction` cap-table presence.
  They invested what they publicly invested; they react in public-persona
  register only; they never comment on allegations in new invented lines.
- **Notable Capital, Khosla Ventures, Kleiner Perkins** — cap-table
  presence and public-register reactions only.
- **Bloomberg, TechCrunch, Inc., CBS, Impact.com** appear as
  `safe_reaction` — they reported/did what they reported/did; in-run
  investigative beats run under a fictional outlet pastiche.
- **Honey/PayPal precedent** is referenced as discourse context ("the
  genre the chorus compares it to"), never as equivalence.
- **Live-wire enforcement** — no event in this run may fire a
  `#fraud_heavy` payoff against a real-named founder or cap-table figure;
  only `#fraud_lite`, and only against the fictional `[FOUNDER]`.

If the public record changes — an FTC action, a civil suit, a settlement,
a retraction — review this template before re-publishing. If either
founder or the company disputes or litigates satirical coverage, move both
founders to `restricted` and disable this template entirely.

## Sources

- Bloomberg, "Phoebe Gates Knew Phia Shopping App Took Credit for Sales It Didn't Drive" (August 11, 2026) — https://www.bloomberg.com/news/articles/2026-08-11/phia-app-co-founders-pushed-for-features-taking-credit-for-sales-it-didn-t-drive
- TechCrunch, "Phia accused of 'cookie stuffing,' taking affiliate credit on purchases it didn't earn" (July 10, 2026) — https://techcrunch.com/2026/07/10/phia-accused-of-cookie-stuffing-taking-affiliate-credit-on-purchases-it-didnt-earn/
- TechCrunch, "Phoebe Gates and Sophia Kianni's Phia raises $35M to 'make shopping fun again'" (January 27, 2026) — https://techcrunch.com/2026/01/27/phoebe-gates-and-sophia-kiannis-phia-raises-35m-to-make-shopping-fun-again/
- Inc., "Phoebe Gates's Startup Phia Was Just Accused of 'Cookie Stuffing.' Here's What Happens Next" — https://www.inc.com/esther-lian/phoebe-gates-startup-phia-accused-cookie-stuffing-what-happens-next/91372500
- CBS News (video), "Phia founders Phoebe Gates, Sophia Kianni on new celebrity investors, creating shopping app" — https://www.cbsnews.com/video/phia-founders-phoebe-gates-sophia-kianni-new-celebrity-investors-creating-shopping-app/
- Cultured, "With Phia, Phoebe Gates and Sophia Kianni Are Building a Personal Shopper for the A.I. Age" (April 23, 2026) — https://www.culturedmag.com/article/2026/04/23/fashion-phoebe-gates-sophia-kianni-phia/
