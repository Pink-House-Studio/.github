# `.github` — les fichiers de process par défaut de Pink House Studio

Ce dépôt ne contient **aucun code**. Il porte les *default community health files* de
l'organisation : les fichiers que GitHub applique à tous les dépôts qui n'ont pas leur propre
version. Il est public parce que GitHub n'hérite ces fichiers que d'un `.github` public.

## Pas de gabarit de PR par défaut (depuis le 2026-10-18)

Mathieu, le 18-10 : personne ne lit les PR. Un dépôt interne n'a donc aucun gabarit, et une PR
y tient en deux ou trois lignes libres.

Les **dépôts de maintenance client** portent leur propre `.github/pull_request_template.md`,
copié du starter `astro-sanity-brevo-starter` : « Explication client », « Quoi », « Vérifié ».

- **« Explication client » est lue.** Sa phrase entre telle quelle dans le journal du portail
  client (portail.pinkhouse.fr). Vide, la PR n'y entre pas. Le portail cherche l'intitulé exact
  `## Explication client` : le renommer vide le journal du client.
- **La ligne `Demande : XXXMAINT-12`** nomme la demande client que la PR traite, hors de
  « Explication client ». Quand l'aperçu est prêt, phs-mcp passe ce ticket à « Aperçu prêt »
  (phs-vps `docs/phs-mcp.md`).
