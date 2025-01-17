Q.2.3.2  
Nous pouvons voir que le type de système de stockage est raid1 pour md0 et lvm (Logical volume management) pour cp3 sous md0p5.

Q.2.4.1  
bareos-dir agit en tant que contrôleur du système de sauvegarde du réseau.  
bareos-sd  reçoit et stocke les données du File Daemon sur les supports de sauvegarde configurés.  
bareos-fd  s'exécute sur le client pour sauvegarder et restaurer les données selon les instructions de bareos-dir.  

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

