# Périmètre v1 : biens durables / semi-durables achetés neufs

Le skill `achete-pas` ne gouverne, en v1, que l'achat de **biens durables ou
semi-durables neufs** (électronique, électroménager, outillage, mobilier, vélo,
etc.). C'est le seul périmètre où l'ensemble du protocole tient : défaut « pas de
neuf », échelle d'évitement, occasion/réparation, coût réel incluant l'empreinte
(extraction, fabrication, CO2, déchet).

## Hors-scope (explicite)

- **Consommables / nécessités** (alimentation, hygiène, médicaments) : griller un
  achat récurrent et vital serait absurde et hostile. Le skill doit le détecter
  et ne pas dérouler la Phase 0.
- **Abonnements / services / numérique** : le *gate* « en as-tu vraiment besoin »
  s'y applique fort, mais les volets occasion / réparation / empreinte n'ont pas
  de sens. Extension naturelle post-v1, avec une Phase 0 adaptée.

## Cas particulier : le cadeau

Un achat pour un tiers reste dans le scope, mais en sous-cas de la Phase 0 : les
questions « tu possèdes déjà ? / usage réel » se redirigent vers le **destinataire**,
pas l'acheteur. Pas une catégorie séparée.

## Considered

Inclure les abonnements/services dès la v1 — écarté : ça dédoublerait la Phase 0
(deux protocoles distincts) avant même d'avoir validé le protocole principal sur
sa cible la plus nette.
