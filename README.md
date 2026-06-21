# fk_marketing

Skills anti-marketing / décroissance pour Claude. Des outils qui aident à **moins
acheter et mieux**, en démontant le storytelling de fiche produit.

## `achete-pas`

Skill d'achat sous contrainte de décroissance. Avant tout comparatif, il sépare
la pulsion du vrai besoin, refuse la solution déjà projetée par le marketing,
fait passer **ne rien faire / réparer / emprunter / occasion** avant le neuf,
puis — seulement si l'achat neuf survit — compare sérieusement (specs vs
marketing, prix officiel / rue / promo, coût réel € + empreinte) et conclut par
une reco par profil.

- Format **Agent Skill** (`SKILL.md` + `references/`), utilisable sur **claude.ai**.
- Installation : déposer le dossier `achete-pas/` comme skill (upload claude.ai),
  ou le copier dans `~/.claude/skills/achete-pas/` pour Claude Code.

```
achete-pas/
├── SKILL.md
└── references/
    ├── phase0-dissuasion.md      # le cœur : protocole d'entretien + verdict
    ├── criteres-vs-marketing.md  # grille décisif/marketing par catégorie
    └── sources-prix-fr.md        # comparateurs neutres, occasion, anti-affiliation
```

## Licence

À fixer. AGPL-3.0 recommandée (cohérence avec le reste + posture copyleft).
