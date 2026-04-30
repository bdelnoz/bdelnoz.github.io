# Prompt Codex Web - création exhaustive de index.new.md avec GO explicite intégré

Tu travailles sur mon dépôt GitHub Pages portfolio :

- Dépôt cible : bdelnoz/bdelnoz.github.io
- Fichier actuel à conserver intact : ./index.md
- Nouveau fichier à créer : ./index.new.md
- Site : https://bdelnoz.github.io
- Profil GitHub : https://github.com/bdelnoz
- Date courante : 2026-04-29

GO EXPLICITE

GO.

Je donne explicitement mon accord dès maintenant pour exécuter toute la tâche décrite ci-dessous.

Tu ne dois pas t’arrêter pour me demander une confirmation supplémentaire avant de créer ou modifier les fichiers autorisés.

Ce GO explicite vaut validation utilisateur pour :

1. analyser le dépôt bdelnoz.github.io ;
2. analyser tous les dépôts GitHub bdelnoz accessibles ;
3. préparer et créer ou mettre à jour les fichiers de spécifications requis par ./AGENTS.md ;
4. créer ./index.new.md ;
5. produire le rapport final.

Même si ./AGENTS.md impose normalement une étape de présentation des spécifications avant implémentation, considère ce prompt comme contenant mon GO explicite préalable pour cette tâche précise.

Tu dois donc appliquer le workflow dans l’ordre correct, mais sans attendre une nouvelle confirmation :

1. analyser ;
2. préparer les spécifications requises ;
3. créer ou mettre à jour les fichiers de spécifications autorisés ;
4. créer ./index.new.md ;
5. valider ;
6. rapporter.

CONTEXTE

Le fichier ./index.md actuel est dépassé. Il indique encore que le portfolio GitHub a été scanné le 2025-12-30 et liste seulement 24 dépôts publics. Ce n’est plus correct.

Mon inventaire GitHub actuel, obtenu avec gh repo list bdelnoz --limit 1000, contient beaucoup plus de dépôts. Je veux que le brouillon du portfolio inclue TOUS les dépôts individuellement, y compris les dépôts privés et les forks.

Important :

- Ne modifie PAS ./index.md dans cette tâche.
- Crée d’abord ./index.new.md.
- Je comparerai moi-même ./index.md et ./index.new.md avant tout remplacement éventuel.
- Je supprimerai moi-même ensuite les entrées que je ne veux finalement pas exposer.
- Le portfolio peut être long.
- L’exhaustivité est plus importante que la concision.
- Ne remplace pas les dépôts privés par un simple résumé groupé.
- Chaque dépôt doit avoir sa propre entrée individuelle.
- Les forks doivent aussi être inclus individuellement et marqués comme forks.
- Les dépôts privés doivent aussi être inclus individuellement et marqués PRIVATE.
- Si la visibilité exacte PUBLIC/PRIVATE n’est pas connue depuis la commande fournie, utilise gh repo view ou gh repo list avec le champ visibility pour confirmer.

LANGUE

- Réponds-moi en français dans le chat.
- Les fichiers livrables du dépôt doivent rester en anglais.
- ./index.new.md doit être en anglais.
- ./SPECIFICATIONS.md doit être en anglais.
- ./SPECIFICATIONS_GLOBAL.md doit être en anglais.
- ./SPECIFICATIONS_FR.md doit être en français.

OBJECTIF PRINCIPAL

Reconstruire une nouvelle version complète du portfolio GitHub dans ./index.new.md, sans modifier ./index.md.

Le nouveau fichier ./index.new.md doit refléter correctement l’ensemble actuel de mon écosystème GitHub :

1. Tous les dépôts publics doivent être listés individuellement.
2. Tous les dépôts privés doivent être listés individuellement.
3. Tous les forks doivent être listés individuellement.
4. Chaque dépôt doit être clairement marqué PUBLIC ou PRIVATE.
5. Chaque fork doit être clairement marqué FORK.
6. Les dépôts publics doivent avoir leur URL GitHub publique.
7. Les dépôts privés ne doivent pas avoir d’URL GitHub privée dans le portfolio public final, sauf si le dépôt est finalement confirmé public.
8. Chaque dépôt doit avoir une description factuelle dérivée de ses propres fichiers.
9. Les descriptions doivent rester professionnelles, utiles pour un portfolio, et exploitables par un recruteur ou un reviewer technique.
10. Aucune information sensible ne doit être publiée.

RÈGLES DU DÉPÔT

1. Lis et respecte strictement ./AGENTS.md.
2. Ne modifie pas ./AGENTS.md.
3. Ne modifie pas ./CLAUDE.md sauf uniquement pour restaurer le lien symbolique requis CLAUDE.md -> AGENTS.md si ./AGENTS.md l’exige explicitement.
4. Applique obligatoirement le workflow SPECIFICATIONS.md avant toute création de ./index.new.md.
5. Si ./AGENTS.md l’exige, crée ou mets à jour :
   - ./SPECIFICATIONS_GLOBAL.md
   - ./SPECIFICATIONS.md
   - ./SPECIFICATIONS_FR.md
6. Ce prompt contient déjà mon GO explicite. Ne t’arrête pas pour demander une validation intermédiaire.
7. Après avoir analysé et préparé les spécifications, crée ou mets à jour les fichiers de spécifications requis, puis crée ./index.new.md.
8. Ne modifie jamais ./index.md dans cette tâche.

INVENTAIRE GITHUB FOURNI

Voici l’inventaire GitHub complet fourni par l’utilisateur, avec nom complet, statut fork, et URL de clone.

Utilise cette liste comme base obligatoire de contrôle. Ne te limite pas aux anciens 24 dépôts publics de ./index.md.

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

La liste ci-dessus doit être traitée comme la base de contrôle fournie par l’utilisateur.

Tu dois aussi confirmer l’état réel avec GitHub CLI si disponible.

Utilise d’abord :

gh repo list bdelnoz --limit 1000 --json nameWithOwner,name,description,url,isPrivate,isFork,primaryLanguage,updatedAt,visibility

Puis utilise les résultats pour confirmer :

- nombre total de dépôts ;
- dépôts publics ;
- dépôts privés ;
- forks ;
- URLs publiques ;
- langage principal ;
- description GitHub disponible.

Si un dépôt de la liste fournie n’apparaît pas dans le résultat GitHub CLI, signale-le dans le rapport final au lieu de l’ignorer silencieusement.

Si GitHub CLI n’est pas disponible ou non authentifié, travaille à partir de la liste fournie et indique clairement cette limitation.

SOURCES À UTILISER POUR CHAQUE DÉPÔT

Utilise uniquement des informations factuelles dérivées du dépôt, de préférence :

- ./index.md
- ./README.md
- ./SPECIFICATIONS.md
- ./SPECIFICATIONS_GLOBAL.md
- ./WHY.md
- ./INSTALL.md
- ./CHANGELOG.md
- en-têtes de scripts
- fichiers de métadonnées du projet
- description GitHub du dépôt
- langage principal détecté par GitHub ou par les fichiers du dépôt

N’invente pas :

- descriptions ;
- métriques ;
- versions ;
- technologies ;
- dates ;
- réalisations ;
- nombres d’utilisateurs ;
- résultats ;
- clients ;
- statistiques ;
- performances ;
- statuts de production.

TRAITEMENT DES DÉPÔTS PUBLICS

Pour chaque dépôt public :

- inclure le nom complet du dépôt ;
- inclure l’URL GitHub publique ;
- inclure la visibilité PUBLIC ;
- inclure si c’est un fork ou non ;
- inclure le langage ou la technologie principale ;
- inclure une description courte et factuelle ;
- inclure la catégorie professionnelle ;
- utiliser prioritairement les fichiers du dépôt et la description GitHub ;
- ne pas inventer d’informations absentes des sources.

TRAITEMENT DES DÉPÔTS PRIVÉS

Pour chaque dépôt privé :

- inclure le dépôt individuellement ;
- marquer clairement la visibilité PRIVATE ;
- inclure si c’est un fork ou non ;
- inclure le nom du dépôt sauf si le nom lui-même contient manifestement un secret, token, mot de passe ou donnée trop sensible ;
- ne pas inclure d’URL privée GitHub ;
- inclure une description haut niveau sûre, dérivée de la documentation du dépôt ;
- inclure le langage ou la technologie principale si connu ;
- inclure la catégorie ou le domaine technique ;
- ne pas omettre les dépôts privés parce que le portfolio devient long ;
- ne pas remplacer la liste individuelle par un résumé groupé ;
- tu peux ajouter un résumé groupé en complément, mais jamais à la place de la liste individuelle.

TRAITEMENT DES FORKS

Pour chaque dépôt forké :

- l’inclure individuellement ;
- marquer clairement FORK ;
- expliquer sobrement qu’il s’agit d’un fork maintenu, exploré, adapté ou conservé dans mon environnement GitHub ;
- ne pas prétendre que j’en suis l’auteur original ;
- ne pas présenter le code upstream comme mon code original ;
- si des modifications locales/personnelles sont détectées, les décrire uniquement si elles sont vérifiées dans le dépôt.

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

Si un nom de dépôt semble lui-même sensible, inclus-le sous la forme :

PRIVATE repository name redacted

et explique brièvement que le nom a été masqué par sécurité.

STRUCTURE ATTENDUE POUR ./index.new.md

Le fichier ./index.new.md doit être une nouvelle version complète du portfolio.

Structure suggérée :

1. Header / identity block
2. Executive summary
3. Featured Projects
4. Complete Public Repository Portfolio
5. Complete Private Repository Portfolio
6. Forked Repositories
7. AI, LLM, Voice and Automation
8. Cybersecurity, WiFi and Network Security
9. Linux, System Administration and Hardening
10. Media, Audio, Video and Signal Processing
11. Developer Tools and GitHub Automation
12. Web, Browser Extensions and Productivity
13. Backup, Migration and Storage Automation
14. Raspberry Pi, Lab and Hardware Projects
15. Repository Statistics / Scan Summary
16. Technical Expertise
17. Contact and availability

Tu peux améliorer cette structure si l’analyse des dépôts montre une meilleure classification, mais ./index.new.md doit obligatoirement contenir une entrée individuelle pour chaque dépôt découvert ou fourni.

FORMAT DES ENTRÉES

Pour les dépôts publics, utiliser un format proche de ceci :

| Visibility | Fork | Project | Language / Tech | Description | Source basis |
|-----------|------|---------|-----------------|-------------|--------------|
| PUBLIC | No | [repo-name](https://github.com/bdelnoz/repo-name) | Shell | Factual description derived from repository sources. | README.md, GitHub metadata |

Pour les dépôts privés, utiliser un format proche de ceci :

| Visibility | Fork | Project | Language / Tech | Description | Source basis |
|-----------|------|---------|-----------------|-------------|--------------|
| PRIVATE | No | repo-name | Python / Shell | Safe high-level factual description derived from repository sources. | README.md, SPECIFICATIONS.md |

Pour les forks, utiliser :

| Visibility | Fork | Project | Language / Tech | Description | Source basis |
|-----------|------|---------|-----------------|-------------|--------------|
| PUBLIC or PRIVATE | Yes | repo-name | C / Python / Other | Forked repository retained for study, adaptation, maintenance or integration. Do not claim original authorship unless verified. | GitHub metadata, README.md |

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
- ./CLAUDE.md, sauf uniquement pour restaurer le lien symbolique requis CLAUDE.md -> AGENTS.md si ./AGENTS.md l’exige explicitement
- fichiers dans les autres dépôts
- fichiers source
- scripts
- documentation non liée
- fichiers de configuration non nécessaires

ORDRE D’EXÉCUTION OBLIGATOIRE

Tu as déjà mon GO explicite dans ce prompt.

Exécute directement dans cet ordre, sans demander de confirmation supplémentaire :

1. Analyse ./AGENTS.md.
2. Analyse le dépôt actuel bdelnoz.github.io.
3. Analyse l’inventaire GitHub fourni dans ce prompt.
4. Confirme l’inventaire avec gh repo list si GitHub CLI est disponible.
5. Analyse tous les dépôts bdelnoz accessibles.
6. Construis un inventaire complet des dépôts.
7. Identifie tous les dépôts publics.
8. Identifie tous les dépôts privés.
9. Identifie tous les forks.
10. Prépare un plan de portfolio complet par dépôt.
11. Crée ou mets à jour ./SPECIFICATIONS_GLOBAL.md si requis.
12. Crée ou mets à jour ./SPECIFICATIONS.md.
13. Crée ou mets à jour ./SPECIFICATIONS_FR.md.
14. Crée ./index.new.md.
15. Valide le résultat.
16. Fournis le rapport final.

VALIDATIONS OBLIGATOIRES

Après création de ./index.new.md :

1. Valide que ./index.new.md possède un front matter Markdown/Jekyll valide.
2. Valide que chaque dépôt découvert ou fourni est représenté individuellement.
3. Valide que tous les dépôts publics découverts sont listés.
4. Valide que tous les dépôts privés découverts sont listés.
5. Valide que tous les forks sont listés et marqués.
6. Valide qu’aucun code privé ni donnée sensible n’a été exposé.
7. Valide que ./AGENTS.md est resté inchangé.
8. Valide que ./index.md est resté inchangé.
9. Valide que ./style.css est resté inchangé.
10. Valide que ./_config.yml est resté inchangé.

RAPPORT FINAL ATTENDU

À la fin, fournis un rapport en français indiquant :

- nombre total de dépôts découverts ;
- nombre de dépôts publics inclus ;
- nombre de dépôts privés inclus ;
- nombre de forks inclus ;
- dépôts présents dans la liste fournie mais non retrouvés par GitHub CLI, s’il y en a ;
- dépôts présents dans GitHub CLI mais absents de la liste fournie, s’il y en a ;
- liste des dépôts ignorés, s’il y en a, avec raison exacte ;
- liste des dépôts dont le nom a été masqué, s’il y en a ;
- fichiers créés ;
- fichiers modifiés ;
- confirmation explicite que ./index.md est resté inchangé ;
- confirmation explicite que ./AGENTS.md est resté inchangé ;
- confirmation explicite que ./style.css est resté inchangé ;
- confirmation explicite que ./_config.yml est resté inchangé ;
- validations effectuées ;
- éléments non vérifiés ;
- limites éventuelles de l’analyse.

CRITÈRES D’ACCEPTATION

La tâche est acceptée seulement si :

- ./index.md reste inchangé.
- ./index.new.md est créé.
- ./index.new.md est en anglais.
- ./index.new.md ne prétend plus qu’il n’y a que 24 dépôts publics.
- La date de scan dans ./index.new.md est mise à jour au 2026-04-29.
- Chaque dépôt public découvert est listé individuellement.
- Chaque dépôt privé découvert est listé individuellement.
- Chaque fork découvert est listé individuellement.
- Les forks sont clairement marqués FORK.
- Les dépôts publics ont des liens publics.
- Les dépôts privés sont clairement marqués PRIVATE.
- Les dépôts privés ne sont pas remplacés uniquement par des résumés groupés.
- Aucun code privé n’est publié.
- Aucun secret ni détail opérationnel sensible n’est publié.
- Aucune affirmation non vérifiée n’est ajoutée.
- ./AGENTS.md reste inchangé.
- ./style.css reste inchangé.
- ./_config.yml reste inchangé.
- Le portfolio peut être long.
- L’exhaustivité est préférée à la concision.
- Les fichiers de spécifications requis par ./AGENTS.md sont créés ou mis à jour avant ./index.new.md.

RÈGLE FINALE IMPORTANTE

Ne raccourcis pas le portfolio pour des raisons de lisibilité. Je veux explicitement une page longue et exhaustive. Inclue chaque dépôt individuellement. Je supprimerai moi-même les entrées que je ne veux finalement pas exposer.

Ne me demande pas de confirmation supplémentaire. Le GO explicite est déjà donné dans ce prompt.
