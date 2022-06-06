Sur un serveur, on prévoit de créer : 
- un volume nommé "Données" en RAID 5, capacité 6 Go, accessible depuis le lecteur D:\
- un volume miroir de 4 Go monté dans C:\INFO-TOOLS et reposant sur les disques 1 et 3
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


