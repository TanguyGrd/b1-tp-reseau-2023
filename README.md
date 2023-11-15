# b1-tp-reseau-2023
## 🌞 Affichez les infos des cartes réseau de votre PC
```
Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::4fda:d2ef:336f:c0a7%8
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.78.60
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0
   Passerelle par défaut. . . . . . . . . : 10.33.79.254

   ```
   ```
   Carte Ethernet Ethernet :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::ef3d:c54c:dda4:b048%21
   Adresse d’autoconfiguration IPv4 . . . : 169.254.97.236
   Masque de sous-réseau. . . . . . . . . : 255.255.0.0
   Passerelle par défaut. . . . . . . . . :
   ```

## 🌞 Affichez votre gateway

    ```Passerelle par défaut. . . . . . . . . : 10.33.79.254 ```

## 🌞 Déterminer la MAC de la passerelle
```
     10.33.79.254          7c-5a-1c-d3-d8-76     dynamique
```

## 🌞 Trouvez comment afficher les informations sur une carte IP (change selon l'OS)
```
en utilisant le cmd:
  - utiliser la commande ipconfig ou ipconfing /all (pour plus d'info)
 Adresse IPv4. . . . . . . . . . . . . .: 10.33.78.60(préféré)
 Passerelle par défaut. . . . . . . . . : 10.33.79.254
  Adresse physique . . . . . . . . . . . : 28-6B-35-F0-78-A0
  ```
 
  ## 🌞 Il est possible que vous perdiez l'accès internet.
```
pour reprendre l'exemple : Lorsqu'une personne à l'extérieur envoie une lettre (données) à cette adresse, le facteur (routeur ou commutateur) est confus, car il ne sait pas quelle maison est la bonne destination.
autrement dit il est possible de perdre son accès car l'IP que nous avons rentré manuellement est peut être déjà prise
```

## 🌞modifiez l'ip de 2 machines pour qu'elle soit dans le meme reseau 

```
Cliquez avec le bouton droit de la souris sur l'icône du réseau dans la barre des tâches, puis sélectionnez "Ouvrir les paramètres réseau et Internet".

Cliquez sur "Modifier les options d'adaptateur".

Cliquez avec le bouton droit de la souris sur la carte réseau que vous souhaitez configurer et sélectionnez "Propriétés".

Sélectionnez "Protocole Internet version 4 (TCP/IPv4)" dans la liste, puis cliquez sur "Propriétés".

Puis changer L'ip et le masque reseau 
```
