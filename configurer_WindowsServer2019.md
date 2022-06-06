On a installé l'image ISO de Windows Server 2019 standard sur deux machines virtuelles. 
Pour suivre le TP en question, quelques configurations sont à faire.

SYSPREP

Sysprep nous permettra de créer une image que l'on pourra par la suite déployer sur d'autres machines.

1. Dans "exécuter", chercher le logiciel sysprep : 

![image](https://user-images.githubusercontent.com/105868197/172115097-855171c5-2a6a-4a75-bed2-f05e71fb7bb4.png)


2 : Double-cliquer sur l'exécutable de sysprep : 

![image](https://user-images.githubusercontent.com/105868197/172115199-2c9cc697-58fd-473a-ac9b-3a88c031fa77.png)


3 : Sélectionner "Généraliser", puis "Redémarrer".

![image](https://user-images.githubusercontent.com/105868197/172115286-b77594d3-2e91-4f21-a059-d9442edc0285.png)


Il faut sélectionner "Généraliser" pour que l'image créée supprime les informations spécifiques à notre VM, et pour que l'image soit ainsi déployable sur plusieurs machines différentes.


RESEAU

On doit configurer nos machines selon le schéma suivant :

![image](https://user-images.githubusercontent.com/105868197/172117512-1176b379-84f6-4400-867b-ec322cb152ae.png)

NOTE : Pour lancer une session, il faut taper la combinaison Ctrl+Alt+Del, ce qui est difficile lorsqu'on a affaire à une machine virtuelle puisque la commande outrepasse le logiciel.
Pour y remédier, on peut faire un clic droit sur l'onglet de notre machine, et cliquer sur "Send Ctrl Alt Del"

![image](https://user-images.githubusercontent.com/105868197/172118122-25855d65-97f2-4a1b-9fa1-e6665be94bc9.png)

Pour modifier une adresse IP sur Windows Server 2019, on se rend dans le panneau de configuration, puis "Connexions réseaux" : 

![image](https://user-images.githubusercontent.com/105868197/172119366-19a13dfe-94a6-42c0-81d1-0a6c386ac9a8.png)

On fait ensuite un clic droit sur la connexion qui apparaît, puis "Propriétés". La fenêtre "Propriétés de Ethernet0 s'affiche ; là, on sélectionne le "Protocole Internet version 4" et on clique encore une fois sur le bouton "Propriétés".

![image](https://user-images.githubusercontent.com/105868197/172119820-f02ba91e-1890-4165-a513-d9b614a9c108.png)


Dans la fenêtre qui s'ouvre, on peut enfin renseigner une adresse IP, un masque de sous-réseau, une passerelle par défaut, et des adresses de serveur DNS :

![image](https://user-images.githubusercontent.com/105868197/172120850-07322b65-7def-44f4-bd33-987511f4e897.png)

Il ne faut pas oublier de cocher le bouton "Valider les paramètres en quittant", puis "Ok".


ROLES ET FONCTIONNALITES

INSTALLER IIS (INTERNET INFORMATION SERVICES)

Dans le Gestionnaire de serveur, cliquer sur "Gérer" puis "Ajouter des rôles et fonctionnalités" : 

![image](https://user-images.githubusercontent.com/105868197/172123455-90ac43e0-ed33-47ff-97b1-2dad46df0c3a.png)

Ensuite, sélectionner "Installation basée sur un rôle ou une fonctionnalité", puis "Suivant". Il faut ensuite sélectionner le serveur sur lequel on souhaite installer IIS. Dans la liste qui apparaît, on sélectionne le rôle "Serveur Web (IIS)".

![image](https://user-images.githubusercontent.com/105868197/172123968-220d4ba1-67f7-463c-8c08-e509719d05d4.png)

Après avoir cliqué sur "Suivant", on nous propose cette fois de sélectionner des rôles. On choisit alors (dans le cadre du TP) l'Outil de sauvegarde windows server.

![image](https://user-images.githubusercontent.com/105868197/172124324-63f8a9c0-a929-4277-9241-0a29af1f88e6.png)

L'assistant propose ensuite de sélectionner des "services de rôle". On clique ensuite sur "Installer".




