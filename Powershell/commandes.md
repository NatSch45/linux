# Commandes PowerShell

Le préfixe de la commandelette (commande PowerShell) est appelé verbe bien qu'il n'en soit pas toujours un. Il est appelé ainsi car il détermine l'action à effectuer sur les entités désignédes dans la phrase. S'en suit d'un nom séparé par un tiret.

## Liste des verbes : 

1. **Add** : permet d'**ajouter** des données ou informations sur le nom qui le suit

2. **Get** : permet d'**obtenir** des données ou informations sur le nom qui le suit
3. **Clear** : permet de **réinitialiser** un affichage ou une variable
4. **Import/Export** : permet d'**importer/exporter** des fichiers de commande ou des alias
5. **New** : permet de créer de nouveaux objets ou variables
6. **Set** : permet de définir des données ou informations sur le nom qui le suit
7. **Write** : permet d'écrire des données ou informations sur le nom qui le suit et peut agir comme le compte-rendu d'une commande

<br>
<br>

# Les commandes à savoir

- **`Get-help NomDeLaCommande`** : Ici, la commande renvoie des informations sur comment utiliser la commande "NomDeLaCommande". Le flag **-examples** est très pratique car il permet d'afficher des exemples d'utilisation d'une commande et de ses flags.

- **`Update-help`** : Permet de mettre à jour les fichiers *help* (d'aides) sur les modules PowerShell. Attention : il faut relancer le logiciel afin que les mises à jour soient correctement effectives.

- **`Get-Location`** : Renvoie le dossier dans lequel on se trouve.

- **`Get-ChildItem`** : Renvoie le contenu d'un dossier ainsi que des informations sur les items présents. Par défaut, il sera affiché les attributs (Mode), la date de dernière modification (LastWriteItem), la taille de l'item (Length) puis le nom de l'item (Name). Concernant la colonne "Mode", les attributs peuvent être 'l' (link), 'd' (directory'), 'a' (archive), 'r' (read-only), 'h' (hidden), 's' (system).  
Le flag **-Path** indique dans quel dossier la commande sera effectuée.
    - Par exemple, pour afficher le contenu d'un sous-dossier nommé *MonDossier*, on tapera :  
    `Get-ChildItem -Path .\MonDossier`

- **`clear`** : Permet de nettoyer l'interface de commande 

- **`Read-Host`** : Permet de récupérer des données à rentrer dans la console. Ceci affiche ensuite la valeur en question

- **`New-Item`** : Permet de créer un nouvel item (dossier, fichier...). Le flag **-Path** permet d'indiquer l'emplacement de création de l'item, **-Name** spécfie le nom de l'item, **-ItemType** indique le type de l'item (Directory ou File), **-Value** permet d'ajouter une valeur à notre fichier
    - Par exemple, pour créer un dossier nommé *NomDuDossier*, il faut faire la commande  
    `New-Item -Name "NomduDossier" -ItemType Directory`
    - Pour créer un fichier nommé *MonFichier* dans le dossier courant contenant le texte "Voici le texte", il faudra utiliser la commande  
    `New-Item -Path . -Name "MonFichier" -ItemType File -Value "Voici le texte"`

- **`Copy-Item`** : Permet de copier un fichier ou un dossier d'un dossier à un autre, il est possible également de changer le nom de l'item. Le flag **-Destination** permet de préciser dans quel dossier l'item sera copié, **-Recurse** sera appelé afin de faire une copie récursive, c'est-à-dire d'un dossier ou du contenu d'un dossier.
    - Par exemple, pour copier le fichier *MonFichier.txt* présent dans le sous-dossier *MonDossier* vers le sous-dossier *MonAutreDossier* :  
    `Copy-Item .\MonDossier\MonFichier.txt -Destination .\MonAutreDossier`
    - Pour copier le contenu d'un dossier vers un autre dossier existant, on utilisera une commande similaire à celle-ci :  
    `Copy-Item -Path .\MonDossier\* -Destination .\DossierExistant -Recurse`
<br>
<br>

## Les Alias

PowerShell utilise de nombreux **alias** pour assurer une certaine ressemblance avec les commandes les plus usitées (ex. *Curl*, *ls*, *mkdir*, ...). Les commandes PowerShell s'écrivent indifféremment avec leur intitulé par défaut ou leur alias.
Voici une [liste des alias](https://vulgumtechus.com/Liste_des_alias_dans_PowerShell) proposée par PowerShell.

Il est également possible de créer ses propres alias à l'aide de la commande Set-Alias. Le flag **-Name** correspond au nom donné à l'alias et le flag **-Value** correspond lui à la commande qui est doit être appelée.
Dans ce cas, on crée un alias nommé *MonAlias* qui exécute la commande Get-help :
`Set-Alias -Name MonAlias -Value LaCommande`  

![alias_help](./pictures/alias_help.PNG "Alias \"help\"")

<button name="button" onclick="https://git.ytrack.learn.ynov.com/NSCHNEIDER/linux/src/branch/master/Powershell/README.md">Test</button>
