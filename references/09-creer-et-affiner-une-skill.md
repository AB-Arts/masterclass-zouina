# Créer et affiner une skill, concrètement (partie 2)

La partie 1 a expliqué ce qu'est une skill et la courbe de l'effort. Ici, on passe à la
pratique : comment on en fabrique une vraiment, et comment on la corrige.

## D'abord un cluster, pas tout de suite une skill

Le réflexe à garder : tu ne commences jamais par « fais une skill ». Tu commences par
**créer ton cluster**, c'est-à-dire discuter du travail avec Claude jusqu'à obtenir un
résultat qui te plaît.

Exemple (le cas Flow) : tu vas chez le client, tu l'enregistres (par exemple trois fichiers
audio), tu rentres, tu fais une transcription dans des fichiers MD (de simples fichiers texte, au format Markdown). Tu ouvres un chat dans
Claude Code, tu expliques ton projet : « j'ai un client dans tel secteur, voici mes
enregistrements, je veux au final un document qui ressemble à ça ». À ce moment-là, tu **ne
crées pas encore une skill** : tu débogues, tu montes ton cluster.

Quand le résultat est bon, alors seulement tu dis : « fais une skill de ça ».

## Le déclencheur d'une skill, c'est toi

Une question fréquente : qu'est-ce qui déclenche la création d'une skill ? Réponse : **c'est
toi qui la demandes**. Il n'y a pas de formule magique à connaître. Tu dis simplement « fais
une skill de ça » et c'est parti.

Ce qui compte vraiment, ce n'est pas la formulation, ce sont les **inputs** (les informations que tu fournis). Tu expliques à
Claude : « les inputs que je te donnerai seront le nom du client et les enregistrements, et
tu devras générer le même type de document ». Un bon réflexe : viser **le moins d'inputs
possible pour le plus gros output possible** (le résultat produit). Comme ça, une seule skill couvre une grande
partie du travail que tu ne referas plus à la main.

## Une skill ou plusieurs ? La granularité

Il n'y a pas de règle. Ça dépend de la complexité du projet :

- **Projet simple** (je prends des audios, je les analyse, je sors un PDF) : tu peux tout
  faire dans **une seule** skill.
- **Projet complexe** : mieux vaut **saucissonner** en plusieurs skills (par exemple une skill
  pour le design, une pour le contenu, une pour la stratégie), puis les faire travailler
  ensemble.

Au début tu feras peut-être trop de skills, ou des skills trop grosses. C'est normal. Après
une semaine de pratique, ça devient très intuitif. On fait souvent **une skill par
délivrable** (par « output final »).

Petite parenthèse importante : si tu veux que tes documents respectent **exactement ta charte
graphique**, mets d'abord en place une **skill de design** (voir
`10-claude-design-et-design-system.md`). Elle sera réutilisée pour tous tes PDF.

## Corriger une skill (sans tout casser)

Rappel de la partie 1 : quand quelque chose cloche, tu modifies **la skill**, pas le cluster
(voir `03-skills-et-memoire.md`).

En pratique : imagine que ta skill de design déconne, tu as une marge qui saute ou du texte
coupé en bas de page. Tu fais une capture d'écran, tu l'envoies à Claude et tu dis : « corrige
la skill de design, fais la modification et commit ». Claude corrige la skill, garde la version
corrigée sur ton ordinateur, et sauvegarde cette nouvelle version sur ton Git.

## Le mode plan pour construire ton cluster sans gaspiller

Pour discuter de ton projet avant de le lancer, utilise le **mode plan** : Claude n'édite
rien, il te dit seulement ce qu'il ferait. C'est parfait pour poser ton cluster tranquillement
sans consommer trop de tokens (il ne régénère pas ton document à chaque échange). Quand tu es
d'accord, tu passes en **mode auto** et tu dis « vas-y, fais-le ». Voir
`13-interface-et-modes-claude-code.md`.
