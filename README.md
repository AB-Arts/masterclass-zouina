# Masterclass ZOUINA — skill de révision

Skill Claude qui répond au client **ZOUINA** sur ce qu'il a appris pendant sa masterclass
IA donnée par **AB-Arts**. Elle ne répond que dans les limites du cours et redirige le reste
vers [ab-arts.be/academy](https://ab-arts.be/academy).

## Comment ça marche

Le client tape `/ab-arts-masterclass-zouina`, la skill lui demande **ce qu'il veut savoir**
et dans **quelle langue** (FR, EN ou NL). Elle répond au niveau débutant du cours, en
s'appuyant uniquement sur le contenu du dossier `references/`. Si la question dépasse ce qui
a été vu, elle oriente vers une masterclass dédiée sur l'academy.

## Contenu du dépôt

```
SKILL.md                     le comportement de la skill (à ne pas casser)
references/
  00-carte-et-perimetre.md   la carte des sujets + la limite de ce qui a été vu
  01-philosophie-et-comprendre-lia.md
  02-prompts-et-modeles.md
  03-skills-et-memoire.md
  04-git-et-securite.md
  05-prix-tokens.md
  06-agents-stack-exemples.md
  07-flow-grow.md
```

## Installer la skill

Cloner le dépôt dans le dossier des skills de Claude, par exemple :

```bash
git clone https://github.com/AB-Arts/masterclass-zouina.git ~/.claude/skills/ab-arts-masterclass-zouina
```

La skill devient disponible sous `/ab-arts-masterclass-zouina`.

## Mettre à jour avec la partie 2 du cours

Cette base couvre la **partie 1** de la masterclass. Pour ajouter la partie 2 :

1. Ajouter un fichier `references/08-...md` avec les nouveaux sujets.
2. Compléter la carte `references/00-carte-et-perimetre.md` (déplacer les points « partie 2 »
   vers les sujets couverts, ajouter les nouveaux).
3. Commit et push.

Le périmètre de la skill s'élargit automatiquement : elle lit toujours la carte en premier.

---

AB-Arts SRL · [ab-arts.be](https://ab-arts.be) · The Academy
