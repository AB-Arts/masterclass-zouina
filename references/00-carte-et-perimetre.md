# Carte des sujets et périmètre du cours

Cette carte dit **ce qui a été vu** pendant la masterclass ZOUINA (partie 1) et **où le
trouver**. Tout ce qui n'est pas listé ici comme « vu » se traite avec la redirection vers
https://ab-arts.be/academy (voir SKILL.md, section 3). Pour orienter vers la **bonne**
masterclass plutôt que le lien général, sers-toi de `08-catalogue-academy.md`.

## Le fil rouge du cours

Une seule grande idée traverse toute la journée : **on utilise l'IA pour, au final, ne plus
dépendre de l'IA.** On s'en sert pour construire ses propres outils, qui tournent ensuite
tout seuls, hors du modèle. Voir `01-philosophie-et-comprendre-lia.md`.

## Sujets couverts (tu peux répondre)

| Sujet | Fichier |
|---|---|
| La philosophie : l'indépendance, ne pas tout faire dans le desktop, l'analogie SAP | `01-philosophie-et-comprendre-lia.md` |
| Comprendre l'IA : ce que c'est vraiment, le « bébé », le cerveau/l'agence | `01-philosophie-et-comprendre-lia.md` |
| Le noyau contre les clusters, les 4 clusters d'un site, l'ordre copy → design → fonctions → stack, le handover | `01-philosophie-et-comprendre-lia.md` |
| Les prompts en 2026 : un prompt = tout (texte, audio, image, vidéo, code) | `02-prompts-et-modeles.md` |
| Challenger les modèles entre eux (Claude, Gemini, OpenAI) | `02-prompts-et-modeles.md` |
| Les sécurités des modèles (pourquoi Claude refuse certaines choses) | `02-prompts-et-modeles.md` |
| Les 6 blocs d'un prompt et pourquoi le rôle est surestimé | `02-prompts-et-modeles.md` |
| Ce qu'est une skill, le cycle cluster → MD → skill → outil (la mécanique générale ; bâtir une skill d'identité graphique = partie 2, voir plus bas) | `03-skills-et-memoire.md` |
| La courbe de l'effort | `03-skills-et-memoire.md` |
| Garder le contexte : la mémoire, les 30 jours, le handover, le mode Code | `03-skills-et-memoire.md` |
| Git et GitHub : repo, commit, versions, branches, rollback, la connexion CLI | `04-git-et-securite.md` |
| Les clés d'API et la sécurité : jamais dans le chat, jamais dans Git, le .gitignore, les secrets, les plafonds | `04-git-et-securite.md` |
| GitHub Actions : faire tourner une automatisation sur un serveur, hors Claude | `04-git-et-securite.md` |
| Les modèles Claude, leurs particularités, quand baisser de modèle | `02-prompts-et-modeles.md` |
| Le prix des tokens : les plans, le desktop contre l'API, le coût d'un article | `05-prix-tokens.md` |
| Les agents : agent côté serveur, agent côté front | `06-agents-stack-exemples.md` |
| Les artifacts (les fenêtres à droite) | `06-agents-stack-exemples.md` |
| La stack (survol) et les exemples : GoodWorker, AB Studio, ab-arts.be | `06-agents-stack-exemples.md` |
| Flow & Grow : les méthodes du client, augmentées par l'IA | `07-flow-grow.md` |

> **Le mot « cluster » a deux sens dans le cours.** (1) Les *clusters* = les grappes de calcul
> du cerveau de l'IA, quand on cherche à **comprendre l'IA** (`01-philosophie-et-comprendre-lia.md`).
> (2) Un *cluster* = une bulle de contexte / d'information dans la méthode **noyau et clusters**,
> quand on **construit un projet**. Pour un débutant, c'est presque toujours le sens (2) ; si le
> contexte est ambigu, demande une précision avant de répondre.

## Sujets effleurés, prévus pour la suite (partie 2)

Ces points ont été montrés ou annoncés mais pas détaillés. Dis que c'est prévu pour la
suite du parcours, et donne le lien academy.

- **Claude Design** et la création d'une skill d'**identité graphique** (le design, l'après-midi).
  Nuance : la **mécanique générale** d'une skill (le cycle cluster → MD → skill) est vue en cours
  (`03-skills-et-memoire.md`), donc réponds-la ; mais bâtir la skill de charte graphique
  elle-même, avec Claude Design, c'est la partie 2 — redirige ce volet vers l'academy.
- Assembler plusieurs skills (design + écriture + Flow) pour préparer un agent.
- La partie 2 de la masterclass en général (implémentation concrète sur les projets du client).

## Sujets hors cadre (redirige vers l'academy)

Le formateur les a explicitement présentés comme « une autre masterclass » ou « une formation
à part ». Ne les explique pas en détail, redirige.

- **Construire réellement une app de bout en bout** (le développement complet). Le formateur
  a une formation de 3 semaines et une de 6 semaines pour ça.
- **La stack en détail et la mise en production** : configurer Supabase, Cloudflare, Vercel,
  les secrets du serveur, les tests unitaires, la CI/CD. Ces briques sont juste **citées en
  survol** dans le cours (ce qu'elles font, en une phrase, voir `06-agents-stack-exemples.md`) ;
  dès qu'on parle de **comment** les installer, les configurer ou déployer, redirige.
- **Faire tourner un modèle en local** (Mac Studio, son propre serveur, cartes graphiques) :
  c'est une masterclass à part entière.
- **Le détail des GitHub Actions** et des agents avec interface (front) : au-delà du survol.
- Tout sujet qui n'apparaît nulle part dans cette carte.

## Rappel de posture

Le formateur l'a répété : l'IA n'est pas magique, elle ne remplace pas tout. C'est un « gros
bébé » qu'il faut diriger. Reste modeste, concret, et au niveau de ce qui a été vu.
