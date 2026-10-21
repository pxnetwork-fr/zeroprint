# 🧹 zeroprint — clean up your digital footprint with Claude

[🇫🇷 Français](README.md) · 🇬🇧 **English**

<p align="center"><img src="https://pix-geeks.com/wp-content/uploads/2026/10/effacer-traces-numeriques-123846-1200x675.jpg.webp" alt="Erase your digital footprint with Claude" width="100%"></p>

> Shrink the traces you leave online, methodically: inventory, ready-to-send erasure requests, search delisting, data breaches, and follow-up reminders.

This skill turns Claude into a digital clean-up assistant. It starts from what **you** find about yourself online, ranks each trace by sensitivity, drafts the requests that fit your country (GDPR, UK GDPR, CCPA, KVKK) and leaves you with a tracking table of deadlines, reminders and a complaint template.

**Claude sorts, drafts and tracks. It deletes nothing itself.** You send every request, and the recipient is the one who acts on it.

> ℹ️ The skill itself is written in French (instructions, letter templates, legal notes). Claude still works with it in English: ask in English and it answers in English. The letter templates for the UK (UK GDPR) and California (CCPA) are already in English.

---

## Contents

- [Why this skill](#why-this-skill)
- [What it does](#what-it-does)
- [What it does not do](#what-it-does-not-do)
- [Installation](#installation)
- [Usage](#usage)
- [Step by step](#step-by-step)
- [What you get](#what-you-get)
- [Legal frameworks covered](#legal-frameworks-covered)
- [Repository layout](#repository-layout)
- [Safeguards](#safeguards)
- [Known limits](#known-limits)
- [Prevention](#prevention)
- [Contributing](#contributing)
- [Disclaimer](#disclaimer)
- [Author](#author)
- [License](#license)

---

## Why this skill

In May 2026, a viral thread ("6 hours with Claude", picked up again in October 2026) showed that you could get much of your personal data taken off the internet with help from an AI. The idea was good. The method had blind spots:

| The viral thread | This skill |
|---|---|
| Promises erasure | Says honestly what will go and what will stay |
| Mixes up laws (Europeans invoking the CCPA) | Picks the law from your country of residence and checks it against the official source |
| Writes "they are required to delete" | Reminds you of the legal exceptions (press, retention duties…) |
| Stops once the letters are sent | Adds a tracking table, reminders and a complaint template |
| "6 to 7 hours" | One to two hours of preparation, then several weeks of follow-up |
| Ignores data breaches | Handles breaches (passwords, 2FA, accounts to close) |

Results come mostly from follow-up: a broker that never answers, a listing that reappears three months later. The skill is built around that reality.

---

## What it does

- 🔎 **Inventory** of your traces from the results you paste in: data brokers, social networks, old accounts, third-party pages, breaches.
- 🗂️ **Prioritisation** by sensitivity: home address, phone number and date of birth come before a username.
- ✉️ **Ready-to-send requests**, one per recipient, in the right language and on the right legal basis.
- 🔗 **Official forms first**: the skill looks for the broker's opt-out page before drafting a letter.
- 👻 **Forgotten accounts**: a method to find them in your inbox and delete them for good (not just deactivate).
- 🔍 **Delisting** from search engines, kept separate from the request to the source site.
- 🔐 **Data breaches**: the order of actions (password, 2FA, account closure).
- 📅 **Follow-up**: a table with computed deadlines, reminders drafted in advance, a complaint template for the regulator, and a 6–12-month check-up.

## What it does not do

- ❌ It deletes nothing itself and sends nothing on your behalf.
- ❌ It does not map **someone else's** footprint without an explicit mandate.
- ❌ It gives no legal advice: it provides templates and explains the process.
- ❌ It never suggests fake content, fake reviews or abusive takedown reports to "bury" a result.
- ❌ It never asks for an ID document, a password or a card number.

---

## Installation

### Option 1 — Claude (claude.ai, desktop or mobile app)

1. Download this repository (**Code → Download ZIP**), or just the `nettoyage-empreinte-numerique/` folder.
2. Zip the `nettoyage-empreinte-numerique/` folder: `SKILL.md` must sit at the top of the zipped folder.
3. In Claude, open the skills settings and upload the `.zip` file.
4. Turn the skill on.

> Custom skills must be available on your plan. See Claude's help centre (support.claude.com) if the option does not show up.

### Option 2 — Claude Code

```bash
# Personal skill, available in all your projects
git clone https://github.com/pxnetwork-fr/zeroprint.git
cp -r zeroprint/nettoyage-empreinte-numerique ~/.claude/skills/
```

Or, for a single project, copy the folder into `.claude/skills/` at the project root.

### Option 3 — API / Agent SDK

Load the folder as a custom skill following Anthropic's documentation (docs.claude.com, "Agent Skills" section).

---

## Usage

The skill triggers on its own for requests such as:

- "I want my data removed from the internet"
- "Get my address and phone number off people-search sites"
- "Help me opt out of data brokers"
- "Help me delete my old accounts"
- "Draft a GDPR erasure request"
- "I want an article about me delisted from Google"
- "Has my email been in a data breach?"
- "I saw the '6 hours with Claude' thread, can we do that?"

### Sample first exchange

> **You:** I want to clean up my digital footprint, my address shows up on people-search sites.
>
> **Claude:** To set things up: which country do you live in? Which identifiers should we cover (name and variants, usernames, emails, phone numbers, previous address)? And what's the main goal: less spam, a job search, safety, one specific piece of content?

Then you search your name, emails and phone numbers on two search engines, paste the links or screenshots, and Claude builds the inventory.

---

## Step by step

```
 0. Scope           country, identifiers, goal → applicable law, verified
 1. Inventory       your results → table ranked by sensitivity
 2. Data brokers    official opt-out form, otherwise a letter
 3. Accounts        inbox + justdeleteme → permanent deletion
 4. Pages & engines request to the site / delisting from the engine
 5. Breaches        haveibeenpwned → password, 2FA, closure
 6. Follow-up       deadlines, reminders, complaint, 6–12-month check
```

### Step 0 — Scope
Claude asks, in one go, for your country of residence, the identifiers to cover and your goal. The country sets the applicable law, which the skill **checks against the official source** before writing down any deadline. If you mention a danger (harassment, violence, threats), it starts with protective steps and handles your address and phone number first.

### Step 1 — Inventory
You run the searches yourself and paste the results. Claude sorts them:

| category | site | URL | exposed data | sensitivity | action | legal basis |
|---|---|---|---|---|---|---|
| data broker | example-directory.com | https://… | address, phone | high | opt-out form | GDPR |
| old account | old-forum.net | https://… | username, email | medium | account deletion | GDPR |

Claude does not search for you beyond what you provide.

### Step 2 — Data brokers
For each broker, the skill first looks for the official opt-out page, often faster than a letter. Failing that, it drafts a request for erasure **and** an end to resale, with the listing URLs and a request for acknowledgement.

### Step 3 — Forgotten accounts
A search for welcome emails ("confirm your address", "welcome"…) plus justdeleteme.xyz. For each account: export first if useful, permanent deletion, announced purge delay.

### Step 4 — Third-party pages and search engines
- Content on a site: request to the site, with the exact URL and the reason.
- A result tied to your name: delisting request through the engine's forms.
- If nothing can come down: the "publish better" approach (professional profile, personal page) is presented for what it is: slow, and nothing gets removed.

### Step 5 — Data breaches
You check your emails on haveibeenpwned.com. Claude ranks by risk: password to change (especially if reused), 2FA to enable (an authenticator app rather than SMS), account to close.

### Step 6 — Follow-up and reminders
A tracking table built from `assets/suivi-demandes.csv`: a computed deadline for each request, a reminder drafted in advance, a complaint template for the EU, a reminder to keep proof of every submission, and an offer to redo the inventory every 6 to 12 months.

---

## What you get

1. **A prioritised inventory** of your traces.
2. **Ready-to-send requests**, one per recipient, with the form or address to send them to.
3. **A tracking table** with deadlines, reminders and, where relevant, the complaint template.
4. **One honest line on the expected outcome**: what can go, what will stay, when to check again.

---

## Legal frameworks covered

| Residence | Law | Response time (benchmark) | Recourse |
|---|---|---|---|
| 🇫🇷 France | GDPR (Art. 17, 21, 12) | 1 month, +2 months if complex | CNIL |
| 🇪🇺 EU / EEA | GDPR | same | national authority |
| 🇬🇧 United Kingdom | UK GDPR | 1 month | ICO |
| 🇹🇷 Turkey | KVKK (Law 6698) | 30 days | KVKK Board |
| 🇺🇸 California | CCPA / CPRA | 45 days | CPPA, DROP portal |
| 🌍 Elsewhere | local law / opt-out | varies | local authority |

⚠️ These deadlines are **benchmarks dated October 2026**. The skill re-checks them against the official source before putting them in a letter. Details and selection rules (in French): [`references/droit-applicable.md`](nettoyage-empreinte-numerique/references/droit-applicable.md).

---

## Repository layout

```
.
├── README.md                          ← documentation (French)
├── README.en.md                       ← this page (English)
├── LICENSE
└── nettoyage-empreinte-numerique/     ← the skill (folder to install)
    ├── SKILL.md                       ← instructions Claude reads
    ├── references/
    │   ├── droit-applicable.md        ← legal frameworks, deadlines, exceptions
    │   └── modeles-courriers.md       ← 8 templates (FR, EN, TR)
    └── assets/
        └── suivi-demandes.csv         ← tracking table template
```

### Letter templates included

1. Erasure request — GDPR (France / EU), in French
2. Erasure request — UK GDPR, in English
3. Deletion request — CCPA (California), in English
4. Erasure request — KVKK, in Turkish
5. Account deletion where no online process exists
6. Reminder after the deadline
7. Complaint to the regulator (CNIL): documents to gather
8. Delisting from a search engine

They are templates to adapt, never to send as is.

---

## Safeguards

The skill applies these rules before doing anything:

- **Your own data only**, or that of someone who has given you a mandate (a minor child, an elderly parent, a client with power of attorney). Mapping a third party's footprint without a mandate is building a surveillance file.
- **No promise of erasure.** Caches, archives and leaked databases survive.
- **Never "they are required to".** The right to erasure has exceptions.
- **No legal advice.** For a dispute: a lawyer or the data protection authority.
- **Data minimisation.** Only name, emails, phone numbers and country. No ID document, password or bank card: letters state that proof of identity will be provided on request.
- **Law checked before it is written.** Deadlines, forms and laws change.

---

## Known limits

- **Listings come back.** Brokers re-collect public data or buy it again. Plan a new pass every 6 to 12 months.
- **Not everything can be erased.** Public registers, court decisions and legitimate press articles stay online.
- **Archives.** The Wayback Machine and caches keep copies.
- **Breaches are permanent.** Leaked data keeps circulating; you limit the damage, you do not get it back.
- **US data brokers** do not fall under the CCPA for a European resident: use their own opt-out process.

---

## Prevention

- An **email alias** for every sign-up (SimpleLogin, addy.io or your mail provider's aliases): if one leaks, delete it.
- A **browser or extension** that blocks trackers by default.
- **Social networks** set to private: profile not indexed, friends list hidden.
- A **secondary phone number** for sign-ups and classified ads.
- A **password manager** and 2FA wherever possible.

---

## Contributing

Contributions are welcome, especially:

- 🌍 **new legal frameworks** (Switzerland/nFADP, Quebec/Law 25, Brazil/LGPD…) in `references/droit-applicable.md`;
- ✉️ **letter templates** in other languages;
- 🔄 **updates** when a deadline, portal or form changes, with a link to the official source.

Open an *issue* or a *pull request*. Please cite the official source for any legal information.

---

## Disclaimer

This skill provides general information and letter templates. **It is not legal advice.** Laws, deadlines and procedures change: check them with the official sources (CNIL, ICO, CPPA, KVKK…) before taking action. For a dispute, consult a lawyer or your country's data protection authority.

---

## Author

Created by **Fabien Elharrar** · [fabien.elharrar.com](https://fabien.elharrar.com/) · [@fabienelh](https://github.com/fabienelh)

---

## License

Released under the [MIT](LICENSE) license: you are free to use, fork, modify and redistribute it, including commercially. The only condition is to keep Fabien Elharrar's copyright notice in your copies.

---

<sub>Made by [Fabien Elharrar](https://fabien.elharrar.com/) · A skill for [Claude](https://claude.ai), by Anthropic.</sub>
