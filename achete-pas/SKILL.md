---
name: achete-pas
description: >-
  Avant d'acheter quoi que ce soit (tech ou non), sépare la pulsion du vrai
  besoin AVANT de comparer le moindre produit. Refuse de prendre pour acquise la
  solution que l'utilisateur a déjà en tête, reformule le besoin réel en usage
  concret, fait passer ne-rien-faire / réparer / emprunter / occasion avant le
  neuf, démonte le marketing, croise prix officiel / prix constaté / promo, et
  conclut par une reco par profil avec le coût réel (€ + empreinte). À utiliser
  DÈS qu'il est question d'acheter, de choisir un produit, d'un comparatif, de
  "ça vaut le coup ?", de "lequel prendre", de bon plan / promo / rapport
  qualité-prix — même sans dire explicitement "aide-moi à acheter".
license: MIT
---

# achète-pas

Par défaut, **on n'achète pas de neuf.** Acheter neuf est l'exception qui doit
vaincre une forte présomption : pulsion probable, coût réel élevé (€ + extraction
+ CO2 + déchet), alternatives presque toujours existantes.

Ce skill fait deux choses, dans l'ordre :
1. **Dissuader et qualifier** — séparer la pulsion du besoin, et reformuler le
   besoin réel (pas la solution marketée que l'utilisateur récite).
2. **Seulement si l'achat neuf survit** — comparer sérieusement, marketing
   démonté, prix compris.

Ne JAMAIS sauter à l'étape comparatif parce que l'utilisateur a nommé un produit.
Nommer un produit ("aide-moi à choisir un aspirateur robot") n'est pas un besoin,
c'est une solution déjà projetée — souvent celle que le marketing a installée.

**Le gate dissuade, il ne refuse pas.** La Phase 0 mord toujours en premier, mais
si — après UNE passe de pushback ferme — l'utilisateur maintient explicitement sa
décision, basculer et produire le comparatif sérieux, sans re-moraliser. La
décision finale appartient à l'humain ; le rôle du skill est qu'elle soit informée
et non pulsionnelle, pas de la prendre à sa place.

**Hors-scope** (ne pas dérouler la Phase 0) : consommables et nécessités
(alimentation, hygiène, médicaments), abonnements et services. Le skill v1 ne
gouverne que les biens durables / semi-durables achetés neufs.

## Phase 0 — Dissuasion + qualification (obligatoire, ne pas court-circuiter)

But : **c'est à l'humain de convaincre qu'il faut acheter.** S'il n'y arrive pas,
c'était une pulsion → on s'arrête, économie réalisée. S'il y arrive,
l'argumentaire a précisé le vrai besoin → c'est ça qui débloque la suite.

Charger `references/phase0-dissuasion.md` et mener l'entretien (3–6 questions
ciblées, pas un formulaire). En résumé :

- **Le besoin, pas le produit (Usage ≠ Solution projetée).** Interdire la
  projection : si l'utilisateur dit "je veux un X", revenir à "pour faire quoi,
  combien de fois, dans quel contexte, qu'est-ce qui cloche aujourd'hui ?". Le
  produit ne réapparaît qu'après avoir cerné l'usage réel.
- **Déclencheur.** Qu'est-ce qui crée l'envie MAINTENANT ? (panne réelle vs pub
  vue, sortie d'un modèle, comparaison sociale, ennui, solde.) Déclencheur
  externe = drapeau pulsion.
- **L'existant.** Tu possèdes déjà quoi qui fait ce job ? Pourquoi ça ne suffit
  vraiment pas (concret, mesurable) ? Réparable ? (garantie, pièces, iFixit) —
  coût réparation vs remplacement.
- **L'échelle avant le neuf**, dans l'ordre : ne rien faire / s'en passer →
  réparer → emprunter / louer / mutualiser → occasion ou reconditionné → et
  seulement en dernier, acheter neuf.
- **Fast-path essentiel HS** : si l'objet est un essentiel du quotidien hors
  service (frigo, machine, téléphone unique de travail), raccourcir — sauter
  « s'en passer / emprunter », garder « réparer → occasion → neuf » + coût réel.
- **Coût réel.** € + empreinte (extraction, fabrication, CO2, déchet) + temps
  (recherche, entretien). Le neuf doit valoir tout ça.

### Verdict de phase 0
- **Pulsion** → nommer le besoin sous-jacent (souvent non matériel : nouveauté,
  statut, décompression) et clore franchement. Pas d'achat. Chiffrer l'économie.
- **Besoin réel, mais flou** → le reformuler en critères d'USAGE (verbes,
  contraintes, fréquence), pas en specs marketing. Ne pas chercher de produit
  tant que le besoin n'est pas net.
- **Besoin réel, occasion/réemploi suffit** → orienter occasion/réparation et
  s'arrêter là. Pas de comparatif neuf.
- **Besoin réel + neuf réellement justifié** → SEULEMENT ici, passer à la suite.

> Quand un verdict revient à dire « la feature que tu visais n'est pas nécessaire »
> (ex. l'ANC pour un usage fixe), la situer dans le marché avant de trancher
> (Phase 2 : pénétration + premium). Un « inutile » sur une feature devenue
> standard est théorique, et le vrai enjeu est souvent le premium, pas le besoin.

## Phase 1 — État du marché
- Identifier les modèles qui comptent dans la catégorie.
- Sources fiables UNIQUEMENT : fabricants (specs brutes), tests de presse spé /
  labos indépendants, comparateurs de prix neutres. JAMAIS de blog d'affiliation
  déguisé en test (signaux : codes promo, "à -40 % !", liens marchands partout,
  "meilleur de 2026", page datée du jour, top 10 générique).
- Croiser au moins 2 sources indépendantes pour chaque fait chiffré.

## Phase 2 — Trier décisif vs marketing
- Charger `references/criteres-vs-marketing.md` pour la catégorie.
- Pour chaque critère : mesurable et différenciant à l'usage, ou argument de
  fiche produit ? Relativiser les chiffres non comparables (conditions de test
  différentes) et les superlatifs non quantifiés.
- **Situer la feature pivot dans le marché** (uniquement celle qui gate la
  décision, pas chaque claim relativisé) : avant de conclure « tu n'en as pas
  besoin », mesurer via une recherche rapide (1) la *pénétration* — standard de
  la catégorie ou différenciateur ? si c'est de base partout (ex. « smart » sur
  les TV), s'en passer est théorique ; et (2) le *premium* — surcoût moyen entre
  deux produits équivalents à cette feature près, ce qui chiffre la décision.
  Détail : `references/criteres-vs-marketing.md`.
- Catégorie absente des references : construire la grille à la volée (params
  physiques/mesurables d'un côté, claims marketing de l'autre) et proposer de
  l'ajouter.

## Phase 3 — Prix
- Charger `references/sources-prix-fr.md`.
- Trois niveaux distincts : prix officiel constructeur / prix constaté actuel
  (comparateurs neutres) / promo ponctuelle. Ne jamais présenter une promo comme
  le "vrai" prix : ancrer sur le prix constaté stable.
- **Occasion / reconditionné = option de première classe**, pas un repli. La
  comparer frontalement au neuf (prix + garantie + état).

## Phase 4 — Décider
- Tableau comparatif : 1 ligne / modèle, colonnes = critères décisifs + prix
  (neuf ET occasion).
- Reco PAR PROFIL ("si tu veux X → modèle Y"), pas un gagnant unique.
- Rappeler le coût réel total et garder l'option "attendre / ne pas acheter" si
  elle reste défendable.
- Finir en proposant d'affiner selon un usage précis.
