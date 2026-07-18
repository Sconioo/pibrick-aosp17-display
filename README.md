# Android 17 sur piBrick — AMOLED et HDMI

Ce projet ajoute le support de l’écran AMOLED du piBrick Pocket CM5 et corrige
les deux sorties HDMI avec KonstaKANG AOSP 17.

## Télécharger

### [⬇️ Télécharger le paquet cumulatif](https://github.com/Sconioo/pibrick-aosp17-display/releases/download/display-v2-hdmi-60hz/pibrick-aosp17-display-v2-hdmi-60hz.tar.gz)

Une seule archive contient le noyau et l’overlay AMOLED, le compositeur HDMI
corrigé, les patchs sources et l’installateur automatique.

## Installation en trois étapes

### 1. Installer Android 17

Télécharger l’image depuis la
[page officielle KonstaKANG AOSP 17](https://konstakang.com/devices/rpi5/AOSP17/)
et l’écrire sur le stockage du piBrick avec Raspberry Pi Imager.

### 2. Installer le correctif piBrick

Placer le piBrick en mode `rpiboot`, décompresser le paquet téléchargé, puis
lancer dans son dossier, **sans sudo** :

```bash
./install.sh
```

Contrôler le périphérique affiché et taper `INSTALLER`. Le script sauvegarde
automatiquement les fichiers présents avant de modifier `boot` et `vendor`.

### 3. Démarrer

Quitter le mode `rpiboot` et démarrer le piBrick. AMOLED et HDMI peuvent rester
branchés simultanément.

Résultat validé :

- AMOLED 1080×1240 à 60 Hz ;
- HDMI-1 fonctionnel ;
- HDMI-2 fonctionnel ;
- piBrick Pocket CM5 ;
- AOSP 17 du 2 juillet 2026.

> L’image Android complète n’est pas redistribuée. KonstaKANG interdit les
> miroirs de ses builds ; utilisez toujours son lien officiel.

La [release AMOLED 60 Hz précédente](https://github.com/Sconioo/pibrick-aosp17-display/releases/tag/display-v1-60hz)
reste disponible comme solution de repli.
