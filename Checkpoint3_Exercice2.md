# Partie 1 : Gestion des utilisateurs  
Q.2.1.1  
![Q 2 1 2](https://github.com/user-attachments/assets/9bdbc4e1-ac1a-404b-a185-f6094786d25f)  

Q.2.1.1  
Je recommande d'utiliser un mot de passe fort avec des caractères spéciaux et d'une longueur d'au moins 8, c'est pourquoi j'ai choisi Azerty1*.

# Partie 2 : Configuration de SSH  
Q.2.2.1  
![SSHDCONFIG](https://github.com/user-attachments/assets/02061d51-c175-4e69-9ab5-b20fc108568e)  
![Q 2 2 1](https://github.com/user-attachments/assets/060ecd8b-dfc9-4fca-b5c3-79978ca37c50)  
![Q 2 2 15](https://github.com/user-attachments/assets/b24874e0-d295-4605-b30a-abfa268401c7)  

Q.2.2.2  
![Q 2 2 2](https://github.com/user-attachments/assets/c4db07a5-bc76-4aa7-aa9f-f6d1f3ab1d07)  
![Q 2 2 15](https://github.com/user-attachments/assets/ca67a43e-0bd2-4a42-a714-7615112f96b6)  

Q.2.2.3  
![Q 2 2 3](https://github.com/user-attachments/assets/20aafe28-8210-4c9e-baee-ebd487639654)  
![Q 2 2 3 1](https://github.com/user-attachments/assets/fd62a182-5d3b-4995-b6ff-5edade98a51d)  
![SSHDCONFIG](https://github.com/user-attachments/assets/1a723dc9-7fe5-4ef0-ba1d-ee8d3a90a7b7)
![Q 2 2 3 2](https://github.com/user-attachments/assets/fb663fde-da69-4702-9f14-1d47ef3fabfd)
![Q 2 2 3 3](https://github.com/user-attachments/assets/78152264-4eed-4ded-9d36-f2ad2a5247cf)  
![Q 2 2 3 4](https://github.com/user-attachments/assets/9b2c2be5-60d5-44a3-9794-5c9c0517c9c9)  

# Partie 3 : Analyse du stockage  
Q.2.3.1  
![Q 2 3 1](https://github.com/user-attachments/assets/11f4fc0e-8d9b-4f9d-93dd-78d26a3bb76c)  
Nous pouvons voir que md0p1 et les deux cp3 sont montés.

Q.2.3.2  
Nous pouvons voir que le type de système de stockage est raid1 pour md0 et lvm (Logical volume management) pour cp3 sous md0p5.  

Q.2.3.3  
![Q 2 3 3](https://github.com/user-attachments/assets/10d91f26-1ced-4046-b5b0-206562e958de)  
![Q 2 3 3 1](https://github.com/user-attachments/assets/a2164cb7-e0b4-43b6-9a7b-4fec2e54dd4a)  
![Q 2 3 3 2](https://github.com/user-attachments/assets/1d600377-03e5-4a02-b216-af62c8f21b65)  

Q.2.3.4  
![Q 2 3 4](https://github.com/user-attachments/assets/526bd0de-a507-4ad5-b457-01b827de091f)  
![Q 2 3 4 1](https://github.com/user-attachments/assets/91f16120-f419-42ae-8254-60110b56db72)
![Q 2 3 4 15](https://github.com/user-attachments/assets/b23ac6f7-1725-4af9-beb7-807643c4e849)
![Q 2 3 4 2](https://github.com/user-attachments/assets/876af3b1-e4ef-4377-9f9a-2adc8238e96e)  
![Q 2 3 4 3](https://github.com/user-attachments/assets/c3738fb6-dd57-415d-bfe8-9e0846d5fe26)  

Q.2.3.5  
![Q 2 3 4 4](https://github.com/user-attachments/assets/bb31308a-c01e-47df-88ac-715afda983e7)
Nous pouvons constater qu'il y a 1,79 Go de libre dans le groupe de volumes.  

# Partie 4 : Sauvegardes  
Q.2.4.1  
bareos-dir agit en tant que contrôleur du système de sauvegarde du réseau.  
bareos-sd  reçoit et stocke les données du File Daemon sur les supports de sauvegarde configurés.  
bareos-fd  s'exécute sur le client pour sauvegarder et restaurer les données selon les instructions de bareos-dir.  

# Partie 5 : Filtrage et analyse réseau  

Q.2.5.1  
![Q 2 5 1](https://github.com/user-attachments/assets/8c501ee9-e0cc-4357-a874-57c52bc81eba)  
Règles de filtrage applicables à ipv4 et ipv6.  

Q.2.5.2  
Les communications acceptées sont :   
suivi des connexions préétablies (CT)   
iifname (comparaison avec le nom de l'interface)  
tcp dport 22  
protocole ip icmp  
ip6 nexthdr ipv6-icmp  

Q.2.5.3  
les communications interrompues sont :   
les suivi de connexion invalide (CT)   

Q.2.5.4  
nft add rule ip filter input ip saddr 192.168.1.0/24 tcp dport 9101 accept

# Partie 6 : Analyse de logs
Q.2.6.1  
![Q 2 6 1](https://github.com/user-attachments/assets/0951130d-81e5-4912-8039-7176243e9e07)  
Pour la date et l'heure, on a du 21 décembre à 14:47:19 jusqu'au 17 janvier à 11:37:38 mais nous n'avons pas trouvé d'adresse IP... ou seulement des tentatives de connexion.



