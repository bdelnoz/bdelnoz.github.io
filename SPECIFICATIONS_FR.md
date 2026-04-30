<!--
Document : SPECIFICATIONS_FR.md
Author : Bruno DELNOZ
Email : bruno.delnoz@protonmail.com
Version : v1.0.0
Date : 2026-04-30 00:00 UTC
-->

# Objectif
Reconstruire `index.new.md` comme page portfolio professionnelle complète, en conservant le style et la structure de `index.md` tout en actualisant la section GitHub.

# Portée
- Créer `index.new.md` en anglais.
- Conserver `index.md` inchangé.
- Conserver les fichiers protégés inchangés.
- Inclure individuellement tous les dépôts fournis par l'utilisateur avec une catégorisation professionnelle.

# Comportement existant vérifié
- `index.md` suit un format CV/portfolio avec en-tête, badges, tableaux catégorisés et sections longues d’expertise.
- Aucun fichier de spécifications n’existait avant cette tâche.

# Exigences fonctionnelles
- `index.new.md` doit conserver le front matter Jekyll et la structure de profil.
- La section GitHub doit être entièrement reconstruite et catégorisée.
- Tous les dépôts de l’inventaire fourni doivent être représentés individuellement.
- Les forks doivent être marqués explicitement.
- Les projets privés doivent être listés sans exposer d’URL privée ni contenu sensible.

# Exigences non fonctionnelles
- Rédaction professionnelle et non générique.
- Aucune phrase de fallback de faible qualité interdite.
- Aucune fuite d’information sensible.

# Entrées
- Règles `AGENTS.md`.
- Style de `index.md`.
- Inventaire des dépôts fourni.
- Outillage local limité (`gh` indisponible).

# Sorties
- `SPECIFICATIONS.md` (anglais).
- `SPECIFICATIONS_FR.md` (français synchronisé).
- `index.new.md` (anglais).

# Fichiers et répertoires concernés
- `SPECIFICATIONS_GLOBAL.md`
- `SPECIFICATIONS.md`
- `SPECIFICATIONS_FR.md`
- `index.new.md`

# Interfaces et commandes
- Outils shell (`sed`, `cat`, `python3`, `git`).

# Contraintes et règles de sécurité
- Ne pas modifier `index.md`, `AGENTS.md`, `style.css`, `_config.yml`.
- Ne pas exposer d’informations internes de dépôts privés.
- Ne pas inventer d’affirmations techniques non supportées.

# Validation et critères d’acceptation
- `index.new.md` existe et est en anglais.
- Les fichiers protégés restent inchangés.
- Chaque dépôt est représenté et les forks sont marqués.
- Aucune phrase interdite n’apparaît.

# Hors périmètre
- Modification de dépôts externes.
- Modification du CSS ou de la configuration Jekyll.

# Changelog
- v1.0.0 | 2026-04-30 00:00 UTC | Bruno DELNOZ
  - Ajout : Spécification de tâche pour la reconstruction du portfolio.
  - Modification : N/A.
  - Suppression : N/A.
  - Raison : Rebuild de `index.new.md` validé par l’utilisateur.
