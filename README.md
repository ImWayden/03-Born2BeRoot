# 03-Born2BeRoot
Ce Readme contiendra toute les reponses aux question posable 
durant la correction de Born2BeRoot 
ATTENTION CETTE VERSION EST UN PREMIER JET ET PEUT NE PAS CORRESPONDRE A VOTRE SUJET
DE PLUS LES REPONSES N'ONT PAS ENCORE TOUTES ETE VALIDEE 
la majorite des reponses ont ete generee par [GPT3](https://chat.openai.com/chat)

de plus ces reponses sont bases sur le sujet du 5/24/2021 et peut ne pas etre a jour
# Questions

## Project Overview
### Comment fonctionne une machine Virtuelle
--------------

Une machine virtuelle est `un logiciel` qui permet à un ordinateur d'`exécuter des systèmes d'exploitation `et des logiciels `indépendamment les uns des autres`, comme s'il s'agissait de `machines physiques distinctes`. Cela signifie que vous pouvez exécuter `plusieurs systèmes` d'exploitation sur `un seul ordinateur` en même temps, chacun dans sa propre machine virtuelle.

Pour fonctionner, une machine virtuelle a besoin d'`un logiciel d'émulation`, appelé `hyperviseur`, qui crée `un environnement isolé` pour chaque système d'exploitation. L'hyperviseur `gère les ressources de l'ordinateur`, comme la `mémoire`, le `stockage` et les `périphériques` d'entrée/sortie, et `attribue ces ressources` aux différentes machines virtuelles de manière à les faire `fonctionner de manière indépendante`.

Lorsqu'un utilisateur lance une application dans une machine virtuelle, l'hyperviseur redirige les données d'entrée et de sortie vers l'application et gère les interactions avec les autres systèmes d'exploitation et les applications installées sur l'ordinateur. Cela permet à chaque système d'exploitation et à chaque application de fonctionner `comme s'ils étaient installés sur une machine physique distincte`, tout en `partageant les ressources de l'ordinateur physique`.

### Quel est l'Os que vous avez choisit
 Debian ou CentOS

### La difference basic entre CentOS et Debian

`Debian et CentOS` sont tous deux des `systèmes d'exploitation basés sur Linux`, mais ils ont des différences importantes.

`Debian` est une distribution Linux `libre et open source` qui a été créée en 1993. Elle est connue pour sa stabilité et sa `flexibilité`, et est largement utilisée pour les serveurs Web et `les ordinateurs personnels`. Debian est géré par `une communauté d'utilisateurs et de développeurs bénévoles` à travers le monde.

`CentOS`, quant à lui, est une distribution Linux basée sur `Red Hat Enterprise Linux` (RHEL), une `distribution commerciale` qui est largement utilisée pour `les serveurs d'entreprise`. CentOS est `également libre et open source`, et est géré par une communauté d'utilisateurs et de développeurs. Contrairement à Debian, CentOS est principalement utilisé pour `les serveurs d'entreprise` et les environnements de développement.

En résumé, Debian et CentOS sont des distributions Linux libres et open source, mais elles sont gérées par des communautés différentes et sont principalement utilisées pour des cas d'utilisation différent, `Debian` et considere comme `plus facile a utiliser` et plu `adapte aux ordinateurs personnels` tandis que `Centos` est plus destiné aux `aplication professionel` 

### Le but d'une machine virtuel
------------------------
Le but principal d'`une machine virtuelle` est de permettre à un ordinateur d'`exécuter plusieurs systèmes d'exploitation` et des logiciels `indépendamment les uns des autres`, comme s'il s'agissait de `machines physiques distinctes`. Cela signifie que vous pouvez exécuter plusieurs systèmes d'exploitation `sur un seul ordinateur` en même temps, `chacun dans sa propre machine virtuelle`.

Cela a de nombreux avantages, tels que :

Permettre à un utilisateur d'`exécuter des applications` qui ne sont compatibles qu'avec un système d'exploitation particulier `sur un ordinateur qui utilise un autre système d'exploitation`.
Faciliter le développement et les tests de logiciels en créant des `environnements` de développement et de test `isolés`.

`Protéger les données et les applications sensibles` en les `isolant des autres systèmes d'exploitation` et des applications installées sur l'ordinateur.
`Economiser de l'argent` en permettant à `un seul ordinateur` d'exécuter `plusieurs systèmes d'exploitation` et applications, plutôt que d'avoir à acheter plusieurs machines physiques distinctes.

En somme, l'utilisation de machines virtuelles permet une meilleure utilisation des ressources de l'ordinateur et une plus grande flexibilité dans l'exécution de différents systèmes d'exploitation et applications. 

### Si vous avez choisit CentOs, qu'est ce que SELinux et DNF
---------------------
#### SELinux

SELinux est un système de `contrôle d'accès sécurisé` pour les systèmes d'exploitation Linux. Il est utilisé pour `renforcer la sécurité` du système en `limitant les actions` que les programmes peuvent effectuer sur les fichiers et les ressources du système. 

#### DNF

DNF, quant à lui, est un `gestionnaire de paquets` pour Linux. Il est utilisé pour `installer, mettre à jour et supprimer des logiciels` sur les systèmes d'exploitation qui utilisent le `format de paquet RPM`, comme Fedora et Red Hat Enterprise Linux. DNF est l'acronyme de "Dandified Yum", car il est `basé sur l'outil de gestion de paquets Yum`, mais avec des améliorations pour rendre son utilisation `plus simple et plus efficace`. source 


### Sivous avez choisit Debian, qu'elle est la difference entre aptitude et apt, et c'est quoi APPArmor
-----------------
#### aptitude et apt

`Aptitude et apt` sont des `outils de gestion de paquets` pour les systèmes d'exploitation basés sur `Linux` qui utilisent le format de paquet DEB. Ils sont utilisés pour `installer, mettre à jour et supprimer des logiciels` sur ces systèmes.

La principale différence entre aptitude et apt est que `aptitude` est une application en mode texte qui offre une `interface utilisateur plus avancée` et plus complète que apt. Aptitude a également une `meilleure gestion des dépendances`, ce qui signifie qu'il peut résoudre les problèmes de dépendances entre les paquets de manière plus efficace que apt.

Cependant, `apt` est généralement `plus rapide` et `plus léger` que aptitude, car il est uniquement en `ligne de commande` et n'offre `pas les fonctionnalités avancées de aptitude`. De plus, apt est plus souvent utilisé que aptitude, car il est `plus simple à utiliser et plus rapide`.

En résumé, aptitude et apt sont `des outils similaires` pour gérer les paquets sur les systèmes d'exploitation Linux, mais `aptitude` offre une `interface utilisateur` plus `avancée` et une meilleure `gestion des dépendances`, tandis que `apt` est `plus rapide et plus léger`.


## Simple setup
----------------------
### Check si le service ufw est en cour

```
systemctl status ufw
```
### Check si le service SSH est en cour
----------------------------
```
systemctl status ssh
```
### Check que l'Os choisit soit bien debian ou CentOS
--------------------------------
```
uname -a
```
## User
------------------------
### Check la presence d'un user portant votre login et son appartenance aux groupe sudo et user42
------------------------
```
cat /etc/passwd | grep [user]
```
### Verifier que les regles concernant la politique de mots de passes fort a ete mises en place
--------------------------
Creer un nouvel utilisateur et lui assigner un mot respectant les regles
```
useradd [user]
```
expliquer comment ca a ete mise place

-----------------
instalation pam
```
sudo apt-get install libpam-modules
```
in
```
cd /etc/pam.d
sudo vi common-pasword
```
at line:
```
25 password requisite
``` 
add
```
retry=3 #nombre de retry pour le mot de passe
ucredit=-1 #nombre minimal de uppercase
dcredit=-1 #nombre minimal de diggit
maxrepeat=3 #nombre de caractere max de suite
usercheck=1 #empeche l'utilisateur de choisir un mot de passe courant tel que sn propre nom
difok=7 #plus de 7 caractere different avec l'ancien mot de passe
enforce_for_root #applique ces regle au mot de passe du user root
minlen=10 force un mt de passe de 10 caracteres
```
line final
```
25 password requisite pam_pwquality.so retry=3 ucredit=-1 dcredit=-1 maxrepeat=3 usercheck=1 difok=7 enforce_for_root minlen=10 
```
changer la duree de validite d'in mote de passe et le temps avant que l'utilisateur soit prevenu
```
sudo nano /etc/login.defs
```
changer ca
```
PASS_MAX_DAYS 9999
PASS_MIN_DAYS 0
PASS_WARN_AGE 7
```
en ca
```
PASS_MAX_DAYS 30
PASS_MIN_DAYS 2
PASS_WARN_AGE 7
```
pour le root et les utilisateur deja creer 
```
chage -m[nb min_day] -M[nb Max_day] -W[warn_age]
```
creer un groupe nomer evaluating et y ajouter l'utilisateur nouvelement creer enfn checker que l'utilsateur fait bien partie du bon group

--------------------
```
sudo addgroup [user] evaluating
```
### Quels sont les avantages et desavantages de cette politique de mot passe
-------------------------------
`Les avantages` d'une politique de mot de passe fort sont qu'elle peut `aider à protéger les comptes d'utilisateurs` contre les attaques de piratage. Cela peut également aider à `empêcher les` utilisateurs d'utiliser des `mots de passe faciles à deviner` ou à trouver, ce qui peut `augmenter la sécurité générale des comptes`.

`Les désavantages` d'une politique de mot de passe fort peuvent inclure une `plus grande complexité pour les utilisateurs`, ce qui peut les inciter à utiliser des `mots de passe faciles à retenir mais faciles à deviner`, ou à `écrire leurs mots de passe dans des endroits non sécurisés`. Cela peut également entraîner une plus `grande frustration pour les utilisateurs`, qui doivent se souvenir de plusieurs mots de passe complexes pour différents comptes.
 
## Hostname and partition
-----------------------

### Checkque lehostname de lamachine est correct (login42)
------------------------------
```
hostname
```
### modifier le hostname et remolacer par le votre
------------------------------
```
sudo vim /etc/hostname
```
change 
```
[login]42
```
par
```
[login evaluateur]42
```
### afficher les partitions de sa machine virtuelle
-----------------------------
```
lsblk
```
### How LVM Works 
----------------------------
`LVM`, ou Logical Volume Management, est un `système pour gérer les partitions de disque` sur un système `Linux`. Il vous permet de créer, redimensionner et supprimer des partitions de disque sans avoir à vous soucier de la disposition physique sous-jacente des disques.

Dans une configuration LVM typique, `un disque physique est divisé` en un ou plusieurs `volumes physiques`. Ces volumes physiques sont ensuite `regroupés dans un groupe de volumes`. Le groupe de volumes `agit comme un disque virtuel`, et il peut être `divisé en volumes logiques`, qui sont `les partitions utilisées par le système d'exploitation`.


## Sudo
-----------------------------
### Check que sudo soit bien installe sur la VM
------------------------------
```
which sudo
```
ne renvois rien si sudo n'est pas instalé
### assigner le nouvel utiisateur au groupe sudo
en etant root ou sudo
```
sudo usermod -aG sudo [user]
sudo visudo
```
ajouter la ligne
```
[user] ALL=(ALL) ALL
```
peut necesiter un reboot pour prendre effet
### expliquer la valeur et operation de sudo
---------------------------------
`Sudo` est un `outil` utilisé dans les systèmes d'exploitation `Linux` et Unix-like pour permettre à un utilisateur de `lancer des programmes avec les privilèges` de sécurité d'un autre utilisateur, en général l'utilisateur `superutilisateur` (root). Cela est utile pour `permettre aux utilisateurs non privilégiés` d'exécuter des programmes qui `nécessitent des privilèges élevés`, tels que changer les paramètres système ou installer des logiciels. 

Pour utiliser la commande sudo, `l'utilisateur doit être inclus dans le fichier sudoers`, qui liste les utilisateurs autorisés à utiliser sudo. Lorsqu'un utilisateur exécute `une commande avec sudo`, il est invité à `entrer son propre mot de passe` pour vérifier son identité. Cela offre une couche supplémentaire de sécurité en garantissant que `seuls les utilisateurs autorisés peuvent utiliser sudo`.    
### verifier /var/log/sudo/sudo + check le contenue de celui ci

```
cd /var/log/sudo/
```
verifier la presence de sudo.log
## UFW
---------------------------
### Check si le service ufw est installee
```
sudo dpkg -l | grep ufw
```
### verifier qu'ufw fonctionne correctement

```
sudo ufw status
```
### expliquer l'utilite d'ufw
----------------------------------------
`ufw` est un acronyme pour "uncomplicated firewall". Il s'agit d'un `outil en ligne de commande` qui permet de `configurer facilement le pare-feu` de votre ordinateur ou de votre serveur. `Un pare-feu est un logiciel` ou un matériel qui `filtre les données entrantes et sortantes` d'un ordinateur ou d'un réseau, en `bloquant les paquets de données non autorisés` et en `autorisant uniquement les paquets de données autorisés`. Cela permet de `protéger votre ordinateur` ou votre réseau contre les attaques provenant d'Internet. ufw est un `outil simple à utiliser` qui vous permet de configurer rapidement votre pare-feu sans avoir besoin de connaissances approfondies en matière de sécurité informatique.

### ajouter une regle pour ouvrir le port 8080 et lister toute les regles actives
```
sudo ufw allow 8080
sudo ufw status
```

### supprimer la nouvelle regle
```
sudo ufw delete allow 8080
```
## SSH
--------------------
### verifier que le ssh est installer
```
ssh -V
```
### verifier que ssh fonctionne
```
sudo systemctl status ssh
```
### expliquer l'utilite de ssh
-------------------------
`SSH` (Secure Shell) est un protocole de réseau qui `permet de créer une connexion sécurisée entre deux ordinateurs`. Il est souvent utilisé pour se connecter à des serveurs distants et exécuter des commandes à distance, mais il peut également être utilisé pour établir une connexion sécurisée à un ordinateur local pour transférer des fichiers ou pour utiliser internet de manière sécurisée lorsque vous êtes connecté à un réseau non sécurisé. 

### verifier que le ssh n'utilise que le port 4242
permet d'aller voir quel port est configurer pour la connexion via ssh 
```
grep -E '^Port' /etc/ssh/sshd_config
```
sinon vous pouvez verifier a la main 
```
cat /etc/ssh/sshd_config
```
### se connecter a la vm via ssh et verifier que le rot user ne peut pas se connecter
Dans un terminl a part:
```
ssh localhost@[user] -p [port] 
```
le port 4242 etant deja utiliser vous avez du faire une derivation, c'est ce pert qui vas dans [port]
[user] coorespond au nom d'utilisateur avec lequel vous voulez vous connecter 
si vous souhaitez tentez de vous connecter avec root remplacer [user] par root

## Script Monitoring
-----------------------------

### expliquer comment fonctionne votre script
-----------------------------
cela depend de votre monitoring.sh

### qu'est ce qu'est cron
----------------------------
Cron est un programme qui permet de planifier l'exécution de commandes ou de scripts à des moments précis. Cela peut être utile pour automatiser des tâches répétitives, telles que la sauvegarde des données ou l'exécution de scripts de maintenance. 

### expliquer comment vous avez fait pour le script se lance toute les 10 min depuis le start serveur
expliquer que vous avez effectuer les manipulations suivantes
```
sudo crontab -u root -e
```
ajouter les lignes
```
@reboot [/path/monitoring..sh]
*/10 * * * [/path/monitoring.sh]
```

attention a ne pas oubler de remplacer [/path/monitoring..sh] par le chemin vers votre script

### faire fonctionner le script toutes les 30 secs 
remplacer
```
*/10 * * * [path/monitoring.sh]
```
par
```
* * * * * /bin/bash -c ' for i in {1..X}; do YOUR_COMMANDS ; sleep Y ; done '
```

### faire que le script ne se lance pas sans modifier le script lui meme

commenter la ligne responsable du lancement de votre script
dans le fichier crontab du root user

----------------

# Bonus
## bonus 
------------------------

### montrer comment mettre en place des partitions

```
```
### montrer comment mettre en place wordpress mariaDB PHP et lighttpd
```
```
### montrer comment fonctionne votre service supplementaire
-----------------------

