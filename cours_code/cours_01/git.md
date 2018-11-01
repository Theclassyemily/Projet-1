<h2>1. Git et GitHub</h2>
<h3>1.1 Introduction</h3>
Ce cours t'introduira à Git et Github, deux fantastiques outils qui permettent de faire des sauvegardes efficaces d'unprojet, et de travailler à plusieurs sur le même dossier.

Dans cette leçon, nous allons te montrer comment installer Git, comment s'en servir, et comment le faire marcher. Pour ceci, nous allons nous aider de l'excellent [cours](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github) sur OpenClassrooms de Marc Gauthier, sur Git et GitHub.

<h3>1.2. Historique</h3>
Git est un outil de versionning de code, c'est à dire que c'est une commande qui permet de faire des sauvegardes, avec commentaires d'un projet. Ainsi, il est facile de revenir d'une version de sauvegarde à l'autre, et c'est même optimisé pour les projets où tout le monde travaille sur le même fichier !  

En gros, c'est la même chose quand vous faîtes une grosse présentation PPT. Vous faites tellement de modifications dessus que vous vous retrouvez à la fin avec le nom "VF_ avec_ retours_ Jean01_final.ppt". Le versionning vous permet d'avoir toutes les versions sauvegardées, et de revenir à celles que vous voulez à tout moment, et de nous éviter ces tracas.

Voilà à quoi Git sert : à mieux gérer ses versions entre les fichiers d'un projet (bonus : Git marche pour tous les fichiers d'un dossier concerné, donc c'est encore plus puissant que CTRL + S). Et GitHub permet de mettre en ligne ton projet, comme ça vous pourrez travailler facilement en équipe dessus.

Pour information, Git a été créé en 2005 par Linus Torvald, qui a (entre autres) créé le système d'exploitation Linux.

<h3>1.3. Le cours</h3>
<h4>1.3.1. Installer Git</h4>

Avant de pouvoir se servir de Git, il faut l'installer. Cela tombe bien, il y a un [chapitre éponyme](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github/installer-git) dans le cours sur OC.

<h4>1.3.2. Première introduction à Git</h4>

J'ai fait une petite vidéo d'introduction à Git, que tu pourras retrouver ci-bas:
![youtube](http://image.noelshack.com/fichiers/2018/44/4/1541071993-thp.png) 

Ensuite, tu peux suivre le cours de Marc Gauthier jusqu'à la partie [Récupérez des modifications](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github/recuperer-des-modifications). Nous verrons dans la formation THP comment faire les branches et autres joyeusetés 😇

<h3>1.4. Points importants à retenir</h3>
<h4>1.4.1 Les commandes pratiques</h4>
Voici un récap des commandes de base:  

* $ git init : il faut TOUJOURS commencer par initialiser git avec cette commande. Avec cette commande, le répertoire courant est considéré comme un repository git  
* $ git add [fichier] : ajoute aux sauvegardes le fichier mentionné. **Protip** : si tu as plusieurs fichiers à ajouter, tu peux utiliser $ git add . qui ajoute au repository tous les fichiers du dossier  
* $ git commit -m [commentaire] : créé un commit (commit = sauvegarde suivie d'un commentaire).  
* $ git status : te dit le status actuel de git.
<h3>1.4.2 Lire l'historique</h3>
$ git log : permet de voir l'historique et de voir tous les commits. Les commits sont rangés avec:  

* SHA: liste de chiffres et lettres qui identifient de façon unique le commit.  
* Auteur  
* Date  
* Message donné durant le commit: avec ce message, tu vas comprendre ce que faisait le commit. C'est pour cela qu'il est important d'avoir un bon nom.
<h5>Pour quitter le log, il faut appuyer sur Q.</h5>

<h3>1.4.3 Se positionner sur un commit donné</h3>
Imaginons que veut vérifier un truc sur un vieux commit. On va utiliser la commande $ git checkout, utilisée comme ceci :  

* $ git checkout 45581cebdd2cae494f80f4401af9e4a86c9b8fa: on dit à git de se positionner sur ce sha précis.  
* $ git checkout master: une fois que l'on a fini de se balader, il faut revenir à la version présente de notre repository avec cette commande.

⚠️ **ALERTE ERREUR COMMUNE**

>$ git checkout ne marche que si tu n'as pas de modification non sauvegardée. Si tu es entre deux commits, git checkout ne marchera pas. Du coup il te faudra soit faire une sauvegarde (== faire un commit), soit effacer tout pour revenir au commit d'avant.
>
>$ git checkout n'est pas une commande pour revenir en arrière et faire des modifications sur les anciens commits. Si tu fais ça, tu vas te retrouver avec une erreur qui a donné lieu à [l'un des threads](https://stackoverflow.com/questions/5772192/how-can-i-reconcile-detached-head-with-master-origin) les plus célèbres de Stack Overflow. Pour tout effacer et revenir en arrière, le chapitre suivant sera là pour toi.

<h3>1.4.4. Revenir en arrière</h3>

J'ai fait des trucs, mais cela ne me convient pas. Comment revenir en arrière ? (inspiré par [cette excellente](https://stackoverflow.com/questions/4114095/how-to-revert-git-repository-to-a-previous-commit/4114122#4114122) réponse de Stack Overflow)

<h4>1.4.4.1. Effacer pour revenir au commit d'avant</h4>
La fonction $ git reset --hard permet de revenir au commit précédent, en effaçant tout. C'est une commande pratique quand on veut essayer de nouvelles choses à la volée, puis de revenir en arrière comme si de rien n'était ✌️

<h4>1.4.4.2. Tout effacer et revenir à un ancien commit</h4>
On peut faire ceci avec : $ git reset --hard 45581cebdd2cae494f80f44010af9e4a86c9b8fa, avec 45581c le SHA sur lequel tu veux revenir.

<h3>1.5. Pour aller plus loin</h3>

Au vu des apologies que l'on lui donne, le [cours de OpenClassrooms](https://openclassrooms.com/courses/gerer-son-code-avec-git-et-github) sur Git est un très bon point pour aller plus loin. Il explique notamment la notion de branches et de fusions.

Aussi, voici [un cours](https://www.vikingcodeschool.com/web-development-basics/getting-to-know-git) sur Git de la Viking Code School. Il explique bien les bases de Git et est une bonne alternative au notre.

