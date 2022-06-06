Sur un serveur, on prévoit de créer : 
- un volume nommé "Données" en RAID 5, capacité 6 Go, accessible depuis le lecteur D:\
- un volume miroir de 4 Go monté dans C:\INFO-TOOLS et reposant sur les disques 0 et 2
- un volume nommé "Database", capacité 8 Go, optimisé pour les performances en lecture/écriture, accessible via le lecteur E:\

Ouvrir la console de gestion des disques en tapant "diskmgmt.msc" dans "exécuter". En faisant un clic droit sur le Disque 0, un menu apparaît. 
Cliquer sur "Initialiser le disque" : 

PARTITIONNER EN RAID 5

![image](https://user-images.githubusercontent.com/105868197/172156790-679cd58e-6b63-4fe5-a1e4-6bf165e0b797.png)

Ensuite, en faisant un clic droit sur le Disque 0, le menu suivant apparaît : 

![image](https://user-images.githubusercontent.com/105868197/172157336-fed73b1f-aacc-4548-9e5a-08f1af513a10.png)

Cliquer sur "Nouveau Volume RAID-5". Comme il s'agit de RAID 5, il faut sélectionner au moins 3 disques pour que ça fonctionne.

![image](https://user-images.githubusercontent.com/105868197/172157846-137b537e-eabc-4fc4-a29b-135beaeb704f.png)

On lui attribue ensuite la lettre D, et le système de fichiers NTFS.

![image](https://user-images.githubusercontent.com/105868197/172158029-f0b7de6e-b7d2-4b4d-b44e-6c4db0454052.png)

Notre partitionnement apparaît ainsi : 

![image](https://user-images.githubusercontent.com/105868197/172158315-3810c76c-bbdd-4767-b6a3-9bf214fabb49.png)

PARTITIONNER EN VOLUME MIROIR
En faisant un clic droit sur l'espace vide de 4 Go du Disque 0, on choisit "Nouveau volume en miroir". 
Il faut sélectionner au moins deux disques pour créer ce type de volumes, donc on choisit les disques 0 et 2 comme spécifié. 
Au moment d'attribuer la lettre, comme on souhaite accéder à ce volume depuis C:\INFO-TOOLS, on choisit : "Monter dans le dossier NTFS vide suivant".

![image](https://user-images.githubusercontent.com/105868197/172159572-7c9e155e-d7fc-40d3-bc14-57131a7fbbe7.png)

Voilà, à présent, comment apparaît notre partitionnement : 

![image](https://user-images.githubusercontent.com/105868197/172159860-ed01031d-48f6-4f0a-b081-bc8803eec87c.png)

Pour notre dernier volume, on choisit le volume agrégé par bandes.

SIMULATION DE PANNES

Après avoir crée des fichiers un peu partout dans nos lecteurs, on supprime notre disque SCSI n°3.
On peut ensuite en rajouter un et faire un clic droit sur l'ancien disque, puis "Réparer".


