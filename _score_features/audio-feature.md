---
layout: score-feature
title:  "Sound files"

permalink: /score/features/audio.html
category: "site-score"
image: /assets/features/audio.png
description: "Playing sound files in ossia score"

tag: "Audio"
visible: false
---

- Drag'n'drop depuis le système
- Drag'n'drop depuis la bibliothèque
- Les fichiers avec information de tempo sont mis en boucle & timestretch automatiquement
- 4 modes de timestretch: 
  * Raw: pas de timestretch
  * Timestretch: timestretch normal, adapté aux instrus mélodiques
  * Timestretch (percussive): timestretch normal, adapté aux instrus percussifs
  * Repitch: change la hauteur

- Les fichiers .wav / .aiff à la même fréquence d'échantillonnage que celle de score sont lus depuis le disque
- Tous les autres fichiers sont convertis et stockés en RAM 
  - Note : mentionner le ramdisk trick
- Formats supportés: tous ceux supportés par ffmpeg 
  * http://www.ffmpeg.org/general.html#Audio-Codecs