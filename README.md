### Découpage de réseaux IP ###
Leréseau 172.16.1.0/24

*** Découpge Symétrique ***
/24 veut dire que 225.225.225.00000000
Dans notre exercice on veut diviser le réseau en 4 et nous choisissons le département avec plus d’équipements (50). 
Pour avoir 50, il faut faire 2 puissance 6 qui est égale à 64, moins 2 égale à 62 hosts valables. 
Donc notre masque devient: 225.225.225.11000000 -> 225.225.225.192 soit /26. 
LA taille ne notre réseau est 64

 *** Le 1er réseau disponible est : ***
172.16.1.0/26
* First host: 172.16.1.1 
* Last  host: 172.16.1.62
* Broadcast address: 172.16.1.63

*** Le 2eme réseau disponible est : ***
172.16.1.64/26
* First host: 172.16.1.65 
* Last  host: 172.16.1.126
* Broadcast address: 172.16.1.127

*** Le 3eme réseau disponible est : ***
172.16.1.128/26
* First host: 172.16.1.129 
* Last  host: 172.16.1.190
* Broadcast address: 172.16.1.191

*** Le 4eme réseau disponible est:
172.16.192.0/26
* First host: 172.16.1.193 
* Last  host: 172.16.1.254
* Broadcast address: 172.16.1.255

*** Découpage Asymétrique ***

Nous avons le réseau 172.16.1.0/24 
Pour le Pole informatique, il faut 50 équipements. 
Pour avoir 50, il faut 2 puissance 6 qui est égale à 64. 64 - 2 = 62. Donc, il nous faut 6 bits à 0 et 2 bits à 1 dans la 4eme octet du mask, ce qui nous donne 255.255.255.11000000 soit 255.255.255.192 ou /26. La taille du réseau sera 256-192 = 64. 
*** Notre réseau Pole informatique sera: ***
172.16.1.0/26
* Allocated size: 62 
* Needed size: 50
* First host: 172.16.1.1 
* Last  host: 172.16.1.62
* Broadcast address: 172.16.1.63

|:-:Subnet Name |:-:Needed size|:-:Allocated Size|:-:Address|:-: Mask  |:-: Dec Mask | :-: Assignable Range |:-: Broadcast |  
|:-: Pole informatique |:-:50  |:-:62 |:-:172.16.1.0|:-:/26 |:-: 255.255.255.192|:-:172.16.1.1 - 172.16.1.62|:-:172.16.1.63|

