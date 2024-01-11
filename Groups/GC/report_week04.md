# Maxime

Le point essentiel du cours se concentrait sur le double dispatch, un design pattern que j'avais déjà eu la chance d'étudier et que j'avais déjà trouvé très pratique car c'est une sorte de conditionnel bien plus facilement maintenable, et permet de choisir les responsabilités que l'on donne aux objets (on avait étudié un cas où l'on modélisait un péage, et différent types de véhicules passaient et le péage ne connaissant pas quel type de véhicule passe (interface Véhicule) il devait tout de même donner le prix à payer et la responsabilité ne pouvait pas revenir au Véhicule qui pouvait frauder, on a donc dû appliquer le double dispatch). De mon côté je suis allé chercher le livre "Pharo by Examples" qui me sert d'appui technique sur l'anayse des modules que l'on fait dernièrement.

# Thomas

Nous avons eu un cours sur le double dispatch. J'ai eu du mal à comprendre cela au début.
Nous avons pu travailler avec maxime sur l'analyse des différents projets en proposant une nouvelle PR sur AVL.

https://github.com/pharo-containers/AVL/pull/8