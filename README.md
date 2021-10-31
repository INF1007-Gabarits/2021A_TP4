# TP4: Bibliothèques scientifiques et graphiques | Tests et outils de correction

- [Directives particulières](#directives-particuli%C3%A8res)
- [Objectifs](#objectifs)
- [Partie 1: Exploration de la base de données](#partie-1-Lire-et-construire-la-base-de-donn%C3%A9es)
- [Partie 2: Affichage graphique des données](#partie-2-analyse-des-donn%C3%A9es)
- [Partie 3: Rédaction des tests](#partie-3-rédactions-des-tests)

:alarm_clock: [Date de remise le dimanche 14 novembre à 23h59](https://www.timeanddate.com/countdown/generic?iso=20210406T2359&p0=165&font=cursive)

## Directives particulières
* Un fichier TP4.ipynb sera utilisé;
* Il suffit de faire un 'pip install jupyter' puis de rajouter jupyter sur pycharm afin de l'ouvrir, les jupyter notebook sont intéressants pour leur affichage rapide et vous familiariserons avec un outil communément utilisé;
* N'oubliez pas également d'installer les librairies manquantes (seaborn, numpy et pandas) via anaconda ou directement via pycharm; 
* Pas de librairies externes autres que celles déjà importées.

## Objectifs
Le TP4 se concentre sur l'utilisation de librairies scientifiques et graphiques. Plus précisément, vous aurez à vous familiariser avec numpy et pandas, des librairies essentielles en python en plus de visualiser certaines données avec matplotlib et seaborn. Exceptionnellement, les étapes à suivre pour les parties 1 et 2 seront expliquées entièrement dans le jupyter notebook nommé TP4.ipynb. Pour ce qui est de la partie 3 sur la rédaction de tests, un élément important lors de la réalisation de projet en programmation, les instructions sont ci-dessous.

## Partie 3: Rédactions des tests
Il est primordial de tester extensivement le code écrit. Toutefois, cette pratique est souvent mise de côté par manque de temps ou d'envie. Elle demeure néanmoins une bonne habitude à entreprendre pour vos futurs projets en tant qu'ingénieur en informatique/logiciel.

Pour votre première rédaction de tests, vous allez vous inspirer de codes déjà rédigés auparavant lors du TP1. Les codes en question sont les suivants. 

```python
# Fonction fizzBuzz 
def fizzBuzz(n):
    # TODO imprimer la chaine de caractère appropriée avec la fonction print().
    #  Assigner ensuite la valeur à la variable resultat
    toPrint = ""
    if n%3==0:
        toPrint += "fizz"
    if n%5==0:
        toPrint += "buzz"
    if toPrint == "":
        toPrint = str(n)

    resultat = toPrint
    print(resultat)

    return resultat

if __name__ == '__main__':
    n = int(input("indiquez le nombre: "))
    fizzBuzz(n)

#Fonction CalculerPosition
import math


def calculerPosition(positionInitiale, vitesseInitiale, duree, vitesseFinale):
    # TODO faites les calculs intermediaires, vous pouvez initialiser des variables locales.
    # il faut convertir les km/h en m/s, trouver l'accélération et calculer la position finale.
    vitesseInitiale/= 3.6
    vitesseFinale/= 3.6
    acceleration = (vitesseFinale - vitesseInitiale)/duree
    # TODO calculer la position finale, assigner la valeur à la variable "positionFinale"
    positionFinale = positionInitiale + vitesseInitiale * duree + 0.5 * acceleration * duree**2

    return positionFinale


if __name__ == '__main__':
    positionInitiale = int(input("Entrez la position initiale en mètre"))
    vitesseInitiale = int(input("Entrez la vitesse initiale en km/h"))
    duree = int(input("Entrez la duree en secondes"))
    vitesseFinale = int(input("Entrez la vitesseFinale en km/h"))
    print(calculerPosition(positionInitiale, vitesseInitiale, duree, vitesseFinale))
```

Le fichier *tests.py* est celui que vous devez compléter afin de réaliser les tests en question et vous assurez que les fonctions fizzBuzz() et CalculerPosition() implémentées ci-haut sont belles et bien fonctionnelles. Pour ce faire, il vous suffit de compléter quelques cas de tests pour ces deux fonctions. N'oubliez pas que vous pouvez toujours reconsulter les nombreux fichiers de test_assignment que vous possédez des anciens TP et projets.



