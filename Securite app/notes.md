## Définitions
#### Utilisateur:
- Connexion utilisant la base de donnée connectée à un schéma
- Créer un utilisateur : `CREATE USER`*`nom_user`*`IDENTIFIED BY`*`password`*
**Schéma :**
    - Ensemble d'objets apartenant à un utilisateur 
    - Automatiquement crée 
    - Même nom que l'utilisateur
#### Privilèges
- Permissions quant aux interactions avec la *bd*
- **Privilèges systèmes :**
    - Privilèges valables sur la base entière
- **Privilèges objets :**
    - Privilèges sur des tables ou colonnes spécifiques
- **Commandes**
    - **GRANT** : Donner des permissions
    - **REVOKE** : Retirer des permissions
#### Rôle:
- Regroupement de permissions
- **Étapes :**`
    - Créer rôle : `CREATE ROLE`*`nom_role`*
    - Donner des permissions au rôle : `GRANT`*`PERMISSIONS nom_role`*
    - Donner le rôle à un utilisateur : `GRANT`*`nom_role`*`TO`*`user`*

#### Profil:
- Limitations attribuées à un rôle ou utilisateur
- **Deux axes :**
    - Limitations Mot de Passe
    - Limitations utilisation de ressources
# Admnisitration
#### DBA

#### CDB
- Nommé **CDB$ROOT**
- Username précédé par **C##**
- Regroupe et gère les PDB
- Utilisateur CDB a accès à toutes les PDB
#### PDB
- Accès local uniquement
- Sert séparer la *bd* en petites équipes


#### Tablespace
- Permet de regrouper des objets de *bd* reliés 
----
## Mots clés
### Oracle
|Instruction|Définition|
|-|-|
|**`CREATE`**|Créer|
|**`GRANT`**|Ajouter des permissions <br> à un utilisteur ou à un rôle|
|**`ALTER`**|Changer un objet|
|**`UPDATE`**|Changer une valeur|

### Utilisateurs
|Mot|Définition|
|-|-|
|**`QUOTA`**|Taille Maximum d'utilisation d'un utilisateur|
### Profils
|Mot|Définition|
|-|-|
|**`SESSIONS_PER_USER`**|Nombre de sessions pouvant <br> être ouvertes en même temps|
|**`CONNECT_TIME`**|Temps maximal de connection <br> par session|
|**`IDLE_TIME`**|Temps maximal d'inactivité <br> avant déconnexion (en **minutes**)|
|**`LOGICAL_READS_PER_SESSION`**|Nombre maximal de lectures <br> logiques par session|
|**`FAILED_LOGIN_ATTEMPS`**|Maximum de tentatives <br> échouées|
|**`PASSWORD_LIFE_TIME`**|Temps de validité du mot de <br> passe avant d'avoir à le changer <br>(en **jours**)|
|**`PASSWORD_LOCK_TIME`**|Temps d'attente après maximum <br> de tentatives atteint (en **jours**)|
|**`PASSWORD_GRACE_TIME`**|Temps de validité du mot de <br> passe après expiration <br>(en **jours**)|
|**`COMPOSITE_LIMIT`**|Nombre maximal de ressources <br> qu'une session peut utiliser|
|**`CPU_PER_SESSION`**|Limite totale de temps CPU <br> qu'une session peut utiliser|
|**`CPU_PER_CALL`**|Limite de temps CPU qu'un <br> appel peut utiliser|
----
## Commandes
| Action | Commande |
-|-|
|Créer| `CREATE` <table><tr><th>Action<th>Commande<tr><td>Nouvel utilisateur<td>`USER `**`username`**` IDENTIFIED BY`**` "password"`**<tr><td>Nouveau rôle<td>`ROLE`**`nom_du_role`**<tr><td>Créer un profil<td>`PROFILE`**`nom_profil`**`LIMIT`</table>|
|Montrer le nom de la session|`SHOW CON_NAME`|
|Changer de session|`ALTER SESSION SET CONTAINER = `**`session`**|
|Donner des privilèges|`GRANT`**`commande`**`TO`**`username`**<br>ou<br>`GRANT`**`commande`**`TO`**`role`**<table><tr><th>Privilège</th><th>Commande</th></tr><tr><td>Se connecter à la *bd*<td>**`CREATE SESSION`**<tr><td>Créer une table<td>**`CREATE TABLE`**<tr><td>Donner un rôle<td>**`nom_du_role`**<tr><td>Donner permissions à un rôle<td>**`permission1,permission2...permissionN`**<br>`TO`**`role`**</table> Ajouter des permissions pour une table spécifique <br> `GRANT commande`**`ON table`**`TO target`|



# Légende
|Abbréviation|Signification|
|-|-|
|*bd*|**B**ase de **D**onnées|
|*DBA*|**D**ata**B**ase **A**dminitrator