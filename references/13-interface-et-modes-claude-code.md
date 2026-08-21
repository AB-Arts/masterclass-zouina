# L'interface de Claude Code : dossiers, modes et applications (partie 2)

Une petite visite guidée de l'outil, pour t'y retrouver.

## Où on travaille

On travaille dans le **chat de Claude Code**. Le formateur reste dans le chat normal pour les
corrections de bugs : il existe aussi une version console (en ligne de commande), mais elle est
plus indigeste pour un débutant. Le chat suffit très bien.

## Assigner un chat à un dossier

Chaque chat peut être rattaché à un **dossier** de ton ordinateur. Tu fais « new » (nouveau
chat), et **juste en dessous** tu choisis le dossier de travail. À partir de là, tout ce qui se
passe dans ce chat concerne ce dossier. Tu peux ajouter plusieurs dossiers.

Attention : un **nouveau chat repart d'un contexte vide**. Il ne sait plus ce que tu faisais
avant. Avant de committer, revérifie donc que tu es dans le bon projet. Bonne nouvelle : Claude
est assez malin pour te prévenir s'il s'apprête à committer sur un repo qui ne correspond pas
au code.

## Les réglages en bas du chat

- **La fenêtre de contexte** (en bas à droite) montre les tokens utilisés (voir
  `05-prix-tokens.md`).
- **L'effort de Claude**, c'est sa **vitesse**, pas son intelligence : il fait la même chose,
  plus vite ou moins vite. Le **mode rapide** travaille plus vite mais consomme plus de tokens
  (souvent le double). À ne pas activer à la légère.
- **Les modèles** : tu choisis lequel utiliser (voir `02-prompts-et-modeles.md`).
- **Le micro** pour lui parler, le **« + »** pour ajouter des photos ou des dossiers.
- **Les commandes slash** (« / ») : ce sont **toutes tes skills** à disposition, plus celles
  déjà fournies dans Claude.

## Les modes de travail (très utile)

- **Mode plan** : Claude n'édite rien et ne touche pas à ton ordinateur, il te dit seulement ce
  qu'il **ferait**. Idéal pour discuter et construire ton cluster sans gaspiller de tokens
  (voir `09-creer-et-affiner-une-skill.md`).
- **Mode auto** : il agit tout seul et applique les modifications.
- **Mode manuel** : il te demande d'accepter (ou de faire toi-même) chaque étape.
- **Ignorer les permissions** : plus aucune validation, il fait tout sans demander. C'est le
  contrôle total, à **éviter** tant que tu débutes.

## « Obtenir les applications » (les add-ons)

Dans le menu, tu peux ajouter des applications qui étendent Claude :

- **Claude Design** (voir `10-claude-design-et-design-system.md`).
- Des **add-ons pour la suite Microsoft** : Excel, Word, PowerPoint.
- Un **add-on Chrome** : tu donnes à Claude l'accès à ton navigateur.
- Le **Bureau** : Claude a accès à ton ordinateur comme si c'était toi.
- **Claude Code** en application de bureau (terminal, VS Code).
- Des intégrations comme **Slack**.
- Sur **mobile** : piloter ton Claude de bureau depuis ton téléphone (ton ordinateur reste
  allumé à la maison, et tu envoies des demandes depuis le mobile). Pratique, mais vite
  addictif.

Tu as aussi, dans le menu, le bouton pour **signaler un bug**.
