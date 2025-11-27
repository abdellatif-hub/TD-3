
## Exercice 1

**1. Différence entre ring 0 et ring 3**  
- **Ring 0 :** niveau de privilège maximal — utilisé par le noyau (kernel).  
- **Ring 3 :** niveau utilisateur — utilisé par les applications (accès restreint).

**2. Pourquoi une application ne peut pas contrôler l’OS ?**  
Parce qu’elle s’exécute en **ring 3** sans privilèges matériels ; l’accès direct au matériel est bloqué pour assurer sécurité et stabilité.

**3. Guest OS**  
Système d’exploitation *invité* exécuté dans une machine virtuelle (VM).

---

## Exercice 2

**1. Différence entre hyperviseur Type I et Type II**  
- **Type I (bare-metal)** : installé directement sur le matériel (meilleures performances).  
- **Type II (hosted)** : installé sur un OS hôte (plus simple d’usage mais moins performant).

**2. Exemples**  
- *Type I* : VMware ESXi, Microsoft Hyper-V, Xen.  
- *Type II* : VirtualBox, VMware Workstation, Parallels Desktop.

---

## Exercice 3

**1. Deux caractéristiques de la virtualisation complète**  
- Le **Guest OS n’a pas besoin d’être modifié**.  
- Le matériel est **émulé intégralement**.

**2. Pourquoi la para-virtualisation modifie le noyau invité ?**  
Parce que le Guest OS doit être *conscient* de l’environnement virtuel et remplacer certaines opérations matériel par des **hypercalls**.

**3. Avantage / Inconvénient**  
- **Avantage :** meilleures performances (moins d’émulation).  
- **Inconvénient :** nécessite modification du Guest OS → compatibilité réduite.

---

## Exercice 4

**1. Principe du partitionnement**  
Le matériel est **découpé en partitions physiques** (CPU, mémoire, I/O) et chaque partition exécute son propre OS.

**2. Pourquoi ce type ne permet pas d’exécuter Windows ?**  
Car le partitionnement ne fournit pas l’abstraction matérielle complète nécessaire pour certains OS commerciaux ; la compatibilité n’est pas garantie.

---

## Exercice 5

**1. Technologies Intel/AMD pour la virtualisation matérielle**  
- **Intel VT-x**  
- **AMD-V**

**2. Rôle du ring −1**  
Niveau réservé à l’**hyperviseur** (plus privilégié que ring 0 invité) pour contrôler et isoler les OS invités.

**3. Que fait l’instruction `VMXON` ?**  
Active le mode de virtualisation matérielle Intel (VT-x) sur le processeur.

---

## Exercice 6

**1. Qu’est-ce que le cloisonnement ?**  
Création d’environnements isolés (containers) au sein d’un même noyau.

**2. Avantages / Inconvénients**  
- *Avantages :* léger, démarrage rapide.  
- *Inconvénients :* isolation moins forte que VMs ; tous partagent le même noyau.

**3. Exemple**  
Docker, LXC, FreeBSD Jails.
