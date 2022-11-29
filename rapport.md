# Rapport

## 1. Synthèse de l'article
- Contexte : quelle est la problématique générale abordée par l'article ?

      La problématique traité par ce papier décole du fait qu'en astronomie, les images contiennent une énorme quantié de sources lumineuses. L'extraction manuelle de chacun de ces sources n'est pas envisageable. De plus, beaucoup de ces sources ont une intensité faible, ils se rapprochent quasiment au niveau de bruit.

- Objectifs : quel est le but de la méthode proposée dans l'article ?

      Cet article propose une méthode pour extraire de manière automatique sur des photographies, ces sources lumineuses, que l'on a mentionné plus haut. Cette méthode s'appelle MTObjects.


- Hypothèses : pourquoi l'approche proposée est-elle pertinente pour atteindre les objectifs ?

      Cet article compare la méthode MTObjects avec SExtractor, une méthode de référence pour l'extraction de sources. MTObjects pourrait être plus pertinente que SExtractor pour l'extraction de sources, car contrairement à SExtractor, MTObjects n'utilise un mécanisme de treshold fixe, mais il se base sur chaque node de l'arbre Max-Tree.

- Méthode : comment fonctionne la méthode proposée ?

      L'algorithme mtObjects prend en entrée une image I, une fonction nodeTest, un niveau de significance α, un gain g et un facteur de déplacement λ. Il renvoie un arbre Max-Tree M. Les nœuds de M correspondant aux objets sont marqués. L'algorithme mtObjects est décrit en détail dans l'article.
      Dans un premier temps on éstime la moyenne et la variance de l'arrière plan de l'image. On applique ensuite un seuillage à l'image I, en soustrayant la moyenne de l'arrière plan. On crée ensuite une représentation Max-Tree de l'image. On applique ensuite la fonction SignificantNodes sur l'arbre Max-Tree. On trouve ensuite les objets dans l'arbre Max-Tree. On déplace ensuite les objets vers le haut de l'arbre Max-Tree.

- Méthodologie de validation : quels sont les tests proposés par les auteurs pour valider leurs hypothèses ? pour valider leur méthode ?

      Ils ont réalisé des tests sur différents types d'objets celestes, sur une image d'une simulation de 25 étoiles pour tester la détéction du background et du bruit avec la segmentation de SExtractor, sur des galaxies et autres objets avec des régions extérieures plus pâles et des objets imbriqués, sur une portion d'image représentant la fragmentation d'une fine lamentation faible entre deux galaxies, sur des voies de poussières et des artefacts.


- Résultats : quels sont les résultats obtenus par les auteurs ?

      Les tests précédent révèlent que de manière générale, MTObjects conserve mieux les contours de faible intensité des objets et les objets imbriqués. MTObjects est plus rapide que SExtractor. MTObjects est plus robuste que SExtractor face au bruit et aux artefacts. MTObjects est plus fiable que SExtractor face à la fragmentation d'objets. MTObjects gère mieux que la présence de poussières que SExtractor.

- Opinion personnelle : quelle est votre impression personnel sur l'article ? (intérêt, qualitén d'écriture, des hypothèses, de la méthode, des tests ,des résultats, etc.)

      On aurait aimé voir un paper plus modeste, faisant preuve d'humilité.

## 2. Etude de l'implémentation
- la portée des programmes fournis : le code fourni permet-il de reproduire la totalité des experiences présentées dans l'article ? (si non, quels sont les points manquants ?)
- la structure : quelles sont les interfaces fournies ? le code est-il bien structuré ? pensez vous pouvoir le réutiliser dans un autre contexte ?
- la fidélité : le code fourni correspond-il à ce qui est décrit dans l'article ? Si non, quelles sont les différences notables ?

## 3. Expérimentations
- expériences reproduites : décrivez les expériences que vous avez choisies de reproduire.

      Nous avons reproduit les expériences sur les images de galaxies, de poussières et d'artefacts.

- configuration des tests : précisez les paramètres que vous avez utilisés pour reproduire les expériences. (choix des images, choix des paramètres).



- analyse des résultats : analysez les résultats obtenus, sont-ils conformes aux résultats présentés dans l'article ? (comparaison avec les résultats de l'article)



- expériences complémentaires : pouvez-vous proposer des expériences complémentaires pour évaluer la méthode ? (choix des images, choix des paramètres).
      
      Oui, images prisent sur internet