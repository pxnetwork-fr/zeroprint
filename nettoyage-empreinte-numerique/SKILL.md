---
name: nettoyage-empreinte-numerique
description: À utiliser dès qu'une personne veut réduire sa propre empreinte numérique ou cite le thread viral « 6 heures avec Claude » — « supprimer mes données d'Internet », « effacer mon empreinte numérique », « retirer mon adresse / mon téléphone de sites », « me faire retirer des data brokers », « supprimer mes vieux comptes », « faire une demande RGPD d'effacement », « déréférencer un article sur moi », « vérifier si mon e-mail a fuité », « arrêter le spam et le démarchage », « supprimer les comptes d'un proche décédé », « retirer une photo de mon visage », « mes données dans ChatGPT ou Meta AI ». Ne s'applique qu'aux données de la personne elle-même ou d'une personne qui l'a mandatée.
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
- **Justificatif d'identité : envoyé par la personne, jamais nu.** Quand un destinataire exige une copie de pièce d'identité, elle l'envoie elle-même, avec un filigrane qui indique le destinataire et la date (en France, le service de l'État filigrane.beta.gouv.fr), le numéro du document masqué et le recto seul si cela suffit. Si un courtier exige une pièce pour un simple opt-out, chercher d'abord sa voie sans pièce (vérification par e-mail) et le noter dans le suivi.
- **Vérifier le droit en vigueur avant de l'écrire.** Délais, guichets, formulaires et lois changent : une recherche web sur la source officielle (CNIL, ICO, agence californienne, KVKK) avant de citer un délai ou une procédure. Les délais de `references/droit-applicable.md` sont des repères à confirmer, pas des certitudes. **Sans accès au web**, donner à la personne l'adresse de la source officielle à consulter et marquer chaque délai « à vérifier » dans les courriers et le tableau de suivi.

## Étape 0 — Cadrer

Demander en une seule fois :
- le **pays de résidence** (il fixe le droit applicable) ;
- les **identifiants à couvrir** : nom et variantes, pseudos, e-mails, téléphones, ancienne adresse si elle circule ;
- l'**objectif** : moins de spam, recherche d'emploi, sécurité après un harcèlement, un contenu gênant précis.

Choisir le cadre juridique avec `references/droit-applicable.md`, le vérifier par une recherche (ou le signaler « à vérifier » sans accès au web), puis annoncer le plan en une ligne. Si la personne évoque un danger (harcèlement, violences, menaces), donner d'abord les démarches de protection et les contacts d'aide de son pays, puis traiter en priorité l'adresse et le téléphone.

L'**objectif** fixe l'ordre des étapes :

| Objectif | Commencer par | Ensuite |
|---|---|---|
| moins de spam et de démarchage | opposition à la prospection (modèle 9), courtiers B2B (`references/courtiers.md`), alias e-mail | fuites (étape 5), comptes oubliés (étape 3) |
| recherche d'emploi, image professionnelle | anciennes publications et photos (étape 3), résultats liés au nom (étape 4) | courtiers (étape 2) |
| sécurité après harcèlement ou violences | adresse et téléphone : courtiers, annuaires et liste rouge, moteurs de visage (`references/courtiers.md`) | comptes et réseaux en privé, fuites |
| un contenu précis | demande au site, déréférencement, archives (étape 4) | le reste seulement si la personne le souhaite |

Trois **cas particuliers** changent le fondement et les justificatifs :

- **Mineur** (ou données publiées pendant la minorité) : c'est le motif d'effacement le plus fort (RGPD, art. 17, § 1, f) ; le dire dans chaque courrier. En France, la loi Informatique et Libertés (art. 51) renvoie au RGPD et prévoit une saisine rapide de la CNIL si le site ne répond pas dans le mois (à vérifier sur cnil.fr). Les parents exercent les droits d'un mineur ; un adulte peut invoquer sa minorité au moment de la collecte.
- **Personne décédée** : le RGPD ne s'applique plus. En France, la loi Informatique et Libertés (art. 85) permet aux héritiers de demander la clôture des comptes et la prise en compte du décès, avec acte de décès et preuve de la qualité d'héritier ; la personne a pu laisser des directives post-mortem. Passer d'abord par les procédures dédiées des grands services (Google : formulaire pour le compte d'un proche décédé ; Meta : commémoration ou suppression ; Apple : contact légataire), sinon modèle 11. Hors France, vérifier la loi locale : beaucoup n'en prévoient rien.
- **Mandat** (parent âgé, client) : joindre une procuration écrite (modèle 10) et une pièce du mandataire ; le destinataire la demandera. Sans mandat écrit, s'en tenir aux conseils, sans courrier au nom du tiers.

## Étape 1 — Inventaire

La personne cherche elle-même sur Google et sur un second moteur (Bing, DuckDuckGo), puis colle les résultats : liens ou captures. Lui donner les **requêtes à lancer** : le nom entre guillemets, seul puis avec la ville et l'employeur ; chaque variante (prénom abrégé, nom de naissance, pseudo) ; chaque e-mail entre guillemets ; chaque téléphone sous ses formats courants (06 12 34 56 78, 0612345678, +33612345678) ; une recherche d'image inversée sur sa photo de profil (Google Images, puis, si elle l'accepte, un moteur de reconnaissance faciale comme PimEyes, qui montre où son visage circule). Si Google propose dans son pays l'outil « Résultats vous concernant », le signaler : il repère les pages qui affichent ses coordonnées, permet d'en demander le retrait des résultats et avertit quand une nouvelle page apparaît. L'assistant classe le tout dans un tableau :

`catégorie | site | URL | donnée exposée | sensibilité | action | cadre juridique`

- **catégorie** : courtier en données (grand public ou B2B) / réseau social / ancien compte / page tierce (article, annuaire, forum) / photo ou visage / fuite
- **sensibilité** : haute (adresse, téléphone, date de naissance, photo du domicile), moyenne (e-mail, employeur), faible (pseudo)
- **action** : formulaire d'opt-out / courrier d'effacement / suppression de compte / demande au site / déréférencement / retrait d'image / sécurisation

Trier par priorité : d'abord la sensibilité haute, ensuite ce qui est facile à retirer. Ne pas lancer soi-même de recherche sur la personne au-delà de ce qu'elle a fourni.

## Étape 2 — Courtiers en données

Pour chaque courtier, chercher d'abord sa **page d'opt-out officielle** (recherche web sur le domaine du courtier ; sans accès au web, demander à la personne de la trouver ou de coller la page). Un formulaire est souvent plus rapide qu'un courrier : donner le lien et la marche à suivre. Sinon, rédiger la demande avec le modèle adapté de `references/modeles-courriers.md`, en indiquant les URL des fiches, les données visées, la demande d'effacement **et** d'arrêt de la revente, le délai, la demande d'accusé de réception.

Joindre à chaque demande d'effacement une **demande de la source des données** (RGPD, art. 15, § 1, g) : savoir d'où le courtier tient l'adresse ou le téléphone (annuaire, registre, autre courtier, fuite) permet de remonter à la source et d'éviter que la fiche revienne. Le modèle 1 contient ce paragraphe ; ajouter la source trouvée à l'inventaire.

Les **courtiers B2B** (ZoomInfo, Apollo, Lusha, Kaspr, Cognism, RocketReach…) alimentent l'essentiel du démarchage professionnel ; chacun a une page d'opt-out avec vérification par e-mail, sans pièce d'identité. Demander l'opposition à toute nouvelle collecte en plus de l'effacement, sinon la fiche revient à la prochaine extraction. `references/courtiers.md` liste les pages d'opt-out connues (courtiers B2B, annuaires, moteurs de visage, archives, IA génératives), datées et à vérifier : s'en servir avant de chercher.

Les courtiers américains (Spokeo, BeenVerified, Whitepages, MyLife…) ne relèvent pas de la CCPA pour un résident européen : utiliser leur propre procédure d'opt-out, et le RGPD seulement s'ils visent le marché européen.

Pour un **résident de Californie**, commencer par le guichet DROP de la CPPA (cppa.ca.gov) : une seule demande, après vérification d'identité, vise tous les courtiers enregistrés dans l'État, qui doivent la consulter régulièrement et la traiter dans le délai fixé par la CPPA (repère : 90 jours, à vérifier). Les courtiers non enregistrés et les sites hors Californie restent à traiter un par un.

## Étape 3 — Comptes oubliés

Lister les services dont la personne se souvient, puis compléter avec :
- une recherche dans sa boîte mail des messages de bienvenue (« bienvenue », « confirmez votre adresse », « welcome », « verify your email ») ;
- justdeleteme.xyz, qui indique la difficulté de suppression et le lien direct par service ;
- la liste des applications connectées via « Se connecter avec Google / Apple / Facebook », dans les réglages de sécurité de ces comptes ;
- les entrées du gestionnaire de mots de passe et les mots de passe enregistrés dans le navigateur.

Pour chaque compte : export préalable des données si utile, procédure de **suppression définitive** (pas de simple désactivation), délai de purge annoncé par le service. Si aucune procédure n'existe, courrier d'effacement.

Pour les réseaux sociaux encore utilisés : retirer les identifications non souhaitées, supprimer ou archiver les anciennes publications publiques avec l'outil de gestion de l'activité du réseau, désactiver l'indexation du profil par les moteurs. Pour les comptes Google, Apple et Meta encore utilisés, régler la suppression automatique de l'historique d'activité et des positions.

## Étape 4 — Pages tierces et moteurs de recherche

- **Contenu sur un site tiers** : demande au site lui-même (responsable du traitement), avec l'URL exacte et le motif.
- **Lien associé au nom dans un moteur** : demande de **déréférencement** directement au moteur, via ses formulaires (Google propose un formulaire de suppression d'informations personnelles et un formulaire RGPD de déréférencement ; vérifier leur emplacement actuel par recherche).
- **Après un retrait obtenu**, le résultat peut rester affiché des semaines : demander au moteur de rafraîchir sa copie (Google : outil « Supprimer un contenu obsolète », à retrouver par recherche) et noter la vérification dans le tableau de suivi.
- **Photo ou visage** : demander le retrait au site qui héberge l'image, puis à Google (formulaire de suppression d'informations personnelles, ou « Supprimer le résultat » depuis Google Images). Pour un moteur de reconnaissance faciale, l'opt-out du moteur (PimEyes : formulaire d'opt-out, qui demande une photo et une pièce d'identité masquée ; il ne retire que ses propres résultats, pas les pages sources). Pour une image intime diffusée sans consentement : StopNCII.org (empreinte calculée sur l'appareil de la personne, qui fait la démarche elle-même, adultes seulement) et le formulaire Google dédié ; c'est une infraction, mentionner la plainte.
- **Archives** : la Wayback Machine ne retire rien seule. Demander l'exclusion à info@archive.org avec les URL exactes et la période ; aucune garantie ni délai annoncés. archive.today a son propre formulaire de signalement (à vérifier).
- **IA génératives** : si ChatGPT ou Meta AI restituent des données sur la personne, OpenAI accepte une demande de retrait des réponses via son portail de confidentialité (privacy.openai.com, « Make a Privacy Request », motivée : inexact, excessif, obsolète) ; Meta propose dans son Centre de confidentialité un formulaire d'opposition (UE et Royaume-Uni) et un formulaire pour les informations de tiers, sans retrait automatique. Le retrait porte sur les réponses à venir, pas sur l'entraînement passé.
- **Si rien ne peut être retiré**, la stratégie « publier mieux » (profil professionnel, page personnelle, contenus propres bien référencés) reste possible, mais l'annoncer pour ce qu'elle est : le contenu reste en ligne, il recule seulement dans les résultats, et cela prend des mois. Ne jamais proposer de faux contenus, de faux avis, de signalements abusifs ni de pression sur un journaliste.

## Étape 5 — Fuites de données

La personne vérifie ses e-mails sur haveibeenpwned.com et colle la liste des fuites. L'assistant classe par risque actuel :
1. **mot de passe à changer** d'abord, surtout s'il a été réutilisé ailleurs ;
2. **authentification à deux facteurs** à activer (application d'authentification de préférence au SMS) ;
3. **compte à supprimer** s'il ne sert plus.

Recommander un gestionnaire de mots de passe. Ne jamais demander de mot de passe dans la conversation.

## Étape 6 — Suivi et relances

C'est l'étape que le thread viral oublie, et celle qui fait le résultat. Produire un **tableau de suivi** à partir de `assets/suivi-demandes.csv` (en fichier tableur — CSV ou Excel — si l'outil sait en produire, sinon en tableau dans la réponse, à copier dans un tableur) :

`destinataire | catégorie | type de demande | canal | URL concernée | date d'envoi | délai légal | échéance | réponse reçue le | résultat | relance envoyée le | plainte déposée le | statut | preuve`

Statut : une valeur parmi `à envoyer`, `envoyée`, `accusé reçu`, `effectuée`, `refusée`, `relancée`, `plainte déposée`, `revenue` (fiche réapparue : ouvrir une nouvelle demande). Une demande passe à `effectuée` seulement quand la personne a constaté que la fiche a disparu **et** que le résultat de recherche a disparu.

- calculer chaque échéance à partir de la date d'envoi et du délai vérifié à l'étape 0 ;
- rédiger d'avance la **relance** et, pour l'UE, le **modèle de plainte** à l'autorité (`references/modeles-courriers.md`) ;
- rappeler de garder une preuve de chaque envoi (capture, accusé de réception, copie du courriel) ;
- proposer une **veille automatique** entre deux inventaires : une alerte Google Alerts (google.com/alerts) par identifiant, chaque fois entre guillemets (« Prénom Nom », chaque e-mail, chaque téléphone dans ses formats courants), fréquence « au fur et à mesure ». L'alerte ne voit que les nouvelles pages indexées par Google : elle ne remplace pas l'inventaire, elle sert à ouvrir une nouvelle demande dès qu'une fiche réapparaît ;
- proposer de refaire l'inventaire **tous les 6 à 12 mois**, parce que les fiches reviennent. Si la personne le souhaite et que l'outil sait créer des rappels ou des tâches planifiées, créer le rappel ; sinon, donner les dates à noter dans son agenda.

## Prévention

- Alias e-mail jetables pour chaque inscription (SimpleLogin, addy.io, ou les alias de son fournisseur de messagerie) : si un alias fuit, on le supprime.
- Navigateur ou extension qui bloque les traqueurs par défaut.
- Réglages de confidentialité des réseaux sociaux (profil non indexé, liste d'amis masquée).
- Numéro de téléphone secondaire pour les inscriptions et les annonces.
- Téléphone fixe en **liste rouge** chez l'opérateur (gratuit ; le fixe est publié par défaut dans l'annuaire, le mobile seulement sur demande ; à redemander à chaque changement d'opérateur). Les annuaires (Pages Blanches, 118 712) acceptent aussi une demande RGPD directe.
- Nom de domaine personnel : vérifier chez le registrar que les coordonnées WHOIS sont masquées.
- Contre le spam et le démarchage, l'**opposition à la prospection** (RGPD, art. 21, § 2, modèle 9) s'impose sans exception, indépendamment de l'effacement. En France, depuis le 11 août 2026, le démarchage téléphonique commercial requiert un consentement préalable (décret n° 2026-662 ; Bloctel n'existe plus) : ne rien cocher lors des inscriptions, et signaler un appel non sollicité sur SignalConso.

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
- Laisser la personne envoyer une pièce d'identité sans filigrane ni masquage.
- Traiter un mineur ou un défunt comme un cas ordinaire : le fondement et les justificatifs diffèrent.
- Recommander l'enfouissement par faux contenus ou faux avis.
- Marquer une demande « effectuée » sans que la personne ait vérifié la disparition de la fiche et du résultat de recherche.
