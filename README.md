# `.github` — les fichiers de process par défaut de Pink House Studio

Ce dépôt ne contient **aucun code**. Il porte les *default community health files* de
l'organisation : les fichiers que GitHub applique automatiquement à tous les dépôts qui n'ont
pas leur propre version. Aujourd'hui, un seul — le gabarit de pull request.

## Pourquoi il est public alors que tous les autres dépôts sont privés

Ce n'est pas un choix, c'est une contrainte de GitHub : **les gabarits d'issue et de pull
request ne sont hérités que depuis un dépôt `.github` public.** Un `.github` privé n'est pas
supporté pour ces fichiers-là. Le contenu ici est de la prose de process — aucun secret,
aucun nom de client, aucune information d'infrastructure.

L'alternative aurait été de recopier le gabarit dans chaque dépôt : quinze copies que rien
ne compare, et un nouveau dépôt qui naît sans gabarit jusqu'à ce que quelqu'un y pense.

## Ce qu'il contient

| Fichier | Effet |
|---|---|
| `.github/PULL_REQUEST_TEMPLATE.md` | pré-remplit le corps de toute nouvelle PR dans un dépôt de l'org qui n'a pas son propre gabarit |

Un dépôt qui possède son propre `.github/pull_request_template.md` **écrase** celui-ci — c'est
le cas de `phs-vps`, dont le gabarit porte en plus des points propres à l'infrastructure.

## La section « Passe adverse » est lue, pas décorative

Le gabarit pose trois questions : comment ce changement peut échouer sans rien dire, ce qui a
été tenté pour le casser, ce qui n'a **pas** été vérifié. Là où la garde
`pr-adversarial-pass` est branchée (workflow réutilisable dans `ci-workflows`), une réponse
vide fait échouer le check.

⚠️ **Si tu renommes une des trois questions ici, la garde ne la reconnaît plus.** Ça ne passe
pas inaperçu : les PR des dépôts concernés échouent immédiatement sur « intitulé absent de la
section ». Le fragment d'intitulé attendu est défini dans `ci-workflows`, dans
`.github/actions/pr-adversarial/cli.mjs` (`FIELDS`) — change les deux ensemble.
