# Claude Design et le design system (partie 2)

## À quoi sert Claude Design

**Claude Design** est l'outil pour faire du **design** : construire un design system (ta charte
graphique en pratique) et passer d'un texte à une **maquette**. C'est un travail en amont qui
te sert ensuite partout.

Deux choses à retenir :

- **Ça prend du temps.** Tu envoies ta demande, tu passes à autre chose, et tu reviens plus
  tard voir le résultat (parfois envoyé le matin, relu l'après-midi). Il faut être patient.
- **Tu peux éditer à la main.** Dans Claude Design, tu peux cliquer et modifier toi-même les
  éléments (changer la tête d'un bouton, par exemple). C'est ce que tu ne peux pas faire dans
  Claude Code. En gros, ça remplace un outil comme Figma.

Attention : Claude Design fait du **design et du vectoriel** (des dessins nets qui ne pixelisent pas quand on les agrandit), pas des **photos**. Pour générer
des images, il faut une clé d'API (voir `12-cles-api-et-securite.md`).

## Choisir le modèle dans Claude Design

Comme ailleurs, tu choisis ton modèle. Le réflexe du cours : Fable est souvent trop cher pour
rien, Opus suffit très bien, et tu peux même descendre sur un Opus 4.7 ou 4.8 (moins cher, et
ça fait aussi bien le travail). Tu montes en gamme seulement si la qualité n'y est pas. Pour
les prix, voir `05-prix-tokens.md`.

## Le déroulé : de la demande au handoff

1. **Tu envoies une demande simple.** Par exemple : « fais un design system complet pour PDF
   verticaux et horizontaux, avec couverture (cover), pied de page (footer) et bouton d'action (call to action) ; analyse le site et dirige
   vers le contact si besoin ». Tu ne réfléchis pas trop : les informations qui manquent,
   Claude Design te les demandera.
2. **Il te pose ses questions.** Langue des documents, types de documents en priorité, à qui
   ils s'adressent, contenu réel ou gabarit ou un mix, points de contact (site, LinkedIn,
   WhatsApp), éléments de charte à inclure. Il s'appuie sur ce qu'il trouve sur ton site.
3. **Il travaille**, puis tu fais un **handoff** : Claude Design te prépare un fichier **ZIP**
   avec des fichiers **HTML** (le langage des pages web) qui contiennent toute ta charte.
4. **Tu ranges le handoff.** Tu dézippes, et tu mets le dossier dans un dossier de design de
   ton dossier de travail (par exemple un dossier `.design`). Ensuite tu donnes ce lien à
   Claude Code.

C'est ce handoff qui te permet de créer une **skill de design** réutilisable : de là, tous tes
documents auront la même tête. Tu peux faire un handoff **par livrable** (un pour le site, un
pour le catalogue), c'est plus simple à réutiliser ensuite.

## L'exemple GoodWorker (pour situer la puissance)

Le formateur a montré, dans Claude Design, tout le design de son site GoodWorker : la page
d'accueil, les pages boutique et produits, le tableau de bord d'administration, la version
mobile (avec du vrai contenu tiré de sa base de données). À partir de ce design system, il a
généré un **catalogue papier d'environ 650 pages**, avec ses milliers de produits, un sommaire,
et un QR code par produit qui renvoie vers le site. Ce travail, qui prenait des semaines à la main, s'est fait d'un coup. Les images du catalogue ont été générées via une clé
d'API (Gemini).

Reste au niveau « vitrine » : cet exemple montre ce qui est possible, ce n'est pas un tutoriel.
