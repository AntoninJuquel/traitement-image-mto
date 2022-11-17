# Rapport

## 1. Synthèse de l'article
- Contexte : quelle est la problématique générale abordée par l'article ?

      In astronomy, sky surveys contain a huge quantity of light-emitting sources, representing astronomical objects. Manually extracting every object is not feasible, due also to the low intensities of many sources, often close to the noise level.

      <!-- translation in french -->

      En astronomie, les cartographies du ciel contiennent une quantité énorme de sources lumineuses, représentant des objets astronomiques. Extraire manuellement chaque objet n'est pas faisable, en raison aussi des faibles intensités de nombreuses sources, souvent proches du niveau de bruit.

- Objectifs : quel est le but de la méthode proposée dans l'article ?

      The goal of this paper is to propose a method to automatically extract astronomical sources from sky surveys optimal with faint extended sources.

      <!-- translation in french -->

      L'objectif de cet article est de proposer une méthode pour extraire automatiquement des sources astronomiques à partir de cartographies du ciel optimales avec des sources étendues faibles.

- Hypothèses : pourquoi l'approche proposée est-elle pertinente pour atteindre les objectifs ?

      Using SExtractor as a reference, the paper describes an improvement of a previous method proposed by the authors. It is a Max-Tree-based method for extraction of faint extended sources without using a stronger image smoothing.

      <!-- translation in french -->

      En utilisant SExtractor comme référence, l'article décrit une amélioration d'une méthode précédente proposée par les auteurs. Il s'agit d'une méthode basée sur les Max-Trees pour l'extraction de sources étendues faibles sans utiliser un affinage d'image plus fort.

- Méthode : comment fonctionne la méthode proposée ?

      The Max-Tree structure is a hierarchical representation of an image, in which attributes can be computed in every node. Object detection is performed on the nodes of the tree and it relies on the distribution of a statistic calculated using the power attribute, compared to the expected distribution in case of noise. Statistical tests are presented, a comparison with the object extraction of SExtractor is shown and results are discussed.

      <!-- translation in french -->

      La structure Max-Tree est une représentation hiérarchique d'une image, dans laquelle des attributs peuvent être calculés dans chaque nœud. La détection d'objets est effectuée sur les nœuds de l'arbre et elle repose sur la distribution d'une statistique calculée à l'aide de l'attribut de puissance, comparée à la distribution attendue en cas de bruit. Des tests statistiques sont présentés, une comparaison avec l'extraction d'objets de SExtractor est montrée et les résultats sont discutés.

- Méthodologie de validation : quels sont les tests proposés par les auteurs pour valider leurs hypothèses ? pour valider leur méthode ?
- Résultats : quels sont les résultats obtenus par les auteurs ?
- Opinion personnelle : quelle est votre impression personnel sur l'article ? (intérêt, qualitén d'écriture, des hypothèses, de la méthode, des tests ,des résultats, etc.)

## 2. Etude de l'implémentation
- la portée des programmes fournis : le code fourni permet-il de reproduire la totalité des experiences présentées dans l'article ? (si non, quels sont les points manquants ?)
- la structure : quelles sont les interfaces fournies ? le code est-il 
- la fidélité : le code fourni correspond-il à ce qui est décrit dans l'article ? Si non, quelles sont les différences notables ?

## 3. Expérimentations
- expériences reproduites : décrivez les expériences que vous avez choisies de reproduire.
- configuration des tests : précisez les paramètres que vous avez utilisés pour reproduire les expériences. (choix des images, choix des paramètres).
- analyse des résultats : analysez les résultats obtenus, sont-ils conformes aux résultats présentés dans l'article ? (comparaison avec les résultats de l'article)
- expériences complémentaires : pouvez-vous proposer des expériences complémentaires pour évaluer la méthode ? (choix des images, choix des paramètres).