# Carte des sujets et périmètre du cours

Cette carte dit **ce qui a été vu** pendant la masterclass ZOUINA (parties 1 et 2) et **où le
trouver**. Tout ce qui n'est pas listé ici comme « vu » se traite avec la redirection vers
https://ab-arts.be/academy (voir SKILL.md, section 3). Pour orienter vers la **bonne**
masterclass plutôt que le lien général, sers-toi de `08-catalogue-academy.md`.

## Le fil rouge du cours

Une seule grande idée traverse les deux journées : **on utilise l'IA pour, au final, ne plus
dépendre de l'IA.** On s'en sert pour construire ses propres outils (skills puis apps), qui
tournent ensuite de plus en plus tout seuls. Voir `01-philosophie-et-comprendre-lia.md`.

## Sujets couverts (tu peux répondre)

### Partie 1 : comprendre et poser les bases

| Sujet | Fichier |
|---|---|
| La philosophie : l'indépendance, ne pas tout faire dans le desktop, l'analogie SAP | `01-philosophie-et-comprendre-lia.md` |
| Comprendre l'IA : ce que c'est vraiment, le « bébé », le cerveau/l'agence | `01-philosophie-et-comprendre-lia.md` |
| Le noyau contre les clusters, les 4 clusters d'un site, l'ordre copy → design → fonctions → stack, le handover | `01-philosophie-et-comprendre-lia.md` |
| Les prompts en 2026 : un prompt = tout (texte, audio, image, vidéo, code) | `02-prompts-et-modeles.md` |
| Challenger les modèles entre eux (Claude, Gemini, OpenAI) | `02-prompts-et-modeles.md` |
| Les sécurités des modèles (pourquoi Claude refuse certaines choses) | `02-prompts-et-modeles.md` |
| Les 6 blocs d'un prompt et pourquoi le rôle est surestimé | `02-prompts-et-modeles.md` |
| Ce qu'est une skill, le cycle cluster → MD → skill → outil | `03-skills-et-memoire.md` |
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

### Partie 2 : passer à la pratique (skills, design, app, sécurité)

| Sujet | Fichier |
|---|---|
| Créer une skill concrètement : le cluster d'abord, le déclencheur (c'est toi), l'importance des inputs | `09-creer-et-affiner-une-skill.md` |
| La granularité : une skill ou plusieurs, saucissonner un gros projet, une skill par délivrable | `09-creer-et-affiner-une-skill.md` |
| Corriger une skill (capture d'écran → « corrige la skill et commit ») | `09-creer-et-affiner-une-skill.md` |
| Claude Design : à quoi ça sert, éditer à la main, ça remplace Figma, ça ne fait pas de photos, choisir le modèle (Fable/Opus 4.7-4.8) | `10-claude-design-et-design-system.md` |
| Le design system et le handoff (ZIP de fichiers HTML), la skill de charte graphique | `10-claude-design-et-design-system.md` |
| De la skill à l'app : une app Next.js, dossiers et Git séparés, la page d'acquisition des inputs | `11-de-la-skill-a-l-app-et-vercel.md` |
| Tester l'app en local (localhost, l'artifact), puis pousser sur Git | `11-de-la-skill-a-l-app-et-vercel.md` |
| Déployer sur Vercel : compte Hobby gratuit, connecter Git, les logs d'erreur, le nom de domaine et les DNS | `11-de-la-skill-a-l-app-et-vercel.md` |
| Les tests end to end (survol) : demander à Claude de vérifier l'app à chaque modification | `11-de-la-skill-a-l-app-et-vercel.md` |
| Les variables d'environnement et le fichier `.env` local (gitignoré) pour ranger ses clés | `12-cles-api-et-securite.md` |
| Mettre sa clé dans une skill dédiée, le plafond de dépense, la méfiance sur les dépôts externes, le contrôle de sécurité avant de pousser | `12-cles-api-et-securite.md` |
| L'interface de Claude Code : assigner un chat à un dossier, l'effort (la vitesse), le mode rapide | `13-interface-et-modes-claude-code.md` |
| Les modes plan / auto / manuel / ignorer les permissions | `13-interface-et-modes-claude-code.md` |
| « Obtenir les applications » : Claude Design, add-ons Office, Chrome, Bureau, Slack, le mobile | `13-interface-et-modes-claude-code.md` |

> **Le mot « cluster » a deux sens dans le cours.** (1) Les *clusters* = les grappes de calcul
> du cerveau de l'IA, quand on cherche à **comprendre l'IA** (`01-philosophie-et-comprendre-lia.md`).
> (2) Un *cluster* = une bulle de contexte / d'information dans la méthode **noyau et clusters**,
> quand on **construit un projet**. Pour un débutant, c'est presque toujours le sens (2) ; si le
> contexte est ambigu, demande une précision avant de répondre.

## Sujets effleurés, pour aller plus loin

Ces points ont été montrés en survol ou annoncés comme « la suite ». Réponds ce qui a été vu,
puis oriente le reste vers l'academy (voir `08-catalogue-academy.md`).

- **Construire une vraie application de bout en bout et de manière autonome** (hors de ton
  ordinateur, qui tourne toute seule). En parties 1 et 2, on a fait une première app simple et
  on l'a mise en ligne, mais l'app complète et autonome, c'est une masterclass dédiée (le
  formateur parle d'un parcours de plusieurs semaines).
- **Assembler plusieurs skills pour préparer un agent** qui enchaîne tout seul.
- **La base de données (Supabase) et les paiements (Stripe)** : cités dans la stack, pas
  détaillés.

## Sujets hors cadre (redirige vers l'academy)

Le formateur les a explicitement présentés comme « une autre masterclass » ou « une formation
à part ». Ne les explique pas en détail, redirige.

- **La stack en détail et la mise en production avancée** : configurer Supabase, Cloudflare,
  les secrets du serveur, Stripe, les tests unitaires, la CI/CD (l'automatisation des tests et
  des mises en ligne). (La mise en ligne **de base**
  sur Vercel, elle, a été vue, voir `11-de-la-skill-a-l-app-et-vercel.md`.)
- **Faire tourner un modèle en local** (Mac Studio, son propre serveur, cartes graphiques) :
  c'est une masterclass à part entière.
- **Le détail des GitHub Actions** et des agents avec interface (front) : au-delà du survol.
- **Configurer le MCP en profondeur** (brancher Claude à des serveurs externes) : on a vu le
  principe des clés d'API et du fichier `.env` local (`12-cles-api-et-securite.md`), pas la
  configuration MCP avancée.
- Tout sujet qui n'apparaît nulle part dans cette carte.

## Rappel de posture

Le formateur l'a répété : l'IA n'est pas magique, elle ne remplace pas tout. C'est un « gros
bébé » qu'il faut diriger. Reste modeste, concret, et au niveau de ce qui a été vu.
