---
statut: brouillon
para: projet
domaines:
- recherche
auteurs:
- Michaël Launay
confidentialite: publique
publication:
- notes-publiques
rag: true
titre: KR Glossaire métier
type: document
themes:
- genie-logiciel
- glossaire
- democratie
- decentralisation
- kuneagi
resume: 'Glossaire métier de Kunereti : communauté, membre, contribution, idée, proposition, amendement, scrutin, bulletin, mention, jeton, avis, agent et les autres termes du domaine.'
schema_version: 1
uid: 01M7AK890X92K64Q31SK54M489
date_creation: 2026-11-13
langue: fr
date_modification: 2026-11-20
metadata_verifiees: false
---

- **Kunereti** : Outil de délibération et d'innovation participative réparti, sans serveur central. Il reprend les règles de Nova-Ideo et de KuneAgi et les fait reposer sur des dépôts de fichiers signés. Le projet s'est d'abord appelé « KuneAgi V2 ».
- **reteKuneAgi** : Outil de démocratie délibérative réparti, appliquant certaines des règles de fonctionnement de Kunereti au cas particulier de l’élaboration et de la sélection des actions d’un collectif.
- **KuneAgi, Nova-Ideo** : Les logiciels serveurs dont Kunereti reprend les concepts. Nova-Ideo date de 2014 ; KuneAgi en est la variante de la coopérative Cosmopolitical. Ils restent en service.
- **Communauté** : L'ensemble des membres qui délibèrent ensemble sous une même charte. Techniquement, un dépôt de communauté et son QR code. Le dépôt contient : (1) la charte, (2) les clefs racines, (3) la liste des liens vers les dépôts des communautés auxquelles elle ouvre ses contenus en lecture, (4) dans le cas d’une admission robuste, la liste des hashcodes des triplets identifiants des membres.
- **Charte** : Le texte et les règles de la communauté : conditions pour être membre, taille des groupes, nombre de groupes par membre, nombre de jetons, durées, quorums, méthode de vote, liste des étiquettes. Elle se modifie par un vote.
- **Membre** : Personne admise dans la communauté après procédure d’admisson (légère ou robuste). Connue par un pseudonyme et des clés publiques, jamais par son identité civile.
- **Fiche de membre** : Le fichier qui représente un membre dans le dépôt de communauté : son pseudonyme, ses clés publiques, son état d'admission, ses rôles. Elle ne contient aucune donnée d'identité en clair. Lorsque l’admission se fait par mode “robuste”, elle contient le hashcode du triplet identifiant du membre (prénoms, noms, date de naissance).
- **Candidat** : Personne qui a déposé sa candidature et n'est pas encore admise. Elle n’a pas accès aux contenus (ni en lecture, ni en écriture).
- **Triplet identifiant** : Le triplet identifiant d’une personne physique est constitué de (1) son ou ses prénoms, (2) son ou ses noms de famille, (3) sa date de naissance.
- **Admission légère** : Le processus d’admission dans lequel le système se contente de vérifier que le candidat est un humain (et non un robot).
- **Admission robuste** : Le processus d'admission hérité de KuneAgi : des membres tirés au sort vérifient qu'un candidat est une personne réelle, que le triplet identifiant qu’elle revendique est conforme à celui de ses documents d’identité officiels, et qu’il remplit les conditions fixées pour l’appartenance à la Communaute. La vérification que la personne n'a pas déjà un compte est faite par la machine, en comparant le hashcode du triplet identifiant du candidat avec la liste des hashcodes des triplets identifiants des membres existants.
- **Attestation** : L'avis signé qu'un membre vérificateur dépose après avoir vérifié un candidat, ou un membre qui a perdu ses clés. L'admission se décide sur les attestations réunies ; le dépôt ne garde rien d'autre de la vérification.
- **Pseudonyme** : Le nom public d'un membre. Aucune donnée d'identité (en dehors du hashcode du triplet identifiant des membres - dans le cas d’une admission “robuste”) n'est écrite dans les dépôts.
- **Clés** : Chaque membre détient deux paires de clés, l'une pour signer, l'autre pour recevoir des messages chiffrés. La clé privée ne quitte pas son appareil. Perdre ses clés oblige à être réadmis.
- **Phrase de secours** : Suite de mots que l'application fait noter au membre quand elle crée ses clés, et qui lui permet de les retrouver sur un autre appareil. Qui a perdu à la fois son appareil et sa phrase de secours doit être réadmis par ses pairs.
- **Signature** : Preuve, vérifiable par tous, qu'un fichier a été écrit par le détenteur d'une clé et n'a pas été modifié depuis. Publier, voter, soutenir : c'est toujours signer.
- **Dépôt** : Un dossier de fichiers avec tout son historique, géré par Git, que chaque membre copie intégralement. Il existe un dépôt de communauté et un dépôt par groupe de travail.
- **Notice** : Le fichier qui présente un dépôt et en porte les règles. La notice d'un dépôt de communauté contient la charte et la liste fixe de ses étiquettes ; celle d'un dépôt de groupe de travail contient le titre et le résumé de la proposition, la liste de ses sections, la durée et le mode de l'itération en cours. Elle est signée.
- **Forge** : Un service qui héberge des dépôts Git. La communauté en utilise au moins deux ; aucune n'est indispensable.
- **Copie personnelle (fork)** : La copie d'un dépôt qui n'appartient qu'à un membre. C'est là que vivent ses brouillons. C'est aussi le moyen de dupliquer une proposition ou de se séparer d'un groupe.
- **Synchronisation** : L'échange des nouveautés entre l'appareil d'un membre et un dépôt partagé. Rien n'arrive ni ne part en dehors d'elle.
- **En-tête (frontmatter)** : Le bloc de propriétés placé en tête de chaque fichier. Il porte le type du contenu, son identifiant, son état, ses liens et sa signature.
- **Problème** : Le texte qu'un groupe de travail co-écrit et décrivant une situation dans le monde jugée négativement, et qui demande donc à être transformée. Le Problème est divisé en sections.
- **Proposition d’Action** : Le texte qu'un groupe de travail co-écrit, et décrivant des actions susceptibles de résoudre ou d'atténuer le Problème auquel la Proposition d’Action est reliée, et donc d'atteindre un état du monde jugé meilleur. La Proposition d’Action est divisée en sections.
- **Section** : Un morceau du texte d'un Problème ou d’une Proposition d’Action, dans son propre fichier. Un amendement vise une ou plusieurs sections.
- **Groupe de travail** : Les participants qui co-écrivent un Problème ou une Proposition d’Action : douze au plus par défaut. Un groupe, une proposition, un dépôt.
- **Participant** : Membre inscrit dans un groupe de travail. Un membre participe à cinq groupes au plus par défaut.
- **Liste d'attente** : Les membres qui attendent une place dans un groupe complet.
- **Itération (cycle)** : Période de travail à durée limitée, à l'issue de laquelle le groupe vote sur les amendements au document sur lequel il travaille. Sa durée et son mode sont choisis par les participants.
- **Mode wiki** : Mode de co-écriture où chaque modification enregistrée produit une nouvelle version, sans validation.
- **Mode avec amendements** : Mode de co-écriture en parallèle : chacun modifie de son côté, puis les modifications sont mises en concurrence par le vote.
- **Amendement** : Une ou plusieurs modifications corrélées, réunies par une même intention et justifiées par leur auteur.
- **Empreinte** : Courte suite de caractères calculée à partir d'un texte, qui change dès que le texte change. Elle désigne la version exacte sur laquelle on vote.
- **Scrutin** : La définition d'un vote : la question, les candidats, la liste figée des votants, les dates, le quorum, la méthode.
- **Bulletin** : Le vote d'un membre : un fichier signé, un par votant.
- **Jugement majoritaire** : Méthode de vote de Balinski et Laraki. Chaque votant attribue à chaque candidat une mention parmi sept, de « Excellent » à « À rejeter » ; le candidat retenu est celui dont la mention médiane est la meilleure, avec une règle pour départager les propositions ayant la meilleur note médiane.
- **Mention** : L'appréciation qu'un votant attribue à un candidat dans un scrutin au jugement majoritaire. Il y en a sept, de « Excellent » à « À rejeter ». Un bulletin porte une mention par candidat. Le mot est réservé à ce sens.
- **Dépouillement** : Le calcul du résultat d'un scrutin. Il est déterministe : chacun peut le refaire et doit trouver le même résultat.
- **Co-signature** : Signature du résultat d'un scrutin par plusieurs membres qui l'ont recalculé. Sans elle, le résultat ne vaut rien.
- **Scrutin scellé** : Scrutin où chaque votant ne publie d'abord que l'empreinte de son bulletin, et ne le révèle qu'après la clôture.
- **Quorum** : Nombre minimal de bulletins pour qu'un scrutin produise un effet.
- **Jeton de Priorité** : Marque de priorité qu'un membre pose sur un Problème publié. Chaque membre en a sept ; quand ils sont tous posés, il faut en reprendre un pour le placer ailleurs.
- **Avis** : *Avis d'un membre tiré au sort* : la réponse signée d'un membre vérificateur, d'un modérateur, d'un contrôleur de conformité ou d'un juré ; la décision se prend à la majorité des avis exprimés.
- **Rôle** : Qualité inscrite dans la fiche d'un membre à la suite d'un vote : autorité, examinateur, membre du comité. Il n'existe pas de compte privilégié.
- **Autorité** : Membre qui administre un dépôt et y fusionne ce qui est légal. C'est un greffier : il exécute, il ne décide pas.
- **Vérificateur** : Deux sens à distinguer. *Membre vérificateur* : membre tiré au sort pour vérifier l'identité d'un candidat. *Vérificateur* tout court : les scripts de contrôle, hébergés hors des dépôts, qui refusent toute écriture mal formée, mal signée ou illégale.
- **Processus (workflow)** : Document qui déclare les états d'un contenu, les passages permis d'un état à l'autre, qui peut les déclencher et à quelle condition.
- **Transition** : Le passage d'un contenu d'un état à un autre. Elle est légale si la définition du processus l'autorise et si ses conditions sont réunies.
- **Tirage au sort vérifiable (tiré au sort)** : Désignation de membres vérificateurs, de modérateurs, de contrôleurs de conformité ou de jurés par un calcul que chacun peut refaire, à partir d'une valeur publique imprévisible. Dans Kunereti, tout tirage au sort est vérifiable : « tiré au sort » veut toujours dire cela.
- **Jury** : Membres tirés au sort pour trancher un signalement ou la contestation d'un scrutin.
- **Message** : Petit fichier signé qui cite l'objet dont il parle et, le cas échéant, le message auquel il répond.
- **Fil de discussion** : L'ensemble des messages qui citent le même objet.
- **Notification** : Information calculée par l'appareil du membre à partir de ce qui a changé depuis sa dernière synchronisation. Aucun serveur ne l'envoie.
- **Signalement** : Message par lequel un membre ou l'agent veilleur demande qu'un jury examine un contenu.
- **Masquer** : Décision d'un jury : le contenu n'est plus affiché, mais il reste dans l'historique.
- **Agent** : Modèle de langage muni d'une clé, d'une mission et d'un périmètre d'écriture limité, déclarés dans une fiche votée par la communauté. Cinq agents : curateur, assistant d'amendement, synthétiseur, traducteur, veilleur de modération.
- **Exécutant** : Le membre volontaire ou la tâche planifiée qui fait tourner un agent pour le compte de la communauté.
- **Objet dérivé** : Contenu produit par un agent ou par un calcul, que l'on peut effacer et recalculer : synthèse, traduction, index. Il n'a aucun poids dans les décisions.
- **Synthèse** : Résumé d'un fil ou d'une itération rédigé par un agent, toujours marqué comme tel.
- **Lien de catalogue** : Référence signée d'une communauté vers une autre. La fédération est la somme de ces liens.
- **QR code** : L'image qui contient l'adresse du dépôt de communauté et l'empreinte de sa clé racine. On rejoint une communauté en le scannant.
- **Observateur** : Membre qui suit un groupe de travail sans y participer : il lit, apporte des arguments, ne vote pas.
- **Statut de membre** : Qualité qui ouvre des droits différents selon la charte, par exemple membre ordinaire et coopérateur. Un droit peut être suspendu et rétabli.
- **Quarantaine** : Délai pendant lequel une personne qui a quitté la communauté ne peut pas y être réadmise (180 jours dans KuneAgi).
- **Modération avant publication** : Option de la charte : tout nouveau contenu est relu par des membres tirés au sort, qui ne jugent que sa forme. À ne pas confondre avec le signalement, qui intervient après coup.
- **Principes** : Les valeurs et règles de fond de la communauté, auxquelles une proposition doit être conforme pour être soumise à tous.
- **Note de comportement coopératif** : Option de la charte : note tirée des appréciations (+1, 0, −1) que les participants d'un groupe se donnent quand l'un d'eux en sort, et qui s'efface avec le temps.
- **Centre d'intérêt** : Recherche mémorisée par un membre sur son appareil, sous forme de phrase logique connectant des étiquettes de la liste fixe, qui l'alerte quand un contenu nouveau y répond.
- **Durée de validité d'une décision** : Délai pendant lequel on ne peut pas remettre au vote une décision déjà prise : nouvelle demande d'entrée, d'exclusion, ou nouveau signalement.
- **Clé racine** : La clé d'origine d'une communauté, dont découle la confiance dans ses autorités.