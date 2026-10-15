# Nouveautés de kiln

Une entrée par version, la plus récente en tête : `## vN — date`, puis une ligne par
changement visible (`- …`). `kiln update` montre les entrées des versions qu'un projet passe ;
la skill `base:version` rédige celle de la version qu'elle sort, sur la branche `release/vN`.

## v1 — 2026-10-15
- Première version publiée : `main` ne reçoit plus que des versions, les projets se mettent à jour d'une version à l'autre et ce journal en montre les nouveautés à chaque `kiln update`.
- `kiln status` dit de quelle version part chaque repo (`f611f82 → v1`), le hook de début de session propose l'outil puis le repo quand une version sort.
- Nouvelle interface : four rieur en bannière, écran d'accueil par sections, roue animée et durée pour chaque commande externe, bilan encadré des étapes ; aucune couleur hors terminal, `KILN_VERBOSE=1` pour la sortie complète.
- `kiln doctor` : diagnostic du poste et du repo, chaque problème avec la commande qui le corrige.
- `kiln dev` : sorties des serveurs entrelacées, préfixées par service en couleur.
- `kiln update --all` fusionne directement chaque repo dont les contrôles passent, sans PR.
- Backend Java (Maven), skill `maj-kiln`, lien `.claude/kiln` vers le plugin, réglages du poste par `kiln set`.
- Les workflows et actions réutilisables se citent `@main` : les projets à jour n'utilisent plus `develop`.
