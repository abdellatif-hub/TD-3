Rapport du TD 3
🧩 Exercice 1
1. Différence entre ring 0 et ring 3

Ring 0 : niveau de privilège maximal, utilisé par le noyau.

Ring 3 : niveau le plus faible, utilisé par les applications.

2. Pourquoi une application ne peut pas contrôler le système d’exploitation ?

Parce qu’elle fonctionne en ring 3 et n’a pas les privilèges nécessaires pour accéder directement au matériel.

3. Signification de « Guest OS »

Un Guest OS est un système d’exploitation invité qui tourne dans une machine virtuelle.

🧩 Exercice 2
1. Différence entre hyperviseur Type I et Type II

Type I (bare-metal) : fonctionne directement sur le matériel.

Type II (hosted) : fonctionne au-dessus d’un OS hôte.

2. Exemples

Type I : VMware ESXi, Hyper-V Server.

Type II : VirtualBox, VMware Workstation.

🧩 Exercice 3
1. Deux caractéristiques de la virtualisation complète

Le Guest OS n’a pas besoin d’être modifié.

Le matériel est totalement émulé.

2. Pourquoi la para-virtualisation nécessite la modification du noyau invité ?

Parce que le Guest OS doit être capable d'utiliser des hypercalls au lieu d’instructions non autorisées.

3. Avantage et inconvénient de la para-virtualisation

Avantage : meilleures performances.

Inconvénient : nécessite un Guest OS modifié (ex : Windows non compatible).

🧩 Exercice 4
1. Principe de la virtualisation par partitionnement

Le matériel est divisé en partitions physiques et chaque partition exécute un OS différent.

2. Pourquoi ce type ne permet pas d’exécuter Windows ?

Parce qu’il ne fournit pas une émulation matérielle complète, seulement un partage du matériel.

🧩 Exercice 5
1. Technologies Intel et AMD pour la virtualisation

Intel VT-x

AMD-V

2. Rôle du ring -1

Il permet à l’hyperviseur d’avoir un niveau de privilège supérieur au noyau invité.

3. Rôle de l’instruction VMXON

Active le mode de virtualisation matérielle Intel VT-x.

🧩 Exercice 6
1. Qu’est-ce que le cloisonnement ?

C’est la création d’environnements isolés dans un même OS (ex : containers).

2. Avantages et inconvénients

Avantages :

Très léger

Rapide à lancer

Inconvénients :

Isolation plus faible

Dépend du même noyau pour tous les environnements

3. Exemple de technologie

Docker

LXC

FreeBSD Jails
