# Apprentissage avancé: Transfer Learning on Stack Exchange Tags

Bienvenu sur notre projet d'apprentissage avancé, où nous tentons d'apporter une réponse au challenge kaggle Transfer Learning on Stack Exchange Tags.

### Truc à tenter:
Voir comment on s en sort pour retrouver les tags déjà, voir si on peut faire un classifieur.
Dans le notebook "Learning" j'ai tenté de transformer les textes en tableaux de boolean (1 si le mot est présent 0 sinon), puis avec une fonction calculer le tfidf. Ensuite faire de la classification multilabel, les labels étant les tags.
ça marche pas pour l'instant, bloqué à l'étape du tfidf.


### Idées:

On a 0 tag pour la physique: Il faut trouver le rapport entre un texte et ses tags.
Il faudrait trouver une méthode qui à partir d'un texte sans connaitre les tag existants génère de nouveaux tags.

D'après l'exploration des données ça me parait pas gagné, les mots les plus courants du titre et contenu étant relativement éloigné des tags les plus courants. Mais c'est juste des stat après tout.

On pourrait commencer par trouver les mots inhabituels qui reviennent le plus de fois dans le texte, et décider que ce sont des tags simplement, et voir ce que ça donne.

On pourrait aussi faire ça en plusieurs étapes:
- Traiter tout les textes pour extraire une liste de tag
- Assigner les tag de la liste de tag à chaque article

Avec cette méthode, on pourra assigner un tag qu'on aurait pas vu au départ à un article qui en aurait besoin, en découvrant le tag dans un autre article plus loin. Mais comment faire ?