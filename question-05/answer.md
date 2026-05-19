<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>5. Il y a un autre schéma pour obtenir un signal triangulaire.{Chapitre 12}</b></h2>

### <em>Dessine le circuit qui réalise cette fonction.</em>

Le schéma (présent page globale 170) est basé sur un intégrateur de Miller :

- Un amplificateur opérationnel avec son entrée non inverseuse (+) reliée à la masse.

- Une résistance $R$ sur l'entrée inverseuse (-), par laquelle arrive la tension d'entrée $V_{in}$.

- Un condensateur $C$ placé dans la boucle de contre-réaction (entre la sortie et l'entrée inverseuse).

- En parallèle avec ce condensateur $C$, il y a un interrupteur $S$. Cet interrupteur est commandé par un circuit logique composé d'un "Compteur" et d'une porte ET (marquée UI HC110).

### <em>Dessine les signaux sur un diagramme temporel.</em>

Selon le diagramme de la page globale 170 :

<b>Graphe du haut ($V_{in}$) :</b> On y trace un train d'impulsions régulières et négatives (de tension $-V$). Chaque impulsion a une largeur $T_p$ et elles sont séparées par une période $T$. Entre les impulsions, la tension est à 0.

<b>Graphe du bas (Sortie) :</b> Le signal commence à zéro et forme un escalier montant. Chaque marche est créée pendant l'impulsion négative : elle est légèrement oblique (elle monte en diagonale avec une pente). Entre les impulsions (quand l'entrée est à 0), la tension de sortie fait un palier plat. À la fin du cycle (lorsque l'interrupteur se ferme), la tension chute brutalement pour revenir à 0.

### <em>Explique le fonctionnement de ce circuit en revenant, au besoin, sur les rappels de début de chapitre.</em>

<b>Rappel sur l'intégrateur (pages 157-158) :</b> L'intégrateur convertit une tension constante (une impulsion) en une rampe de tension (une croissance linéaire) car le condensateur se charge avec un courant constant. Si l'entrée est à zéro, l'intégrateur garde sa charge en mémoire et maintient sa tension de sortie constante.Fonctionnement du montage (page 170) :

1. À chaque fois qu'une impulsion négative arrive en entrée, l'intégrateur charge le condensateur $C$. Cela crée une rampe positive en sortie : c'est la partie montante (oblique) de la marche. La pente de cette charge est de $V/RC$ et la hauteur de chaque marche est de $V \cdot T_p / RC$.

2. Entre les impulsions, la tension d'entrée est nulle. Le condensateur arrête de se charger et conserve sa tension. La sortie reste constante, formant la partie plate de la marche.

3. Le compteur enregistre le nombre d'impulsions reçues. Au bout d'un nombre prédéfini, la porte ET se déclenche et ferme l'interrupteur $S$.

4. La fermeture de l'interrupteur court-circuite le condensateur, qui se décharge instantanément. La tension de sortie retombe à zéro pour entamer un nouveau cycle.

### <em>Démontre la formule de la fréquence de cet oscillateur. Pas le VCO.</em>

La démonstration est réalisée avec des calculs simplifiés où l'on pose que les résistances de la bascule sont égales : $R_1 = R_2 = R$ (page globale 167 et 168).

<b>Étape 1 : Lien entre les tensions de la bascule</b>

Sur l'entrée non inverseuse de la bascule, la tension $v_2$ est définie par les résistances. La formule du circuit donne l'équation :

$v_2 = \frac{v_1 - v_{out}}{2} + v_{out}$

Ce qui se simplifie pour isoler $v_{out}$ :

$v_{out} = 2v_2 - v_1$

<b>Étape 2 : L'équation de l'intégrateur</b>

Supposons qu'à l'instant $t_0$, le condensateur est déchargé et que la tension de la bascule $v_1$ est à la saturation positive ($+V_{ali}$).

La formule connue pour un intégrateur donne une rampe de la forme :

$v_{out} = \frac{-V_{ali}}{RC}t + k$

Puisque le condensateur est déchargé à $t_0$, la constante $k = 0$.

<b>Étape 3 : Calcul du temps de basculement ($t_1$)</b>

On égalise les deux expressions de $v_{out}$ trouvées aux étapes 1 et 2 :

$2v_2 - V_{ali} = \frac{-V_{ali}}{RC}t$

On isole le temps $t$ :

$t = \left(\frac{2v_2 - V_{ali}}{-V_{ali}}\right)RC$

Le basculement se produit exactement au temps $t_1$, qui correspond au moment où la tension $v_2$ traverse $0V$. En remplaçant $v_2$ par $0$ dans l'équation :

$t_1 = \left(\frac{- V_{ali}}{-V_{ali}}\right)RC$

On obtient : $t_1 = RC$

<b>Étape 4 : Déduction de la fréquence</b>

D'après l'observation géométrique du diagramme temporel (page globale 168), le temps $t_1$ correspond exactement à un quart du cycle total.

La période totale $T_0$ est donc de 4 fois ce temps :

$T_0 = 4RC$

La fréquence étant l'inverse de la période ($f = \frac{1}{T_0}$), on obtient la formule finale :

$f = \frac{1}{4RC}$

</div>

<!-- TODO: find images for this question -->

Vers [Question 6](../question-06/answer.md)
