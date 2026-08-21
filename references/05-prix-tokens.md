# Le prix des tokens et des modèles

Attention : les prix bougent vite. Ce sont les ordres de grandeur donnés pendant le cours
(2026), à vérifier au moment où tu en as besoin. Ce qui ne change pas, c'est la **logique**.

## Ce qu'est un token, en un mot

Un token est un petit fragment de texte (environ les trois quarts d'un mot). Tu paies ce que
le modèle lit et ce qu'il écrit. Plus tes prompts sont longs (surtout en audio), plus ça
consomme.

## Les abonnements Claude

- **Gratuit** : tu ne sais quasiment rien faire de sérieux. Tu peux chatter, c'est tout.
- **20 € par mois** : tu fais quelques trucs, mais après une demi-heure tu es bloqué et tu
  dois attendre environ 3 h que ça se relance. En gros, tu tapes cinq prompts, dix minutes,
  et c'est fini.
- **90 € par mois (le plan Max 5x)** : tu sais déjà faire du développement lourd. Mais sur un
  gros projet (comme le site GoodWorker), tu vas cramer tes heures vite (par exemple 4 h de
  quota en 2 h) et devoir attendre la recharge.
- **200 € par mois (le plan Max 20x)** : le formateur, avec tout ce qu'il envoie, n'a jamais
  réussi à le faire bloquer.

## Le desktop contre l'API : le vrai piège de prix

Dans le desktop de Claude, pour chaque token dépensé, **Claude t'en offre quatre**. Donc si
tu fais exactement la même action via l'**API** (au lieu du desktop), tu paies **cinq fois**
le prix.

- Sur l'abonnement à 90 € (Max 5x), tu paies environ **1/5** du prix du token.
- Sur l'abonnement à 200 € (Max 20x), tu paies environ **1/20** du prix du token.

Autrement dit : plus ton plan est costaud, plus le desktop absorbe de tokens pour toi ;
l'API, elle, reste au **plein tarif**.

C'est voulu : l'abonnement te pousse à **créer** (généreux dans le desktop, dans Claude Chat,
dans Claude Code). Mais dès que tu **automatises** et que ça passe par l'API, hors de Claude,
tu paies **plein pot**. Ces sociétés savent très bien que si tu crées à moindre frais, tu
finiras par vouloir sortir tes outils pour ne plus payer l'abonnement. C'est tout le fil
rouge du cours : construire des outils autonomes.

## Un exemple concret de coût (un article publié)

Pour un article publié automatiquement, avec les API, hors chat :

- Le texte via l'API de Claude : environ **2 €**.
- Cinq images via l'API de Google : environ **0,50 €**.
- Une vidéo de 10 secondes (par exemple Seedance) : environ **5 €**.

Total : autour de **7 à 8 €** pour l'article complet.

C'est la réalité que peu de gens connaissent, parce que la plupart restent dans un chat à
20 € par mois et deviennent de plus en plus dépendants de cet écosystème.

## Choisir le bon modèle

Chaque modèle a sa particularité. Deux réflexes du cours :

- Tu n'es pas obligé de rester sur le modèle le plus cher. Opus 5 est très cher ; pour
  beaucoup de tâches, un modèle moins cher (par exemple Opus 4.8) fait très bien le travail.
  Garde les modèles chers pour le développement lourd à faire vite.
- Dans une app, tu peux connecter plusieurs modèles (Claude, Gemini, OpenAI) et basculer de
  l'un à l'autre selon le coût ou la force de chacun.

## Les fournisseurs d'API évoluent aussi

Attention, les fournisseurs changent leurs formules. Google, par exemple, est passé d'un plan
gratuit à un plan « à l'usage » (tu paies ce que tu consommes), puis vers des plans mensuels
et annuels. C'est un marché qui bouge, garde un œil dessus et mets toujours un plafond de
dépense (voir `04-git-et-securite.md`).
