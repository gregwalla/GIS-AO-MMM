# Python vision environment developping Methods 


We will stay as much "agnostic" as possible :
use of standards python libraries 
windows path variables are not used because they require admin rights
Windows Powershell (PS) will be used
virtual env is set up with venv standard library
visual studio code is installed (check if admin rights needed) 


- if possible we will try to use TotalEnergies Github space 



## installation of a virtual env  

### Find where python is installed : 
ps python (not python3)

---python
>>> import os, sys
>>> os.path.dirname(sys.executable)
---
example : 
'C:\\Users\\J0102113\\AppData\\Local\\Programs\\Python\\Python39'

https://docs.python.org/3/library/venv.html

### Creation of the environnement 

c:\>c:\Python35\python -m venv c:\path\to\myenv

Using a virtualenv enables you to install python libraries more easily because python libraries are installed on your documents folder

### Activation 

PS C:\Users\J0102113\Documents\a-SIGetWeb\AO\mul\Scripts\activate.ps1

### vscode start

Start at the parent folder of the project where a .vscode folder is situated. 
It will then discover the python interpreter of venv

## Installation of geopandas

Dependencies must be installed locally , this article shows how to :   
https://towardsdatascience.com/geopandas-installation-the-easy-way-for-windows-31a666b3610f


## Installation of jupyter via pip

Selection de l'interpreteur VS  code sous l'environnement vituel
Nécessite peut être de redémarrer si vs code a été ouvert avant

## initiate git repo and add a gitignore file

gitignore is taken from a template in github (template gitignore)
"#for this project" lines are specifically added

## push code to github 
Start with a local public then a private repo , use ssh 
For TotaEnergies You need to follow a prodedure that will require time and some debuging
Set up github desktop (?) 



## Hypothèses de modélisation : 

### Référentiel géographique 
    - WSG84 

### données sources : 
    - forme des IRIS 
    source :  data de mulhouse 
    - Attribut de population des IRIS (POP 2017)

    - Données SIRENE pour les commerces
    - Données Stations de BEMO (12/2021)
    - Communes de l'agglomération

### métode proposée : 

- la visualisation des iris donne une première indication
    - les IRIS sont regroupés par communes

- On réalise des simulations sur tout l'espace 
    - on projette des points sur la carte 
    - chaque point a une surface d'influence (à définir)


- les IRIS sont la base pour le calcul de scores
    - La surface d'influence des points peut toucher un ou plusieurs IRIS
    - On calcule une densité de population par IRIS
    - [P2] On calcule une densité des commerces par IRIS
    - [P3] On ajoute les stations déja installées



- On peut calculer un score pour chaque point :
    - Le score dépend de la  [Moyenne] des valeurs des Iris touchés de densité de population  (+), de la concentration de commerces (+) , 
    - de distance par rapport à la concurrence (-) sur les iris touchés par le point

- On réalise des analyses complémentaires : 
    - Prise en compte des grands axes 
    - Prise en compte des réseaux élécrtiques
    - Prise en compte des parkings (?)

- On ajuste précisément les points retenus sur la carte :
    les points étant générés n'importe comment sur la carte il faut les repositionner légèrement manuellement 

### Ressources nécessaires : 
    temps , budget 

### Format des livrables 

### Délais 

