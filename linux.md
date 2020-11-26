# Module linux

## Architecture linux

### Fichiers de l'architecture Linux, disponible à la racine du système (/) :

```
\
├── boot // système pour le lancement. ce sont les fichiers qui sont exécutés lors du lancement de l'OS
|   ├── grub
|   └── ... -amd64
|
├── dev // fichiers pilotes des périphériques
|   ├── stdin
|   ├── stdout
|   ├── cdrom
|   └── ...
|
├── etc //configuration système
|   ├── cron.d
|   ├── cron.daily
|   ├── cron.hourly
|   ├── cron.monthly
|   ├── crontab // plannification de tâche réccurentes, chronologiques, et automatique
|   └── dhcp // configuration automatique de l'adressage IP en réseau
|   └── dpkg // "debian package" gestionnaire de package de debian
|   └── group // fichier qui contient les groupes d'utilisateurs sur la machine
|   └── hosts // DNS
|   └── init.d // Dossier contenant les services
|       └── apache2
|       └── cron
|       └── mysql
|       └── nginx
|       └── ssh
|       └── sudo
|   └── ldap // Gestion d'annuaire
|   └── mime.types // liste de tous les types de fichiers pris en charges / autorisés
|   └── passwd // fichier qui contient les utilisateurs sur la machine
|   └── ssh // permet de gérer des connexion grâce au protocol SSH
|   └── sudoers // permet de gérer le fonctionnement de la commande "sudo"
|   └── ...
|
├── home
|   └── __user__ // dossier utilisateur qui contient ses fichiers
|   └── .bashrc // fichier permettant de gérer les "alias" et donc les raccourcis" (entre autre)
|       └── ... // dossiers et fichiers "personnels" de l'utilisateur
|
├── mnt // (mount) point de montage pour les montages temporaires
|
├── opt // répertoire des logiciels "autres" que système
|
├── proc // tous les fichiers temporaires de processus. Contient des informations système
|   └── ... 
|
├── root // répertoire admin système (de l'utilisateur "root")
|
├── run // fichiers contenant des données d'execution
|   ├── alsa
|   ├── cup
|   └── ...
|
├── srv // fichiers contenant des données d'execution fournis par le système
|
├── sys // fonctionnalité système
|   ├── block
|   ├── bus
|   ├── class
|   ├── dev
|   ├── device
|   ├── firmware
|   ├── fs
|   ├── hypervisor
|   ├── kernel
|   ├── module
|   └── power
|
├── tmp // Fichiers temporaires
|   └── ...
|
├── usr // Hiérarchie secondaire = besoin non vital
|   ├── bin //contient les commandes de LINUX
|       ├── cd
|       ├── nano
|       ├── mv
|       └── ...
|   ├── games
|   ├── include
|   ├── lib
|   ├── lib32
|   ├── lib64
|   ├── libexec
|   ├── libx32
|   ├── local
|   ├── sbin
|   ├── share
|   └── src
|
└── var // données variables
|   └── www // en général racine des serveurs web
|   └── ...
```

### Fichiers disponibles à la racine de l'utilisateur (~) :

- Dossiers reservés à l'utilisateur :
    - *Desktop*
    - *Downloads*
    - *Pictures*
    - *Videos*
    - *Documents*
    - *Music*
    - *Public*
    - *Templates*
- Dossiers cachés (système Linux) :
    - *.gnupg* (GNU Privacy Guard) : Application servant à chiffer des données
    - *.ssh* : stocke sous forme de fichiers ordinaires les clés d'identification ssh publique ou privée
    - *.local/share* : Répertoire où les données de l'utilisateur sont stockées
    - *.cache* : Stocke les données de cache, ce sont les fichiers de données non-essentielles
    - *.config* : Stocke des données de configuration
    - *.pki* (Public Key Infrastructure) : Système permettant de gérer des clés publiques
- Autres :
    - *snap* (dossier) : Répertorie les applications installées via snap
    - *.NomDuLogiciel* : Executables repréentant les logiciels installés sur le système (exemples: Mozilla, VS code, Chromium...)


## Histoire de Linux

### Les dates clés :

- 1965 : MULTICS
- 1969 : AT&T, Bell laboratories - Ken Thompson et Dennis Ritchie créent la - première version de Unix
- 1970 : UNIX
- 1974 : La 4ème version de Unix est donnée à Berkeley une université - californienne. 2 versions de Unix existent, l'AT&T et la BSD (Berkeley - SOftware DIstribution)
- 1979 : AT&T vend les premières licences Unix
- 1984 : Projet GNU
- 1984 : Le MIT crée la norme X Windows, un système de multifenêtrage - graphique
- 1987 : AT&T et BSD s'allient pour normaliser Unix
- 1991 : Création de Linux par le finlandais Linus Torvalds à la suite d'un - travail sur Minix (OS à finalité pédagogique)
- 1992 : Linux devient Open Source ( adoption de la licence GPL )
- 1993 : Création de la distribution Slackware - ancienne version toujours - maintenue
- 1995 : La première expo de Linux
- 1996 : Linux à sa mascotte ( Tux, un manchot, le logo et emblème du projet)
- 1997 : Création du projet GNOME
- 1998 : KDE 1.0 est disponible
- 1999 : Red Hat entre en bourse ( La société est la première spécialisée - dans Linux à entrer en bourse.)
- 2000 : Steve Jobs propose a Linus Torvalds de travailler qur MacOS
- 2001 : Windows considère Linux comme un réel problème commercial
- 2002 : Microsoft engage 421 millions de $ pour contrer la propagation de - Linux
- 2003 : une publicité diffusée durant le Superbowl ( Illustration de la - place prise par Linux.)
- 2004 : Ubuntu 4.10 est disponible.
- 2005 : Linus Torvalds crée Git.
- 2006 : Microsoft et Novell concluent un accord de coopération
- 2007 : Linux fait un partenariat avec ASUS pour la création d'un nouvel - ordinateur
- 2008 : Lancement de la version 1.0 d'Android basée sur le noyau Linux.
- 2009 : Google annoce Chrome OS basé sur le noyau Linux.
- 2010 : Linux popularisé sur mobile Red Hat devient la première société Open - Source valant 1 Milliard de dollars
- 2011 : La majorité des personnes dans le monde utilisent Linux sans souvent - en avoir conscience. Comme le rappelle la Linux Fondation, Linux équipe 75% - des places boursières dans le monde, dont Wall Street, ainsi que 95% des - supercalculateurs. Les serveurs Web sont en majorité sous Linux
- 2012 : Linus Torvald se plaint de Nvidia lors d'une conférence à stockholm - et réplique le célèbre "fuck you Nvidia".
- 2013 : Le téléphone Ubuntu est annoncé.
- 2014 : Microsoft s'entendent bien Linux
- 2015 : Microsoft a sa propre version de Linux.