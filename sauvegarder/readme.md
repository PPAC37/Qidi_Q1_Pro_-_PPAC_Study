
# Tentative de sauvegarde

En mode un poil brut (il faut avoir la clé USB de connecté) et je sauve baucoup de choses par forcement utils ...


- Donc a affiner / adapter car là je `tar` vers un ficher dont le nom sera de la forme `PPAC_Save_OS_Q1Pro_2024-03-21_03-16-22.tar` (la date change) sur la clé USB les dossiers
  - /home
  - /root
  - /etc
- Mais en prennat soin d'exclure car il y a le point de montage de la clé dedant et car j'ai déja pris soint de sauver mes .gcode
  - /home/mks/gcode_files

Avec la commande :

~~~
tar -cvf /home/mks/gcode_files/sda1/PPAC_Save_OS_Q1Pro_`date "+%Y-%m-%d_%H-%M-%S"`.tar --exclude=/home/mks/gcode_files  /home /root /etc
~~~

Et pour vérifier le résultat

~~~
ls -lh /home/mks/gcode_files/sda1/PPAC_Save_OS_Q1Pro_*
~~~
<pre>
root@mkspi:~# ls -lh /home/mks/gcode_files/sda1/PPAC_Save_OS_Q1Pro_*
-rw-rw-rw- 1 root users 872M Mar 21 03:17 /home/mks/gcode_files/sda1/PPAC_Save_OS_Q1Pro_2024-03-21_03-16-22.tar
root@mkspi:~# 
</pre>

---

Là par précaution. Mais cela n'a pas été util lors de la mise a jour de v4.4.13 vers v4.4.15 du firmware.

en me basant sur https://github.com/fran6p/Qidi_X-Max3/blob/main/OS/sauvegarder_bdd_moonraker.md

Une méthode de sauvegarde de la base de donnée de moonraker ( qui contient entre autre l'historique d'impression )

Mais je n'ai pas entièrement adapté ( étape injecter la sauvegarde de la base, démarrer **moonraker** )

<!--

## Préserver l'historique des impressions

A chaque mise à jour si aucune précaution n'a été prise, l'historique des impressions est remis à zéro ☹️

Il est possible de faire une sauvegarde de la base de données pour pouvoir ensuite la réinjecter.

### Comment faire ?
-->

1. Connecté en ssh sur la carte en utilisateur **mks**, installer le paquet `lmdb-utils`
   
```
sudo apt install lmdb-utils
```

2. Faire une sauvegarde de la base actuelle dans un fichier texte 

<!--
```
cd ~
mdb_dump -f bkup-moonraker-db.txt -a .moonraker_database
```
-->

~~~
mdb_dump -f /home/mks/gcode_files/sda1/PPAC_Save_OS_Q1Pro_bkup-moonraker-db-`date "+%Y-%m-%d_%H-%M-%S"`.txt -a /home/mks/.moonraker_database
~~~
<pre>
root@mkspi:~# mdb_dump -f /home/mks/gcode_files/sda1/PPAC_Save_OS_Q1Pro_bkup-moonraker-db-`date "+%Y-%m-%d_%H-%M-%S"`.txt -a /home/mks/.moonraker_database
root@mkspi:~# ls -lh /home/mks/gcode_files/sda1/PPAC_Save_OS_Q1Pro_*
-rw-rw-rw- 1 root users 872M Mar 21 03:17 /home/mks/gcode_files/sda1/PPAC_Save_OS_Q1Pro_2024-03-21_03-16-22.tar
-rw-rw-rw- 1 root users 308K Mar 21 03:21 /home/mks/gcode_files/sda1/PPAC_Save_OS_Q1Pro_bkup-moonraker-db-2024-03-21_03-21-43.txt
root@mkspi:~# 
</pre>


Faire la mise à jour Qidi (clé USB contenant à la racine le dossier QD_Update et son contenu)
Toujours connecté en ssh, utilisateur mks

3. Faire la mise à jour Qidi (clé USB contenant à la racine le dossier QD_Update et son contenu)

4. Toujours connecté en ssh, utilisateur **mks**
  - Arrêter le daemon **moonraker**
  ```
  sudo systemctl stop moonraker
  ```
  - Supprimer les deux fichiers du répertoire **.moonraker_database** (répertoire caché)
  ```
  cd .moonraker_database
  rm -rf data.mdb
  rm -rf lock.mdb
  ```
  - Remonter à la racine du répertoire personnel (**/home/mks**), injecter la sauvegarde de la base, démarrer **moonraker**
  ```
  cd ~
  mdb_load -f bkup-moonraker-db.txt -s -T ~/.moonraker_database
  sudo systemctl start moonraker       
  ```   

Source: [Voron Community Documentation](https://docs.vorondesign.com/community/howto/kyleisah/transferring_machine_history.html#something-went-wrong-moonraker-isnt-coming-back-up)

Il doit être possible de créer une macro «shell_command» pour automatiser la sauvegarde la base (point 2 ci-dessus). A suivre donc…

---

