# <ins>**Créer des VLAN**<ins>
Sur Cisco Packet Tracer, on installe 4 PC reliés à 1 switch. On souhaite créer "VLAN 10", qui comprendra PC 0 et PC1, et VLAN 20, qui comprendra PC2 et PC3.
  
  
![Capture](https://user-images.githubusercontent.com/105868197/171627772-332a75e8-dc9e-4b5a-beda-ace800546cd8.PNG)



**Etape 1 : créer les VLAN**
```
enable
configure terminal
vlan 10
name Administration
end
configure terminal
vlan 20
name Education
end
```

**Etape 2 : Leur affecter des ports **
  
Si l'on laisse le curseur de la souris sur le switch, on se rend compte que le VLAN 1 a été affecté à tous les ports par défaut. 
PC0 et PC1 sont branchés aux ports FastEthernet 0/1 et FastEthernet0/2, donc on affecte ces ports au VLAN 10 : 
```  
enable 
configure terminal
interface FastEthernet0/1
switchport mode access
switchport access vlan 10
end
interface FastEthernet0/2
switchport mode access
switchport access vlan 10
```
PC2 et PC3 sont branchés aux ports FastEthernet 0/3 et Fast Ethernet 0/4, donc on affecte ces ports au VLAN 20 :
```
enable 
configure terminal
interface FastEthernet0/1
switchport mode access
switchport access vlan 20
end
interface FastEthernet0/2
switchport mode access
switchport access vlan 20
```
**Etape 3 : Vérifications**

Pour s'assurer que nos deux VLAN sont maintenant bien affectés aux premiers ports du switch, on tape la commande : 
show vlan brief
Elle affiche le résultat suivant :
```
  
VLAN Name                             Status    Ports

1    default                          active    Fa0/5, Fa0/6, Fa0/7, Fa0/8
                                                Fa0/9, Fa0/10, Fa0/11, Fa0/12
                                                Fa0/13, Fa0/14, Fa0/15, Fa0/16
                                                Fa0/17, Fa0/18, Fa0/19, Fa0/20
                                                Fa0/21, Fa0/22, Fa0/23, Fa0/24
                                                Gig0/1, Gig0/2
10   Administration                   active    Fa0/1, Fa0/2
20   Education                        active    Fa0/3, Fa0/4
1002 fddi-default                     active    
1003 token-ring-default               active    
1004 fddinet-default                  active    
1005 trnet-default                    active    
```
  
On peut notamment faire un ping du PC0 au PC4 ainsi que du PC3 au PC1 par exemple ; puis faire un ping de PC0 à PC1 et de PC3 à PC4. Si les premiers pings échouent et les seconds réussissent, 
alors notre configuration est réussie.

