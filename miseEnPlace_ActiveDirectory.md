Pour réaliser cette mise en place d'Active Directory, on utilise une VM avec Windows Server 2019.

**CREATION D'UN CONTEXTE DE DOMAINE ACTIVE DIRECTORY**

**AJOUT DU ROLE ACTIVE DIRECTORY **

Dans Gestionnaire de serveur, cliquer sur "Gérer" puis "Ajouter des rôles et fonctionnalités".
Cliquer sur "suivant". Sur la fenêtre "type d'installation", cliquer sur suivant. Sur la fenêtre "Sélection du serveur", cliquer encore sur "Suivant".
Dans la fenêtre "Sélectionner des rôles de serveurs", cocher le bouton "Services AD DS". 

Une fenêtre s'ouvre : 

![image](https://user-images.githubusercontent.com/105868197/172636531-0eb410d4-d769-4a75-93a1-aea5dfe19e16.png)

Cliquer sur "Ajouter des fonctionnalités".

Cliquer à nouveau sur le bouton "Suivant". Sur la fenêtre "Sélectionner des fonctionnalités", cliquer encore une fois sur "Suivant", et encore une fois sur la fenêtre "Services de domaine Active Directory".
Dans la fenêtre "Confirmer les sélections d'installations, cocher la case suivante : 

![image](https://user-images.githubusercontent.com/105868197/172637224-d4eb267d-3fcd-4b88-b502-43213f810f0c.png)

Puis cliquer sur le bouton "Oui" de la fenêtre contextuelle qui apparaît.

Cliquer enfin sur le bouton "Installer", puis "FERMER".

**CREATION D'UNE FORET **

Cliquer sur le drapeau qui vient d'apparaître sur le Tableau de bord.

![image](https://user-images.githubusercontent.com/105868197/172637980-bef7bde5-2cf3-42f4-9006-971b649573a7.png)

Cliquer ensuite sur "Promouvoir ce serveur en contrôleur de domaine".

![image](https://user-images.githubusercontent.com/105868197/172638102-f9a8541a-45ec-4ed8-8ddd-11f7885a1636.png)


