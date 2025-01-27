# 💪 Challenge

## Exercice 1 : Manipulations pratiques sur VM Windows (temps estimé : 1h30)  

### Partie 1 : Gestion des utilisateurs

$${\color{red}Q.1.1.1}$$ Ok  

$${\color{red}Q.1.1.2}$$ Ok  

$${\color{red}Q.1.1.3}$$  Ok    

$${\color{red}Q.1.1.4}$$ Ok   


### Partie 2 : Restriction utilisateurs  

$${\color{red}Q.1.2.1}$$ Ok 
 
$${\color{red}Q.1.2.2}$$ Ok  

$${\color{red}Q.1.2.3}$$ Ok   
 

### Partie 3 : Lecteurs réseaux

Q.1.3.1 Créer une GPO Drive-Mount qui monte les lecteurs E: et F: sur les clients.

![Capture d'écran 2025-01-27 150448](https://github.com/user-attachments/assets/2f4c3561-9316-4a67-a820-d648b15a4372)

---  
---
## Exercice 2 : Manipulations pratiques sur VM Linux (temps estimé : 2h30)

### Partie 1 : Gestion des utilisateurs  

$${\color{red}Q.2.1.1}$$ Ok  

Q.2.1.2 Quelles préconisations proposes-tu concernant ce compte ?  

Mon compte est un compte personnel , je choisis donc d'appliquer le principe de moindre privilèges , et je choisis un mot de passe robuste que je change de façon régulière . Je déplace mon compte dans le groupe users . 

### Partie 2 : Configuration de SSH

$${\color{red}Q.2.2.1}$$ Ok  

$${\color{red}Q.2.2.2}$$ Ok  

$${\color{red}Q.2.2.3}$$ Ok  

### Partie 3 : Analyse du stockage  

Q.2.3.1 Les systèmes de fichiers actuellement montés sont ext2 et ext4  

![Q 2 3 1](https://github.com/user-attachments/assets/c08c1497-d042-4d6a-bc25-9a55ac27bf2c)

Q.2.3.2 Quel type de système de stockage ils utilisent ?  

![Q 2 3 2](https://github.com/user-attachments/assets/1af9535c-2e72-47db-8753-9a9cb71564b6)

$${\color{red}Q.2.3.3}$$ Ok  

$${\color{red}Q.2.3.4}$$ Ok   

$${\color{red}Q.2.3.5}$$ Ok  

### Partie 4 : Sauvegardes  

$${\color{red}Q.2.4.1}$$ Ok  

### Partie 5 : Filtrage et analyse réseau
$${\color{red}Q.2.5.1}$$ Ok  

Q.2.5.2 Quels types de communications sont autorisées ?  
 - ct state established,related acceptautoriser les connexions établies
 - iifname "lo" acceptautoriser le trafic de bouclage
 - tcp dport 22 acceptautoriser les connexions TCP destinées au port 22 (port SSH)
 - ip protocol icmp acceptautoriser les paquets ICMPV4
 - ip6 nexthdr icmpv6 acceptautoriser les paquets ICMPV6

Q.2.5.3 Quels types sont interdit ?  
ct state invalid drop: paquets ne pouvant pas être identifiés et tout le reste  

Q.2.5.4 Sur nftables, ajouter les règles nécessaires pour autoriser bareos à communiquer avec les clients bareos potentiellement présents sur l'ensemble des machines du réseau local sur lequel se trouve le serveur.  
![Capture d'écran 2025-01-27 153303](https://github.com/user-attachments/assets/8bab7955-6d77-4a00-87af-250ddb1d6078)

