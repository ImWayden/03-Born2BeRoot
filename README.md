# 03-Born2BeRoot
Ce Readme contient tote les reponses aux question posable 
durant la correction de Born2BeRoot 
ATTENTION CETTE VERSION EST UN PREMIER JET ET PEUT NE PAS CORRESPONDRE A VOTRE SUJET
DE PLUS LES REPONSES N'ONT PAS ENCORE TOUTES ETE VALIDEE 
# Questions

## Project Overview
### Comment fonctionne une machine Virtuelle

une machine virtuelle est un environnement entièrement virtualisé qui fonctionne sur une machine physique. Elle exécute son propre système d’exploitation (OS) et bénéficie des mêmes équipement qu’une machine physique : CPU, mémoire RAM, disque dur et carte réseau.

### Quel est l'Os que vous avez choisit
 Debian ou CentOS
### La difference basic entre CentOS et Debian
Debian est developpe par la communaute linux tandis que CentOs est dev par directement a partir du code source de red Hat entreprise donc linux est plus adaptable tandis que Cents est plus stable car developper sur plus de temps

### Le but d'un machine virtuel
Tester un nouveau système d’exploitation sans avoir besoin de partitionner son disque dur.
Le test peut ainsi s’effectuer sans risques d’endommager le disque dur de votre machine.

Développer un logiciel ou un programme pour un autre système d’exploitation.

Se servir de logiciels qui ne peuvent pas tourner sur le système d’exploitation de votre machine 
physique. Vous pouvez ainsi disposer d’une machine virtuelle par système d’exploitation et même de plusieurs versions du même système d’exploitation.

Réaliser des économies en installant plusieurs machines virtuelles sur un seul support physique plutôt que de multiplier les ordinateurs en service.

### Si vous avez choisit CentOs, qu'est ce que SELinux et DNF
#### SELinux
(Security-Enhanced Linux) est une architecture de sécurité pour systèmes Linux® qui permet aux administrateurs de mieux contrôler les accès au système. 
SELinux définit les contrôles d'accès pour les applications, processus et fichiers d'un système. Il utilise des politiques de sécurité, c'est-à-dire des ensembles de règles qui lui indiquent ce à quoi un utilisateur peut accéder ou non, pour mettre en application les autorisations d'accès définies par une politique. 
source [redhat](https://www.redhat.com/fr/topics/linux/what-is-selinux)
### Sivous avez choisit Debian, qu'elle est la difference entre aptitude et apt, et c'est quoi APPArmor



## Simple setup
### Check si le service ufw est en cour
```

```
### Check si le service SSH est en cour
```

```
### Check que l'Os choisit soit bien debian ou CentOS
```

```
## User
### Check la presence d'un user portant votre login et son appartenance aux groupe sudo et user42
```

```
### Verifier que les regles concernant la politique de mots de passes fort a ete mises en place
Creer un nouvel utilisateur et lui assigner un mot respectant les regles
```

```
expliquer comment ca a ete mise place
```

```
creer un groupe nomer evaluating et y ajouter l'utilisateur nouvelement creer enfn checker que l'utilsateur fait bien partie du bon group
```

```
### Quels sont les avantages et desavantages de cette politique de mot passe

## Hostname and partition

### Checkque lehostname de lamachine est correct (login42)
```

```
### modifier le hostname et remolacer par le votre
```

```
### afficher les partitions de sa machine virtuelle
```

```
### How LVM Works 

## Sudo
### Check que sudo soit bien installe sur la VM
```

```
### assigner le nouvel utiisateur au groupe sudo
```

```
### expliquer la valeur et operation de sudo
    
### verifier /var/log/sudo/sudo + check le contenue de celui ci
```

```

## UFW
### Check si le service ufw est installee
```

```
### verifier qu'il fonctionne correctement
```

```
### expliquer l'utilite d'ufw
ufw est un firewall c'est a dire qu'il vas permettre de filtrer les connection entrante et sortante
l'interet c'est de ne pas laisser 'importe qui acceder a n'importe quoi

### ajouter une regle pour ouvrir le port 8080 et lister toute les regles actives

### supprimer la nouvelle regle

## SSH
### verifier que le ssh est installer
```
```
### verifier que c fonctionne
```

```
### expliquer l'utilite de ssh

### verifier que le ssh n'utilise que le port 4242
```
```
### se connecter a la vm via ssh et verifier que le rot user ne peut pas se connecter
Dans un terminl a part:
```
ssh localhost@[user] -p [port] 
```
le port 4242 etant utiliser vous avez du faire une derivatio, c'est ce prt qui vas dans [port]
[user] coorespond au nom d'utilisateur avec lequel vous voulez vous connecter si vous souhaitez tentez de vous connecter avec root remplacer [user] par root

## Script Monitoring

### expliquer comment fonctionne votre script
cela depend de votre monitoring.sh

### qu'est ce qu'est cron
cron est un programmeur de taches, il permet d'effectuer des commandes de maniere automatique
a condition que l'on est ajouter les regles correspondante dans 

### expliquer comment vous avez fait pour le script se lance toute les 10 min depuis le start serveur
```
```
### faire fonctionner le script toutes les 30 secs 
```
```
### faire que le script ne se lance pas sans ;odifier le script lui meme
```
```
commenter la ligne responsable du lancement de votre script

# Bonus

## bonus

### montrer comment mettre en place des partitions 
```
```
### montrer comment mettre en place wordpress mariaDB PHP et lighttpd
```
```
### montrer comment fonctionne votre service supplementaire

