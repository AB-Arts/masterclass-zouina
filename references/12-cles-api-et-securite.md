# Les clés d'API et les variables d'environnement (partie 2)

C'est la partie qui « pique » un peu, mais c'est la plus importante pour ta sécurité. Elle
prolonge la règle numéro un de la partie 1 (voir `04-git-et-securite.md`).

## Le rappel de base

Une **clé d'API** laisse une application communiquer avec une autre (par exemple, ton code qui
utilise Gemini pour générer des images). La règle absolue reste la même :

- **JAMAIS** de clé d'API dans le **chat de Claude**.
- **JAMAIS** dans un **repo Git**, ni dans le **code**, ni dans une **skill** partagée.

D'ailleurs, Claude t'empêche de coller une clé directement dans le chat.

## Où vont les clés : les variables d'environnement

Dans les outils de développement et d'hébergement (ton projet, Vercel, Supabase, les réglages sécurisés de GitHub...), il existe un endroit
prévu pour les **variables d'environnement**. Ce sont les informations sensibles (comme tes clés d'API) qui ne doivent jamais être partagées. C'est la **zone de haute sécurité** : le
programme va y chercher ses clés de manière **chiffrée** (codée, illisible pour quelqu'un d'autre), sans jamais les diffuser au public.

Concrètement, sur ton ordinateur, ça prend la forme d'un **fichier local** (souvent nommé
`.env`) rangé dans le dossier de ta skill ou de ton app. Ce fichier est mis en **`.gitignore`**
(voir `04-git-et-securite.md`) : il reste chez toi et ne part pas dans Git. Pour y coller ta
clé, tu ouvres ce fichier avec un **éditeur de code** (comme VS Code), tu colles, tu sauves.

## La méthode simple vue en cours : une skill dédiée

Plutôt que de bricoler une configuration globale de Claude (ça peut vite coincer, surtout sur
Mac), la méthode montrée est plus propre : on crée une **skill dédiée** (par exemple une skill
« générateur d'images ») avec **son propre fichier `.env` local** pour la clé. La clé reste sur
ton ordinateur, et c'est la skill qui s'en sert quand tu l'appelles.

Pour récupérer une clé Gemini : Google AI Studio, connexion avec ton compte Google, tu ajoutes
une carte de paiement, puis tu copies la clé (bouton copier).

Bon à savoir : Claude ne génère des images **que** s'il a accès à une clé (Gemini, par exemple).
Sans la clé, pas d'images. Et rappel : Claude Design fait du design, pas des photos.

## Se protéger pour de vrai

- **Le plafond de dépense.** Si ta clé fuit et que tu as activé un **rechargement automatique**
  (auto top-up), un robot peut vider ton compte. Mets toujours un **plafond** chez le
  fournisseur (voir `04-git-et-securite.md`). Certains outils (Google, Cloudflare) permettent
  même de **limiter une clé à un seul domaine**.
- **Méfiance sur les dépôts externes.** Si, pour brancher une clé, Claude propose d'installer
  un **dépôt externe** inconnu, c'est un signal de prudence. Demande-lui plutôt de développer
  la skill à partir de zéro.
- **Le contrôle de sécurité avant de pousser.** Avant d'envoyer sur Git, Claude fait un
  contrôle : il vérifie qu'aucune clé n'apparaît dans les fichiers suivis et met bien le
  fichier de clés en `.gitignore`. Il fait de plus en plus attention à ça.

## Une histoire pour retenir la leçon

Le formateur a raconté qu'une grande enseigne (il citait McDonald's) avait ouvert une interface
d'IA sur son chat. Elle était tellement ouverte que des gens s'en servaient pour générer leurs
propres contenus... avec la clé de l'enseigne, jusqu'à ce qu'elle soit bloquée. La morale
rejoint l'anecdote du bot de trading (voir `02-prompts-et-modeles.md`) : une clé laissée
ouverte, c'est tout le monde qui dépense à ta place.

Enfin, côté pratique : le studio du formateur (AB Studio) offre des **tokens gratuits** pour
générer des images et des vidéos, inclus avec la formation (voir `06-agents-stack-exemples.md`).
