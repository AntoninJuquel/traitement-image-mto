# Rapport

## 1. Synthèse de l'article
- Contexte : quelle est la problématique générale abordée par l'article ?

      La problématique traité par ce papier décole du fait qu'en astronomie, les images contiennent une énorme quantié de sources lumineuses. L'extraction manuelle de chacun de ces sources n'est pas envisageable. De plus, beaucoup de ces sources ont une intensité faible, ils se rapprochent quasiment au niveau de bruit.

      Il semble que la problématique générale abordée par l'article concerne l'extraction automatisée d'objets astronomiques dans les relevés du ciel, qui peuvent contenir de nombreuses sources lumineuses à des intensités proches du niveau de bruit. SExtractor est un outil largement utilisé pour cette tâche, mais il peut ne pas être optimal pour l'extraction de sources étendues faibles. L'article décrit une amélioration d'une méthode précédemment proposée par les auteurs, qui est une méthode basée sur l'arbre Max pour l'extraction de sources étendues faibles sans utiliser de lissage d'image plus fort. L'objectif de cette méthode est d'améliorer l'extraction de sources étendues faibles par rapport à SExtractor, en utilisant une représentation hiérarchique de l'image connue sous le nom d'arbre Max et en comparant la distribution d'une statistique calculée à l'aide de l'attribut de puissance à la distribution attendue dans le cas du bruit.

- Objectifs : quel est le but de la méthode proposée dans l'article ?

      Cet article propose une méthode pour extraire de manière automatique sur des photographies, ces sources lumineuses, que l'on a mentionné plus haut. Cette méthode s'appelle MTObjects.

      le but de la méthode MTObjects est de détecter et de mesurer les propriétés de sources d'image dans les images en astrophysique de manière plus précise et plus efficace que les méthodes existantes, en particulier pour les sources de faible intensité. La méthode vise également à améliorer la méthode de seuil fixe utilisée par SExtractor en utilisant une approche plus adaptative qui tient compte des propriétés des objets détectés.

      Le but de la méthode proposée dans l'article est d'améliorer l'extraction de sources étendues faibles dans les relevés du ciel en utilisant une représentation hiérarchique de l'image connue sous le nom d'arbre Max. Cette méthode vise à améliorer les performances de SExtractor, qui est un outil largement utilisé pour l'extraction automatisée d'objets astronomiques, mais qui peut ne pas être optimal pour l'extraction de sources étendues faibles. La méthode proposée utilise l'arbre Max pour calculer différents attributs à différents noeuds de l'arbre, puis effectue la détection d'objets sur les noeuds de l'arbre en comparant la distribution d'une statistique calculée à l'aide de l'attribut de puissance à la distribution attendue dans le cas du bruit. Le but final de cette méthode est de permettre une extraction plus précise et fiable de sources étendues faibles dans les relevés du ciel, sans avoir besoin de recourir à un lissage d'image plus fort.

      La méthode est particulièrement utile pour détecter des sources de faible intensité dans les images, comme celles présentes dans les images de galaxies en interaction ou superposées.


- Hypothèses : pourquoi l'approche proposée est-elle pertinente pour atteindre les objectifs ?

      Cet article compare la méthode MTObjects avec SExtractor, une méthode de référence pour l'extraction de sources. MTObjects pourrait être plus pertinente que SExtractor pour l'extraction de sources, car contrairement à SExtractor, MTObjects n'utilise un mécanisme de treshold fixe, mais il se base sur chaque node de l'arbre Max-Tree.

      Il semble que l'approche de la méthode MTObjects est pertinente pour atteindre ses objectifs pour plusieurs raisons :

      Utilisation d'une représentation hiérarchique de l'image : en utilisant une représentation hiérarchique de l'image sous forme d'un arbre de composants ou d'un arbre max, MTObjects peut traiter les images de manière efficace en exploitant les relations hiérarchiques entre les pixels de l'image. Cette approche permet également de détecter des sources de faible intensité en parcourant l'arbre de haut en bas et en descendant vers les nœuds de faible intensité.

      Utilisation de seuils adaptatifs : la méthode MTObjects utilise des seuils adaptatifs qui tiennent compte des propriétés des objets détectés. Cela permet de détecter des sources de faible intensité de manière plus précise en utilisant une approche plus adaptative que la méthode de seuil fixe utilisée par SExtractor.

      Utilisation d'un processus de découpage quantifié : la méthode MTObjects utilise un processus de découpage quantifié pour séparer les sources imbriquées ou superposées. Cela permet de détecter et de mesurer les propriétés des sources imbriquées de manière plus précise en utilisant une approche basée sur les intensités des pixels.

      En utilisant ces approches, MTObjects peut atteindre ses objectifs de détection et de mesure de sources d'image de manière plus précise et plus efficace que les méthodes existantes, en particulier pour les sources de faible intensité.

- Méthode : comment fonctionne la méthode proposée ?

      L'algorithme mtObjects prend en entrée une image I, une fonction nodeTest, un niveau de significance α, un gain g et un facteur de déplacement λ. Il renvoie un arbre Max-Tree M. Les nœuds de M correspondant aux objets sont marqués. L'algorithme mtObjects est décrit en détail dans l'article.
      Dans un premier temps on éstime la moyenne et la variance de l'arrière plan de l'image. On applique ensuite un seuillage à l'image I, en soustrayant la moyenne de l'arrière plan. On crée ensuite une représentation Max-Tree de l'image. On applique ensuite la fonction SignificantNodes sur l'arbre Max-Tree. On trouve ensuite les objets dans l'arbre Max-Tree. On déplace ensuite les objets vers le haut de l'arbre Max-Tree.

      MTObjects utilise une représentation hiérarchique de l'image appelée arbre de composants ou arbre max pour détecter les sources, en s'appuyant sur des attributs associés à chaque nœud de l'arbre pour le filtrage ou la segmentation de l'image.

      MTObjects utilise une approche basée sur les arbres de composants ou les arbres max pour détecter les sources dans les images en astrophysique. Selon la description que vous avez fournie, cette méthode consiste à représenter l'image sous forme d'un arbre hiérarchique, où chaque nœud de l'arbre représente un groupe de pixels connectés à un niveau donné d'intensité. Ensuite, des attributs sont associés à chaque nœud de l'arbre pour le filtrage ou la segmentation de l'image.

      Pour détecter les sources, MTObjects parcourt l'arbre de haut en bas, en commençant par les nœuds les plus intenses et en descendant vers les nœuds de faible intensité. Les sources sont identifiées en tant que groupes de pixels connectés qui satisfont certaines conditions de seuil. Ensuite, la méthode utilise un processus de découpage quantifié pour séparer les sources imbriquées ou superposées.

      Il semble que cette méthode a été conçue pour améliorer la détection de sources de faible intensité dans les images, en particulier dans les images de galaxies en interaction ou superposées. Elle vise également à améliorer la méthode de seuil fixe utilisée par SExtractor en utilisant une approche plus adaptative qui tient compte des propriétés des objets détectés.

      En utilisant une représentation hiérarchique de l'image appelée arbre de composants ou arbre max, et en associant des attributs à chaque nœud de l'arbre pour le filtrage ou la segmentation de l'image, MTObjects peut détecter les sources d'image de manière plus précise en se basant sur des caractéristiques de l'image telles que l'intensité, la forme et la position des sources. Cette méthode est particulièrement utile pour la détection de sources de faible intensité dans les images, comme celles présentes dans les images de galaxies en interaction ou superposées.

- Méthodologie de validation : quels sont les tests proposés par les auteurs pour valider leurs hypothèses ? pour valider leur méthode ?

      Ils ont réalisé des tests sur différents types d'objets celestes, sur une image d'une simulation de 25 étoiles pour tester la détéction du background et du bruit avec la segmentation de SExtractor, sur des galaxies et autres objets avec des régions extérieures plus pâles et des objets imbriqués, sur une portion d'image représentant la fragmentation d'une fine lamentation faible entre deux galaxies, sur des voies de poussières et des artefacts.


- Résultats : quels sont les résultats obtenus par les auteurs ?

      Les tests précédent révèlent que de manière générale, MTObjects conserve mieux les contours de faible intensité des objets et les objets imbriqués. MTObjects est plus rapide que SExtractor. MTObjects est plus robuste que SExtractor face au bruit et aux artefacts. MTObjects est plus fiable que SExtractor face à la fragmentation d'objets. MTObjects gère mieux que la présence de poussières que SExtractor.

- Opinion personnelle : quelle est votre impression personnel sur l'article ? (intérêt, qualitén d'écriture, des hypothèses, de la méthode, des tests ,des résultats, etc.)

      Au premier abord, la méthode MTObjects est une approche prometteuse pour la détection et la mesure de sources d'image en astrophysique, en particulier pour les sources de faible intensité. Elle utilise une représentation hiérarchique de l'image sous forme d'un arbre de composants ou d'un arbre max, ainsi que des seuils adaptatifs et un processus de découpage quantifié pour améliorer la précision de la détection et de la mesure de sources imbriquées ou superposées.

      Cependant, comme pour toute méthode, il est important de souligner que la méthode MTObjects a ses limites et que son efficacité dépend de la qualité et des caractéristiques de l'image utilisée. Il est donc important de continuer à évaluer et à améliorer cette méthode pour en maximiser l'utilité et la précision.

## 2. Etude de l'implémentation
- la portée des programmes fournis : le code fourni permet-il de reproduire la totalité des experiences présentées dans l'article ? (si non, quels sont les points manquants ?)

      Le code fourni permet de reproduire les expériences présentées dans l'article, cependant les images utilisées ne sont pas fournies. Il est donc nécessaire de les trouver sur internet ou de les générer soi-même.

      Les fichiers nécessaires à l'installation du code sont fournis, mais il est nécessaire de les compiler soi-même en lançant le fichier `recompile.sh` et d'installer les dépendances nécessaires à Python décrites dans le `README.rst`.

- la structure : quelles sont les interfaces fournies ? le code est-il bien structuré ? pensez vous pouvoir le réutiliser dans un autre contexte ?

      Il n'y a pas d'interface graphique. L'utilisation du code se fait donc uniquement en ligne de commande et est donc limitée à des utilisateurs avertis.
      
      Le code est bien structuré, il est facile à comprendre et à modifier, chaque fonction est commentée et expliquée. Plus particulièrement, le code est divisé en plusieurs fichiers, ce qui facilite la compréhension et la modification du code. De plus, il est bien documenté par un README qui contient des exemples d'utilisation.
      
      Nous pensons que le code peut être réutilisé dans un autre contexte, mais il faudrait le modifier pour qu'il puisse être utilisé avec d'autres types d'images que les FITS, en effet la détéction de sources d'image est un problème récurrent dans de nombreux domaines de l'astrophysique, et il est donc possible que ce code puisse être réutilisé dans d'autres domaines.

- la fidélité : le code fourni correspond-il à ce qui est décrit dans l'article ? Si non, quelles sont les différences notables ?

      Le code fournis semble correspondre à ce qui est décrit dans l'article. On parvient à retrouver les différents algorithmes décrits dans l'article dans le code.
      
      Algorithm 1: IsFlat(T,α) dans background.py fonction check_tile_is_flat
      Algorithm 2: SignificantNodes(M,nodeTest,α,g,ˆσ2bg) dans mt_objects.c fonction mt_significant_nodes_up et mt_significant_nodes_down
      Algorithm 3: FindObjects(M) dans mt_objects.c fonction mt_find_objects
      Algorithm 4: MoveUp(M,λ,g,ˆσ2bg) dans mt_objects.c fonction mt_move_up
      Algorithm 5: MTObjects(I,nodeTest,α,g,λ) dans mt_objects.c fonction mt_objects

## 3. Expérimentations
- expériences reproduites : décrivez les expériences que vous avez choisies de reproduire.

      Nous avons reproduit les expériences sur les images de galaxies, de poussières et d'artefacts.

- configuration des tests : précisez les paramètres que vous avez utilisés pour reproduire les expériences. (choix des images, choix des paramètres).

      Nous avons utilisé les images de galaxies, de poussières et d'artefacts. Nous avons utilisé les paramètres par défaut.

- analyse des résultats : analysez les résultats obtenus, sont-ils conformes aux résultats présentés dans l'article ? (comparaison avec les résultats de l'article)

      Les résultats obtenus sont conformes aux résultats présentés dans l'article.

- expériences complémentaires : pouvez-vous proposer des expériences complémentaires pour évaluer la méthode ? (choix des images, choix des paramètres).

      Nous avons mené des expériences complémentaires sur les images de galaxies, de poussières et d'artefacts. Et des images sur internet.