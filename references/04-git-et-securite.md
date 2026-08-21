# Git, GitHub et la sécurité des clés d'API

## Git, c'est du stockage de versions

**Git / GitHub** est essentiel dans cet écosystème. C'est un système de **stockage de
versions** (des sauvegardes horodatées, des « snapshots »), **pas** un lecteur en temps réel.

Le principe :

- Ta skill (ou ton code) reste toujours **sur ton ordinateur**. C'est la version que tu
  utilises, la version « en prod ».
- Dès que Claude fait une modification sur ton ordinateur, il en fait une **copie de
  sauvegarde sur Git**.
- Sur Git, tu as **toutes** les versions dans le temps ; sur ton ordinateur, juste la version
  actuelle.

Le vocabulaire :

- Un **repo** (repository) : un dossier de sauvegarde d'un projet, avec ses versions. Tu crées
  un repo par projet.
- Un **commit** : une version sauvegardée. Quand un développeur dit « tu as commité sur le
  repo ? », il parle de ça.
- Le gros avantage : tu peux **revenir en arrière** (rollback). Si une version de skill a
  merdé, tu dis à Claude « reprends ce commit-là » et il remet cette version sur ton
  ordinateur, **sans supprimer les autres**.
- Les **branches** (branch) et les **forks** : tu peux repartir d'une version pour faire
  autre chose dans une branche séparée (par exemple une branche « Zoina », ou une branche
  « Gemini » où Gemini retravaille ta skill à sa façon), puis décider de la fusionner
  (merge) avec la branche principale ou de la garder à part.

## Toujours en privé

Tu crées tes repos **toujours en privé**. Tu ne mets un repo en **public** que si tu décides
vraiment de partager quelque chose avec le monde entier, car public = accessible par tout le
monde.

## La connexion CLI (relier Git et Claude)

Claude se connecte à Git via un **CLI** : c'est un tunnel de connexion entre Git et Claude.
C'est facile à mettre en place. La bonne pratique : crée ton repo **toi-même**, à la main,
dans GitHub, puis donne son lien à Claude (« on va travailler dans ce Git là, pour ce
dossier »). Si tu laisses Claude créer le repo tout seul, ça devient vite le bazar.

Quand tu dis à Claude « va dans ce Git », il répond souvent « je ne sais pas y aller,
veux-tu que je configure un CLI ? ». Tu dis oui, il ouvre la fenêtre GitHub où tu
t'authentifies (connexion recommandée en SSO Google), et c'est fait. Ensuite, dis-lui de
faire un commit à chaque modification (« yes, and every time »).

Une fois connecté, tout devient limpide pour Claude, même si ça paraît touffu pour un
débutant. Et comme GitHub est mainstream, tu peux y connecter Claude, Gemini et OpenAI en
même temps, chacun sur sa branche.

## La règle numéro un : les clés d'API

Une **clé d'API**, c'est une clé qui permet à une application de communiquer avec une autre
application. Par exemple, une clé qui laisse ton code utiliser Gemini pour générer des
images.

La règle absolue, répétée plusieurs fois pendant le cours :

- **JAMAIS** de clé d'API dans le **chat de Claude**.
- **JAMAIS** de clé d'API dans un **repo Git**, même privé.
- **JAMAIS** de clé d'API dans une **skill** ou dans le **code**.

Où vont les clés ? Uniquement **sur ton ordinateur** (et, si tu veux, sur un drive sécurisé
ou un disque dur externe chez toi). En production, en ligne, tu remplis tes clés dans les
**« secrets »** du serveur.

## Le fichier .gitignore

Le fichier **`.gitignore`** dit ce qui **ne doit pas** partir dans Git. Tu peux garder, dans
ton dossier de travail, un fichier avec tes clés d'API : si tu l'inscris dans le
`.gitignore`, il ne sera **pas** envoyé dans Git.

Et Claude le sait : il peut lire et écrire des clés d'API en local, mais tout ce qu'il lit
en local dans un fichier, il ne l'intègre **pas** à sa mémoire publique et ne l'envoie pas
dans le cloud. Il le garde en local, puis il l'oublie. Tes clés ne partent donc ni sur le
cloud, ni dans Git.

## Pourquoi c'est si important (les dégâts d'une fuite)

- Une clé d'API volée donne accès au **produit** que tu utilises, pas à ta machine. Exemple :
  une clé de génération d'images volée peut te faire cramer 10 000 € de tokens en une journée.
- Une clé ClickUp volée : quelqu'un peut mettre le bazar, tout effacer ou injecter des données.
- Protection simple : mettre un **plafond de dépense** chez le fournisseur (par exemple 40 €
  par mois chez Google). Même si une clé fuit, la personne ne pourra pas dépenser plus que ce
  plafond.

Petit rappel de bon sens sur la sécurité en général : nos données se font pomper (bases de
données pas à jour, hameçonnage). Reste vigilant, ne clique pas sur les liens douteux, et
protège tes clés comme des mots de passe.

## GitHub Actions : faire tourner une automatisation hors de Claude

GitHub ne sert pas qu'à stocker. Il offre aussi des **Actions** : un serveur qui fait des
choses pour toi en ligne. C'est ce qui te permet de dire : « ma skill fonctionne, mais je ne
veux plus avoir à l'appeler depuis le chat de Claude. Je veux qu'elle se fasse toute seule
tous les jours à 10 h, que mon ordinateur soit allumé ou éteint. »

Pour ça, il faut un serveur externe. C'est comme ça que le formateur fait tourner, par
exemple, son pipeline éditorial (publier des articles sur les réseaux) **hors de Claude**,
grâce aux GitHub Actions.

Le détail de la mise en place des Actions (et des agents avec interface) dépasse la partie 1
du cours : c'est de la mise en production, à voir dans une masterclass dédiée.
