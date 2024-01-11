Jump to :
[Nizar](#nizar)
[Lina](#lina)
[Rachid](#rachid)

# Rachid

### Ce que j'ai appris

- L'existence des "traits", dont j'ai pu comprendre l'utilité en posant des questions à Guille.

- J'ai revu ce que représentaient self et super (le receveur du message pour les deux) et le fait qu'ils initiaient le mécanisme de look up à des endroits différents.
Self fait démarrer le look up dans la classe du receveur (la méthode à appeler est donc trouvée dynamiquement) tandis que super fait démarrer le look up dans la superclasse de la classe qui utilise super (la méthode à appeler est donc connue statiquement puisqu'elle ne dépend pas du receveur du message contrairement à self).

### Comment j'ai appris

En suivant le cours et en posant des questions à Guille. J'ai aussi lu un peu de code du projet Artefact en faisant un "inspect it" sur certains éléments pour essayer d'en comprendre l'implémentation.

### Ce que j'aimerais comprendre

- Je n'ai toujours pas trouvé de réponse à la question que je me posais en semaine 1.
- J'aimerais m'ameliorer en reverse engineering, j'ai tendance à vouloir tout comprendre, ce qui n'est pas le but car le temps est précieux.


# Lina

Cette semaine, j'ai revu les notions de polymorphisme, late binding et héritage, ainsi que la différence entre self et super. J'ai maintenant une définition précise de ces deux éléments.

J'ai ensuite réalisé l'implémentation du 'or' en pharo, sans utiliser de conditionnelles (if).

J'ai également commencé à travailler sur le projet Artefact avec Rachid, en vue de la présentation.
On a installé le projet sur pharo, commencé à regarder les différents packages, classes, méthodes et lu les questions auxquelles il faut qu'on réponde en analysant ce projet.
On n'a pas encore commencé l'analyse du projet mais cela nous permet de savoir quoi chercher par la suite.

En parallèle, j'ai aussi regarder les vidéos concernant les notions de cours abordées pendant les 2 premières séances pour vérifier que tout était clair pour moi et vérifier qu'il n'y avait pas des informations que j'avais manqué en cours.


# Nizar

### Ce que j'ai appris

Pendant cette deuxième semaine, je me suis rendu compte du vrai intérêt du late binding et son impact sur la fléxibité et la polymorphie dans la POO.

En implémentant la version eager du ou ( | ) expliquée dans le cours, j'ai mieux compris l'intérêt de faire en sorte que toute (chose) soit un objet.

Le reste du cours étant porté sur l'héritage, la différence entre this et super, cela a été un rappel des notions acquises en génie logiciel pendant la L3.

Je travaillerai prochainement sur l'analyse du projet AVL, Lina et Rachid ayant choisi le projet Artefact.

### Comment j'ai appris

Mon apprentissage s'est principalement déroulé en relisant les diapo du cours et en regardant les vidéos mises à notre disposition. L'implémentation du OR m'a aidé aussi.

### Ce que j'aimerais comprendre

Les rappels de cours que l'on a eus pour l'instant ont été très clairs.

J'aimerais surtout apprendre de nouvelles notions de la POO et éventuellement corriger et/ou étendre les principes acquis lors du cours GL de l'année dernière.
