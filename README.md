# Second exercice Figma

## Note introductive

Cette fois-ci tout sera sur base de FLEX. Faudrait que je vienne noter ici les règles à garder en tête et mes feedbacks persos...

## Règles

### Flex

Pour faire du flex, la règle de base est pour l'élément que je veux bouger de 

display: flex;

#### Flex horizontal ⇄

*justify-content:*

##### Variables possibles

flex-start      Les éléments s'alignent au côté gauche du conteneur.
flex-end        Les éléments s'alignent au côté droit du conteneur.
center          Les éléments s'alignent au centre du conteneur.
space-between   Les éléments s'affichent avec un espace égal entre eux.
space-around    Les éléments s'affichent avec un espacement égal à l'entour d'eux.

#### Flex vertical ⇅

*align-items:*

##### Variables possibles

flex-start     Les éléments s'alignent au haut du conteneur.
flex-end       Les éléments s'alignent au bas du conteneur.
center         Les éléments s'alignent au centre vertical du conteneur.
baseline       Les éléments s'alignent à la ligne de base du conteneur.
stretch        Les éléments sont étirés pour s'adapter au conteneur.

#### Flex sens  ⇋

*flex-direction:*

/!\ Fonctionne selon le principe de l'axe de rotation !
/!\/!\ Inversera la logique haut/bas gauche/droite ! En fait, la référence est le "point de vue des items" et pas celui de l'observateur ! Enfant du démon !


##### Variables possibles

row                Les éléments sont disposés dans la même direction que le texte.
row-reverse        Les éléments sont disposés dans la direction opposée au texte.
column             Les éléments sont disposés de haut en bas.
column-reverse     Les éléments sont disposés de bas en haut.

#### Flex ordre  

*.nom_de_classe {
    order: *int* ;
}*

Ici, on part tjs d'un objet d'une liste, et on utilise l'argument "order3" et on lui attribue la bonne valeur.

/!\ On part toujours de la valeur relative à là où on est !

#### Flex un seul élement   

*.nome_de_classe {
    align_self:  ;
}*

Ici, on part tjs d'un objet d'une liste, et on utilise l'argument "order3" et on lui attribue la bonne valeur.

/!\ On part toujours de la valeur relative à là où on est !

##### Variables possibles

flex-start     Les éléments s'alignent au haut du conteneur.
flex-end       Les éléments s'alignent au bas du conteneur.
center         Les éléments s'alignent au centre vertical du conteneur.
baseline       Les éléments s'alignent à la ligne de base du conteneur.
stretch        Les éléments sont étirés pour s'adapter au conteneur.

#### Flex wrap   

*flex-wrap:*

Ici, on part tjs d'un objet d'une liste, et on utilise l'argument "order3" et on lui attribue la bonne valeur.

/!\ On part toujours de la valeur relative à là où on est !

##### Variables possibles

nowrap           Tous les éléments sont tenus sur une seule ligne.
wrap             Les éléments s'enveloppent sur plusieurs lignes au besoin.
wrap-reverse     Les éléments s'enveloppent sur plusieurs lignes dans l'ordre inversé.

#### Flex-flow   

*flex-flow:*

Fait du *flex-direction* et du *flex-wrap* en même temps, et prend les variables des deux !

##### Variables possibles

row                Les éléments sont disposés dans la même direction que le texte.
row-reverse        Les éléments sont disposés dans la direction opposée au texte.
column             Les éléments sont disposés de haut en bas.
column-reverse     Les éléments sont disposés de bas en haut.
nowrap             Tous les éléments sont tenus sur une seule ligne.
wrap               Les éléments s'enveloppent sur plusieurs lignes au besoin.
wrap-reverse       Les éléments s'enveloppent sur plusieurs lignes dans l'ordre inversé.

#### Align-content

*align-content:* 

Va gérer l'espace entre les lignes, sans bouger d'éléments.

##### Variables possibles

flex-start         Les lignes sont amassées dans le haut du conteneur.
flex-end           Les lignes sont amassées dans le bas du conteneur.
center             Les lignes sont amassées dans le centre vertical du conteneur.
space-between      Les lignes s'affichent avec un espace égal entre eux.
space-around       Les lignes s'affichent avec un espace égal autour d'eux.
stretch            Les lignes sont étirées pour s'adapter au conteneur.



## Réflexions en cours de dev

Je vais attaquer le contenu de la carte blanche. 

Je dois :

* Télécharger les deux logos et les mettre dans le bon dossier
* Créer cinq img, en deux .classes différentes :
    * .true
        * en CSS, utiliser les attributs suivants :  
        
            .true {
                width: 20px;
                height: 20px;
            }

    * .false
        * en CSS, utiliser les attributs suivants :  
        
            .false {
                width: 20px;
                height: 20px;
            }

* Créer huit p, en quatre .classes différentes :
    * .basic
        *en CSS, utiliser les attributs suivants :
            color: #292929;
            font-family: Noto Sans Symbols;
            font-size: 36px;
            font-style: normal;
            font-weight: 300;
            line-height: 36px; /* 100% */
    * .feature
        *en CSS, utiliser les attributs suivants :
            color: #000;
            font-family: Noto Sans Symbols;
            font-size: 16px;
            font-style: normal;
            font-weight: 600;
            line-height: normal;
            letter-spacing: 0.96px;
            text-transform: uppercase;
    * .free
            *en CSS, utiliser les attributs suivants :
                color: #292929;
                font-family: Noto Sans Symbols;
                font-size: 36px;
                font-style: normal;
                font-weight: 700;
                line-height: 36px; /* 100% */
                letter-spacing: 4.68px;
    * .forever
            *en CSS, utiliser les attributs suivants :
                color: #2D4480;
                font-family: Allan;
                font-size: 36px;
                font-style: normal;
                font-weight: 400;
                line-height: 36px; /* 100% */
* Créer la ligne et la mettre entre le dernier p .feature et .free
    *en CSS, faire 188*1/0/0/0
    width: 188px;
    height: 1px;
    background-color: #000;

^^^^ Ceci était globalement ma réflexion pour écrire ma .whitecard, identifier le nombre p, images, div nécessaires, déterminer le nombre et types de classes pour les répartir, l'ordre dans lequel mettre tout ça. Je pense qu'en me posant et "planifiant" mon code d'avance, j'ai été plus efficace qu'en codant à "essayons voir".

**Je pense adopter pour la suite la méthode suivante; travailler en "zoom": partir du large avant de faire le spécifique. ici, j'ai d'abord fait le fond, la .whitecard, son contenu, puis le .yellowbuton et son contenu, les éléments de "chaque niveau" étant travaillés les uns à la suite des autres.**

La galère est venue quand j'ai voulu display:flex; cet ensemble d'éléments isolés les uns par rapport aux autres. Comment ça a été résolu (et grâce à l'aide de qui) ? RDV dans la section feedback perso !


## Feedback perso

Jusqu'à mettre tous les éléments, c'était nickel ! Cependant, je me suis vautré dans la manière d'arranger mes éléments :

* Je serais parti pour des heures de prise de tête en display flex avec des éléments en roue libre
* Selon **Hugo**, j'aurais dû partir sur des listes, où j'aurais modifié les dots et ce qui va en face
* Voyant l'expression de désespoir et de profonde tristesse se peindre sur mon visage, il m'a dit qu'avec des <div .bloc>, en vrai, ça peut le faire.
    * Et **Elodie** m'a confirmé que ça le fait !
    * --> Dans tous les cas, **TOUJOURS ASSOCIER D'UNE MANIERE OU D'UNE AUTRE LES ELEMENTS ALLANT ENSEMBLE**, que ce soit avec des listes, des div, ...

    14h44:  * j'ai compris des trucs ! .feature ne doivent pes être centrées, mais on joue avec les margin right et left, sans oublier de tripoter le gap !
            * white card va bouffer un padding haut de 35px et bas de 69px !

    EUREKA !!!!!! Pour avoir .whitecard et .yellowcard l'un en dessous de l'autre, il faut qu'ils,soient dans une p... de colonne !

    Astuce :    **Loukas** m'a montré les position: relative/absolute; permet de bouger des éléments les uns par rappoort aux autres !
                et pour aller plus loin, dès qu'un élément est en "relative", on peut le bouger avec top/right/bottom/left: ;

                J'ai bien tenté de bosser en utilisant par curiosité des margin-x:y; pour pisitionner .whitecard et .yellowbuton, mais c'est la foire aux déformations...

Enfin, ultime correction, j'ai changé le nom des features.