# Les skills, la courbe de l'effort et la mémoire

## Ce qu'est une skill

Une **skill**, c'est un cluster plus la capacité, entraînée par toi, d'un modèle à répondre
parfaitement à un type de cluster. Dit autrement : c'est un mode d'emploi réutilisable pour
une tâche précise que tu fais souvent.

Exemple : tu dois faire dix sites par an pour des indépendants du même genre (menuisier et
similaires). Si tu redemandes à chaque fois, l'IA te refait plus ou moins le même site sans
affiner. À la place, une fois que tu as réussi un site parfait, avec un cluster de copy
vraiment comme tu le veux, tu en fais une skill : « on va faire une skill de ce truc que
j'aime bien, tu as vu tout le déroulé, mes questions, là où tu t'es trompé, là où je t'ai
corrigé. » Cette skill va te faire diminuer ton temps de travail sur les projets suivants.

## Le cycle : cluster → MD → skill → outil

Le formateur travaille en couches :

1. **Le cluster.** Tu discutes, tu affines, tu obtiens un résultat dont tu es content. Ça
   donne un fichier MD (markdown, un texte structuré).
2. **La skill.** De ce cluster validé, tu fais une skill : un outil qui te permet de répéter
   la tâche.
3. **L'affinage de la skill.** Si, après deux ou trois jours, tu remarques que ça ne va pas
   (les gens ne comprennent pas, il faut simplifier le contexte), tu ne modifies **plus le
   cluster**, tu modifies **la skill**. Et cette correction s'appliquera à tous tes futurs
   projets. Tu édites la skill (par exemple « création copy site ») et tu corriges.
4. **L'outil / l'app.** À partir du moment où tu as utilisé ta skill deux ou trois fois pour
   d'autres clients, que ça marche super bien et qu'elle ne te prend plus que deux minutes,
   tu peux en faire un outil pour ton site (une app). Cette dernière étape dépasse la partie 1
   du cours (voir la redirection academy).

## La courbe de l'effort

C'est le schéma clé de cette partie. Il montre pourquoi une skill « rapporte » :

- **Au début**, tu passes beaucoup de temps à mettre en place ton contexte et tes clusters.
  Beaucoup de clients disent « ça m'a pris plus de temps de le faire en IA que de le faire
  moi-même ». C'est normal : au début, tu parlais à un bébé, tu devais tout peaufiner.
- **Ensuite**, tu bascules ton temps en skills : tu passes de moins en moins de temps, parce
  que ta skill se termine et s'affine.
- **À la fin**, tu prends encore un peu de temps pour en faire une app ou une automatisation,
  puis ça tourne sur tes serveurs et tu n'as plus qu'à donner tes cinq ou six inputs (les infos que tu fournis).

Ce que tu faisais en une demi-journée, tu finis par le taper, et c'est fait.

## Exemple concret : le rapport (méthode Grow / Flow)

Le client a préparé, sur trois jours, un questionnaire pour interviewer des cliniques
esthétiques, et il veut en extraire un rapport. Sa méthode, très fragmentée :

- Il a d'abord fait « mapper » le projet : quelles étapes pour arriver à un rapport de ce
  type ?
- Il a défini des **quality checks** (des points de contrôle qualité) intermédiaires et des **prompts intermédiaires** : quand
  une étape est validée, on passe à la suivante.
- Chaque étape produit des fichiers MD, puis on consolide tout dans un rapport final.
- Détail utile : dans une interview, pour le rapport, on ne garde que le contenu de la
  personne interviewée, pas celui de l'intervieweur, sinon le poids du contenu est faussé.

Ce qu'il n'a pas encore fait : en faire une **skill**. Le principe pour y arriver : prendre
le **rapport final comme point zéro**, le modèle idéal. Puis dire à l'IA quelque chose comme :
« ce qu'on a livré ici est exactement ce que je veux pour ce client. Maintenant, mets en
place une skill : prends 100 % des paramètres et des retours qui ont mené à cet output, mais
pour un autre client. Les inputs que je te donnerai seront le nom du client et les
enregistrements / transcriptions, et tu devras générer le même type de document. »

Ensuite, tu appelles ta skill, tu mets tes inputs, et tu regardes ce que ça donne.

## Garder le contexte, sinon tu perds tout

Point crucial : ne pas perdre la mémoire de ce que tu fais.

- Les chats sont stockés dans la **mémoire de Claude** (dans le répertoire racine de Claude).
  Si tu supprimes un chat, tu perds **tout le contexte**. Tu ne gardes que les fichiers MD de
  résultat, mais tu perds le déroulé et le sens.
- Claude **supprime tout seul la mémoire au bout de 30 jours** (la mémoire des 30 jours
  d'avant). Selon le plan, l'historique peut remonter plus loin, mais ne compte pas dessus.
- Donc tu dois **faire une sauvegarde** (un backup). À la fin d'un chat, tu demandes un **handover** : un fichier qui
  récapitule tout ce qui a été bon dans le chat, le contexte et l'output final, rangé dans
  ton dossier. Dans un même projet, Claude peut faire un handover de plusieurs chats.

## Travailler en mode Code

Pour ce genre de travail, le formateur travaille **toujours en mode Code**. Pourquoi ? Parce
qu'en mode Code tu peux **assigner un dossier**, et tout se passe dans ce dossier. Tu y
retrouves l'historique du chat, tu y fais tes handovers, tu y ranges tes skills. C'est plus
propre et tu ne perds rien.

Tu peux aussi exporter la mémoire de Claude depuis les paramètres (section mémoire).

## Et les artifacts ?

Un **artifact**, ce sont tout simplement les fenêtres qui s'ouvrent à droite : l'aperçu d'un
site, ou ce que tu es en train de développer, visible en local. C'est l'**output visuel**.
