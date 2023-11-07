## Fonctionnement du groupe 
Chacun fais son propre rapport. Puis on fusionne nos rapport pour savoir ce qu'on va dire et qu'elles sont les grand axes qui s'en dégége. Notre objectif est de comprendre à quoi sert ce frmaework, comment s'en servir et comment il est structuré. 

## Premier contacte avec le projet
 - Lecture du readme
 - Recherche d'un UML -> il n'y a pas d'UML, ce qui aurait pus donner une vision globale du projet
 - Lecture du guide.md
 - Lecture du Tutorial.md

## Installation du projet
 - Ouverture du playground
 - Execution de la commande
 - Je n'ai pas réussi à installer les artefacts
Le readme est clair et bien détaillé, dommage que certaine commande ne marche pas.

## Comment nous procédons
 - Lecture et application du guide
 - Lecture et application du tutoriel
 - Lecture des packages :
       - Il y a un package de test *Artefact-Core-Test*
       - Un package pour les exemples *Artefact-Exemple*
       - Un package pour la compatibilité avec Pharo *Artefact-Pharo60-Compatibility*
       - *Artefact-Core* doit être le coeur du projet
       - Je ne comprend pas ce que font les 2 autres packages
- Je reprend les commandes du guide et je vais observer les classes utiliser en lisant la doc
- Je regarde les méthodes utiliser et je vais lire leur noms et la documentation
- Si je ne comprend pas ce que font les classes/méthodes je vais regarder dans le code, si je ne comprend toujours pas j'ignore
- Il est également possible d'aller lire le nom des commits, de verifier la qualité des tests grâce aux mutants, etc
- Mon point de départ est cette ligne qui permet de faire un pdf :
       ```PDFDocument new add: (PDFPage new add: (PDFTextElement new text: 'Hello'; from: 10mm@10mm)); exportTo: 'test.pdf' asFileReference writeStream```


## Ce que nous apprenons du projet
 - En Smalltalk
 - Est un framwork qui permet de générer des pdf
 - Les pdf sont en effet simple à créer pour l'utilisateur, et les exemples sont assez explicite
 - J'ai réussi à creer tous les pdf des exemples, ils sont dans le dossier pdf de l'image et il y a le tests à la racine de celle-ci
 - Tous les tests passent
 - Tout hérite de pdfComposite
 - On peut personnaliser beaucoup de chose comme la font, le style, les couleurs, l'ordre des pages, la polices
 - Il y a 6 packages
 - PDFDocument permet de mettre en page le pdf
 - La classe abstraite PDFElement permet d'ajouter des elements comme des dessins, des images, du textes
 - Il y a aussi des classes qui s'occupe de la mise en page, de la font, ... etc
 - On peut gérer le type de donnée voulus gràce à la classe PDFDataType
 - Le package ```ArtefactExample``` donne des exemples de pdf faisable

### Design Pattern
 - Visiteur, on observe un visiteur avec la classe abstraite PDFDataType
 - Composite, PDFCompositeCodeSegement. Il y a des composite à différents endroit du code ils sont là pour s'occuper de la structure

## Ce que nous apprennons sur pharo
 - Les classe avec un T vert représente un trait
 - Quand une classe est une exception il y a un petit éclair

## Tests
 - Il y a un coverage de 42,86% ce qui est bas, il faudrait un coverage plus élevé
 - Selon le coverage il y a 4 méthodes non testé
 - Les tests sont surement pas assez précis
 - Je me suis interessé aux tests de PDFDataTypeTest la classe avec le visiteur, ce ne sont que des tests très basiques au vus du coverage c'est surement pareil dans tout le code aux vue du coverage
 - Dans le package de test 2 classes abstraites sont définis elle retourne des "résultat fixe", et sont utilisé dans des méthodes de tests pour ne rien faire, ces classes ne servent pas elles pourraient être dans les tests.

## Exception
 - Il y a des exceptions au seins du projet ce qui signifie qu'un endroit doit lever ces exceptions
 - L'exception ArtefactOverSizeContent est appelé uniquement dans la classe PDFParagrapheElement elle permet de vérifier qu'on ne dépasse pas taille
 - D'ailleurs la méthode ```splitOn: aPage using: aFont``` a une complexité de O(n²), elle semble assez longue, elle est surement simplifiable, apres avoir regardé elle n'est même pas testé
 - Il faudrais donc tester cette méthode et avec plusieurs tests, étant donné qu'il y a plusieurs conditions, une exception
 - Pour la seconde exception ```ArtefactundefinedAttribute``` est présente dans la classe PDFElement et la classe PDFElementTest
 - Dans la classe de tests il y a 2 méthodes qui utilisent l'interface mais aucune de ces méthodes ne test la méthode checkAttribute de PDFElement

## Debugger
 - Dans le package ArtefactsExemple, dans la classe PDFDemos il y a la méthode cellTest qui est apparement bugger selon le point d'exclamation à coté de la la methode
 - Apres avoir regardé la méthode il y a en faite un TODO et du code commenté dedans ce qui est moche en dehors de ça le code est long et devrais être simplifié
 - 
 

## Questions
 - Il y a des sortes de sous packages vides
