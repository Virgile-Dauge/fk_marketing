# Déploiement : claude.ai uniquement (zip), pas Claude Code

`achete-pas` se déploie **uniquement sur claude.ai**, par upload d'un `.zip` du
dossier `achete-pas/` via *Réglages > Fonctionnalités* (plans Pro/Max/Team/
Enterprise, exécution de code activée). Le **repo GitHub** (`Virgile-Dauge/
fk_marketing`) est la **source de vérité** d'où l'on construit le zip ; il n'est
pas une cible d'exécution.

## Le « non » à Claude Code (explicite)

On ne documente **pas** d'installation Claude Code (`~/.claude/skills/`). C'est un
skill grand public qui n'a rien à faire dans un environnement de développement —
l'y installer polluerait l'espace de dev. Le dossier `achete-pas/` vit à la racine
du repo, que Claude Code **n'auto-découvre pas** (il ne scanne que `~/.claude/
skills/` et `.claude/skills/`) : la source reste donc inerte dans le workspace.

## Hors-scope : l'API

L'API Claude est une surface distincte (upload séparé, partagé workspace, **sans
accès réseau**) qui casserait l'accès prix/promos temps réel. À reconsidérer
seulement si un besoin réel apparaît.

## Conséquence

Les surfaces ne se synchronisent pas : tout déploiement est un **upload manuel**.
En v1, pas d'automatisation de sync (et de toute façon impossible entre surfaces).
