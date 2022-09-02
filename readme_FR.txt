Nessie Viewer 

L'application Nessie Viewer permet aux auditeurs en sécurité des systèmes
de charger un ou plusieurs rapports Nessus (fichiers au format XML v2), afin 
d'y naviguer et d'exécuter rapidement des actions sur les enregistrements 
qu'ils contiennent. Un mécanisme de filtres permet de trouver très rapidement
des entrées, tandis que des listes cliquables de machines correspondant à tel
ou tel critère peuvent être générées. 

Exemples de traitements réalisés en un clic : 
- Affichage de la liste des ports ouverts par machine 
- Affichage de la liste des patchs manquants par machine 
- Affichage de la liste des IP possédant la vulnérabilité MSXX-XX 
- Affichage de la liste des IP écoutant sur un port donné 
- Génération de la liste des IP utilisant un service web donné 



------------------------------ 
Principales fonctionnalités 
------------------------------ 


* Affichage des informations sur une machine, regroupées par catégories 
 |-> Action : Double-cliquer sur l'adresse IP ou le hostname en question dans la 
table principale 


* Génération de listes de ports ouverts par machine 

Action : Menu 'Generate' -> 'Generate open ports' 

 Exemples : 
 192.168.0.110 (20) - 80,135,137,139,445,1037,1039,1494,1551,2301,2381,2512,2513,
    2967,3389,13722,13724,13782,13783,49400 
 192.168.10.15 (15) - 80,135,137,139,445,1033,1038,1494,1938,2301,2381,2512,2513,
    2967,3389 
 10.10.0.100 (16) - 9,13,17,19,80,135,445,1034,1040,1088,1494,2301,2381,2967,3389 


* Génération de la liste des patchs Microsoft manquants sur les machines 
scannées 

Action : Menu 'Generate' -> 'Generate patch list' 

 Exemples : 
 192.168.0.110 - MS08-067,MS09-001,MS06-035 
 192.168.10.15 - MS08-067,MS06-035,MS09-001 
 10.10.0.100 - MS08-067,MS09-001,MS06-035 

 

* Génération de listes d'adresses IP correspondant à une condition 
 
Action : cliquer sur une entrée du tableau (port, service, operating system, 
         plugin id, plugin name) 

 Exemples : 
 - Génération de la liste des machines écoutant sur le port 1521 
   |-> double-cliquer sur le port 1521 de la colonne "port" de la table 
 - Génération de la liste des machines possédant un service web 
   |-> double-cliquer sur la case "www" de la colonne "service" de la table 
 - Génération de la liste des machines "Microsoft Windows 2000 Service Pack 2" 
   |-> double-cliquer sur la case "Microsoft Windows Server 2003 Service Pack 2" de 
   la colonne OS 

   
   
* Génération de liens cliquables avec la possibilité de choisir un programme 
personnalisé pour ouvrir le lien 

Action : Menu 'Generate' -> 'Generate links' -> Type de lien à générer 

 Exemples : 
 - http://192.168.0.110:3872 
 - http://192.168.10.15:1980
 - http://10.10.0.100:1080 



------------------------------ 
Configuration avancée
------------------------------ 

Le fichier config.np, placé dans le répertoire des données de l'application 
(user App data), permet de modifier la façon dont les liens sont générés ainsi 
que les programmes appelés lorsque ces liens sont cliqués. 

Le fichier config_regexp.np, placé dans le répertoire des données de 
l'application (user App data), indique la facon dont les résultats des plugins 
(plugin output) sont analysés. C'est par exemple dans ce fichier que sont 
intégrées les expressions régulières permettant de générer, à partir des plugins 
d'énumération SMB, les listes d'utilisateurs sur des systèmes Windows. 

Les modifications apportées à ces fichiers de configuration sont prises en  compte sans redémarrer l'application. 




------------------------------ 
Compatibilité et prérequis
------------------------------ 

- Windows XP SP2 ou supérieur 
- .NET Framework 3.5 ou supérieur 



------------------------------ 
Suggestions et feedback 
------------------------------ 

Pour toute suggestion ou feedback, n'hésitez pas à nous contacter sur secviewlab_a-t_gmail


