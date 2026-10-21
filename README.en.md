# 🧹 zeroprint — clean up your digital footprint with AI

[🇫🇷 Français](README.md) · 🇬🇧 **English**

<p align="center"><img src="https://pix-geeks.com/wp-content/uploads/2026/10/effacer-traces-numeriques-123846-1200x675.jpg.webp" alt="Erase your digital footprint with AI" width="100%"></p>

> Shrink the traces you leave online, methodically: inventory, ready-to-send erasure requests, search delisting, data breaches, and follow-up reminders.

This skill turns your AI assistant — **Claude, ChatGPT, Gemini, Hermes, Mistral, Codex…** — into a digital clean-up assistant. It starts from what **you** find about yourself online, ranks each trace by sensitivity, drafts the requests that fit your country (GDPR, UK GDPR, CCPA, KVKK) and leaves you with a tracking table of deadlines, reminders and a complaint template.

**The AI sorts, drafts and tracks. It deletes nothing itself.** You send every request, and the recipient is the one who acts on it.

> ℹ️ The skill itself is written in French (instructions, letter templates, legal notes). Any assistant can work with it in English: ask in English and it answers in English. The letter templates for the UK (UK GDPR) and California (CCPA) are already in English.

---

## Contents

- [Why this skill](#why-this-skill)
- [What it does](#what-it-does)
- [What it does not do](#what-it-does-not-do)
- [Compatibility](#compatibility)
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
- 📵 **Stop the spam**: objection to direct marketing (GDPR Art. 21), and for France the cold-calling rules in force since Bloctel was shut down.
- 🧾 **B2B data brokers** (ZoomInfo, Apollo, Lusha, Kaspr, Cognism, RocketReach…): known opt-out pages, dated, in `references/courtiers.md`.
- 🖼️ **Photos and face**: image removal from Google, opt-out from face search engines, StopNCII for intimate images.
- 🤖 **Generative AI**: request to remove your data from ChatGPT answers, objection with Meta AI.
- 👪 **Special cases**: minors, deceased persons (account closure by heirs), mandate for a relative.
- 📅 **Follow-up**: a table with computed deadlines, reminders drafted in advance, a complaint template for the regulator, Google Alerts on your identifiers, and a 6–12-month check-up.

## What it does not do

- ❌ It deletes nothing itself and sends nothing on your behalf.
- ❌ It does not map **someone else's** footprint without an explicit mandate.
- ❌ It gives no legal advice: it provides templates and explains the process.
- ❌ It never suggests fake content, fake reviews or abusive takedown reports to "bury" a result.
- ❌ It never asks for an ID document, a password or a card number.

---

## Compatibility

The skill follows the **[Agent Skills](https://agentskills.io)** format (`SKILL.md` plus `references/` and `assets/` folders), an open standard read natively by many agents. For consumer assistants that do not support the format, its content works as is as instructions.

| Assistant | How to install | Web search | Tracking table |
|---|---|---|---|
| **Claude** (claude.ai, apps) | skill uploaded as a `.zip` | ✅ | file or spreadsheet |
| **Claude Code** | `~/.claude/skills/` folder | ✅ | CSV file |
| **Codex CLI**, **Gemini CLI**, **Hermes Agent** and other Agent Skills–compatible agents | the agent's skills folder | depends on the agent | CSV file |
| **ChatGPT** | custom GPT or Project: instructions + files | ✅ | file or table |
| **Gemini** | Gem: instructions + files | ✅ | table, Sheets export |
| **Mistral Le Chat**, **Copilot**, local models… | instructions pasted at the start of the chat | depends on the tool | table to copy |

Without web search the skill still works: it points you to the official source to check and marks every deadline "to be verified".

---

## Installation

### Agent Skills–compatible agents (Claude, Claude Code, Codex, Gemini CLI, Hermes…)

Copy the `nettoyage-empreinte-numerique/` folder into your agent's skills folder:

```bash
git clone https://github.com/pxnetwork-fr/zeroprint.git

# Example for Claude Code (skill available in all your projects)
cp -r zeroprint/nettoyage-empreinte-numerique ~/.claude/skills/
```

For other agents (Codex CLI, Gemini CLI, Hermes Agent…), the skills folder location is given in their documentation. On **claude.ai**, zip the folder (with `SKILL.md` at the top) and upload it in the skills settings.

### ChatGPT (custom GPT or Project)

1. Create a **custom GPT** (or a **Project**).
2. Paste the content of `SKILL.md` into the **instructions**, without the header block between `---`.
3. Add as **knowledge files**: `references/droit-applicable.md`, `references/modeles-courriers.md`, `references/courtiers.md` and `assets/suivi-demandes.csv`.
4. Turn on **web search**.

### Gemini (Gem)

1. Create a **Gem**.
2. Paste the content of `SKILL.md` into the **instructions**, without the header block.
3. Add the four files from `references/` and `assets/` as **knowledge files**.

### Any other assistant

Paste the content of `SKILL.md` at the very start of the conversation, then attach (or paste after it) `droit-applicable.md`, `modeles-courriers.md` and `courtiers.md`. Then make your request, for example: "I want my address removed from people-search sites."

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
- "Delete my late father's accounts"
- "Get a photo of my face out of a search engine"
- "I saw the '6 hours with Claude' thread, can we do that?"

### Sample first exchange

> **You:** I want to clean up my digital footprint, my address shows up on people-search sites.
>
> **Assistant:** To set things up: which country do you live in? Which identifiers should we cover (name and variants, usernames, emails, phone numbers, previous address)? And what's the main goal: less spam, a job search, safety, one specific piece of content?

Then you search your name, emails and phone numbers on two search engines, paste the links or screenshots, and the assistant builds the inventory.

---

## Step by step

```
 0. Scope           country, identifiers, goal → law verified, priorities, special cases
 1. Inventory       your results → table ranked by sensitivity
 2. Data brokers    official opt-out form, otherwise a letter
 3. Accounts        inbox + justdeleteme → permanent deletion
 4. Pages & engines site, delisting, photos, archives, generative AI
 5. Breaches        haveibeenpwned → password, 2FA, closure
 6. Follow-up       deadlines, reminders, complaint, alerts, 6–12-month check
```

### Step 0 — Scope
The assistant asks, in one go, for your country of residence, the identifiers to cover and your goal. The country sets the applicable law, which the skill **checks against the official source** before writing down any deadline. If you mention a danger (harassment, violence, threats), it starts with protective steps and handles your address and phone number first. The goal sets the order of the steps (spam → objection and B2B brokers; job search → old posts; safety → address, phone, face). Three special cases have their own legal basis: minors, deceased persons, a mandate for a relative.

### Step 1 — Inventory
You run the searches yourself and paste the results. The assistant sorts them:

| category | site | URL | exposed data | sensitivity | action | legal basis |
|---|---|---|---|---|---|---|
| data broker | example-directory.com | https://… | address, phone | high | opt-out form | GDPR |
| old account | old-forum.net | https://… | username, email | medium | account deletion | GDPR |

It gives you the queries to run (quoted name, variants, emails, phone number formats, reverse image search) and points to Google's "Results about you" tool where it is available in your country. The assistant does not search for you beyond what you provide.

### Step 2 — Data brokers
For each broker, the skill first looks for the official opt-out page, often faster than a letter. Failing that, it drafts a request for erasure **and** an end to resale, with the listing URLs and a request for acknowledgement. Each request also asks where the data came from (GDPR Art. 15), to cut the supply upstream. For a California resident, it points first to the CPPA's DROP portal: one request covers every data broker registered in the state. B2B brokers, the main source of professional cold outreach, have their opt-out pages listed in `references/courtiers.md`.

### Step 3 — Forgotten accounts
A search for welcome emails ("confirm your address", "welcome"…), justdeleteme.xyz, apps connected through Google / Apple / Facebook sign-in, and password manager entries. For each account: export first if useful, permanent deletion, announced purge delay.

### Step 4 — Third-party pages and search engines
- Content on a site: request to the site, with the exact URL and the reason.
- A result tied to your name: delisting request through the engine's forms.
- Removal obtained: ask the engine to refresh its copy, otherwise the result lingers for weeks.
- Photo or face: removal from the site then from Google, opt-out from face search engines, StopNCII.org for intimate images.
- Archives: exclusion request to archive.org, no guarantee.
- Generative AI: removal from ChatGPT answers through OpenAI's privacy portal, objection with Meta.
- If nothing can come down: the "publish better" approach (professional profile, personal page) is presented for what it is: slow, and nothing gets removed.

### Step 5 — Data breaches
You check your emails on haveibeenpwned.com. The assistant ranks by risk: password to change (especially if reused), 2FA to enable (an authenticator app rather than SMS), account to close.

### Step 6 — Follow-up and reminders
A tracking table built from `assets/suivi-demandes.csv`: a computed deadline for each request, a reminder drafted in advance, a complaint template for the EU, normalised statuses (sent, acknowledged, done, refused, reminded, complaint filed, back), a reminder to keep proof of every submission, Google Alerts on your name, emails and phone numbers to catch a listing that comes back, and an offer to redo the inventory every 6 to 12 months.

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
| 🇨🇭 Switzerland | FADP (Art. 25, 32) | 30 days (access); no deadline for erasure | FDPIC, civil action |
| 🇨🇦 Quebec | Law 25 (Art. 28, 28.1, 32) | 30 days | Commission d'accès à l'information |
| 🇨🇦 Canada outside Quebec | PIPEDA | 30 days (access) | Office of the Privacy Commissioner |
| 🇺🇸 California | CCPA / CPRA | 45 days | CPPA, DROP portal |
| 🌍 Elsewhere | local law / opt-out | varies | local authority |

Two situations outside the table are handled separately: **minors** (GDPR Art. 17(1)(f), fast-track referral to the CNIL in France) and **deceased persons** (French Data Protection Act Art. 85, heirs' rights).

⚠️ These deadlines are **benchmarks dated October 2026**. The skill re-checks them against the official source before putting them in a letter. Details and selection rules (in French): [`references/droit-applicable.md`](nettoyage-empreinte-numerique/references/droit-applicable.md).

---

## Repository layout

```
.
├── README.md                          ← documentation (French)
├── README.en.md                       ← this page (English)
├── LICENSE
└── nettoyage-empreinte-numerique/     ← the skill (folder to install)
    ├── SKILL.md                       ← instructions the assistant reads
    ├── references/
    │   ├── droit-applicable.md        ← legal frameworks, deadlines, exceptions
    │   ├── modeles-courriers.md       ← 11 templates (FR, EN, TR)
    │   └── courtiers.md               ← known opt-out pages (B2B, directories, face, archives, AI)
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
9. Objection to direct marketing (GDPR Art. 21), in French
10. Power of attorney to act on behalf of a third party, in French
11. Closure of a deceased person's accounts (France, Data Protection Act Art. 85), in French

They are templates to adapt, never to send as is.

---

## Safeguards

The skill applies these rules before doing anything:

- **Your own data only**, or that of someone who has given you a mandate (a minor child, an elderly parent, a client with power of attorney). Mapping a third party's footprint without a mandate is building a surveillance file.
- **No promise of erasure.** Caches, archives and leaked databases survive.
- **Never "they are required to".** The right to erasure has exceptions.
- **No legal advice.** For a dispute: a lawyer or the data protection authority.
- **Data minimisation.** Only name, emails, phone numbers and country. No ID document, password or bank card: letters state that proof of identity will be provided on request.
- **Protected ID document.** If a recipient demands one, you send it yourself, watermarked (filigrane.beta.gouv.fr in France) with the document number masked.
- **Law checked before it is written.** Deadlines, forms and laws change.

---

## Known limits

- **Listings come back.** Brokers re-collect public data or buy it again. Plan a new pass every 6 to 12 months.
- **Not everything can be erased.** Public registers, court decisions and legitimate press articles stay online.
- **Archives.** The Wayback Machine and caches keep copies; you can ask archive.org for an exclusion, with no guarantee.
- **Breaches are permanent.** Leaked data keeps circulating; you limit the damage, you do not get it back.
- **US data brokers** do not fall under the CCPA for a European resident: use their own opt-out process.

---

## Prevention

- An **email alias** for every sign-up (SimpleLogin, addy.io or your mail provider's aliases): if one leaks, delete it.
- A **browser or extension** that blocks trackers by default.
- **Social networks** set to private: profile not indexed, friends list hidden.
- In France, commercial **cold calling** without prior consent has been banned since 11 August 2026 (Bloctel is gone): tick nothing at sign-up, report unsolicited calls on SignalConso.
- A **secondary phone number** for sign-ups and classified ads.
- Your **landline unlisted** with your carrier (listed by default in the directory, to be requested again after every carrier change) and **WHOIS details** masked for a personal domain name.
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

**Fabien Elharrar** is an AI and automation consultant. He works with craftspeople and small businesses as well as large companies, helping them improve their processes and productivity with AI.

🌐 [fabien.elharrar.com](https://fabien.elharrar.com/) · 🐙 [@fabienelh](https://github.com/fabienelh)

Got an AI or automation project in your company? Visit [fabien.elharrar.com](https://fabien.elharrar.com/).

---

## License

Released under the [MIT](LICENSE) license: you are free to use, fork, modify and redistribute it, including commercially. The only condition is to keep Fabien Elharrar's copyright notice in your copies.

---

<sub>Made by [Fabien Elharrar](https://fabien.elharrar.com/) · A skill in the open Agent Skills format, for any AI assistant.</sub>
