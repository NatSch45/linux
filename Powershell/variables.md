# Variables

## Les types de variables :

- [string] : chaîne de caractères 
- [char] : caractère Unicode 16 bits
- [byte] : caractère sur 8 bits non signés

---

- [int] : nombre entier sur 32 bits signés
- [long] : nombre entier sur 64 bits signés
- [bool] : valeur booléenne (*true* ou *false*)

---

- [decimal] : valeur décimale sur 128 bits
- [single] : valeur décimale à simple précision sur 32 bits
- [double] : valeur décimale à double précision sur 64 bits
- [DateTime] : valeur représentant une date et l'heure

---

- [xml] : objet xml
- [array] : tableau de valeurs de n'importe quel type et à une ou plusieurs entrées
- [hashtable] : objet hashtable 

<br>

## Suffixes de multiplication :

- **d** : decimal data type
- **kb** : multiplicateur kibibyte
- **mb** : multiplicateur mebibyte
- **gb** : multiplicateur gibibyte
- **tb** : multiplicateur tebibyte
- **pb** : multiplicateur pebibyte

Exemple d'utilisation : 10mb = 10485760 ou encore 1.2kb = 1228.8

Il existe également d'autres suffixes compatibles avec d'autres types

<br>

## Forcer le type d'une variable (casting)

Il est possible de forcer le valeur d'une variable avec un "cast operator". Il s'agit du type en question entre crochets comme préfixe à la valeur

Exemple :
```
> [int]"0064"
64
> [int]$false
0
# Ajouter un préfixe '0x' à une string indique que la valeur est un nombre hexadécimale
> [byte]('0x' + 'FF')
255
> $hexnum = 'fa00'
> [int]"0x$hexnum"
64000
```

Il est possible de convertir une valeur numérique en string.

Quand on déclare une variable, il est possible de placer le cast operator comme préfixe à la valeur assignée mais aussi au nom de la variable
```
$variable = [int]0123 <=> [int]$variable = 0123
```

<br>

---

source : *https://ss64.com/ps/syntax-datatypes.html*

[Retour au sommaire](https://github.com/NatSch45/linux/blob/master/Powershell/README.md)
