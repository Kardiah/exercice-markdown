# Utiliser MarkDown sur son site

Quand vous écrivez en Markdown, vous utilisez des notations raccourcies qui sont remplacées par les balises HTML correspondantes. Nous allons découvrir la plupart de ces notations raccourcies ici. À chaque fois, je vous indiquerai l'équivalent HTML de la notation Markdown. :smiley:

Vous allez voir, c'est super simple !

## Tester la syntaxe Markdown

Pour vous entraîner, le plus simple est de faire comme si vous alliez rédiger un message sur les [forums du Site du Zéro](https://openclassrooms.com/forum/categorie/discussions-generales) (attention il faut être inscrit pour poster un message). Cliquez bien sur **Markdown** pour passer en mode de rédaction Markdown (eh oui, certaines personnes moins à l'aise en informatique préfèrent l'éditeur WYSIWYG plus graphique).

## Les paragraphes

Commençons par le plus simple : les paragraphes de texte. Vous devez séparer votre texte par des lignes vides pour créer des paragraphes. C'est très intuitif, regardez :
```
Ceci est un paragraphe de texte.

Ceci est un autre paragraphe de texte !
```
Cela aura pour effet de traduire le texte en HTML, comme ceci :
```
<p>Ceci est un paragraphe de texte.</p>

<p>Ceci est un autre paragraphe de texte !</p>
```
Normalement, vous ne pouvez pas faire de retour à la ligne simple en Markdown au sein d'un paragraphe :
```
Mon paragraphe
Ligne juste en-dessous

```
Heureusement, certains sites (comme le Site du Zéro) utilisent une version modifiée de Markdown (appelée Sundown) qui autorise ces retours à la ligne simples.

## Emphase (gras, italique…)

Pour faire de l'emphase, c'est-à-dire de la mise en valeur, il vous suffit d'entourer les mots de votre choix entre des étoiles __*__ ou des traits de soulignement **_** (au choix, le résultat est le même). Il y a deux types d'emphase : l'emphase faible (généralement affichée en italique) et l'emphase forte (généralement affichée en gras).

## Emphase faible (italique)

On peut utiliser les deux notations suivantes :
```
Voici un mot *important* à mon sens
Voici un mot _important_ à mon sens
```
Dans les deux cas, le résultat sera le suivant :
```
<**p**>Voici un mot <**em**>important</**em**> à mon sens</**p**>

```
## Emphase forte (gras)

On peut utiliser les deux notations suivantes :
```
Voici des mots **très importants**, j'insiste !
Voici des mots __très importants__, j'insiste !
```
Résultat :
```
<p>Voici des mots <strong>très importants</strong>, j'insiste !</p>

```
## Les titres

Il y a plusieurs façons d'écrire des titres en Markdown. Voici la première syntaxe possible :
```
Titre de niveau 1
=================

Titre de niveau 2
-----------------
```
> Notez que le nombre de - et de = importe peu, ce qui compte c'est de "souligner" un peu le titre.

Traduction en HTML :
```
<h1>Titre de niveau 1</h1>

<h2>Titre de niveau 2</h2>

```
Il existe aussi une autre syntaxe pour les titres qui vous permet même de faire des titres de niveau 3 (et 4, et plus si affinités) :
```
# Titre de niveau 1

## Titre de niveau 2

### Titre de niveau 3
```

## Les listes

Créer des listes en Markdown est un vrai bonheur, vous allez voir qu'il n'y a rien de plus simple ! Comme vous le savez sûrement, il existe deux types de listes : les listes à puces et les listes numérotées.

## Les listes à puces
```
* Une puce
* Une autre puce
* Et encore une autre puce !
```
>Vous pouvez remplacer les étoiles par des tirets ou des signes « + », cela aura exactement le même effet !

Résultat en HTML :
```
<ul>
<li>Une puce</li>
<li>Une autre puce</li>
<li>Et encore une autre puce !</li>
</ul>
```
Notez que vous pouvez imbriquer les listes à puces :
```
* Une puce
* Une autre puce
    * Une sous-puce
    * Une autre sous-puce
* Et encore une autre puce !
```
Les listes à puces numérotées
Pour créer une liste numérotée, c'est très intuitif : il suffit de commencer les puces par des numéros !
```
1. Et de un
2. Et de deux
3. Et de trois
````
```
<ol>
<li>Une puce</li>
<li>Une autre puce</li>
<li>Et encore une autre puce !</li>
</ol>
```
## Les citations
Les citations fonctionnent comme les réponses des e-mails : vous devez précéder les lignes citées d'un chevron «> »!
```
> Ceci est un texte cité. Vous pouvez répondre
> à cette citation en écrivant un paragraphe
> normal juste en-dessous !
```
Résultat :
```
<blockquote><p>Ceci est un texte cité. Vous pouvez répondre à cette citation en écrivant un paragraphe normal juste en-dessous !</p></blockquote>
```
Sachez que vous pouvez imbriquer des citations et du Markdown à l'intérieur des citations !
```
> Une citation
>
> > Une réponse à la citation
> >
> > Réponse qui contient une liste à puces :
> >
> > * Puce
> > * Autre puce
```
## Codes source
### Bloc de code
Pour insérer un code source, il suffit de l'indenter, c'est-à-dire de le faire précéder de 4 espaces ou d'une tabulation :
```
Voici un code en C :

    int main()
    {
        printf("Hello world!\n");
        return 0;
    }
```
Résultat :
```
<p>Voici un code en C :</p>

<pre><code>int main()
{
    printf("Hello world!\n");
    return 0;
}
</code></pre>
```
### Code en ligne
Si vous voulez écrire un morceau de code au milieu d'un paragraphe, entourez-le d'accents graves comme ceci : `. Exemple :
```
La fonction `printf()` permet d'afficher du texte
```
Résultat :
```
<p>La fonction <code>printf()</code> permet d'afficher du texte</p>
````

>Sur un clavier AZERTY standard, l'accent grave peut être inséré avec la combinaison de touches Alt Gr + 7 (à effectuer deux fois). Si vous avez un clavier différent du mien la touche est peut-être ailleurs. Je reconnais qu'il y a des touches plus évidentes à trouver sur un clavier !

### Les liens
Pour créer un lien, vous devez placer le texte du lien entre crochets suivis de l'URL entre parenthèses :
```
Rendez-vous sur le [Site du Zéro](http://www.siteduzero.com) pour tout apprendre à partir de Zéro !
```
Résultat :
```
Rendez-vous sur le <a href="http://www.siteduzero.com">Site du Zéro</a> pour tout apprendre à partir de Zéro !
```
### Les images
Les images s'insèrent de la même façon que les liens. Vous devez simplement mettre un point d'exclamation devant les premiers crochets :
```
![Zozor](http://uploads.siteduzero.com/files/420001_421000/420263.png)
```
Le texte entre crochets est le texte alternatif de l'image (je vous invite à le renseigner à chaque fois pour ceux qui ne peuvent pas voir les images). Résultat :
```
<img src="http://www.monsite.com/image.png" alt="Zozor" />
```
### Barre de séparation
Faire une barre de séparation en Markdown ? Rien de plus intuitif !
```
-----------------
```
Vous pouvez aussi remplacer les tirets par des étoiles. Leur nombre importe peu (il faut au moins en mettre quelques-uns !).

Résultat :
```
<hr />
```
### Ressources pour aller plus loin
Vous venez d'avoir une bonne vue d'ensemble du Markdown et vous connaissez maintenant les principales possibilités offertes par ce petit langage étonnant. :) Sachez que nous n'avons pas couvert ici toutes les possibilités. On peut :

* Faire une table des matières de liens (liens par références) en pied de page ;
* Ajouter des infobulles aux liens et aux images ;
* Créer des tableaux (uniquement dans certaines implémentations de Markdown) ;
* etc.

Vous trouverez toutes les informations concernant le langage sur :

[Le site officiel de Markdown](https://daringfireball.net/projects/markdown/syntax)

[Cette traduction en français](https://michelf.ca/projets/php-markdown/syntaxe/)

>Et si ce que je veux faire n'est pas possible en Markdown ? :(

Écrivez simplement du HTML dans ce cas ! En effet, vous pouvez sans problème mixer du Markdown et du HTML quand vous le souhaitez :
```
Ce texte comprend du *Markdown* mais aussi du <abbr title="HyperText Markup Language">HTML</abbr> !
```
