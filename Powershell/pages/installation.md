# Installation

Tout d'abord, il faut savoir que depuis Windows 7, PowerShell est nativement présent sur les systèmes Windows. Il y a donc pas besoin de l'installer ou d'effectuer des réglages spécifiques.

Lien : <https://docs.microsoft.com/fr-fr/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7.1>

Ce lien nous donne les commandes et ce qu'il faut télécharger pour réussir l'installation du Powershell sur Linux.

### Résoudre le problème avec l'installation


Pour ce faire, il faut configurer les sources de APT.

#### Configurer les sources APT:

- Aller dans `\ > etc\ > apt`
- Editer le fichier `sources.list` avec la commande `sudo nano sources.list`
- (Si jamais une des erreurs est *"please insert the disc labeled"*) il faut enlever la ligne (ou la mettre en commentaire avec le `#`) `deb cdrom:[Debian GNU/Linux etc...`
- Ajouter la ligne suivante `deb http://ftp.fr.debian.org/debian/ sid main`

- Faire la commande `sudo apt update`

### Suite de l'installation

Maintenant il faut suivre les instruction du [lien ci-joint]( https://docs.microsoft.com/fr-fr/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-7.1). Il faut se rendre au niveau de l'installation correspondant à votre système.

[Retour au sommaire](https://github.com/NatSch45/linux/blob/master/Powershell/README.md) | [Page suivante -->](https://github.com/NatSch45/linux/blob/master/Powershell/pages/shell.md)
