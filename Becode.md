# Les liens

Pour créer un lien, vous devez placer le texte du lien entre crochets suivis de l'URL entre parenthèses :

```

Rendez-vous sur le [Site du Zéro](http://www.siteduzero.com) pour tout apprendre à partir de Zéro !

```
Résultat :
```

Rendez-vous sur le <a href="http://www.siteduzero.com">Site du Zéro</a> pour tout apprendre à partir de Zéro !

```

# Les images
Les images s'insèrent de la même façon que les liens. Vous devez simplement mettre un point d'exclamation devant les premiers crochets :
```

![Zozor](http://uploads.siteduzero.com/files/420001_421000/420263.png)

```
Le texte entre crochets est le texte alternatif de l'image (je vous invite à le renseigner à chaque fois pour ceux qui ne peuvent pas voir les images).


 Résultat :

 ```

<img src="http://www.monsite.com/image.png" alt="Zozor" />

```

# Barre de séparation
Faire une barre de séparation en Markdown ? Rien de plus intuitif !
```
-----------------
```
Vous pouvez aussi remplacer les tirets par des étoiles. Leur nombre importe peu (il faut au moins en mettre quelques-uns !).


Résultat :


```
<hr />
```
# Ressources pour aller plus loin

Vous venez d'avoir une bonne vue d'ensemble du Markdown et vous connaissez maintenant les principales possibilités offertes par ce petit langage étonnant. :) Sachez que nous n'avons pas couvert ici toutes les possibilités. On peut :

* Faire une table des matières de liens (liens par références) en pied de page

* Ajouter des infobulles aux liens et aux images ;

* Créer des tableaux (uniquement dans certaines implémentations de Markdown) ;

* etc.

Vous trouverez toutes les informations concernant le langage sur :

[Le site officiel de Markdown](https://daringfireball.net/projects/markdown/syntax)

[Cette traduction en français](http://michelf.ca/projets/php-markdown/syntaxe/)

Et si ce que je veux faire n'est pas possible en Markdown ? :(

Écrivez simplement du HTML dans ce cas ! En effet, vous pouvez sans problème mixer du Markdown et du HTML quand vous le souhaitez :
```
Ce texte comprend du *Markdown* mais aussi du <abbr title="HyperText Markup Language">HTML</abbr> !
```
