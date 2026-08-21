# De la skill à l'app, et la mise en ligne sur Vercel (partie 2)

C'est l'étape annoncée en partie 1 : une fois que tes skills sont prêtes et fiables, tu peux
en faire une **app**. La partie 2 montre le chemin complet, jusqu'à la mise en ligne.

## Deux règles de rangement à ne jamais oublier

- **Un dossier par projet**, et **un Git par projet**.
- **Ne mélange jamais tes skills et ton app.** Une app a **son propre dossier** et **son
  propre repo Git** (par exemple un repo `zouina-app` en privé). Tes skills restent dans leur
  dossier et leur repo à elles.

## Le chemin, étape par étape

1. **La page d'entrée.** Dans Claude Design, tu fais une petite **page d'acquisition des
   inputs** : le formulaire où on saisit, par exemple, le nom du client et son secteur.
2. **Tu demandes l'app.** Tu dis à Claude Code : « fais une app en **Next.js**, on va la
   pousser sur Vercel ». Next.js est la technologie choisie parce qu'elle convient à un **front public** (la partie visible du site) bien référencé, un **funnel d'acquisition** (le tunnel qui transforme un visiteur en client). Pour une grosse application très
   « applicative », on utilise plutôt React. Tu n'as pas besoin d'entrer dans le détail.
3. **Quelques consignes utiles pour le formulaire** : qu'il soit **responsive** (mobile et
   ordinateur) ; sur iPhone, garder le champ **au-dessus du clavier** ; éviter le zoom dans
   l'app. Au bout, un bouton pour **télécharger le PDF** (qui appelle ta skill).
4. **Tu testes en local d'abord.** Claude Code ouvre une adresse d'essai sur ton propre ordinateur (par exemple
   `localhost:3100`, une page qui n'existe que chez toi) et l'artifact de droite te montre l'app. Ça tourne **en local**, pas
   encore sur internet. Tu remplis le formulaire, tu vérifies que le PDF se génère, tu testes
   le mobile.
5. **Tu vérifies que l'app est bien poussée sur ton Git.**

## Vercel, le service qui met ton app en ligne

**Vercel** est un service de **déploiement** : il rend ton app accessible en ligne via un nom
de domaine.

- **Créer le compte** : inscris-toi avec ton **compte Google** (le même que pour Git), et
  active la **double authentification** (2FA) dans les paramètres de sécurité.
- **Le plan** : reste en **Hobby**, qui est **gratuit** (le plan Pro sert surtout à collaborer
  et à des besoins RGPD plus poussés). Pour toi, c'est gratuit jusqu'à un certain seuil.
- **Connecter ton Git** : tu relies ton compte Git à Vercel, et Vercel voit tous tes repos.

## Déployer, puis mettre à jour

- **Déployer** : dans Vercel, « add new project », tu choisis ton repo, Vercel détecte tout
  seul que c'est du Next.js, tu cliques **Deploy**, et le serveur déploie. Tu obtiens une
  adresse du type `zouina.vercel.app`.
- **Si le déploiement échoue** : il y a un **log** (un journal). Tu copies ce qui est en rouge
  et tu le colles dans Claude. On trouve ces logs partout (Vercel, et aussi Supabase) : dès
  qu'il y a un souci, on va chercher le log et on le donne à Claude.
- **Un nom de domaine à toi** : « add existing domain », et Vercel t'explique quoi copier dans les **DNS** de ton domaine, ses réglages techniques (chez EuroDNS, GoDaddy, etc.). Tu peux aussi utiliser un
  sous-domaine.
- **Pousser une modification** : « commit et pousse en prod » (en production, la version en ligne que voient les gens). Ça crée un nouveau commit, et
  Vercel refait automatiquement un déploiement.

## À savoir aussi

- **La stack complète** d'un projet comme GoodWorker, c'est **Git + Vercel + Supabase +
  Stripe**. En partie 2, on a vu **Git et Vercel** ; **Supabase** (la base de données) et
  **Stripe** (les paiements) n'ont pas été vus en détail (voir `06-agents-stack-exemples.md`
  et la redirection academy).
- **Les tests end to end** (survol) : une fois l'app en ligne, tu peux demander qu'à chaque
  modification, des **tests écrits** vérifient que tout fonctionne, et même que Claude
  **clique** sur le site pour vérifier, comme le ferait un humain.
- **Le bon réflexe quand tu es bloqué** : dis à Claude « je suis débutant, je n'y connais
  rien, explique-moi très simplement ce que je dois faire ». Il t'explique alors avec des mots
  clairs, au lieu de partir dans du jargon.
