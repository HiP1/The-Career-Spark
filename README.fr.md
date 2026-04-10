# The Career Spark

🇬🇧 [English](README.md) | 🇪🇸 [Español](README.es.md)

Un skill IA pour la création de CV et lettres de motivation, par extraction structurée, construction narrative et rédaction calibrée. L'étincelle est déjà dans le parcours du candidat. Ce skill la trouve et la rend visible.

## Ce que fait ce skill

La plupart des CV sous-vendent le candidat. Ce skill comble cet écart honnêtement.

Il prend le CV existant, le parcours professionnel et les preuves disponibles, extrait les compétences cachées, construit un récit de carrière stratégique, et produit des documents de candidature à la fois entièrement honnêtes et pleinement convaincants. Il a été développé à partir d'un vrai projet de refonte de CV où 44 compétences explicites sont devenues 134 après extraction et inférence, avec des catégories entières totalement absentes du CV d'origine.

**L'objectif :** Aider le candidat à obtenir des entretiens pour des postes où il s'épanouira réellement, grâce à des documents qui le représentent fidèlement à son meilleur niveau.

## Comment ça fonctionne

Sept phases, chacune s'appuyant sur la précédente :

| Phase | Objectif | Livrable |
|-------|----------|----------|
| 1. Extraire | Trouver les vraies compétences | Inventaire des compétences avec lacunes identifiées |
| 2. Narrer | Construire la colonne vertébrale stratégique | Document narratif de carrière |
| 3. Rédiger | Créer le CV | CV au(x) format(s) cible(s) |
| 4. Cibler | Explorer le marché, associer les postes, optimiser pour les ATS | Paysage des postes, données salariales, CV optimisé ATS |
| 5. Couvrir | Rédiger des arguments ciblés | Lettres de motivation par poste |
| 6. Évaluer | Tester du point de vue du recruteur | Rapport de vulnérabilités et plan de préparation |
| 7. Livrer | Faire parvenir les documents à la bonne personne (optionnel) | Stratégie de distribution, plan de prise de contact |

Les corrections du candidat alimentent le processus. Chaque correction dans le projet d'origine a rendu le résultat à la fois plus honnête et plus convaincant. Le skill intègre des points de contrôle à chaque phase.

Le processus supporte le travail multi-session avec un mécanisme de transfert structuré. Quand une session devient longue, l'IA produit un document de transfert détaillé et regroupe tous les fichiers pour que la session suivante reprenne exactement là où celle-ci s'est arrêtée.

## Principes clés

- **Extraction avant rédaction.** Ne jamais rédiger un CV à partir de rien. Extraire les compétences, inférer celles qui manquent, puis construire.
- **Narration avant format.** Sans colonne vertébrale stratégique, le CV n'est qu'une liste d'emplois.
- **Altitude exacte.** Ni sous-vente ni survente. La cible est le cadrage à la fois entièrement honnête et pleinement convaincant.
- **Utile signifie que le candidat est embauché.** Pas "le candidat est content du document." L'approbation n'est pas le service. Le service, c'est que le candidat soit embauché pour un poste où il s'épanouit.
- **Bienveillance et honnêteté ne sont pas en concurrence.** Les retours sont formulés avec soin, pas retenus pour éviter la friction. Le candidat doit sentir que l'IA est de son côté, y compris quand elle est en désaccord.
- **Devoir de vigilance.** Le CV porte le nom du candidat. L'IA vérifie activement les risques juridiques, professionnels et réputationnels, y compris les conséquences que le candidat n'a pas anticipées.
- **Le candidat a toujours raison sur sa propre expérience.** L'IA l'aide ensuite à la formuler dans le langage du marché.
- **Générer des options, pas des conclusions.** Le rôle de l'IA est génératif. Le rôle du candidat est éditorial. Le candidat doit choisir, pas simplement accepter.

## Structure du skill

```
career-spark/
├── SKILL.md                              Workflow principal (point d'entrée)
└── references/
    ├── principles.md                     Principes, redéfinition de l'utilité
    ├── calibration-guide.md              Calibration sous-vente/survente
    ├── overclaiming-guide.md             Psychologie de l'inflation et désescalade
    ├── narrative-archetypes.md           12 archétypes narratifs de carrière
    ├── evidence-without-portfolio.md     Trouver des preuves sans portfolio
    ├── cover-letter-guide.md             Cadre pour lettres de motivation ciblées
    ├── application-intelligence.md       Cartographie, stratégie de distribution
    ├── candidate-psychology.md           États émotionnels, résistances, conflits d'image
    └── cultural-norms.md                 Conventions de CV par pays/région
```

Le SKILL.md est le point d'entrée. Les fichiers de référence sont chargés à la demande selon la phase et la situation du candidat. Le package `.skill` contient uniquement ces 10 fichiers. README et LICENSE sont pour le dépôt, pas pour l'IA.

## Pour qui

- **Professionnels expérimentés** en transition ou repositionnement de carrière
- **Candidats en milieu de carrière** qui sous-vendent leurs compétences
- **Toute personne ciblant des postes spécifiques** qui a besoin de documents sur mesure, pas d'un simple polissage
- **Candidats en début de carrière** qui ont besoin de cadrer une expérience limitée
- **Candidats internationaux** ciblant des marchés avec des conventions de CV différentes
- **Candidats avec un poste de rêve** qui veulent maximiser leurs chances par la recherche organisationnelle et la distribution stratégique

## Ce que ce skill ne fait PAS

Ce skill produit des CV, des lettres de motivation, le récit stratégique qui les sous-tend, et (optionnellement) une stratégie de distribution. Il ne couvre pas la préparation aux entretiens, la négociation salariale, ni la stratégie LinkedIn. Cependant, ses résultats (récit de carrière, inventaire de compétences, recherche organisationnelle et histoires d'entretien collectées) sont conçus comme des inputs naturels pour ces activités.

## Installation

### En tant que Skill Claude

Téléchargez le fichier `.skill` depuis la page [Releases](../../releases), puis installez-le dans votre environnement Claude.

### Gemini

Utilisez le [Career Spark Gem](https://gemini.google.com/gem/1G_9r7u-X_TKPIX5MsdDz-WNJK3EU3n0_?usp=sharing) directement. Pour de meilleurs résultats, sélectionnez le modèle avec la plus haute capacité de réflexion. Pro est recommandé. Le mode Thinking est une bonne alternative. Fast fonctionnera mais risque de manquer certaines nuances de calibration et d'adaptation psychologique.

### ChatGPT

Utilisez le [Career Spark CustomGPT](https://chatgpt.com/g/g-69d26d47523881919acd487ef609384a-the-career-spark). Sélectionnez le meilleur modèle disponible. Note : le CustomGPT ne peut pas accéder à vos mémoires ni à votre historique de conversation. Si vous avez besoin que le skill utilise des conversations précédentes ou du contexte personnel, téléchargez le fichier `.skill` depuis la page [Releases](../../releases) et déposez-le directement dans une conversation.

### Autres fournisseurs IA

Le fichier `.skill` est une archive zip standard. Téléchargez-le depuis la page [Releases](../../releases), renommez-le de `career-spark.skill` en `career-spark.zip`, uploadez-le sur votre plateforme, et demandez au modèle d'utiliser le skill contenu dans le fichier zip. Le `SKILL.md` est le point d'entrée; les fichiers de référence dans `references/` sont chargés selon les besoins. Utilisez le modèle le plus performant disponible sur votre plateforme.

### Manuel

Clonez ou téléchargez ce dépôt. Pointez votre outil IA vers le fichier `SKILL.md` comme point d'entrée.

## Origine

Ce skill a été développé à partir d'un vrai projet de refonte de CV (mars-avril 2026) entre [Ivan "HiP" Phan](https://github.com/hip1) et Claude. Le processus en quatre sessions qui a produit le CV original a été documenté, puis généralisé et étendu lors d'une session dédiée de création de skill pour en faire un outil applicable à tout candidat, dans tout secteur.

Chaque principe a été découvert par la pratique et affiné par les retours du candidat. Les corrections du candidat ont été l'apport le plus précieux du projet original. Un processus qui n'intègre pas de boucles de correction produira des CV polis mais faux. Cette observation est le fondement de tout le skill.

## Licence

Licence MIT. Voir [LICENSE](LICENSE) pour les détails.
