# Apprentissage avanc�: Transfer Learning on Stack Exchange Tags

Bienvenu sur notre projet d'apprentissage avanc�, o� nous tentons d'apporter une r�ponse au challenge kaggle Transfer Learning on Stack Exchange Tags.

### Truc � tenter:
Voir comment on s en sort pour retrouver les tags d�j�, voir si on peut faire un classifieur.
Dans le notebook "Learning" j'ai tent� de transformer les textes en tableaux de boolean (1 si le mot est pr�sent 0 sinon), puis avec une fonction calculer le tfidf. Ensuite faire de la classification multilabel, les labels �tant les tags.
�a marche pas pour l'instant, bloqu� � l'�tape du tfidf.


### Id�es:

On a 0 tag pour la physique: Il faut trouver le rapport entre un texte et ses tags.
Il faudrait trouver une m�thode qui � partir d'un texte sans connaitre les tag existants g�n�re de nouveaux tags.

D'apr�s l'exploration des donn�es �a me parait pas gagn�, les mots les plus courants du titre et contenu �tant relativement �loign� des tags les plus courants. Mais c'est juste des stat apr�s tout.

On pourrait commencer par trouver les mots inhabituels qui reviennent le plus de fois dans le texte, et d�cider que ce sont des tags simplement, et voir ce que �a donne.

On pourrait aussi faire �a en plusieurs �tapes:
- Traiter tout les textes pour extraire une liste de tag
- Assigner les tag de la liste de tag � chaque article

Avec cette m�thode, on pourra assigner un tag qu'on aurait pas vu au d�part � un article qui en aurait besoin, en d�couvrant le tag dans un autre article plus loin. Mais comment faire ?