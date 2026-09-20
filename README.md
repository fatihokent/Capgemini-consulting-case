Ce projet a été réalisé en plusieurs étapes :
1. Une présentation de la société Capgemini
Une introduction claire sur ce que l'entreprise, dans ce cas Capgemini, peut apporter au client grâce à son écosystème technologique, ses multiple projets ainsi que son envergure mondiale

2. Une cartographie des actifs et risques
Lors de cette étape, une étude est réalisée pour déterminer les actifs les plus critiques par exemple la base de données des clients, le serveur DPI ou le réseau du bloc opératoire. Celle-ci permet de classer chaque actif par niveau de criticité en fonction de la triade CIA.
Par la suite, une multitude de scénarios sont émis pour ne pas avoir de surprise et être préparé au maximum, les scénarios sont classés dans une matrice, les points sont calculés avec la formule suivante :
## Probalité X Impact ##
- La probalité représente la mesure de la chance qu'un événement indésirable.
- L'impact quant à lui reflète l'importance des conséquences ou des dégâts si le scénario se réalise.
![matrice_risque](/matrice_risque.png)

3. Stratégies de traitement et plan d'action
Pour chaque risque, il y aura une stratégie à suivre selon le cas :
- Réduction :
  On déploie des mesures afin de réduire le risque comme le déploiement d'un WAF, opter pour une micro-segmentation.
- Évitement :
 Suppression de la surface d'attaque, ex: un remplacement de VPN obsolète par une architecture ZTNA.
- Transfert :
  Souscrire à une assurance cyber afin de couvrir la responsabilité civile, et ainsi le risque sera transféré vers un acteur tiers.
- Acceptation :
  Le risque est acceptée car son impact est minime.

4. L'architecture à réaliser
L'architecture proposée est répartie en 3 zones : la zone LAN qui fait référence à celle du réseau interne où se trouve les actifs les plus sensibles.
La zone DMZ (zone dématérialisée) : qui représente une zone intermédiaire où se trouvent les actifs qui ont besoin d'être connectés à Internet.
La zone Internet c'est la partie que tout le monde connaît. Les différentes zones sont connectés par des pare-feu afin de contrôler le traffic entrant et sortant.

5. Preuve de concept
Une suite de tests est exécutée sur Packet Tracer pour vérifier la robustesse de l'architecture. Dans ce cas, il y a 5 tests :
- Lab 1 pour tester la continuité et la redondance : si par exemple l'un des routeurs tombent en panne, l'autre doit être en mesure de maintenir la connexion.
- Lab 2 pour vérifier la connexion à distance : une connexion SSL par un VPN est obligatoire pour les médecins à distance.
- Lab 3 afin de contrôler les flux du traffic à l'aide de filtrage NAT et les listes ACL.
- Lab 4 qui a pour but de tracer toutes les actions effectuées au sein du système grâce à un SIEM et les logs.
- Lab 5 qui protège l'infrastructure interne avec une neutralisation des menaces grâce au principe du DHCP Snooping.
