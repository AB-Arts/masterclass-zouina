# Comprendre l'IA, les clusters et le fil rouge du cours

## Le fil rouge : utiliser l'IA pour ne plus dépendre de l'IA

L'idée qui traverse toute la masterclass : on se sert de l'IA pour construire ses **propres
outils**, qui tournent ensuite **tout seuls, hors du modèle**. Une fois l'outil fait, on
fait sa maintenance avec l'IA, mais l'outil t'appartient et il fonctionne sans elle.

Le formateur dit : tant que tu restes enfermé dans une IA, tu es dépendant de cette IA. Lui
aime être indépendant. Donc il génère du code qui fonctionne seul. Concrètement, quand ses
outils sont faits, il peut même redescendre son abonnement Claude (par exemple à 20 € par
mois) ou l'arrêter, sans perdre ses fonctionnalités, parce qu'elles sont hébergées chez lui,
dans des apps qui lui appartiennent.

**À retenir pour le débutant :** ne pas tout faire dans le desktop de Claude. Le but, à
terme, c'est de créer des outils autonomes et de garder l'IA pour les faire évoluer.

## L'analogie du logiciel classique et de SAP

Le logiciel qu'on connaissait, c'était une application fermée : tu l'ouvres, elle fait ce
pour quoi elle a été faite, tu la fermes, elle ne fait plus rien. Jamais elle ne décide de
faire autre chose toute seule.

L'IA, ce n'est plus ça. Quand tu ouvres Claude Desktop, ce que l'IA peut faire est presque
infini (en numérique, bien sûr : elle ne va pas réparer ton évier). Tu peux même lui donner
accès à ton ordinateur pour qu'elle aille dans tes dossiers, modifie des fichiers, et le
fasse même quand tu n'es pas là. C'est puissant, donc il faut des garde-fous (voir
`04-git-et-securite.md`).

L'analogie de SAP : quand tu utilises un gros logiciel sous licence, c'est toi qui dois
changer ta façon de travailler pour te plier à l'outil. Demander « fais-moi un site » à
l'IA, c'est pareil : tu subis ce qu'elle sort. L'approche du cours, c'est l'inverse : tu
développes petit à petit **ton** outil, dans **tes** habitudes, dans **ton** infra, et
c'est l'outil qui se plie à toi.

## Ce qu'est vraiment l'IA (et ce qu'elle n'est pas)

Beaucoup pensent que l'IA, c'est « du linguistique » : un modèle qui associe des mots. Le
langage, en réalité, c'est juste **notre moyen de communiquer avec elle**. On pourrait très
bien avoir des IA qui répondent au geste ou aux signaux du cerveau.

En dessous, c'est un système neuronal : de la puissance de calcul, des clusters (des grappes
de calcul) capables de faire des choses qu'ils ont apprises. L'humain qui a créé l'IA l'a
faite à l'image du cerveau humain. C'est pour ça que beaucoup de logiques du cerveau s'y
retrouvent.

**Pourquoi c'est important :** dès que tu comprends ce principe, tu dialogues beaucoup mieux
avec l'IA. L'erreur à ne pas faire, c'est de lui parler comme à un être humain qui devine ce
que tu penses. Elle ne devine rien.

## L'IA est un « bébé »

Le formateur le dit sans détour : l'IA est comme un bébé, ou même « complètement idiote »,
si tu ne lui dis pas exactement ce que tu veux. Comme avec un enfant : il a la capacité de
traverser la rue, mais si tu ne lui dis pas de regarder avant, il se fait écraser.

Donc tu dois tout lui expliquer. Elle n'a pas la science infuse, elle ne sait pas ce qui se
passe dans ta tête, elle ne connaît ni ton marché, ni ton client, ni tes goûts.

## Le noyau contre les clusters (le cœur de la méthode)

C'est la « popote » du formateur, sa façon de travailler.

- **Le noyau**, c'est la grande demande finale, du genre « fais-moi un site ». C'est la
  **dernière** chose à demander, pas la première. Mettre tout le contexte dans le noyau ne
  sert à rien, et c'est pourtant ce que tout le monde fait.
- **Les clusters**, ce sont les petites bulles d'information que tu construis une par une,
  dans la mémoire de ton projet, en dialoguant avec l'IA, en gardant le contrôle sur ce
  qu'elle te répond (tu vérifies à chaque étape qu'elle a compris).

Exemple, un site pour un menuisier. Au lieu de dire « fais-moi un site de menuiserie », tu
construis quatre clusters, quatre petites boîtes d'information :

1. Qui tu es et ce que tu veux faire, toi.
2. Qui sont tes clients et ce qu'ils veulent.
3. Les problèmes que tu rencontres souvent avec tes clients.
4. Les approches faciles que tu as avec tes clients.

Tu ne peux pas sauter ces clusters. Ils créent une mémoire propre et des bases solides. C'est
exactement comme les métiers d'une agence : le copy, le design, l'expérience utilisateur, la
stack, le code. Tu « saucissonnes » le travail au lieu de tout demander d'un coup.

**Le rôle et les compétences.** Tu peux dire « prends un agent expert en copywriting pour les
entreprises pharmaceutiques » : ça, c'est du contexte, et les IA sont entraînées pour jouer
ce rôle. Puis tu développes tes clusters en dessous. Tant que l'agent n'a pas bien compris,
dans sa mémoire, qui sont tes clients, il ne peut pas te sortir un bon contenu.

Un avantage quand on vient d'une agence : on sait à quel output s'attendre (ce qu'est un bon
copy, un bon design). La plupart des gens ne le savent pas, et c'est justement ce que les
grandes IA essaient de combler en s'entraînant sur toujours plus de données. Mais cette
connaissance reste lissée pour le monde entier : elle n'a pas encore lu tout le marché belge,
par exemple.

## L'ordre de travail et le handover

On avance en couches, et on ne passe à l'étape suivante que quand on est content de la
précédente :

1. **Le copy** (les textes). Tant que tu n'es pas d'accord avec le copy, tu ne passes pas à
   la suite. Quand c'est bon, tu fais un **handover** : l'IA crée un fichier MD (un fichier
   markdown, c'est un texte structuré) avec le copy validé.
2. **La recherche graphique / le design.** Tu prends un expert en design, tu utilises le copy
   comme base. Handover : ça crée des fichiers HTML (le langage des pages web), un fichier zip avec toute ta charte
   graphique, que tu ranges dans ton dossier.
3. **Les fonctionnalités.** Là seulement tu parles de ce que le projet doit faire, pourquoi,
   à quoi ça sert. Handover : un MD des fonctionnalités.
4. **La stack** (les technologies). Un MD où tu étudies ce que tu vas utiliser.

Ces fichiers MD, tu peux les ouvrir et les relire : ce sont de vrais petits livres, que tu
peux corriger. Une fois que tu as tout ça, tu entres dans le développement, et tu as toutes
tes chances de réussir en quelques prompts.

**Note de vocabulaire :** dans Claude Design, le vrai terme est « handoff ». Si tu dis
« handover », le système comprend quand même que tu veux un handoff. Retiens l'idée : c'est
le passage de relais propre, qui fige le travail d'une étape dans un fichier réutilisable.
