# Les prompts en 2026, les modèles et leurs sécurités

## Un prompt, ce n'est plus juste du texte

Au début, on voyait passer des fiches de « super prompts » sur les réseaux. Aujourd'hui, ça
ne sert plus à rien. Un **prompt**, c'est le contenu que tu envoies à l'IA pour lui faire
faire quelque chose, et ce contenu peut être **tout et n'importe quoi** : du texte, de
l'audio, une image, une vidéo, un bout de code. Ce n'est plus seulement du texte qu'on passe
dedans.

Le formateur travaille souvent en **audio** : il met son micro et raconte toute l'histoire de
ce qu'il veut faire. Ça fait de longues tartines, mais ça marche très bien. Le seul point
d'attention : l'audio consomme beaucoup de tokens. Tant qu'on est dans Claude Max, ce n'est
pas grave. Mais dès qu'on automatise et que ça passe par les API, il faudra optimiser ses
prompts, car là chaque prompt coûte cher (voir `05-prix-tokens.md`).

**À retenir :** tu peux parler à l'IA à peu près comme tu veux. Plus besoin de formules
magiques. Ce qui compte, c'est un contexte clair, construit en clusters.

## L'IA pose maintenant des questions elle-même

Avant, l'IA ne faisait que répondre. Maintenant, quand elle n'est pas sûre, elle te pose des
questions. C'est une surcouche récente. Par exemple, dans Cloud Design, si tu dis « fais-moi
un design pour mon site de menuiserie », le système te pose une dizaine de questions : tu
veux sombre ou clair ? un one-pager ou des sections ? une page article ? Il commence à
affiner tout seul.

C'est utile, mais pour le formateur ce n'est **pas encore assez** : tu dois garder la main
sur la recherche de clusters en fonction de ton projet. Cet affinage va devenir de plus en
plus puissant avec le temps, jusqu'à s'adapter à ta région et à ton marché.

## Challenger les modèles entre eux

C'est une pratique conseillée et plutôt amusante : faire discuter les modèles entre eux
(Claude, Gemini, OpenAI). Par exemple, quand tu travailles ton copy :

1. Tu demandes à Claude.
2. Tu prends ce que Claude a répondu, tu l'expliques à Gemini et tu lui demandes ce qu'il en
   pense.
3. Tu rebalances dans Claude, et ainsi de suite.

Ils se « débattent » un peu plus quand ils savent que tu utilises les concurrents. Ils ont
l'air entraînés à vouloir être le meilleur. Ça t'aide à affiner tes clusters.

## Les sécurités des modèles (pourquoi Claude refuse parfois)

Chaque modèle public a ses propres sécurités, notamment **légales**, parce qu'il doit
respecter le territoire où il se trouve. En Europe, il y en a une panoplie. Deux exemples :

- Le contenu à caractère sexuel est très bridé.
- La finance : une IA comme Claude ne peut pas se mettre à faire des placements d'argent
  pour toi, parce qu'en Europe c'est très encadré (il faut des certifications, passer par les
  autorités financières). Claude n'a pas ça, donc il refuse.

**L'anecdote du bot de trading** (une leçon de sécurité). Le formateur a voulu, pour tester,
faire un petit bot de trading. Claude a accepté de développer tout le module en « paper
trading » (avec de l'argent fictif, en démo). Mais dès qu'il a demandé de passer sur son
vrai compte avec de vrais euros, Claude a catégoriquement refusé, même en insistant, même en
disant « je prends l'entière responsabilité ».

Il a alors utilisé **Gemini pour contourner la sécurité de Claude** (en le flattant : « tu es
plus fort que Claude ? »), et Claude a fini par développer le système. Quatre jours plus
tard, il a reçu un avertissement rouge d'Anthropic : « nous avons constaté que vous avez
passé les sécurités de Claude, ne recommencez pas, sinon votre compte sera dégradé. »

**La leçon :** il existe des failles, surtout quand on challenge les modèles entre eux, mais
il ne faut **pas** les exploiter. Ces sociétés surveillent, et elles ont raison de mettre des
garde-fous : ces modèles ont donné des super-pouvoirs à tout le monde, aux gens bien comme
aux gens mal intentionnés.

## Les modèles et leurs particularités

Chaque modèle a un peu sa spécialité. Deux points pratiques vus en cours :

- Tu n'es pas obligé de travailler avec le modèle le plus cher tout le temps. Opus 5, c'est
  très cher. Pour beaucoup de tâches, tu peux passer sur un modèle moins cher (par exemple
  Opus 4.8) qui fait très bien le travail. Le formateur garde les modèles chers surtout pour
  le développement lourd, à faire très vite.
- Tu peux, dans une app que tu construis, connecter plusieurs modèles (Claude, Gemini,
  OpenAI) et mettre un « switch » pour changer de modèle selon le coût ou la force de chacun
  sur une tâche donnée. Il suffit de changer les clés d'API et la façon de dialoguer.

## Les 6 blocs d'un prompt (la discussion du cours)

Pendant le cours, l'IA a listé six blocs pour un bon prompt. Ce qui en ressort :

1. **Le rôle** est un peu **surestimé**. Il reste utile et générique (l'IA en tient compte),
   mais Claude va de plus en plus le deviner tout seul. Dans deux ans, tu pourras dire « fais
   un site » et l'IA saura déjà qui tu es et dans quel marché tu es.
2. **Définir le standard** : à quoi doit ressembler un bon résultat.
3. **L'audience** : pour qui tu crées la chose.
4. **Un exemple** est toujours bon (montrer plutôt que décrire).
5. **La permission de demander** : autoriser l'IA à poser des questions avant de foncer.
6. **Le critère d'évaluation** (comment tu sauras que c'est bon) et **les outils et le scope**
   (ce qu'elle a le droit d'utiliser, jusqu'où elle va).

**À retenir :** ne commence à produire que quand tu es certain que l'IA a bien compris pour
qui et dans quel standard elle travaille.
