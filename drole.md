```package
record
```

# Bonjour Taill'Créons va t'apprendre à faire un drôle d'enregistreur vocal
TUTO Taill'Créons - drôle d'enregistreur vocal
## Etape 1 - Bonjour Taill'Crons va t'apprendre à faire un drôle d'enregistreur vocal! @showdialog
Suis bien les instructions à chaques étapes et clique sur SUIVANT pour passer aux prochaines étapes.
N'hésite pas à cliquer sur le bouton d'aide en forme d'ampoule en cas de blocage. 
Clique sur OK pour commencer.

## Etape 2: détecter un apuie sur le bouton A
On veut que lorsque l'on appuie sur le bouton ``||input:A||`` du micro:bit, un enregistrement audio démarre.
Dans la boite à outils, clique sur la section ``||input:Entrée||`` et déplace un bloc
``||Input:Lorsque le bouton A est pressé||`` sur la droite.
Clique sur ``|Next|``.
``` blocks
input.onButtonPressed(Button.A, function () {
})
``` 

## Etape 3: Démarrer l'enregistrement
Dans la boite à outils, clique sur la section ``||Record||`` et déplace le bloc ``||record.setSampleRate(10000, record.AudioSampleRateScope.Recording)||``
à l'intérieur du  bloc ``||Input:Lorsque le bouton A est pressé||`` .  

``` blocks
input.onButtonPressed(Button.A, function () {
 record.setSampleRate(10000, record.AudioSampleRateScope.Recording)
})
``` 

## Step 3
Branche une pince crocodile sur la broche  ``||input:0||``  du microbit  
Enfonce l'autre bout de la broche dans la patate.  
Branche une pince crocodile noir sur la broche ``||input:GND||`` du microbit et tiens l'autre bout dans ta main
Clique ensuite sur  ``|Télécharger|``  pour mettre le programme dans le microbit.  
Touche la patate et écoute ton microbit !

## Step 4
Essaye de faire la même chose avec la broche ``||input:1||`` avec un autre patate placée à droite de la première et en sélectionnant un son différent  ``||Musique:triste||`` 
    
``` blocks
input.onPinPressed(TouchPin.P0, function () {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.happy), SoundExpressionPlayMode.UntilDone)
})
input.onPinPressed(TouchPin.P1, function () {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.sad), SoundExpressionPlayMode.UntilDone)
})
``` 



## Step 5
Fais sourire ton microbit lorsque la patate de gauche est touchée.  
Dans la section  ``||basic:Base|`` , déplace le bloc  ``||basic:montrer l'icône||`` en dessous de la lecture du son heureux.  
Choisir une icône de personnage souriant :) 

``` blocks
input.onPinPressed(TouchPin.P0, function () {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.happy), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Happy)
})
input.onPinPressed(TouchPin.P1, function () {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.sad), SoundExpressionPlayMode.UntilDone)
})
``` 

## Step 6
Fais la même chose avec un personnage mécontent pour le son triste :(

``` blocks
input.onPinPressed(TouchPin.P0, function () {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.happy), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Happy)
})
input.onPinPressed(TouchPin.P1, function () {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.sad), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Sad)
})
``` 

## Step 7
Clique ensuite sur ``|Télécharger|``  pour mettre le programme dans le microbit.  
Touche les patates, regarde et écoute ton microbit !

## Step 8
Faisons maintenant réfléchir notre microb:it. Nous allons lui demander de choisir un chiffre entre 1 et 2.  
Si c'est 1: il veut que tu touches la patate gauche  
Si c'est 2: il veut que ce soit la patate droite.
Clique sur Suivant

## Step 9
Dans la section  ``||loops:Boucle||``, déplace le bloc  ``||loops:Chaque 500 ms||`` dans un endroit libre.  
Modifie la valeur de 500 en 3000.  
Ceci permettra à ton micro:bit de choisir entre gauche et droite toutes les 3 secondes (= 3000 millisecondes)
``` blocks
input.onPinPressed(TouchPin.P0, function () {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.happy), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Happy)
})
input.onPinPressed(TouchPin.P1, function () {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.sad), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Sad)
})

loops.everyInterval(3000, function () {
}
``` 


## Step 10
Dans la section  ``||variables:Variables||``, crée une variable avec comme nom  ``||variables:sens||``,  pour se mémoriser le sens droite ou gauche que le micro:bit aura choisi.    
Déplace le bloc ``||variables:définir sens à 0||`` à l'intérieur du bloc ``||loops:Chaque 3000 ms||``.

``` blocks
input.onPinPressed(TouchPin.P0, function () {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.happy), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Happy)
})
input.onPinPressed(TouchPin.P1, function () {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.sad), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Sad)
})

loops.everyInterval(3000, function () {
sens =0
}
``` 

## Step 13
Dans la section  ``||math:Maths||``, déplace le bloc  ``||math:choisir au hasard de 0 à 10||`` à la place de la valeur 0 du bloc
 ``||variables:définir sens à 0||`` , puis change les nombres pour mettre entre 1 et 2.  
Rappel: 1 = Gauche et 2= Droite
``` blocks
input.onPinPressed(TouchPin.P0, function () {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.happy), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Happy)
})
input.onPinPressed(TouchPin.P1, function () {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.sad), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Sad)
})

loops.everyInterval(3000, function () {
sens = randint(1, 2)
}
``` 


## Step 14
Rappel toi: on veut que le micro:bit choissise la patate de gauche si c'est 1 et de droite si c'est 2.  
Dans la section ``||logic:Logique||``, déplace le bloc ``||logic:si vrai alors||`` en dessous du bloc 
``||variables:définir sens à choisir au hasard de 1 à 2||``

``` blocks

loops.everyInterval(3000, function () {
sens = randint(1, 2)
 if true {
 }
}
``` 

## Step 15
Dans la section ``||logic:Logique||``, prend le bloc ``||logic:0 = 0||`` et positionne le à la place de la valeur  ``||logic:vrai||``.  
Puis remplace la valeur 0 de gauche avec la variable ``||variables:sens||`` dans la section  ``||variables:Variables||``.  
Remplace ensuite la valeur 0 de droite par 1. 
on vient de préparer ce que doit faire le microb:bit si il a choisit le sens Gauche (=1)
``` blocks

loops.everyInterval(3000, function () {
sens = randint(1, 2)
 if (sens == 1) {
 }
}
``` 


## Step 16
Dans la section  ``||basic:Base|`` , déplace le bloc  ``||basic:montrer LEDs||`` en dessous du bloc   ``||logic:si sens = 1 alors||``
et dessine une fléche vers la gauche

``` blocks

loops.everyInterval(3000, function () {
sens = randint(1, 2)
 if (sens == 1) {
  basic.showLeds(`
            . . # . .
            . # . . .
            # # # # #
            . # . . .
            . . # . .
            `)
 }
}
``` 

## Step 17
Clique sur le bouton  ``||logic:+|`` en bas à gauche du bloc ``||logic:si sens = 1 alors ||`` 
et déplace un bloc ``||basic:montrer LEDs||`` pour dessiner  une fléche vers la droite
On vient de finir la partie ou le micro:bit n'a pas choisit la gauche (donc la droite)
``` blocks

loops.everyInterval(3000, function () {
sens = randint(1, 2)
 if (sens == 1) {
  basic.showLeds(`
            . . # . .
            . # . . .
            # # # # #
            . # . . .
            . . # . .
            `)
 } else {
        basic.showLeds(`
            . . # . .
            . . . # .
            # # # # #
            . . . # .
            . . # . .
            `)
    }
}
``` 


## Step 18
Clique sur le bouton ``|Télécharger|``  pour mettre le programme dans ton microbit.  
Observe le résultat.  
Que se passe-t'il? Ton microbit est-t'il bien content lorsque tu choisis la même patate que lui?  


## Step 19
Il faut maintenant faire réagir ton microbit lorsque tu touches la patate de gauche et que c'est la même qu'il a choisi ou non.   
Place ta patate branchée sur la broche  ``||input:P0||`` à gauche et celle sur  ``||input:P1||`` à droite.  
Déplace un bloc ``||logic:si vrai alors||`` en dessous du bloc ``||input:lorsque la broche P0 est activée alors||`` 

``` blocks
input.onPinPressed(TouchPin.P0, function () {
    if (true) {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.happy), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Happy)
         } 
    
})
``` 

## Step 20
Remplace la valeur ``||logic:vrai||``  par un test logique permettant de savoir si la variable  ``||variables:sens||`` est égale à 1 (car 1 = gauche)  
``` blocks
input.onPinPressed(TouchPin.P0, function () {
    if (sens == 1) {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.happy), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Happy)
         } 
    
})
``` 


## Step 21
Clique sur le bouton ``||logic:+||``  afin de lui faire dire qu'il n'est pas content si ce n'est pas la bonne patate de gauche que tu as touché.  

``` blocks
input.onPinPressed(TouchPin.P0, function () {
    if (sens == 1) {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.happy), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Happy)
         } else {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.sad), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Sad)     
    }
    
})
``` 

## Step 22
Essaye de faire la même chose avec la patate de droite 
``` blocks
input.onPinPressed(TouchPin.P1, function () {
    if (sens == 1) {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.happy), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Happy)
         } else {
         music.playSoundEffect(music.builtinSoundEffect(soundExpression.sad), SoundExpressionPlayMode.UntilDone)
         basic.showIcon(IconNames.Sad)     
    }
    
})
``` 


## Step 23
Clique sur le bouton ``|Télécharger|`` pour mettre le programme dans ton microbit et joue avec lui !   
Tu pourrais maintenant accélerer son choix en baissant la valeur de 3000 à 2000 par exemple.
On pourrait également avoir à la place des patates plein de fruits différents et essayer de trouver le fruit qu'il a choisi.  
