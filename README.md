# <center>Mémo pour la syntaxe Markdown </center>
<p>&nbsp</p>

### Introduction




Ce document est mon mémo concernant le markdown et un inventaire de sa syntaxe.


##### Qu'est ce que Markdown ?
Markdown est un système d’édition et de formatage de texte ;
c’est à la fois une syntaxe, un script de conversion texte → HTML et un format de fichier.
  Il est couramment utilisé pour les fichiers de documentation d’un projet ou d’un jeu de données -souvent nommé readme.md. Il est stocké au format texte classique.

La philosophie du système veut que le texte écrit
      soit lisible sans interpréteur particulier en mode texte. Il est léger et épuré de l’essentiel de la verbosité d’un language balisé. Les éléments de syntaxe sont des caractères de ponctuation qui font sens visuellement même non convertis. Une fois converti, le navigateur web (qui joue alors le rôle d’interpréteur) en rendra la lecture plus claire.

Les fichiers sont généralement enregistrés avec l’extension .md (ou .markdown).

Sources :
* [Un guide pour bien commencer avec Markdown](https://blog.wax-o.com/2014/04/tutoriel-un-guide-pour-bien-commencer-avec-markdown/)
* [NicolasJamar /memo-markdown ](https://github.com/NicolasJamar/memo-markdown)


## Sommaire
* [La mise en forme](#la-mise-en-forme)
* [Les titres](#les-titres)
* [Les listes](#les-listes)
* [Les liens](#les-liens)
* [Les images](#les-images.md)
* [Les citations](#les-citations)

<p>&nbsp</p>

### La mise en forme
* Pour mettre en **gras**  : `**du gras**`.
* Pour mettre en *italique*  : `*de l'italique*`.
* pour barrer [u] le texte[/u] : ``
* pour barrer le [u]Texte[/u] : ``

Pour passer à la ligne...
... plutôt que de changer de paragraphe terminez la ligne par deux espace ou plus.
Sinon cela ne marche pas (saut de ligne simple = pas de saut).

Une ou plusieures lignes vides entraînent un changement de paragraphe.

```
Pour passer à la ligne...<espace><espace>
... plutôt que de changer de paragraphe terminez la ligne par deux espace ou plus.
Un simple retour chariot ne suffit pas (saut de ligne simple = pas de saut).





Une ou plusieures lignes vides entraînent un changement de paragraphe
```
Pour sauter plusieurs lignes entre
<p>&nbsp</p>

deux paragraphes, on utilise des balises **html**.
```
Pour sauter plus d'une ligne entre
<p>&nbsp</p>
<p>&nbsp</p>
deux paragraphes
```
**Nativement**, Il n'est pas possible
<center> de centrer le texte,  </center>
<div style="text-align:right;">de l'aligner à droite   </div>
<div style="text-align:left;">ou à gauche.</div>
<p>&nbsp</p>


Il faut utiliser là aussi des balises html.

```
**Nativement**, Il n'est pas possible
<center> de centrer le texte,  </center>
<div style="text-align:right;">de l'aligner à droite   </div>
<div style="text-align:left;">ou à gauche.</div>

```
Idem pour justifier :
<div style="text-align:justify;">Le Lorem Ipsum est simplement du faux texte employé dans la composition et la mise en page avant impression. Le Lorem Ipsum est le faux texte standard de l'imprimerie depuis les années 1500, quand un peintre anonyme assembla ensemble des morceaux de texte pour réaliser un livre spécimen de polices de texte.</div>

```
<div style="text-align:justify;">Le Lorem Ipsum est simplement du faux texte employé dans la composition et la mise en page avant impression. Le Lorem Ipsum est le faux texte standard de l'imprimerie depuis les années 1500, quand un peintre anonyme assembla ensemble des morceaux de texte pour réaliser un livre spécimen de polices de texte</div>
```



[Retour au sommaire](#sommaire)
<p>&nbsp</p>

### Les titres


  ###### Ici un titre de niveau 6
  ##### Ici un titre de niveau 5
  #### Ici un titre de niveau 4

Syntaxe:
```
###### Ici un titre de niveau 6
##### Ici un titre de niveau 5
#### Ici un titre de niveau 4
```
Les titres peuvent servir d'ancre pour des liens. Cf. la section concernant ['les liens'](#les-liens).

[Retour au sommaire](#sommaire)
<p>&nbsp</p>

### Les listes
##### La liste à puces

*Pour créer une liste à puces, procédez de la manière suivante*

 * Ecrivez un astérisque
 * Ecrivez votre texte
 * Faites la même chose à la ligne suivante

Syntaxe :
```
     * Ecrivez un astérisque
     * Ecrivez votre texte
     * Faites la même chose à la ligne suivante
```
[Retour au sommaire](#sommaire)

##### La liste numérotée

*Pour créer une liste numérotée, procédez de la manière suivante*

  1. Mettez un chiffre
  2. Mettez un point
  3. Mettez votre texte
  4. Répétez les 3 points précédents avec la suite logique du chiffre

Syntaxe :
```
    1. Mettez un chiffre
    2. Mettez un point
    3. Mettez votre texte
    4. Répétez les 3 points précédents avec la suite logique du chiffre
```
[Retour au sommaire](#sommaire)


##### La liste à puces imbriquées

  *Pour créer des listes à puces imbriquées, procédez comme suit:*

  * Ecrivez un astérisque
  * Ecrivez votre texte
  * Faites la même chose à la ligne suivante
     * Faire un retrait
       - Créez une nouvelle liste
         - Et ainsi de suite...

Syntaxe :

```
* Ecrivez un astérisque
* Ecrivez votre texte
* Faites la même chose à la ligne suivante
    * Faire un retrait
       * Créez une nouvelle liste
          * Et ainsi de suite...
```
[Retour au sommaire](#sommaire)
<p>&nbsp</p>

### Les liens ###

Exemple : un [lien vers la page Wikipédia sur Markdown](https://fr.wikipedia.org/wiki/Markdown)

Syntaxe :

```
[texte du lien](url_du_lien "facultatif : texte pour le titre")
[lien vers la page Wikipédia sur Markdown](https://fr.wikipedia.org/wiki/Markdown)

```

Le lien peut être absolu ou relatif, il peut pointer sur une page html ou markdownet éventuellement sur une ancre


exemples :
```
(https://monsite/ma_page.HTML "mon_titre")
(./ma_page.md "mon titre")
(./ma_page.html#mon-ancre "mon titre")
()./ma_page.md#mon-ancre)
```

Si l'ancre est sur le même document que le lien, on omet la page.
Exemple :

```
[Retour au sommaire](#sommaire) // renvoie ver la balise 'sommaire' de ce document
```

[Retour au sommaire](#sommaire)
<p>&nbsp</p>

### Les Images
<p>&nbsp</p>

  ![Logo de markdown](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/1200px-Markdown-mark.svg.png "logo Mardown de wikipedia")

   Syntaxe :
```
    ![Texte alternatif](url_de_l'image)

    ![Texte alternatif](url_de_l'image "facultatif : texte pour le titre")

      Ci-dessus :
    ![Logo de markdown](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/1200px-Markdown-mark.svg.png "logo Mardown de wikipedia")
```
[Retour au sommaire](#sommaire)

### Les citations
Elle peuvent être dans une `ligne de texte` ou
```
dans un bloc
```
Ce qui donne :

    Elle peuvent être dans une `ligne de texte` ou
      ```
      dans un bloc
      ```
