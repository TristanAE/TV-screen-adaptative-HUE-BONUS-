# TV-screen-adaptative-HUE-BONUS-
Les lampes connectées de la marque HUE Phillips s’adaptent aux couleurs de la télévision sans boitier de synchronisation à 200€.
Il existe une application sur ordinateur, HUE Sync, permettant de synchroniser la lumière avec les couleurs de l’écran. Nous utiliserons cette application ainsi qu’un programme python très simple pour l’adapter à notre télévision.

# I-	Conception matérielle  

Tout d’abord l’objectif est de récupérer le flux vidéo des chaines TV ou d’une console . 
Pour cela, j’utilise personnellement mon boitier TV Orange ou ma PS4 dont je récupère le flux directement grâce leur câble HDMI. Il faut ensuite pouvoir envoyer ce flux vers un ordinateur ou nano-ordinateur, je vais donc utiliser une carte d’acquisition HDMI 4k USB.

Dans un second temps, nous souhaitons rediriger à la fois le flux vidéo sur notre téléviseur et sur l’ordinateur. Nous devons donc nous procurer un splitter : une entrée HDMI vers 2 sorties HDMI.

L’unique entrée est branchée au boitier Orange ou à la console, une des sorties au téléviseur et enfin la dernière à la carte d’acquisition elle-même connectée à l’ordinateur.

# II-	Conception informatique 

Après avoir splitté le flux, celui-ci s’affiche correctement sur le téléviseur, mais il va maintenant falloir nous servir d’un simple programme python pour afficher le flux à l’écran d’ordinateur.

Nous allons utiliser la bibliothèque OpenCV et la fonction VideoCapture() sur le chanel 1 ou 2 correspondants à la carte d’acquisition connectée à l’ordinateur.
En mettant le retour vidéo en plein écran et en activant l’application Hue Sync, les lampes connectées prendront la couleur de l’écran d’ordinateur soit du retour TV ou console.

Il est ensuite possible de créer son propre boitier avec une Raspberry pu faire un programme plus complexe de traitement d’images.

