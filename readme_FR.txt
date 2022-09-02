Nessie Viewer 

L'application Nessie Viewer permet aux auditeurs en s�curit� des syst�mes
de charger un ou plusieurs rapports Nessus (fichiers au format XML v2), afin 
d'y naviguer et d'ex�cuter rapidement des actions sur les enregistrements 
qu'ils contiennent. Un m�canisme de filtres permet de trouver tr�s rapidement
des entr�es, tandis que des listes cliquables de machines correspondant � tel
ou tel crit�re peuvent �tre g�n�r�es. 

Exemples de traitements r�alis�s en un clic : 
- Affichage de la liste des ports ouverts par machine 
- Affichage de la liste des patchs manquants par machine 
- Affichage de la liste des IP poss�dant la vuln�rabilit� MSXX-XX 
- Affichage de la liste des IP �coutant sur un port donn� 
- G�n�ration de la liste des IP utilisant un service web donn� 



------------------------------ 
Principales fonctionnalit�s 
------------------------------ 


* Affichage des informations sur une machine, regroup�es par cat�gories 
 |-> Action : Double-cliquer sur l'adresse IP ou le hostname en question dans la 
table principale 


* G�n�ration de listes de ports ouverts par machine 

Action : Menu 'Generate' -> 'Generate open ports' 

 Exemples : 
 192.168.0.110 (20) - 80,135,137,139,445,1037,1039,1494,1551,2301,2381,2512,2513,
    2967,3389,13722,13724,13782,13783,49400 
 192.168.10.15 (15) - 80,135,137,139,445,1033,1038,1494,1938,2301,2381,2512,2513,
    2967,3389 
 10.10.0.100 (16) - 9,13,17,19,80,135,445,1034,1040,1088,1494,2301,2381,2967,3389 


* G�n�ration de la liste des patchs Microsoft manquants sur les machines 
scann�es 

Action : Menu 'Generate' -> 'Generate patch list' 

 Exemples : 
 192.168.0.110 - MS08-067,MS09-001,MS06-035 
 192.168.10.15 - MS08-067,MS06-035,MS09-001 
 10.10.0.100 - MS08-067,MS09-001,MS06-035 

 

* G�n�ration de listes d'adresses IP correspondant � une condition 
 
Action : cliquer sur une entr�e du tableau (port, service, operating system, 
         plugin id, plugin name) 

 Exemples : 
 - G�n�ration de la liste des machines �coutant sur le port 1521 
   |-> double-cliquer sur le port 1521 de la colonne "port" de la table 
 - G�n�ration de la liste des machines poss�dant un service web 
   |-> double-cliquer sur la case "www" de la colonne "service" de la table 
 - G�n�ration de la liste des machines "Microsoft Windows 2000 Service Pack 2" 
   |-> double-cliquer sur la case "Microsoft Windows Server 2003 Service Pack 2" de 
   la colonne OS 

   
   
* G�n�ration de liens cliquables avec la possibilit� de choisir un programme 
personnalis� pour ouvrir le lien 

Action : Menu 'Generate' -> 'Generate links' -> Type de lien � g�n�rer 

 Exemples : 
 - http://192.168.0.110:3872 
 - http://192.168.10.15:1980
 - http://10.10.0.100:1080 



------------------------------ 
Configuration avanc�e
------------------------------ 

Le fichier config.np, plac� dans le r�pertoire des donn�es de l'application 
(user App data), permet de modifier la fa�on dont les liens sont g�n�r�s ainsi 
que les programmes appel�s lorsque ces liens sont cliqu�s. 

Le fichier config_regexp.np, plac� dans le r�pertoire des donn�es de 
l'application (user App data), indique la facon dont les r�sultats des plugins 
(plugin output) sont analys�s. C'est par exemple dans ce fichier que sont 
int�gr�es les expressions r�guli�res permettant de g�n�rer, � partir des plugins 
d'�num�ration SMB, les listes d'utilisateurs sur des syst�mes Windows. 

Les modifications apport�es � ces fichiers de configuration sont prises en  compte sans red�marrer l'application. 




------------------------------ 
Compatibilit� et pr�requis
------------------------------ 

- Windows XP SP2 ou sup�rieur 
- .NET Framework 3.5 ou sup�rieur 



------------------------------ 
Suggestions et feedback 
------------------------------ 

Pour toute suggestion ou feedback, n'h�sitez pas � nous contacter sur secviewlab_a-t_gmail


