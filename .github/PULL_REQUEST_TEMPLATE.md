<!--
Gabarit court à dessein : un gabarit long se fait supprimer, et un gabarit supprimé ne
prouve rien. Efface ces commentaires, garde les titres.

⚠️ La section « Passe adverse » est LUE par la garde `pr-adversarial-pass` là où elle est
branchée : elle échoue si la section est absente, si la case n'est pas cochée, ou si l'une
des trois questions est laissée vide. Les PR de Dependabot en sont exemptées, et les
brouillons attendent d'être marqués « prêt pour relecture ».
-->

## Explication client

<!-- Dépôt d'un site client seulement ; ailleurs, efface cette section.
     Une ou deux phrases pour le client, vouvoiement, sans jargon : ce qui change pour lui
     ou pour ses visiteurs. Ex. « La page Contact affiche désormais vos horaires d'été. »
     Le portail client (portail.pinkhouse.fr) la reprend telle quelle dans son journal.
     Laissée vide, la PR n'y entre pas : c'est le bon choix pour un changement invisible. -->

## Ce que ça change, et pourquoi

<!-- Le problème d'abord, le correctif ensuite. Si le problème tient en une ligne, une
     ligne suffit. Lien vers le ticket ou l'issue, s'il y en a un. -->

## Mesuré

<!-- Ce qui a RÉELLEMENT tourné, avec sa sortie — pas « testé », mais la commande, la page
     ouverte, le résultat. Si rien n'a pu être exécuté, écris-le ici : c'est une
     information, pas une faute. -->

## Passe adverse

<!--
Cocher une case ne prouve rien. Ce qui coûte cher sur cette flotte, ce n'est pas une panne,
c'est une panne QUI NE DIT RIEN : un script sorti 0 sans avoir rien fait, une garde qui
compare zéro fichier et affiche « aucune dérive », un déploiement accepté puis échoué en
silence. Alors écris ce que tu as réellement cherché — les trois réponses sont lues.
-->

- [ ] J'ai cherché à faire mentir mon propre changement.

**Comment ça peut échouer sans rien dire**

<!-- Le faux vert de CE changement. Quelle sortie 0, quel écran vert, quelle page qui
     s'affiche quand même pourrait ici recouvrir une vraie panne ? Si tu penses qu'il n'y
     en a pas, écris pourquoi — « rien à signaler » n'est pas une réponse. -->

**Ce que j'ai tenté pour le casser, et ce que ça a donné**

<!-- Des cas limites réellement exercés : contenu absent, liste vide, image manquante,
     champ CMS non rempli, deuxième passage, réseau lent, mobile, secret manquant. -->

**Ce que je n'ai pas vérifié**

<!-- La partie la plus utile de la section. Ce qui reste supposé, et ce qu'il faudrait
     pour le lever. -->

## Portée et retour arrière

<!-- Qu'est-ce qui bouge, chez le client, au moment de la fusion — et comment on revient en
     arrière ? « Rien, c'est de la doc » est une réponse complète.

     Coche ce qui s'applique, ignore le reste :
     - [ ] fusionner ce dépôt redéploie le site live
     - [ ] le contenu vient du CMS → vérifié avec du contenu RÉEL, pas les mocks
     - [ ] Lighthouse / Playwright relus dans la CI, pas seulement « vert »
     - [ ] aucun secret n'est mis en scène (`git diff --cached`) -->
