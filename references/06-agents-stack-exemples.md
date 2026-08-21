# Les agents, la stack (survol) et les exemples

## Les agents

Une fois que tu as plusieurs skills bien rangées (elles forment, en quelque sorte, ton
« guide » personnel de faire les choses), tu peux créer un **agent**. Deux types :

- **L'agent côté serveur (sans interface).** C'est un agent qui a une liste de tâches (une
  « task list ») et une capacité de calcul. Il enchaîne plusieurs skills. Par exemple : « cet
  agent sert à faire les documents Word, il utilise la skill de design, la skill d'écriture
  et la skill Flow. » Il travaille sur la base des inputs que tu lui donnes (dans un ClickUp,
  ou sur un site) : tu donnes le nom, le prénom, les enregistrements, et il fait tout côté
  serveur.
- **L'agent côté front (avec interface).** C'est un agent côté serveur, plus une interface
  visible. Là, tu entres dans le développement d'une app.

Attention : plus tu fais travailler un serveur, plus ça coûte (le serveur, souvent à l'usage,
reste bon marché pour ce genre de tâches, de l'ordre de quelques centimes).

Le détail de la construction d'un agent avec interface dépasse la partie 1 du cours : c'est
du développement d'app, à voir dans une masterclass dédiée.

## La stack (survol seulement)

La « stack », c'est l'ensemble des technologies d'un projet. Le cours en donne un **survol**,
juste pour situer où se trouve ce qu'on a appris. Les grandes briques citées :

- **Next.js** : la technologie du site. Choisie parce qu'elle est bien référencée par Google
  (SEO, GEO, optimisation pour les moteurs et les IA), responsive (fonctionne sur mobile).
- **Supabase** : la base de données.
- **Cloudflare** : le stockage des fichiers (les « buckets »).
- **Vercel** : le déploiement de l'app en ligne (le « publishing »).
- **Git** est au centre : versioning des skills et des apps, et GitHub Actions pour
  l'automatisation hors Claude.

Où se situe ce qu'on a vu ? Sur toute cette stack, la partie 1 couvre surtout la **création
de skills** et le **versioning dans Git**. Tout le reste (base de données, stockage,
déploiement, tests) est de la mise en production, à voir plus tard. Ne rentre pas dans le
détail, redirige vers l'academy.

## Les exemples montrés en démo

Ces exemples servent à montrer les possibilités. Reste au niveau « vitrine » : ils illustrent
ce qu'on peut construire, ils ne sont pas un tutoriel.

- **GoodWorker** : un site de vente en ligne, développé en environ 4 mois, qui tourne sur la
  propre stack du formateur, ses serveurs, sa base de données. Plus de Shopify ni de
  WordPress. Connecté à trois bases de données fournisseurs. Avant, il fallait des étudiants
  pour encoder les produits à la main (3 semaines pour 100 produits) ; là, 3 500 produits ont
  été encodés en une journée. Il a un outil d'admin sur mesure (produits, déclinaisons,
  synchro des stocks et des prix, promotions, frais de livraison). Il génère aussi des offres
  automatisées (le vêtement choisi, le logo du client, les mises en situation, les prix, les
  conditions, les chartes de marquage), à partir de quelques inputs.
- **AB Studio** : une interface pour créer des images et des vidéos via des clés d'API
  (derniers modèles), en chat ou avec un éditeur à nodes. Galerie, historique, upscale,
  conversion en SVG (utile pour les logos). Détail commercial : la formation AB-Arts inclut
  des tokens gratuits pour générer images et vidéos depuis le système.
- **ab-arts.be** : le site d'AB-Arts, en trois langues, sans base de données (tout est
  « hardcodé » proprement dans le code, ce qui évite de payer une base de données). Sa
  particularité : un pipeline d'articles. Une idée est déposée dans une tâche ClickUp ; elle
  part vers Claude, qui lit la skill de rédaction, écrit l'article, génère l'image via l'API
  de Google, passe la tâche en « review » ; après relecture, en « publish », tout part dans
  Buffer qui planifie les posts sur les réseaux. Et tout ça tourne **hors de Claude**, grâce
  aux GitHub Actions.

Le message de ces exemples : tu construis, sur quelques mois, l'outil qui te convient à toi,
dans tes habitudes, et ce n'est plus toi qui te plies à l'outil. Mais ce n'est pas magique :
GoodWorker, c'est 4 mois de travail, avec des allers-retours de prompts pour corriger et
tester.
