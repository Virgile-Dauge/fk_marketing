# fk_marketing

Skills anti-marketing / décroissance pour Claude. Des outils qui aident à **moins
acheter et mieux**, en démontant le storytelling de fiche produit.

## `achete-pas`

Skill d'achat sous contrainte de décroissance. Avant tout comparatif, il sépare
la pulsion du vrai besoin, refuse la solution déjà projetée par le marketing,
fait passer **ne rien faire / réparer / emprunter / occasion** avant le neuf,
puis — seulement si l'achat neuf survit — compare sérieusement (specs vs
marketing, prix officiel / constaté / promo, coût réel € + empreinte) et conclut par
une reco par profil.

- Format **Agent Skill** (`SKILL.md` + `references/`).
- **Déploiement : claude.ai uniquement** (pas Claude Code, pour ne pas polluer
  l'env de dev) — procédure ci-dessous, rationale en
  [`docs/adr/0003`](./docs/adr/0003-deploiement-claude-ai-uniquement.md).
- **Locale : France** (assumé). Comparateurs et déclenchement en français par
  choix — meilleur triggering FR, sources FR. D'autres locales viendront.

```
achete-pas/
├── SKILL.md
└── references/
    ├── phase0-dissuasion.md      # le cœur : protocole d'entretien + verdict
    ├── criteres-vs-marketing.md  # grille décisif/marketing par catégorie
    └── sources-prix-fr.md        # comparateurs neutres, occasion, anti-affiliation
```

## Déploiement (claude.ai)

Prérequis : un plan **Pro / Max / Team / Enterprise** avec **exécution de code**
activée.

1. Construire le zip depuis la racine du repo. Le dossier `achete-pas/` doit être
   **à la racine du zip** (pas son contenu en vrac), et son nom doit matcher le
   `name:` du frontmatter :
   ```sh
   zip -r achete-pas.zip achete-pas -x '**/.*'
   ```
2. Sur claude.ai : *Réglages > Fonctionnalités*, section Skills → **uploader**
   `achete-pas.zip`.
3. Au premier upload, vérifier que le champ frontmatter `license:` est accepté ;
   sinon le déplacer sous `metadata:`.

**Mettre à jour** : refaire l'étape 1 puis ré-uploader. Les surfaces ne se
synchronisent pas (cf. ADR 0003) — c'est manuel à chaque fois.

## Licence

MIT (voir [`LICENSE`](./LICENSE)). Du texte court ; on s'aligne sur la norme de
l'écosystème skills (MIT/Apache) plutôt que de chipoter sur du copyleft.
