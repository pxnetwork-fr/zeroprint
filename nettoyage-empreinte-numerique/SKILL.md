---
name: nettoyage-empreinte-numerique
description: Accompagne une personne qui veut réduire sa propre empreinte numérique — inventaire de ce qui est visible, courriers d'effacement (RGPD, UK GDPR, CCPA, KVKK), suppression de vieux comptes, déréférencement, fuites de données, puis suivi des relances. Déclenche cette skill dès qu'il s'agit de « supprimer mes données d'Internet », « effacer mon empreinte numérique », « retirer mon adresse / mon téléphone de sites », « me faire retirer des data brokers », « supprimer mes vieux comptes », « faire une demande RGPD d'effacement », « déréférencer un article sur moi », « vérifier si mon e-mail a fuité », ou quand quelqu'un cite le thread viral « 6 heures avec Claude ». Ne s'applique qu'aux données de la personne elle-même ou d'une personne qui l'a mandatée.
---

# Nettoyage d'empreinte numérique

Aide une personne à réduire les traces qu'elle laisse en ligne : fiches chez des courtiers en données, vieux comptes, pages qui la citent, résultats de recherche, fuites. La méthode s'inspire du thread viral « 6 heures avec Claude » (@vibeeval, mai 2026, repris en octobre 2026), mais elle en corrige les angles morts.

**L'assistant trie, rédige et suit les démarches. Il n'efface rien lui-même.** C'est la personne qui envoie chaque demande, et c'est le destinataire qui y répond. Le thread le dit d'ailleurs lui-même : « Copiez, envoyez ».

Ces instructions valent pour tout assistant IA (Claude, ChatGPT, Gemini, Hermes, Mistral, Codex…). Quand un outil cité ici manque (recherche web, création de fichiers, rappels), suivre la solution de repli indiquée et le dire à la personne.

## Garde-fous (à appliquer avant tout)

- **Uniquement ses propres données**, ou celles d'une personne qui a donné un mandat explicite (enfant mineur, parent âgé, client avec procuration). Refuser l'inventaire de l'empreinte d'un tiers sans mandat : c'est un dossier de surveillance, pas un nettoyage.
- **Ne jamais promettre l'effacement.** Les copies survivent dans les caches, les archives (Wayback Machine) et les bases piratées. Les courtiers re-collectent les données publiques ou en rachètent, et les fiches reviennent en quelques semaines ou mois. Les registres publics, les décisions de justice et la presse légitime ne s'effacent pas sur simple demande.
- **Ne pas écrire qu'une entreprise est « obligée » d'effacer.** Le droit à l'effacement a des exceptions (liberté d'expression et d'information, obligation légale de conservation, archivage, défense de droits en justice). Écrire « vous pouvez demander », jamais « ils doivent ».
- **Pas d'avis juridique.** L'assistant rédige des courriers types et explique les démarches ; pour un litige, renvoyer vers un avocat ou l'autorité de protection des données.
- **Minimiser les données collectées dans la conversation.** Demander seulement ce qui sert à rédiger : nom, e-mails et téléphones concernés, pays de résidence. Jamais de numéro de pièce d'identité, de carte bancaire ou de mot de passe : le courrier indique qu'une preuve d'identité sera fournie sur demande, sans la recopier.
- **Vérifier le droit en vigueur avant de l'écrire.** Délais, guichets, formulaires et lois changent : une recherche web sur la source officielle (CNIL, ICO, agence californienne, KVKK) avant de citer un délai ou une procédure. Les délais de `references/droit-applicable.md` sont des repères à confirmer, pas des certitudes. **Sans accès au web**, donner à la personne l'adresse de la source officielle à consulter et marquer chaque délai « à vérifier » dans les courriers et le tableau de suivi.

## Étape 0 — Cadrer

Demander en une seule fois :
- le **pays de résidence** (il fixe le droit applicable) ;
- les **identifiants à couvrir** : nom et variantes, pseudos, e-mails, téléphones, ancienne adresse si elle circule ;
- l'**objectif** : moins de spam, recherche d'emploi, sécurité après un harcèlement, un contenu gênant précis.

Choisir le cadre juridique avec `references/droit-applicable.md`, le vérifier par une recherche (ou le signaler « à vérifier » sans accès au web), puis annoncer le plan en une ligne. Si la personne évoque un danger (harcèlement, violences, menaces), donner d'abord les démarches de protection et les contacts d'aide de son pays, puis traiter en priorité l'adresse et le téléphone.

## Étape 1 — Inventaire

La personne cherche elle-même son nom, ses e-mails et ses téléphones sur Google (et sur un second moteur), puis colle les résultats : liens ou captures. L'assistant les classe dans un tableau :

`catégorie | site | URL | donnée exposée | sensibilité | action | cadre juridique`

- **catégorie** : courtier en données / réseau social / ancien compte / page tierce (article, annuaire, forum) / fuite
- **sensibilité** : haute (adresse, téléphone, date de naissance, photo du domicile), moyenne (e-mail, employeur), faible (pseudo)
- **action** : formulaire d'opt-out / courrier d'effacement / suppression de compte / demande au site / déréférencement / sécurisation

Trier par priorité : d'abord la sensibilité haute, ensuite ce qui est facile à retirer. Ne pas lancer soi-même de recherche sur la personne au-delà de ce qu'elle a fourni.

## Étape 2 — Courtiers en données

Pour chaque courtier, chercher d'abord sa **page d'opt-out officielle** (recherche web sur le domaine du courtier ; sans accès au web, demander à la personne de la trouver ou de coller la page). Un formulaire est souvent plus rapide qu'un courrier : donner le lien et la marche à suivre. Sinon, rédiger la demande avec le modèle adapté de `references/modeles-courriers.md`, en indiquant les URL des fiches, les données visées, la demande d'effacement **et** d'arrêt de la revente, le délai, la demande d'accusé de réception.

Les courtiers américains (Spokeo, BeenVerified, Whitepages, MyLife…) ne relèvent pas de la CCPA pour un résident européen : utiliser leur propre procédure d'opt-out, et le RGPD seulement s'ils visent le marché européen.

Pour un **résident de Californie**, commencer par le guichet DROP de la CPPA (cppa.ca.gov) : une seule demande, après vérification d'identité, vise tous les courtiers enregistrés dans l'État, qui doivent la consulter régulièrement et la traiter dans le délai fixé par la CPPA (repère : 90 jours, à vérifier). Les courtiers non enregistrés et les sites hors Californie restent à traiter un par un.

## Étape 3 — Comptes oubliés

Lister les services dont la personne se souvient, puis compléter avec :
- une recherche dans sa boîte mail des messages de bienvenue (« bienvenue », « confirmez votre adresse », « welcome », « verify your email ») ;
- justdeleteme.xyz, qui indique la difficulté de suppression et le lien direct par service.

Pour chaque compte : export préalable des données si utile, procédure de **suppression définitive** (pas de simple désactivation), délai de purge annoncé par le service. Si aucune procédure n'existe, courrier d'effacement.

## Étape 4 — Pages tierces et moteurs de recherche

- **Contenu sur un site tiers** : demande au site lui-même (responsable du traitement), avec l'URL exacte et le motif.
- **Lien associé au nom dans un moteur** : demande de **déréférencement** directement au moteur, via ses formulaires (Google propose un formulaire de suppression d'informations personnelles et un formulaire RGPD de déréférencement ; vérifier leur emplacement actuel par recherche).
- **Si rien ne peut être retiré**, la stratégie « publier mieux » (profil professionnel, page personnelle, contenus propres bien référencés) reste possible, mais l'annoncer pour ce qu'elle est : le contenu reste en ligne, il recule seulement dans les résultats, et cela prend des mois. Ne jamais proposer de faux contenus, de faux avis, de signalements abusifs ni de pression sur un journaliste.

## Étape 5 — Fuites de données

La personne vérifie ses e-mails sur haveibeenpwned.com et colle la liste des fuites. L'assistant classe par risque actuel :
1. **mot de passe à changer** d'abord, surtout s'il a été réutilisé ailleurs ;
2. **authentification à deux facteurs** à activer (application d'authentification de préférence au SMS) ;
3. **compte à supprimer** s'il ne sert plus.

Recommander un gestionnaire de mots de passe. Ne jamais demander de mot de passe dans la conversation.

## Étape 6 — Suivi et relances

C'est l'étape que le thread viral oublie, et celle qui fait le résultat. Produire un **tableau de suivi** à partir de `assets/suivi-demandes.csv` (en fichier tableur — CSV ou Excel — si l'outil sait en produire, sinon en tableau dans la réponse, à copier dans un tableur) :

`destinataire | type de demande | canal | date d'envoi | échéance | réponse | relance envoyée le | statut | preuve`

- calculer chaque échéance à partir de la date d'envoi et du délai vérifié à l'étape 0 ;
- rédiger d'avance la **relance** et, pour l'UE, le **modèle de plainte** à l'autorité (`references/modeles-courriers.md`) ;
- rappeler de garder une preuve de chaque envoi (capture, accusé de réception, copie du courriel) ;
- proposer de refaire l'inventaire **tous les 6 à 12 mois**, parce que les fiches reviennent. Si la personne le souhaite et que l'outil sait créer des rappels ou des tâches planifiées, créer le rappel ; sinon, donner les dates à noter dans son agenda.

## Prévention

- Alias e-mail jetables pour chaque inscription (SimpleLogin, addy.io, ou les alias de son fournisseur de messagerie) : si un alias fuit, on le supprime.
- Navigateur ou extension qui bloque les traqueurs par défaut.
- Réglages de confidentialité des réseaux sociaux (profil non indexé, liste d'amis masquée).
- Numéro de téléphone secondaire pour les inscriptions et les annonces.

## Livrable

1. **Le tableau d'inventaire** priorisé.
2. **Les demandes prêtes à envoyer**, une par destinataire, avec le formulaire ou l'adresse où les envoyer.
3. **Le tableau de suivi** avec les échéances, la relance et, le cas échéant, le modèle de plainte.
4. **Une ligne honnête sur le résultat attendu** : ce qui peut être retiré, ce qui ne le sera pas, quand refaire le point.

Le thread viral parlait de « 6 à 7 heures » ; annoncer plutôt une ou deux heures de préparation, puis plusieurs semaines de suivi.

## Erreurs à éviter

- Laisser croire que l'assistant « supprime » ou « efface » quoi que ce soit.
- Recopier une pièce d'identité, un mot de passe ou un numéro de carte dans la conversation.
- Invoquer la CCPA pour un résident européen face à une entreprise européenne.
- Citer un délai, un formulaire ou une loi de mémoire sans l'avoir vérifié.
- Écrire « ils sont obligés de supprimer » ou promettre un résultat définitif.
- Faire l'inventaire de l'empreinte de quelqu'un d'autre sans mandat.
- Recommander l'enfouissement par faux contenus ou faux avis.
