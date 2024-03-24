# Qidi_Q1_Pro_-_PPAC_Study
Mes notes sur le firmware de la Q1 Pro du constructeur Qidi Tech


En vrac pour l'instant.

## Une bonne pratique et de toujours changer le mot de passe par defaut

Ici il y a deux utilisateurs. L'utilisateur `root` et l'utilisateur `mks` donc pour éviter de faciliter un piratage

~~~
passwd root
~~~

~~~
passwd mks
~~~

---


- Mon sujet de découverte sur le forum de https://www.lesimprimantes3d.fr/
  - https://www.lesimprimantes3d.fr/forum/topic/57668-qidi-tech-q1-pro-le-sujet-de-d%C3%A9couverte/
- La "Q1 Pro" sur le comparateur
  - https://www.lesimprimantes3d.fr/comparateur/imprimante3d/qidi-tech/q1-pro/

- Site officiel de QIDI TECH 
  - https://qidi3d.com/
- La Q1 Pro
  - https://qidi3d.com/products/q1-pro-3d-printer
- dépôt GitHub du firmware de la "Q1 Pro" ( Par précaution ne pas prendre le firmware disponible sur le dépot github. Préférer la version téléchargeable sur https://qidi3d.com/pages/software-firmware )
  - https://github.com/QIDITECH/QIDI_Q1_Pro
- dépôt de QIDISlicer ( "Fork" de Prusa Slicer, qui embarque les profiles des imprimantes QIDI TECH ) mais il n'est pas recommandé de télécharger QIDISlicer depuis le dépôt GitHub préférer les versions téléchargeables sur https://qidi3d.com/pages/software-firmware
  - https://github.com/QIDITECH/QIDISlicer
  - https://github.com/QIDITECH/QIDISlicer/releases (la v1.1.2, embarque normalement le profil de la "Q1 Pro")
- La"Q1 Pro" sur le wiki de QIDI TECH
  - https://wiki.qidi3d.com/en/Q1-Pro

- Pour référence, comme le système d'exploitation et la configuration Klipper est très proche de ce que l'on trouve sur la Qidi X-Max 3
  - https://github.com/fran6p/Qidi_X-Max3/tree/main
