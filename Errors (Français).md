# Erreurs système PS3 et RPCS3 - Explication

Ce document fournit un aperçu complet des différentes erreurs système liées à la PlayStation 3 et à l'émulateur RPCS3.

---

## BSOD (Écran Bleu de la Mort)
- **Description :** Corrompt (supprime des lignes de texte) le fichier de sauvegarde `Xregistry.sys` situé dans `dev_flash2/etc/backup/` et supprime le fichier principal `Xregistry.sys` dans `dev_flash2/etc/`.

---

## BSOD Grave
- **Description :** Supprime le fichier `libuserdata.sprx` (ou similaire) de `dev_flash/sys/external/`.

---

## RSOD (Écran Rouge de la Mort)
- **Description :**
  - Sur RPCS3 : Impossible à déclencher.
  - Sur une PS3 réelle : Supprimez `vsh.self` situé dans `dev_flash/vsh/module/`.

---

## "Une erreur grave s'est produite"
- **Description :** Semblable au RSOD.
  - Sur RPCS3 : Peut être déclenché.
  - Corrompt le fichier `sys_init_osd.self` dans `dev_flash/vsh/module/`.

---

## "Impossible de démarrer. Aucun disque dur approprié n'a été trouvé."
- **Description :**
  - Sur une PS3 réelle : Retirez physiquement le SSD ou le HDD.
  - Sur RPCS3 : Essayez de corrompre des fichiers dans `dev_hdd0`, bien que les résultats puissent varier.

---

## RSOD Grave
- **Description :** Extrêmement rare. Supposé se produire lorsque presque tous les fichiers système essentiels sont corrompus, à l'exception du XMB.

---

## "Le système de fichiers du disque dur est corrompu et sera restauré."
- **Description :**
  - Sur RPCS3 : Supprimez `dev_hdd0`.
  - Sur une PS3 réelle : Corrompez des fichiers dans `dev_hdd0` ou formatez incorrectement le HDD/SSD.

---

## "Données corrompues"
- **Description :** Corrompez le fichier `EBOOT.BIN` de toute application pour déclencher cette erreur.

---

## YLOD (Lumière Jaune de la Mort)
- **Description :** Ne peut pas être simulé. Se produit lorsque les points de soudure du GPU ou du CPU se déconnectent physiquement en raison de la chaleur ou de l'âge.

---

## GLOD (Lumière Verte de la Mort)
- **Description :** Semblable au YLOD mais légèrement moins grave.

---

## GARLOD (Lumière Verte et Rouge de la Mort)
- **Description :** Peut se produire en raison d'une surchauffe du système. Peut partager des causes avec le YLOD si plus grave.

---

## Semi-brick
- **Description :** Se produit lorsqu'une mise à jour système échoue ou que des fichiers non critiques sont corrompus.
  - N'affiche pas "Une erreur grave s'est produite".

---

## Brick Complet
- **Description :** Échec critique. Se produit avec YLOD/GLOD/GARLOD. La PS3 devient complètement inutilisable (pas de vidéo, pas de réponse).
  - Seule solution : Reflasher la puce NOR/NAND.
  - Peut être accompagné d'un BSOD.

---

## Glitches Visuels
- **Description :** Causés par la corruption ou la suppression d'éléments visuels (XMB, WAVE, icônes de démarrage PS3).
  - Si grave, indique que des fichiers système visuels essentiels sont manquants.

---

## Glitches Audio
- **Description :** Les sons du XMB ou du système sont corrompus ou manquants.
  - Sur RPCS3 : Installez le firmware 2.80 ou inférieur.
  - Sur une PS3 réelle : Supprimez les fichiers audio `.arc` ou les fichiers sonores du XMB.

---

## "Le disque doit être formaté"
- **Description :** Apparaît après un formatage interrompu ou échoué.
  - Peut être déclenché en corrompant intentionnellement le format du disque.

---

## Codes d'erreur (par exemple, 800017, 8007E21G)
- **Description :** Généralement dus à des licences RAP manquantes, une activation HEN défectueuse ou un CFW corrompu.
  - La gravité dépend du code spécifique.

---

## Boucle de Démarrage
- **Description :** Le système ne peut pas démarrer complètement et continue de redémarrer.
  - Sur RPCS3 : Supprimez tous les fichiers sauf `vsh.self`.
  - Sur une PS3 réelle : Corrompez les fichiers `dev_flash` qui chargent les modules système précoces.

---

## Gel du Système
- **Description :** Causé par une surcharge de la RAM ou du CPU.
  - Peut également être déclenché par des plugins bogués comme `PS3xPAD` sur des systèmes modifiés.

---

## Données Incompatibles
- **Description :** Se produit lors de l'insertion d'un disque PS2 dans un modèle non rétrocompatible (CECH(D–K)).

---

## Erreur de Lecture du Disque
- **Description :** Causée par des disques illisibles, inconnus ou endommagés, ou un lecteur de disque défectueux.
  - L'icône du disque peut ne pas apparaître du tout.

---

## Déconnexion de Session
- **Description :** Se produit lors de la déconnexion manuelle ou du lancement de HEN pour la première fois.
  - Inoffensif, juste une alerte.

---

*N'hésitez pas à contribuer ou à améliorer cette liste avec d'autres cas d'erreurs !*
