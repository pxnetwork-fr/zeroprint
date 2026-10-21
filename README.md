# 🧹 zeroprint — nettoyer son empreinte numérique avec une IA

🇫🇷 **Français** · [🇬🇧 English](README.en.md)

<p align="center"><img src="https://pix-geeks.com/wp-content/uploads/2026/10/effacer-traces-numeriques-123846-1200x675.jpg.webp" alt="Effacer ses traces numériques avec une IA" width="100%"></p>

> Réduire les traces que vous laissez en ligne, méthodiquement : inventaire, demandes d'effacement prêtes à envoyer, déréférencement, fuites de données et suivi des relances.

Cette skill transforme votre assistant IA — **Claude, ChatGPT, Gemini, Hermes, Mistral, Codex…** — en assistant de nettoyage numérique. Elle part de ce que **vous** trouvez sur vous-même en ligne, classe chaque trace par sensibilité, rédige les demandes adaptées à votre pays (RGPD, UK GDPR, CCPA, KVKK) et vous laisse un tableau de suivi avec échéances, relances et modèle de plainte.

**L'IA trie, rédige et suit les démarches. Il n'efface rien lui-même.** C'est vous qui envoyez chaque demande, et c'est le destinataire qui y répond.

---

## Sommaire

- [Pourquoi cette skill](#pourquoi-cette-skill)
- [Ce qu'elle fait](#ce-quelle-fait)
- [Ce qu'elle ne fait pas](#ce-quelle-ne-fait-pas)
- [Compatibilité](#compatibilité)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Déroulé détaillé](#déroulé-détaillé)
- [Ce que vous obtenez](#ce-que-vous-obtenez)
- [Cadres juridiques couverts](#cadres-juridiques-couverts)
- [Contenu du dépôt](#contenu-du-dépôt)
- [Garde-fous](#garde-fous)
- [Limites à connaître](#limites-à-connaître)
- [Prévention](#prévention)
- [Contribuer](#contribuer)
- [Avertissement](#avertissement)
- [Auteur](#auteur)
- [Licence](#licence)

---

## Pourquoi cette skill

En mai 2026, un thread viral (« 6 heures avec Claude », repris en octobre 2026) a montré qu'on pouvait faire retirer une bonne partie de ses données personnelles d'Internet en se faisant aider par une IA. L'idée était bonne. La méthode avait des angles morts :

| Le thread viral | Cette skill |
|---|---|
| Promet un effacement | Annonce honnêtement ce qui partira et ce qui restera |
| Mélange les lois (CCPA invoquée par des Européens) | Choisit le droit selon le pays de résidence, et le vérifie à la source officielle |
| Écrit « ils sont obligés de supprimer » | Rappelle les exceptions légales (presse, obligations de conservation…) |
| S'arrête à l'envoi des courriers | Ajoute un tableau de suivi, des relances et un modèle de plainte |
| « 6 à 7 heures » | Une à deux heures de préparation, puis plusieurs semaines de suivi |
| N'aborde pas les fuites | Traite les fuites de données (mots de passe, 2FA, comptes à fermer) |

Le résultat dépend surtout du suivi : un courtier qui ne répond pas, une fiche qui revient trois mois plus tard. La skill est construite autour de cette réalité.

---

## Ce qu'elle fait

- 🔎 **Inventaire** de vos traces à partir des résultats que vous lui collez : courtiers en données, réseaux sociaux, vieux comptes, pages tierces, fuites.
- 🗂️ **Priorisation** par sensibilité : l'adresse, le téléphone et la date de naissance passent avant le pseudo.
- ✉️ **Demandes prêtes à envoyer**, une par destinataire, dans la bonne langue et sous le bon fondement juridique.
- 🔗 **Formulaires officiels d'abord** : la skill cherche la page d'opt-out du courtier avant de rédiger un courrier.
- 👻 **Comptes oubliés** : méthode pour les retrouver dans votre boîte mail et les supprimer pour de bon (pas une simple désactivation).
- 🔍 **Déréférencement** auprès des moteurs de recherche, distinct de la demande au site d'origine.
- 🔐 **Fuites de données** : ordre des actions (mot de passe, 2FA, fermeture de compte).
- 📅 **Suivi** : tableau avec échéances calculées, relances rédigées d'avance, modèle de plainte à l'autorité, rappel à 6–12 mois.

## Ce qu'elle ne fait pas

- ❌ Elle n'efface rien elle-même et n'envoie rien à votre place.
- ❌ Elle ne fait pas l'inventaire de **quelqu'un d'autre** sans mandat explicite.
- ❌ Elle ne donne pas d'avis juridique : elle fournit des modèles et explique les démarches.
- ❌ Elle ne propose jamais de faux contenus, de faux avis ni de signalements abusifs pour « enterrer » un résultat.
- ❌ Elle ne vous demande jamais de pièce d'identité, de mot de passe ni de numéro de carte.

---

## Compatibilité

La skill suit le format **[Agent Skills](https://agentskills.io)** (`SKILL.md` + dossiers `references/` et `assets/`), un standard ouvert lu nativement par de nombreux agents. Pour les assistants grand public qui ne gèrent pas ce format, son contenu s'utilise tel quel comme instructions.

| Assistant | Mode d'installation | Recherche web | Tableau de suivi |
|---|---|---|---|
| **Claude** (claude.ai, apps) | skill importée en `.zip` | ✅ | fichier ou tableur |
| **Claude Code** | dossier `~/.claude/skills/` | ✅ | fichier CSV |
| **Codex CLI**, **Gemini CLI**, **Hermes Agent** et autres agents compatibles Agent Skills | dossier de skills de l'agent | selon l'agent | fichier CSV |
| **ChatGPT** | GPT personnalisé ou Projet : instructions + fichiers | ✅ | fichier ou tableau |
| **Gemini** | Gem : instructions + fichiers | ✅ | tableau, export Sheets |
| **Mistral Le Chat**, **Copilot**, modèles locaux… | instructions collées en début de conversation | selon l'outil | tableau à copier |

Sans recherche web, la skill ne bloque pas : elle vous indique la source officielle à consulter et marque chaque délai « à vérifier ».

---

## Installation

### Agents compatibles Agent Skills (Claude, Claude Code, Codex, Gemini CLI, Hermes…)

Copiez le dossier `nettoyage-empreinte-numerique/` dans le dossier de skills de votre agent :

```bash
git clone https://github.com/pxnetwork-fr/zeroprint.git

# Exemple pour Claude Code (skill disponible dans tous vos projets)
cp -r zeroprint/nettoyage-empreinte-numerique ~/.claude/skills/
```

Pour les autres agents (Codex CLI, Gemini CLI, Hermes Agent…), l'emplacement du dossier de skills est indiqué dans leur documentation. Sur **claude.ai**, compressez le dossier en `.zip` (avec `SKILL.md` à la racine) et importez-le dans les réglages des skills.

### ChatGPT (GPT personnalisé ou Projet)

1. Créez un **GPT personnalisé** (ou un **Projet**).
2. Collez le contenu de `SKILL.md` dans les **instructions**, sans le bloc d'en-tête entre `---`.
3. Ajoutez en **fichiers de connaissances** : `references/droit-applicable.md`, `references/modeles-courriers.md` et `assets/suivi-demandes.csv`.
4. Activez la **recherche web**.

### Gemini (Gem)

1. Créez un **Gem**.
2. Collez le contenu de `SKILL.md` dans les **instructions**, sans le bloc d'en-tête.
3. Ajoutez les trois fichiers de `references/` et `assets/` comme **fichiers de connaissances**.

### Tout autre assistant

Collez le contenu de `SKILL.md` en tout début de conversation, puis joignez (ou collez à la suite) `droit-applicable.md` et `modeles-courriers.md`. Commencez ensuite par votre demande, par exemple : « Je veux retirer mon adresse des sites d'annuaires. »

---

## Utilisation

La skill se déclenche toute seule sur des demandes comme :

- « Je veux supprimer mes données d'Internet »
- « Retire mon adresse et mon téléphone des sites d'annuaires »
- « Fais-moi retirer des data brokers »
- « Aide-moi à supprimer mes vieux comptes »
- « Rédige une demande RGPD d'effacement »
- « Je veux déréférencer un article qui parle de moi »
- « Est-ce que mon e-mail a fuité ? »
- « J'ai vu le thread "6 heures avec Claude", on le fait ? »

### Exemple de premier échange

> **Vous :** Je veux nettoyer mon empreinte numérique, il y a mon adresse sur des sites d'annuaires.
>
> **L'assistant :** Pour cadrer : dans quel pays résidez-vous ? Quels identifiants couvrir (nom et variantes, pseudos, e-mails, téléphones, ancienne adresse) ? Et quel est l'objectif principal : moins de spam, recherche d'emploi, sécurité, un contenu précis ?

Ensuite, vous cherchez votre nom, vos e-mails et vos numéros sur deux moteurs, vous collez les liens ou les captures, et l'assistant construit l'inventaire.

---

## Déroulé détaillé

```
 0. Cadrer          pays, identifiants, objectif → droit applicable vérifié
 1. Inventaire      vos résultats → tableau trié par sensibilité
 2. Courtiers       formulaire d'opt-out officiel, sinon courrier
 3. Comptes         boîte mail + justdeleteme → suppression définitive
 4. Pages & moteurs demande au site / déréférencement au moteur
 5. Fuites          haveibeenpwned → mot de passe, 2FA, fermeture
 6. Suivi           échéances, relances, plainte, rappel 6–12 mois
```

### Étape 0 — Cadrer
L'assistant demande en une fois votre pays de résidence, les identifiants à couvrir et votre objectif. Le pays fixe le droit applicable, que la skill **vérifie par une recherche sur la source officielle** avant d'écrire le moindre délai. Si vous évoquez un danger (harcèlement, violences, menaces), elle commence par les démarches de protection et traite en priorité l'adresse et le téléphone.

### Étape 1 — Inventaire
Vous faites les recherches vous-même et collez les résultats. L'assistant les classe :

| catégorie | site | URL | donnée exposée | sensibilité | action | cadre juridique |
|---|---|---|---|---|---|---|
| courtier en données | exemple-annuaire.com | https://… | adresse, téléphone | haute | formulaire d'opt-out | RGPD |
| ancien compte | vieux-forum.net | https://… | pseudo, e-mail | moyenne | suppression de compte | RGPD |

L'assistant ne lance pas de recherche sur vous au-delà de ce que vous fournissez.

### Étape 2 — Courtiers en données
Pour chaque courtier, la skill cherche d'abord la page d'opt-out officielle, souvent plus rapide qu'un courrier. À défaut, elle rédige une demande d'effacement **et** d'arrêt de la revente, avec les URL des fiches et la demande d'accusé de réception. Pour un résident de Californie, elle oriente d'abord vers le guichet DROP de la CPPA : une seule demande pour tous les courtiers enregistrés dans l'État.

### Étape 3 — Comptes oubliés
Recherche des e-mails de bienvenue (« confirmez votre adresse », « welcome »…) et consultation de justdeleteme.xyz. Pour chaque compte : export préalable si utile, suppression définitive, délai de purge annoncé.

### Étape 4 — Pages tierces et moteurs
- Contenu sur un site : demande au site, avec l'URL exacte et le motif.
- Résultat associé à votre nom : demande de déréférencement via les formulaires du moteur.
- Si rien ne peut partir : la stratégie « publier mieux » (profil pro, page perso) est présentée pour ce qu'elle est, lente et sans retrait.

### Étape 5 — Fuites de données
Vous vérifiez vos e-mails sur haveibeenpwned.com. L'assistant classe par risque : mot de passe à changer (surtout s'il est réutilisé), 2FA à activer (application plutôt que SMS), compte à fermer.

### Étape 6 — Suivi et relances
Tableau de suivi généré à partir de `assets/suivi-demandes.csv` : échéance calculée pour chaque envoi, relance rédigée d'avance, modèle de plainte pour l'UE, rappel de conserver chaque preuve, proposition de refaire l'inventaire tous les 6 à 12 mois.

---

## Ce que vous obtenez

1. **Un inventaire priorisé** de vos traces.
2. **Des demandes prêtes à envoyer**, une par destinataire, avec le formulaire ou l'adresse où les envoyer.
3. **Un tableau de suivi** avec échéances, relances et, le cas échéant, le modèle de plainte.
4. **Une ligne honnête sur le résultat attendu** : ce qui peut partir, ce qui restera, quand refaire le point.

---

## Cadres juridiques couverts

| Résidence | Texte | Délai de réponse (repère) | Recours |
|---|---|---|---|
| 🇫🇷 France | RGPD (art. 17, 21, 12) | 1 mois, +2 mois si complexe | CNIL |
| 🇪🇺 UE / EEE | RGPD | idem | autorité nationale |
| 🇬🇧 Royaume-Uni | UK GDPR | 1 mois | ICO |
| 🇹🇷 Turquie | KVKK (loi 6698) | 30 jours | Conseil KVKK |
| 🇺🇸 Californie | CCPA / CPRA | 45 jours | CPPA, guichet DROP |
| 🌍 Ailleurs | loi locale / opt-out | variable | autorité locale |

⚠️ Ces délais sont des **repères datés d'octobre 2026**. La skill les revérifie à la source officielle avant de les écrire dans un courrier. Détail et règles de choix : [`references/droit-applicable.md`](nettoyage-empreinte-numerique/references/droit-applicable.md).

---

## Contenu du dépôt

```
.
├── README.md                          ← cette page (français)
├── README.en.md                       ← documentation (anglais)
├── LICENSE
└── nettoyage-empreinte-numerique/     ← la skill (dossier à installer)
    ├── SKILL.md                       ← instructions lues par l'assistant
    ├── references/
    │   ├── droit-applicable.md        ← cadres juridiques, délais, exceptions
    │   └── modeles-courriers.md       ← 8 modèles (FR, EN, TR)
    └── assets/
        └── suivi-demandes.csv         ← gabarit du tableau de suivi
```

### Les modèles de courriers inclus

1. Demande d'effacement — RGPD (France / UE)
2. Demande d'effacement — UK GDPR
3. Demande de suppression — CCPA (Californie)
4. Demande d'effacement — KVKK (en turc)
5. Suppression d'un compte sans procédure en ligne
6. Relance après échéance
7. Plainte à l'autorité (CNIL) : pièces à réunir
8. Déréférencement auprès d'un moteur de recherche

Ce sont des gabarits à adapter, jamais à envoyer tels quels.

---

## Garde-fous

La skill applique ces règles avant toute action :

- **Vos données uniquement**, ou celles d'une personne qui vous a mandaté (enfant mineur, parent âgé, client avec procuration). Inventorier l'empreinte d'un tiers sans mandat, c'est constituer un dossier de surveillance.
- **Aucune promesse d'effacement.** Caches, archives et bases piratées survivent.
- **Jamais « ils sont obligés ».** Le droit à l'effacement a des exceptions.
- **Pas d'avis juridique.** Pour un litige : un avocat ou l'autorité de protection des données.
- **Minimisation.** Seulement nom, e-mails, téléphones et pays. Pas de pièce d'identité, de mot de passe ni de carte bancaire : les courriers indiquent qu'un justificatif sera fourni sur demande.
- **Droit vérifié avant d'être écrit.** Délais, formulaires et lois changent.

---

## Limites à connaître

- **Les fiches reviennent.** Les courtiers re-collectent les données publiques ou en rachètent. Comptez une nouvelle passe tous les 6 à 12 mois.
- **Tout ne s'efface pas.** Registres publics, décisions de justice et articles de presse légitimes restent en ligne.
- **Les archives.** La Wayback Machine et les caches conservent des copies.
- **Les fuites sont définitives.** Une donnée piratée circule ; on limite les dégâts, on ne la récupère pas.
- **Les courtiers américains** ne relèvent pas de la CCPA pour un résident européen : on passe par leur propre procédure d'opt-out.

---

## Prévention

- Un **alias e-mail** par inscription (SimpleLogin, addy.io ou les alias de votre messagerie) : si l'un fuit, on le supprime.
- Un **navigateur ou une extension** qui bloque les traqueurs par défaut.
- Des **réseaux sociaux** réglés en privé : profil non indexé, liste d'amis masquée.
- Un **numéro secondaire** pour les inscriptions et les petites annonces.
- Un **gestionnaire de mots de passe** et la 2FA partout où c'est possible.

---

## Contribuer

Les contributions sont bienvenues, en particulier :

- 🌍 **nouveaux cadres juridiques** (Suisse/nLPD, Québec/Loi 25, Brésil/LGPD…) dans `references/droit-applicable.md` ;
- ✉️ **modèles de courriers** dans d'autres langues ;
- 🔄 **mises à jour** quand un délai, un guichet ou un formulaire change, avec le lien vers la source officielle.

Ouvrez une *issue* ou une *pull request*. Merci de citer la source officielle pour toute information juridique.

---

## Avertissement

Cette skill fournit des informations générales et des modèles de courriers. **Elle ne constitue pas un conseil juridique.** Les lois, délais et procédures évoluent : vérifiez-les auprès des sources officielles (CNIL, ICO, CPPA, KVKK…) avant toute démarche. Pour un litige, adressez-vous à un avocat ou à l'autorité de protection des données de votre pays.

---

## Auteur

**Fabien Elharrar** est consultant en IA et en automatisation. Il accompagne aussi bien des artisans et des PME que de grandes entreprises pour améliorer leurs process et leur productivité grâce à l'IA.

🌐 [fabien.elharrar.com](https://fabien.elharrar.com/) · 🐙 [@fabienelh](https://github.com/fabienelh)

Un projet d'automatisation ou d'IA dans votre entreprise ? Rendez-vous sur [fabien.elharrar.com](https://fabien.elharrar.com/).

---

## Licence

Distribuée sous licence [MIT](LICENSE) : vous pouvez l'utiliser, la *forker*, la modifier et la redistribuer librement, y compris à des fins commerciales. Seule condition : conserver la mention de copyright de Fabien Elharrar dans vos copies.

---

<sub>Créée par [Fabien Elharrar](https://fabien.elharrar.com/) · Une skill au format ouvert Agent Skills, pour tout assistant IA.</sub>
