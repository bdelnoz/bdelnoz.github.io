# Prompt Codex Web - reconstruire index.new.md en conservant le style de index.md

Tu travailles sur mon dépôt GitHub Pages portfolio :

- Dépôt cible : bdelnoz/bdelnoz.github.io
- Fichier de référence stylistique obligatoire : ./index.md
- Fichier actuel à conserver intact : ./index.md
- Nouveau fichier à créer : ./index.new.md
- Site : https://bdelnoz.github.io
- Profil GitHub : https://github.com/bdelnoz
- Date courante : 2026-04-29

GO EXPLICITE

GO.

Je donne explicitement mon accord dès maintenant pour exécuter toute la tâche décrite ci-dessous.

Ne me demande pas de confirmation supplémentaire.

Ce GO explicite autorise uniquement :

1. l’analyse de ./AGENTS.md ;
2. l’analyse de ./index.md comme modèle stylistique ;
3. l’analyse de tous les dépôts GitHub bdelnoz accessibles ;
4. la création ou mise à jour des fichiers de spécifications requis par ./AGENTS.md ;
5. la création de ./index.new.md ;
6. le rapport final.

Ne modifie jamais ./index.md dans cette tâche.

OBJECTIF RÉEL

Le résultat précédent était mauvais parce qu’il a produit un inventaire brut, laid, non vérifié, avec des descriptions génériques du type :

- "Repository listed in inventory"
- "Not verified"
- "PUBLIC/PRIVATE (unverified in this environment)"
- "detailed per-repo documentation was not available"

Ce type de résultat est interdit.

Je veux un vrai portfolio professionnel, dans le même esprit et la même qualité que le ./index.md actuel.

Le ./index.md actuel est le modèle stylistique obligatoire :

- conserver le style CV/portfolio existant ;
- conserver le header personnel ;
- conserver les badges ;
- conserver la structure professionnelle ;
- conserver le ton marketing technique ;
- conserver les catégories avec emojis ;
- conserver les tables propres par catégorie ;
- conserver les descriptions riches et utiles ;
- conserver les sections longues de compétences, expertise, contact, disponibilité, etc. ;
- remplacer uniquement la partie GitHub/projects dépassée par une version complète, propre, actuelle et bien rédigée ;
- ne pas produire une simple table brute de 100 lignes sans valeur.

LANGUE

- Réponds-moi en français dans le chat.
- Les fichiers livrables du dépôt doivent rester en anglais.
- ./index.new.md doit être en anglais.
- ./SPECIFICATIONS.md doit être en anglais.
- ./SPECIFICATIONS_GLOBAL.md doit être en anglais.
- ./SPECIFICATIONS_FR.md doit être en français.

RÈGLES ABSOLUES DE QUALITÉ

Interdiction de produire un index.new.md contenant :

- "Not verified" comme langage ou description principale ;
- "PUBLIC/PRIVATE (unverified in this environment)" ;
- "Repository listed in inventory" ;
- "detailed per-repo documentation was not available" ;
- une seule table géante non classée ;
- un simple dump de l’inventaire GitHub ;
- des descriptions répétitives copiées-collées ;
- des descriptions paresseuses ;
- une page qui ne ressemble plus au portfolio actuel ;
- une suppression du contenu professionnel actuel hors section projets ;
- une réécriture pauvre du header, du résumé, des compétences ou du profil.

Si un dépôt ne peut pas être analysé correctement, ne génère pas une description nulle.
À la place :

1. tente d’obtenir les informations via gh repo view ;
2. tente de lire README.md, index.md, SPECIFICATIONS.md, SPECIFICATIONS_GLOBAL.md, WHY.md, INSTALL.md, CHANGELOG.md ;
3. tente de cloner ou consulter le dépôt si autorisé ;
4. utilise le nom du dépôt et la catégorie pour produire une description prudente mais professionnelle ;
5. marque seulement la source comme "GitHub metadata / repository name" si aucune documentation interne n’est disponible.

Mais le rendu final doit rester propre.

RÈGLES DU DÉPÔT

1. Lis et respecte strictement ./AGENTS.md.
2. Ne modifie pas ./AGENTS.md.
3. Ne modifie pas ./CLAUDE.md sauf uniquement pour restaurer le lien symbolique requis CLAUDE.md -> AGENTS.md si ./AGENTS.md l’exige explicitement.
4. Applique le workflow SPECIFICATIONS.md exigé par ./AGENTS.md.
5. Ce prompt contient déjà mon GO explicite : ne t’arrête pas pour demander une validation intermédiaire.
6. Crée ou mets à jour les fichiers de spécifications requis avant de créer ./index.new.md.
7. Ne modifie jamais ./index.md dans cette tâche.
8. Ne modifie pas ./style.css.
9. Ne modifie pas ./_config.yml.

FICHIERS AUTORISÉS À MODIFIER OU CRÉER

Tu peux créer ou modifier uniquement :

- ./SPECIFICATIONS_GLOBAL.md, si requis par ./AGENTS.md
- ./SPECIFICATIONS.md
- ./SPECIFICATIONS_FR.md
- ./index.new.md

FICHIERS INTERDITS DE MODIFICATION

Ne modifie pas :

- ./index.md
- ./AGENTS.md
- ./style.css
- ./_config.yml
- fichiers dans les autres dépôts
- fichiers source
- scripts
- documentation non liée
- fichiers de configuration non nécessaires

CONTEXTE

Le fichier ./index.md actuel est dépassé. Il indique encore que le portfolio GitHub a été scanné le 2025-12-30 et liste seulement 24 dépôts publics.

C’est faux aujourd’hui.

Je veux que ./index.new.md contienne :

1. une nouvelle version complète du portfolio ;
2. le même style que ./index.md ;
3. une section GitHub actuelle ;
4. tous les dépôts publics individuellement ;
5. tous les dépôts privés individuellement ;
6. tous les forks individuellement ;
7. une classification professionnelle ;
8. des descriptions propres ;
9. une section statistiques mise à jour ;
10. le reste du profil professionnel conservé ou amélioré sans dégrader le style.

STYLE OBLIGATOIRE À REPRODUIRE

Le ./index.new.md doit ressembler au ./index.md actuel.

Conserve ce type de structure :

- front matter Jekyll :
  ---
  layout: default
  ---

- titre principal :
  # Bruno Delnoz
  # Senior Middleware Integration & Digital Migration Consultant

- localisation/contact/badges comme dans l’actuel ;
- résumé professionnel ;
- section projets GitHub avec catégories ;
- tables Markdown propres ;
- descriptions riches ;
- sections expertise ;
- major projects ;
- professional statistics ;
- languages ;
- contact ;
- closing statement.

Ne transforme pas la page en inventaire technique sec.

La section projets doit rester attractive.

EXIGENCE SUR LA SECTION GITHUB

Remplace l’ancienne section :

"Open‑Source Projects on GitHub (complete list – scanned 30/12/2025)"

par une nouvelle section du type :

"GitHub Repository Portfolio (complete inventory – scanned 2026-04-29)"

ou mieux si tu trouves un titre plus professionnel.

Cette section doit contenir :

1. Featured Projects - AI & Privacy Tools
2. AI, LLM, Voice & Automation Projects
3. Security, WiFi & Network Projects
4. Linux, System Administration & Storage
5. Media, Audio, Video & Signal Processing
6. Developer Tools & GitHub Automation
7. Web, Browser Extensions & Productivity
8. Raspberry Pi, Lab & Hardware Projects
9. Documentation, Standards & Knowledge Bases
10. Private Professional Projects
11. Forked / Upstream-Based Repositories
12. Portfolio & Website
13. Repository Statistics

Tu peux ajuster les catégories si nécessaire, mais tu dois garder un rendu professionnel similaire à l’actuel.

EXIGENCE SUR LES DÉPÔTS PRIVÉS

Je veux que tous les dépôts privés soient inclus individuellement.

Ne les groupe pas seulement par famille.

Pour chaque dépôt privé :

- afficher le nom du dépôt ;
- marquer PRIVATE ;
- ne pas afficher d’URL privée ;
- ne pas exposer de code ;
- ne pas exposer de secrets ;
- produire une description professionnelle, sûre, haut niveau ;
- utiliser les fichiers du dépôt si disponibles ;
- si le nom du dépôt est lui-même trop sensible, utiliser "PRIVATE repository name redacted".

Comme je relirai ensuite moi-même, ne supprime pas arbitrairement les dépôts privés pour raccourcir.

EXIGENCE SUR LES FORKS

Les forks doivent être listés individuellement.

Pour chaque fork :

- marquer FORK ;
- ne pas prétendre que j’en suis l’auteur original ;
- présenter comme fork conservé, étudié, adapté, maintenu, testé ou intégré selon les preuves disponibles ;
- si aucune modification personnelle n’est vérifiée, rester sobre.

INVENTAIRE GITHUB FOURNI

Voici l’inventaire GitHub fourni par l’utilisateur, avec nom complet, statut fork, et URL de clone.

Utilise cette liste comme base obligatoire de contrôle.

bdelnoz/rtl88x2bu	true	https://github.com/bdelnoz/rtl88x2bu.git
bdelnoz/bdelnoz.github.io	false	https://github.com/bdelnoz/bdelnoz.github.io.git
bdelnoz/voicelogin	false	https://github.com/bdelnoz/voicelogin.git
bdelnoz/TEST_REPO	false	https://github.com/bdelnoz/TEST_REPO.git
bdelnoz/systemctl_mounting	false	https://github.com/bdelnoz/systemctl_mounting.git
bdelnoz/Spoon-Knife	false	https://github.com/bdelnoz/Spoon-Knife.git
bdelnoz/scripts-wifi-scan	false	https://github.com/bdelnoz/scripts-wifi-scan.git
bdelnoz/scripts_root	false	https://github.com/bdelnoz/scripts_root.git
bdelnoz/lucivy	true	https://github.com/bdelnoz/lucivy.git
bdelnoz/live-build-config	false	https://github.com/bdelnoz/live-build-config.git
bdelnoz/kdbx	false	https://github.com/bdelnoz/kdbx.git
bdelnoz/divers	false	https://github.com/bdelnoz/divers.git
bdelnoz/DeepEcho	false	https://github.com/bdelnoz/DeepEcho.git
bdelnoz/create_repo_temp	false	https://github.com/bdelnoz/create_repo_temp.git
bdelnoz/cmd.disable_brol_notneeded	false	https://github.com/bdelnoz/cmd.disable_brol_notneeded.git
bdelnoz/captureNoXoZ	false	https://github.com/bdelnoz/captureNoXoZ.git
bdelnoz/regles_contextualisation	false	https://github.com/bdelnoz/regles_contextualisation.git
bdelnoz/firefoxVTTextension	false	https://github.com/bdelnoz/firefoxVTTextension.git
bdelnoz/braveVTTextension_en	false	https://github.com/bdelnoz/braveVTTextension_en.git
bdelnoz/braveVTTextension	false	https://github.com/bdelnoz/braveVTTextension.git
bdelnoz/brave-fb-onlyme-extension-extract-info	false	https://github.com/bdelnoz/brave-fb-onlyme-extension-extract-info.git
bdelnoz/brave-fb-onlyme-extension	false	https://github.com/bdelnoz/brave-fb-onlyme-extension.git
bdelnoz/non_destructive_ntfs_audit	false	https://github.com/bdelnoz/non_destructive_ntfs_audit.git
bdelnoz/init_project	false	https://github.com/bdelnoz/init_project.git
bdelnoz/create_repo	false	https://github.com/bdelnoz/create_repo.git
bdelnoz/create_gitignore	false	https://github.com/bdelnoz/create_gitignore.git
bdelnoz/createCONTACTfromApple	false	https://github.com/bdelnoz/createCONTACTfromApple.git
bdelnoz/cpx	false	https://github.com/bdelnoz/cpx.git
bdelnoz/convdocx	false	https://github.com/bdelnoz/convdocx.git
bdelnoz/checkdeepdisk	false	https://github.com/bdelnoz/checkdeepdisk.git
bdelnoz/catall	false	https://github.com/bdelnoz/catall.git
bdelnoz/Projects_utility	false	https://github.com/bdelnoz/Projects_utility.git
bdelnoz/syncgit	false	https://github.com/bdelnoz/syncgit.git
bdelnoz/purgeaudio	false	https://github.com/bdelnoz/purgeaudio.git
bdelnoz/Packages_Documentation	false	https://github.com/bdelnoz/Packages_Documentation.git
bdelnoz/mountVG	false	https://github.com/bdelnoz/mountVG.git
bdelnoz/findgit	false	https://github.com/bdelnoz/findgit.git
bdelnoz/diff_files_not_copied	false	https://github.com/bdelnoz/diff_files_not_copied.git
bdelnoz/dashboard	false	https://github.com/bdelnoz/dashboard.git
bdelnoz/casamovetokoutou	false	https://github.com/bdelnoz/casamovetokoutou.git
bdelnoz/casa2koutou_config	false	https://github.com/bdelnoz/casa2koutou_config.git
bdelnoz/analyseProcess	false	https://github.com/bdelnoz/analyseProcess.git
bdelnoz/analyseBrave	false	https://github.com/bdelnoz/analyseBrave.git
bdelnoz/Projects_system	false	https://github.com/bdelnoz/Projects_system.git
bdelnoz/wlaninfo	false	https://github.com/bdelnoz/wlaninfo.git
bdelnoz/usb_enc	false	https://github.com/bdelnoz/usb_enc.git
bdelnoz/tapo	false	https://github.com/bdelnoz/tapo.git
bdelnoz/ssh_hardening	false	https://github.com/bdelnoz/ssh_hardening.git
bdelnoz/scan_security	false	https://github.com/bdelnoz/scan_security.git
bdelnoz/rasperry-utils	false	https://github.com/bdelnoz/rasperry-utils.git
bdelnoz/rasperry-scanbt	false	https://github.com/bdelnoz/rasperry-scanbt.git
bdelnoz/rasperry-post-install	false	https://github.com/bdelnoz/rasperry-post-install.git
bdelnoz/rasperry-micro	false	https://github.com/bdelnoz/rasperry-micro.git
bdelnoz/rasperry-bt-scan	false	https://github.com/bdelnoz/rasperry-bt-scan.git
bdelnoz/rasperry	false	https://github.com/bdelnoz/rasperry.git
bdelnoz/QEMU-tapo	false	https://github.com/bdelnoz/QEMU-tapo.git
bdelnoz/ManInTheMiddle	false	https://github.com/bdelnoz/ManInTheMiddle.git
bdelnoz/kali-deep-analyse-timeframe	false	https://github.com/bdelnoz/kali-deep-analyse-timeframe.git
bdelnoz/jeronimo	false	https://github.com/bdelnoz/jeronimo.git
bdelnoz/iptables	false	https://github.com/bdelnoz/iptables.git
bdelnoz/deluge	false	https://github.com/bdelnoz/deluge.git
bdelnoz/create_luks	false	https://github.com/bdelnoz/create_luks.git
bdelnoz/cmd.airmon-to-dos	false	https://github.com/bdelnoz/cmd.airmon-to-dos.git
bdelnoz/Projects_security	false	https://github.com/bdelnoz/Projects_security.git
bdelnoz/Projects_py	false	https://github.com/bdelnoz/Projects_py.git
bdelnoz/Projects_network	false	https://github.com/bdelnoz/Projects_network.git
bdelnoz/song_maker_AI_local	false	https://github.com/bdelnoz/song_maker_AI_local.git
bdelnoz/mp4_to_images_per_second	false	https://github.com/bdelnoz/mp4_to_images_per_second.git
bdelnoz/friture-kali	false	https://github.com/bdelnoz/friture-kali.git
bdelnoz/compressvideo	false	https://github.com/bdelnoz/compressvideo.git
bdelnoz/Projects_multimedia	false	https://github.com/bdelnoz/Projects_multimedia.git
bdelnoz/Projects_installation	false	https://github.com/bdelnoz/Projects_installation.git
bdelnoz/Projects_divers	false	https://github.com/bdelnoz/Projects_divers.git
bdelnoz/root_home	false	https://github.com/bdelnoz/root_home.git
bdelnoz/backup_kali_root	false	https://github.com/bdelnoz/backup_kali_root.git
bdelnoz/backup_create_report	false	https://github.com/bdelnoz/backup_create_report.git
bdelnoz/AI_tools	false	https://github.com/bdelnoz/AI_tools.git
bdelnoz/RikHunter	false	https://github.com/bdelnoz/RikHunter.git
bdelnoz/Emploi_public	false	https://github.com/bdelnoz/Emploi_public.git
bdelnoz/Emploi	false	https://github.com/bdelnoz/Emploi.git
bdelnoz/Overlook_record_cam	false	https://github.com/bdelnoz/Overlook_record_cam.git
bdelnoz/NoXoZVorteX_working	false	https://github.com/bdelnoz/NoXoZVorteX_working.git
bdelnoz/NoXoZVorteX_prompted_en	false	https://github.com/bdelnoz/NoXoZVorteX_prompted_en.git
bdelnoz/NoXoZVorteX_prompted	false	https://github.com/bdelnoz/NoXoZVorteX_prompted.git
bdelnoz/NoXoZVorteX	false	https://github.com/bdelnoz/NoXoZVorteX.git
bdelnoz/NoXoZ_job	false	https://github.com/bdelnoz/NoXoZ_job.git
bdelnoz/NoXoZ4Hunt	false	https://github.com/bdelnoz/NoXoZ4Hunt.git
bdelnoz/Gamblox	false	https://github.com/bdelnoz/Gamblox.git
bdelnoz/DeepEcho_whisper	false	https://github.com/bdelnoz/DeepEcho_whisper.git
bdelnoz/ColtSivers	false	https://github.com/bdelnoz/ColtSivers.git
bdelnoz/codex-update-md	false	https://github.com/bdelnoz/codex-update-md.git
bdelnoz/ChatGPTcreatecontext	false	https://github.com/bdelnoz/ChatGPTcreatecontext.git
bdelnoz/AI_Personal_data	false	https://github.com/bdelnoz/AI_Personal_data.git
bdelnoz/AI_information	false	https://github.com/bdelnoz/AI_information.git
bdelnoz/rasperry-multiboot	false	https://github.com/bdelnoz/rasperry-multiboot.git
bdelnoz/brave_backup_restore	false	https://github.com/bdelnoz/brave_backup_restore.git
bdelnoz/rtk-reduce-tokens	true	https://github.com/bdelnoz/rtk-reduce-tokens.git
bdelnoz/poc_mistral	false	https://github.com/bdelnoz/poc_mistral.git
bdelnoz/scripts	false	https://github.com/bdelnoz/scripts.git
bdelnoz/AI_Projects	false	https://github.com/bdelnoz/AI_Projects.git
bdelnoz/Mega_s4-specs	true	https://github.com/bdelnoz/Mega_s4-specs.git
bdelnoz/ods-cookbook	false	https://github.com/bdelnoz/ods-cookbook.git
bdelnoz/w3id.org	true	https://github.com/bdelnoz/w3id.org.git
bdelnoz/owasp-modsecurity-crs	true	https://github.com/bdelnoz/owasp-modsecurity-crs.git
bdelnoz/active-directory-dotnet-webapi-manual-jwt-validation	true	https://github.com/bdelnoz/active-directory-dotnet-webapi-manual-jwt-validation.git

DÉCOUVERTE ET VALIDATION DES DÉPÔTS

La liste fournie doit être traitée comme base de contrôle obligatoire, mais elle n’est pas suffisante pour rédiger un portfolio de qualité.

Tu dois réellement analyser les dépôts accessibles.

Utilise GitHub CLI si disponible :

gh repo list bdelnoz --limit 1000 --json nameWithOwner,name,description,url,isPrivate,isFork,primaryLanguage,updatedAt,visibility

Pour chaque dépôt, tente ensuite :

gh repo view OWNER/REPO --json nameWithOwner,description,url,isPrivate,isFork,primaryLanguage,updatedAt,visibility

Si le dépôt est accessible, inspecte les fichiers utiles :

- README.md
- index.md
- SPECIFICATIONS.md
- SPECIFICATIONS_GLOBAL.md
- WHY.md
- INSTALL.md
- CHANGELOG.md
- AGENTS.md seulement pour règles, pas pour description marketing
- fichiers metadata
- headers de scripts si nécessaire

Si les dépôts ne sont pas déjà clonés localement mais que GitHub CLI et Git sont disponibles, tu peux cloner temporairement les dépôts accessibles dans un répertoire temporaire de travail pour lire uniquement leur documentation.

Ne modifie jamais ces autres dépôts.

INTERDICTION DE FALLBACK PAUVRE

Si GitHub CLI n’est pas disponible ou si les dépôts ne sont pas accessibles, ne produis pas un index.new.md final de mauvaise qualité basé uniquement sur la liste brute.

Dans ce cas :

- crée les specs requises si nécessaire ;
- crée un rapport d’échec ou de blocage ;
- explique que l’analyse réelle des dépôts est impossible dans cet environnement ;
- ne crée pas un index.new.md composé de descriptions génériques répétitives ;
- ne crée pas une page qui dégrade le portfolio.

Autrement dit : mieux vaut échouer proprement que produire une page de merde.

SOURCES AUTORISÉES POUR LES DESCRIPTIONS

Utilise uniquement des informations factuelles dérivées :

- du dépôt lui-même ;
- de la description GitHub ;
- du nom du dépôt uniquement en dernier recours ;
- des documents README/SPECIFICATIONS/WHY/CHANGELOG ;
- des headers de scripts ;
- du contenu documentaire non sensible.

N’invente pas :

- métriques ;
- versions ;
- technologies ;
- clients ;
- statistiques ;
- performances ;
- statuts de production ;
- résultats ;
- certifications ;
- nombre d’utilisateurs ;
- claims marketing non supportés.

Mais tu dois rédiger proprement, en style portfolio.

TRAITEMENT DES DÉPÔTS PUBLICS

Pour chaque dépôt public :

- inclure le nom complet du dépôt ;
- inclure l’URL GitHub publique ;
- inclure la visibilité PUBLIC ;
- inclure si c’est un fork ou non ;
- inclure le langage ou la technologie principale ;
- inclure une description courte, utile, propre et factuelle ;
- classer dans une catégorie professionnelle ;
- conserver un style proche du ./index.md actuel.

TRAITEMENT DES DÉPÔTS PRIVÉS

Pour chaque dépôt privé :

- inclure le dépôt individuellement ;
- marquer clairement PRIVATE ;
- ne pas inclure d’URL privée ;
- inclure si c’est un fork ou non ;
- inclure une description haut niveau sûre, propre et professionnelle ;
- ne pas publier de contenu sensible ;
- ne pas omettre le dépôt pour raccourcir ;
- ne pas remplacer la liste individuelle par un résumé groupé.

SÉCURITÉ POUR LES DÉPÔTS PRIVÉS

Même si tous les dépôts privés doivent être listés individuellement, ne publie jamais :

- code privé ;
- secrets ;
- mots de passe ;
- tokens ;
- clés API ;
- clés SSH ;
- certificats privés ;
- fichiers .env ;
- contenu de .secrets ;
- chemins locaux sensibles ;
- noms d’utilisateurs système internes ;
- hostnames internes ;
- adresses IP ;
- adresses MAC ;
- logs privés ;
- sorties brutes de commandes ;
- règles firewall exactes ;
- topologie d’infrastructure exacte ;
- noms de clients sauf s’ils sont déjà publics et sûrs ;
- détails opérationnels exploitables ;
- identifiants ;
- contenu de données personnelles ;
- contenu brut de fichiers privés ;
- informations qui peuvent faciliter une intrusion, une usurpation, une reconnaissance ou une exploitation.

STRUCTURE ATTENDUE DE ./index.new.md

Le fichier ./index.new.md doit être un portfolio complet, pas un inventaire brut.

Il doit conserver autant que possible le contenu de ./index.md actuel, notamment :

- header ;
- contact ;
- badges ;
- résumé ;
- technical expertise ;
- major projects ;
- professional statistics ;
- language and communication ;
- career objectives ;
- personal interests ;
- contact and availability ;
- value proposition ;
- closing statement.

La section GitHub actuelle doit être reconstruite et enrichie.

Organisation recommandée :

## GitHub Repository Portfolio (complete inventory – scanned 2026-04-29)

### 🎯 Featured Projects - AI & Privacy Tools
Table propre.

### 🤖 AI, LLM, Voice & Automation Projects
Table propre.

### 🛡️ Security, WiFi & Network Tools
Table propre.

### 🐧 Linux, System Administration & Storage
Table propre.

### 🎥 Media, Audio, Video & Signal Processing
Table propre.

### 🔧 Developer Tools & GitHub Automation
Table propre.

### 🌐 Web, Browser Extensions & Productivity
Table propre.

### 🍓 Raspberry Pi, Lab & Hardware Projects
Table propre.

### 📚 Documentation, Standards & Knowledge Bases
Table propre.

### 🔒 Private Professional Projects
Table propre, avec PRIVATE, sans URL privée.

### 🔁 Forked / Upstream-Based Repositories
Table propre.

### 📊 Repository Statistics
Résumé clair.

FORMAT DES TABLES

Utilise des tables proches du style actuel :

| Project | Visibility | Fork | Language | Description |
|---------|------------|------|----------|-------------|

Pour les projets publics :

**[`repo-name`](https://github.com/bdelnoz/repo-name)**

Pour les projets privés :

**`repo-name`**  
Pas de lien privé.

Descriptions :

- une à deux phrases courtes maximum ;
- style professionnel ;
- pas de répétition ;
- pas de "Not verified" ;
- pas de "Repository listed in inventory" ;
- pas de "documentation unavailable" dans la table finale.

Si vraiment une information est limitée, utilise une formulation propre comme :

"Private utility repository reserved for internal automation and technical experimentation; public-facing details intentionally limited."

Mais n’utilise cette phrase qu’en dernier recours, pas partout.

ORDRE D’EXÉCUTION OBLIGATOIRE

Tu as déjà mon GO explicite dans ce prompt.

Exécute directement dans cet ordre :

1. Analyse ./AGENTS.md.
2. Analyse ./index.md comme modèle stylistique obligatoire.
3. Analyse l’inventaire GitHub fourni.
4. Confirme l’inventaire avec GitHub CLI si disponible.
5. Analyse les dépôts accessibles.
6. Refuse de produire un index.new.md pauvre si les dépôts ne sont pas réellement analysables.
7. Crée ou mets à jour ./SPECIFICATIONS_GLOBAL.md si requis.
8. Crée ou mets à jour ./SPECIFICATIONS.md.
9. Crée ou mets à jour ./SPECIFICATIONS_FR.md.
10. Crée ./index.new.md en conservant le style du portfolio actuel.
11. Valide le résultat.
12. Fournis le rapport final.

VALIDATIONS OBLIGATOIRES

Après création de ./index.new.md :

1. Vérifie que ./index.md est inchangé.
2. Vérifie que ./AGENTS.md est inchangé.
3. Vérifie que ./style.css est inchangé.
4. Vérifie que ./_config.yml est inchangé.
5. Vérifie que ./index.new.md conserve le style général de ./index.md.
6. Vérifie que ./index.new.md n’est pas un simple inventaire brut.
7. Vérifie qu’aucune ligne ne contient :
   - "Not verified"
   - "PUBLIC/PRIVATE (unverified"
   - "Repository listed in inventory"
   - "detailed per-repo documentation was not available"
8. Vérifie que chaque dépôt fourni ou découvert est représenté individuellement.
9. Vérifie que les forks sont marqués.
10. Vérifie qu’aucun contenu privé sensible n’est exposé.

RAPPORT FINAL ATTENDU

À la fin, fournis un rapport en français indiquant :

- nombre total de dépôts découverts ;
- nombre de dépôts publics inclus ;
- nombre de dépôts privés inclus ;
- nombre de forks inclus ;
- fichiers créés ;
- fichiers modifiés ;
- confirmation que ./index.md est inchangé ;
- confirmation que ./AGENTS.md est inchangé ;
- confirmation que ./style.css est inchangé ;
- confirmation que ./_config.yml est inchangé ;
- validation anti-rendu-pauvre ;
- limites éventuelles ;
- dépôts ignorés, s’il y en a, avec raison exacte.

CRITÈRES D’ACCEPTATION

La tâche est acceptée seulement si :

- ./index.md reste inchangé.
- ./index.new.md est créé.
- ./index.new.md est en anglais.
- ./index.new.md ressemble clairement au ./index.md actuel.
- ./index.new.md conserve la structure portfolio/CV.
- La section GitHub est mise à jour au 2026-04-29.
- Tous les dépôts publics sont listés individuellement.
- Tous les dépôts privés sont listés individuellement.
- Tous les forks sont listés individuellement et marqués FORK.
- Les dépôts publics ont des liens publics.
- Les dépôts privés n’ont pas de liens privés.
- Les descriptions sont utiles, professionnelles, non répétitives.
- Aucun contenu privé sensible n’est publié.
- Aucune affirmation non vérifiée n’est ajoutée.
- Aucune ligne ne contient "Not verified".
- Aucune ligne ne contient "Repository listed in inventory".
- Aucune ligne ne contient "PUBLIC/PRIVATE (unverified".
- Le rendu n’est pas une table brute géante sans style.
- ./AGENTS.md reste inchangé.
- ./style.css reste inchangé.
- ./_config.yml reste inchangé.

RÈGLE FINALE IMPORTANTE

Ne produis pas une page médiocre.

Le but n’est pas de transformer le portfolio en dump GitHub.

Le but est de créer un vrai ./index.new.md professionnel, long si nécessaire, exhaustif, mais dans le style du ./index.md actuel.
