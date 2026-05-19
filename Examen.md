# Question électronique B2Q2 - DELPLHIN BLEHOUSSI & ILIES NARENZO ZANZAN

<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>1. Oscillateur à pont de Wien {Chapitre 10}</b></h2>

### <em>Tracer le schéma d'un oscillateur à pont de Wien.</em>

Le schéma complet se trouve à la page 3 (numérotée 116) dans la section 10.3.4.

Il est composé d'un amplificateur opérationnel avec deux boucles de réaction :

- Une boucle de réaction positive qui part de la sortie, traverse le circuit d'avance-retard (composé d'un condensateur et d'une résistance en série, et d'un condensateur et d'une résistance en parallèle) et va vers l'entrée non inverseuse.

- Une boucle de réaction négative qui part de la sortie, traverse un diviseur de tension (par exemple, une résistance 2R' et une lampe tungstène R') et va vers l'entrée inverseuse.

### <em>Enoncer le critère de Barkhausen appliqué à ce montage.</em>

Pour qu'il y ait oscillation, le produit des gains doit respecter le critère suivant (expliqué en page 1 et appliqué en page 4) : il faut que le gain de boucle A.B = 1 avec un déphasage nul.

### <em>Explique le principe avance retard de phase et situe la fameuse fréquence de coupure.</em>

Le principe (expliqué pages 2 et 3, section 10.3.3) repose sur le comportement des condensateurs selon la fréquence :

- Aux très basses fréquences : Le condensateur en série se comporte comme un circuit ouvert. Il n'y a pas de signal de sortie et le déphasage est positif (avance de phase).

- Aux très hautes fréquences : Le condensateur en parallèle se comporte comme un court-circuit. Il n'y a pas de signal de sortie et le déphasage est négatif (retard de phase).

- Entre ces deux extrêmes : La tension de sortie passe par un maximum. C'est à ce point précis que le déphasage est nul.La fameuse fréquence de coupure ($f_c$) correspond exactement à cette fréquence de résonance ($f_r$) où le déphasage est nul (démontré page 4, section 10.3.5).

### <em>Quelles sont les formules de la fc, A, et B (pas les démonstrations).</em>

D'après la page 4 (section 10.3.5), les formules à retenir sont :

- Fréquence de coupure ($f_c$) : $f_c = \frac{1}{2\pi RC}$

- Taux de réaction (B) : $B = \frac{1}{3}$ (à la fréquence de coupure)

- Gain de l'amplificateur (A) : Pour respecter $A.B = 1$, il faut que $A = 3$ (ce qui correspond à $A = 1 + \frac{R_2}{R_1}$).

### <em>Explique une des deux stabilisations d'amplitude. Explique avec les gains A et B.</em>

Explication avec la Méthode 1 (Lampe à tungstène) - page 4, section 10.3.6.1 :Pour que l'oscillation démarre, il faut initialement que le gain de boucle $A.B$ soit supérieur à 1.

- Au démarrage : La lampe à incandescence est froide, sa résistance est donc petite. La réaction négative est faible, ce qui rend le gain de l'amplificateur $A > 3$. Par conséquent, $A.B > 1$, et les oscillations apparaissent et croissent.

- Stabilisation : Au fur et à mesure que l'amplitude des oscillations augmente, le courant fait légèrement chauffer la lampe, ce qui fait augmenter sa résistance. Lorsqu'elle atteint la valeur exacte $R'$, le gain de l'amplificateur diminue et se stabilise exactement à $A = 3$. À ce moment-là, $A.B = 3 \times (\frac{1}{3}) = 1$. L'amplitude est stabilisée sans distorsion.

</div>

<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>2. Conversion du sinusoïdal au carré {Chapitre 12}</b></h2>

### <em>Dessine le circuit qui réalise cette fonction.</em>

Le circuit qui réalise cette fonction s'appelle un comparateur (ou détecteur de passage par zéro). Selon la page 148, il s'agit simplement d'un amplificateur opérationnel connecté sans résistance de réaction.

- Pour un comparateur non inversé : L'entrée inverseuse (-) est reliée à la masse (le point de référence à 0V), et le signal d'entrée ($v_{in}$) est appliqué à l'entrée non inverseuse (+).

- Pour un comparateur inversé : L'entrée non inverseuse (+) est reliée à la masse, et le signal d'entrée ($v_{in}$) est appliqué sur l'entrée inverseuse (-).

### <em>Dessine les signaux sur un diagramme temporel.</em>

Les diagrammes temporels se trouvent à la page 149 (figures a et b).

- On y trace l'onde sinusoïdale d'entrée qui ondule autour de l'axe de 0V.

- On y trace superposée l'onde de sortie : c'est un signal rectangulaire franc, qui alterne entre une tension maximale ($+V_{sat}$) et une tension minimale ($-V_{sat}$).

- Le point crucial sur le diagramme est que le basculement vertical du signal de sortie se produit exactement à l'instant où la sinusoïde d'entrée coupe l'axe horizontal (le point zéro). Dans le cas d'un comparateur inversé, l'onde de sortie est déphasée de 180° par rapport à l'entrée.

### <em>Explique le fonctionnement de ce circuit en revenant au besoin sur les rappels de début de chapitre.</em>

- Rappel du principe (page 148) : La méthode repose sur l'absence de boucle de contre-réaction. Cela fait que l'amplificateur fonctionne avec son "gain en tension en boucle ouverte" ($A_{OL}$) qui est immense (ex: 100 000). De ce fait, la moindre différence de tension à l'entrée (aussi petite que 0,14 mV) est amplifiée de manière si importante qu'elle "sature" la sortie.

- Le fonctionnement (pages 148 et 149) : Le seuil de déclenchement est ici fixé à 0V (puisqu'une des pattes est à la masse). Lorsque le signal sinusoïdal est appliqué, la sortie n'a pas d'autre choix que d'être dans un de ses deux états extrêmes :

    - Dès que la sinusoïde passe légèrement au-dessus de 0V, le comparateur part en saturation positive ($+V_{sat}$).
    
    - Dès que la sinusoïde passe légèrement en dessous de 0V, il bascule instantanément en saturation négative ($-V_{sat}$).Puisque le signal d'entrée est périodique et traverse continuellement le zéro, la sortie bascule de bas en haut et de haut en bas à chaque traversée, créant ainsi une onde rectangulaire ou carrée parfaite.

</div>

<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>3. Conversion du triangulaire à l’impulsionnel. {Chapitre 12}</b></h2>

### <em>Dessine le circuit qui réalise cette fonction.</em>

Le montage (illustré à la figure a, page globale 162) est un comparateur configuré en détecteur à seuil variable.

Il se compose d'un amplificateur opérationnel sans boucle de contre-réaction. Le signal triangulaire d'entrée y est appliqué sur l'une des entrées. Sur l'autre entrée, on trouve un diviseur de tension formé par une résistance fixe ($R_1$) et une résistance variable ou potentiomètre ($R_2$), reliées à la tension d'alimentation ($+V_{CC}$ et la masse). Ce pont diviseur sert à créer la tension de référence ajustable.

### <em>Dessine les signaux sur un diagramme temporel.</em>

Les signaux à tracer correspondent aux figures b et c de la page globale 162.

- Sur le graphique du haut (figure c), on trace l'onde triangulaire d'entrée oscillant autour de 0V. On y superpose une ligne horizontale représentant la tension de référence de déclenchement ($v_{ref}$), située dans la partie positive du triangle.

- Sur le graphique du bas (figures b et c), on trace le signal de sortie. Il est à 0V la plupart du temps, mais forme des impulsions rectangulaires (de largeur $W$ et de période $T$) qui passent à l'état haut (ou positif) exactement aux instants où la pointe du signal triangulaire dépasse la ligne de seuil $v_{ref}$.

### <em>Explique le fonctionnement de ce circuit en revenant au besoin sur les rappels de début de chapitre.</em>

Comme expliqué dans les principes fondamentaux des comparateurs à valeur non nulle (page globale 150), en polarisant l'une des entrées avec un diviseur de tension, on déplace le point de déclenchement à une valeur $v_{ref}$ différente de zéro. Le comparateur compare alors en permanence le signal d'entrée à cette limite.

Dans ce montage spécifique (page globale 161) :

1. Le potentiomètre $R_2$ permet de faire varier manuellement le point de déclenchement ($v_{ref}$) de zéro jusqu'à une valeur positive donnée.

2. Chaque fois que la valeur du signal triangulaire franchit ce point de déclenchement en montant, la sortie du comparateur bascule au niveau haut. Elle repasse au niveau bas dès que le triangle redescend sous ce seuil.

3. Étant donné que la tension de référence $v_{ref}$ est ajustable, on peut décider à quelle "hauteur" du triangle le comparateur va déclencher.

4. Si l'on augmente $v_{ref}$ (en le rapprochant de la crête du triangle), le signal d'entrée ne le dépassera que brièvement : l'impulsion de sortie sera très fine. Si on diminue $v_{ref}$ (proche de zéro), l'impulsion sera plus large.

5. Cela permet donc de modifier la largeur de l'impulsion de sortie ($W$) sur une période ($T$). Autrement dit, ce circuit permet de faire varier le coefficient de remplissage (ou rapport cyclique, $D = W/T$) de 0 à 50 %.

</div>

<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>4. Générateur (oscillateur) à relaxation. {Chapitre 12}</b></h2>

### <em>Dessine le circuit qui réalise cette fonction.</em>

Le schéma se trouve à la page globale 164 (figure a). Il s'agit d'un amplificateur opérationnel avec une double boucle :  

- Une boucle de réaction négative composée d'une résistance $R$ et d'un condensateur $C$ relié à la masse.  

- Une boucle de réaction positive composée d'un diviseur de tension ($R_1$ et $R_2$) qui crée un effet d'hystérésis (bascule de Schmitt).  

### <em>Quelle est la forme du signal produit ? Dessine les tensions sur un diagramme temporel.</em>

Le signal produit à la sortie est un signal rectangulaire (avec un coefficient de remplissage de 50%).

Sur le diagramme temporel (page globale 164, figure b):  

- <b>En haut :</b> On trace la tension du condensateur ($v_c$). Elle a la forme de courbes exponentielles de charge et de décharge, qui oscillent strictement entre le point de déclenchement supérieur (PDS, noté $vers +V_{sat}$) et le point de déclenchement inférieur (PDI).  

- <b>En bas :</b> On trace la tension de sortie ($v_{out}$), qui est une onde carrée franche alternant entre $+V_{sat}$ et $-V_{sat}$.  

### <em>Explique le fonctionnement de ce circuit en revenant au besoin sur les rappels de début de chapitre.</em>

Bien qu'il n'y ait pas de signal d'entrée externe, ce circuit oscille de lui-même.  

1. Supposons qu'au départ, la sortie soit à la saturation positive ($+V_{sat}$).  

2. Le condensateur commence à se charger exponentiellement à travers la résistance $R$ en direction de $+V_{sat}$.  

3. Cependant, il n'atteindra jamais cette tension. Dès que la tension du condensateur traverse le PDS (fixé par la boucle de réaction positive), le comparateur bascule brutalement et la sortie passe à $-V_{sat}$.  

4. La sortie étant maintenant négative, le condensateur se décharge et commence à se charger négativement vers $-V_{sat}$.  

5. Dès que sa tension traverse le PDI, la sortie commute à nouveau vers $+V_{sat}$, et le cycle se répète indéfiniment.  

### <em>Donne les formules en relation avec cet oscillateur.</em>

D'après la page globale 164, les formules sont :

<b>Le taux de réaction ($B$) :</b> $B = \frac{R_1}{R_1 + R_2}$   

<b>La période du signal ($T$) :</b> $T = 2RC \ln\left(\frac{1+B}{1-B}\right)$   

### <em>Comment puis-je passer à un signal triangulaire ? Suite du schéma et explications.</em>

Pour obtenir un signal triangulaire, il faut mettre en cascade l'oscillateur à relaxation avec un intégrateur (page globale 164, section 12.4.1.2). Le schéma complet couple donc la sortie du premier AOP (l'oscillateur) à l'entrée du second AOP (l'intégrateur via une résistance $R_4$ et un condensateur $C_2$).  

### <em>Explique le fonctionnement de ce circuit en revenant au besoin sur les rappels de début de chapitre. </em>

Le signal rectangulaire généré par le premier étage (l'oscillateur à relaxation) va servir à commander le second étage (l'intégrateur). Comme le signal d'entrée de l'intégrateur est une alternance de constantes ($+V_{sat}$ et $-V_{sat}$), l'opération mathématique d'intégration va transformer ces paliers constants en rampes linéaires (une pente montante puis une pente descendante). La succession de ces rampes crée à la sortie un signal triangulaire parfait.  

### <em>Donne la formule de la valeur de la tension de sortie.</em>

La valeur crête à crête de ce signal triangulaire de sortie est donnée par la formule (page globale 164) :

$V_{out(pp)} = \frac{T}{2R_4 C_2} V_{sat}$   

</div>

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

<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>6. Générateur d’échelons (montage 1). {Chapitre 12}</b></h2>

### <em>À quoi sert-il ?</em>

Ce montage sert à obtenir des échelons parfaits (avec des pentes verticales et non plus obliques comme dans le montage précédent). Selon le cours (page globale 172), il est concrètement utilisé pour les oscilloscopes échantillonneurs, pour tracer des réseaux de caractéristiques courant-tension des transistors, ou encore pour échelonner le courant de base ou de grille.

### <em>Dessine le circuit qui réalise cette fonction.</em>

Le schéma complet se trouve à la page globale 171. Il est composé de plusieurs blocs en cascade :

1. Un premier amplificateur opérationnel monté en suiveur de tension (adaptateur d'impédance) qui reçoit l'entrée $v_{in}$.

2. Un condensateur $C_1$ en série.

3. Un jeu de deux diodes $D_1$ (reliée à la masse) et $D_2$ (en série vers la suite du circuit).

4. Un second amplificateur opérationnel monté en intégrateur avec un condensateur $C_2$ dans sa boucle de contre-réaction (et un interrupteur de remise à zéro $B$ en parallèle avec $C_2$).

### <em>Dessine les signaux sur un diagramme temporel.</em>

Les 5 chronogrammes sont illustrés à la page globale 171.

- $v_{in}$ : Un train d'impulsions négatives carrées (de hauteur $-v$).

- $v_{out}$ : Le signal de sortie final forme un escalier négatif parfait. Les descentes de l'escalier (de hauteur $v'$) sont extrêmement raides (quasi verticales), et les paliers sont parfaitement plats.(Les graphes intermédiaires $v_1, vc_1, vc_2$ montrent les pics de transfert de charge très brefs à chaque front de l'impulsion).

### <em>Explique le fonctionnement de ce circuit en revenant, au besoin, sur les rappels de début de chapitre.</em>

L'explication détaillée du transfert de charge est donnée à la page globale 172.

<b>Instant $t_0$ (repos) :</b> Les condensateurs $C_1$ et $C_2$ sont déchargés, les diodes $D_1$ et $D_2$ sont bloquées.

<b>Instant $t_1$ (début de l'impulsion négative $-v$) :</b> La diode $D_1$ se met à conduire. Le condensateur $C_1$ se charge alors très rapidement (la constante de temps est très courte car elle n'est limitée que par l'impédance de sortie du premier ampli et la résistance de la diode). La tension aux bornes de $C_1$ ($vc_1$) atteint la valeur $V$.

<b>Fin de l'instant $t_1$ (fin de l'impulsion, remontée à $0V$) :</b> La tension d'entrée repasse à 0. La tension $v_1$ devient alors positive ($+V$). Cela bloque $D_1$ et fait conduire $D_2$.

<b>Transfert de charge :</b> Le condensateur $C_1$ se décharge d'un coup vers la "masse virtuelle" du second ampli-op. Toute la charge stockée dans $C_1$ est instantanément transférée au condensateur $C_2$.

Selon la formule de la charge $Q = C \cdot V$, on a une conservation de la charge : $C_1 \cdot V = C_2 \cdot V'$.

La hauteur d'une marche (l'échelon) de tension est donc déterminée par le rapport des condensateurs : $V' = V \cdot \frac{C_1}{C_2}$.

Comme ce transfert de charge est presque instantané, on obtient les pentes raides désirées à la sortie ($v_{out} = -V'$ à la fin d'un échelon).

</div>

<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>7. Générateur d’échelons à comparateur mémoire (montage 2). {Chapitre 12}</b></h2>

### <em>À quoi sert-il ?</em>

Selon la section 12.5 (page globale 173), un différenciateur sert à réaliser l'opération mathématique de différentiation. Sa tension de sortie est directement proportionnelle à la vitesse instantanée de variation de la tension d'entrée (la pente). Ses applications classiques sont :

- La détection des fronts avant et arrière d'une impulsion rectangulaire (création de pics).

- La production d'une sortie rectangulaire à partir d'une entrée triangulaire.

### <em>Dessine le circuit qui réalise cette fonction.</em>

Le schéma de principe à amplificateur opérationnel se trouve à la page globale 174 (figure a). Il ressemble à un intégrateur, mais les composants sont inversés :

- Le signal d'entrée ($v_{in}$) traverse un condensateur $C$ en série.

- Une résistance $R$ est placée dans la boucle de contre-réaction (entre la sortie et l'entrée inverseuse).

- L'entrée non inverseuse (+) est reliée à la masse.

### <em>Dessine les signaux sur un diagramme temporel.</em>

Les signaux sont illustrés à la page globale 174 (figure b) :

- <b>En haut ($v_{in}$) :</b> On trace une impulsion rectangulaire (un signal qui passe subitement d'un niveau bas à un niveau haut, y reste un moment, puis redescend).

- <b>En bas ($v_{out}$) :</b> La sortie est normalement à 0V. Lors du front montant de l'entrée (quand la tension grimpe brusquement), on observe un pic (pointe) négatif très étroit. Lors du front descendant, on observe un pic positif très étroit.

### <em>Explique le fonctionnement de ce circuit en revenant, au besoin, sur les rappels de début de chapitre.</em>

L'explication est donnée à la section 12.5.2 (page globale 174) :

Grâce à la masse virtuelle, l'entrée inverseuse de l'ampli op est maintenue à 0V. Le signal d'entrée force un courant à travers le condensateur. Ce courant répond à la formule mathématique fondamentale des condensateurs : $i = C \frac{dv}{dt}$ (où $\frac{dv}{dt}$ représente la pente du signal d'entrée).

La masse virtuelle oblige l'intégralité de ce courant à traverser la résistance de réaction $R$, ce qui crée la tension de sortie. Puisque les fronts d'une impulsion rectangulaire sont presque verticaux (pente infiniment grande), ils génèrent un courant bref et très intense, ce qui se traduit en sortie par l'apparition de pics de tension très étroits.

</div>

<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>8. Le différenciateur. {Chapitre 12}</b></h2>

### <em>À quoi sert-il ?</em>



### <em>Dessine le circuit de principe qui réalise cette fonction.</em>



### <em>Dessine les signaux sur un diagramme temporel.</em>



### <em>Explique le fonctionnement de ce circuit en revenant, au besoin, sur les rappels de début de chapitre.</em>



### <em>Dessine le schéma d’amélioration du différenciateur.</em>



### <em>Dessine les signaux sur un diagramme temporel.</em>



### <em>Explique le fonctionnement de ce circuit.
## Pas le 1.5.3.</em>



</div>


<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>9. Modulation AM. {Chapitre 13}</b></h2>

### <em>En quoi consiste la modulation ?</em>

L'émetteur inscrit l'information provenant d'une source sur une porteuse sinusoïdale de fréquence $f_o$ : c'est cela la modulation. Pour inscrire cette information sur la porteuse, on peut faire varier soit son amplitude, soit sa fréquence, soit sa phase en fonction du signal à transmettre.  

### <em>Qu’est-ce que la Am ?</em>

La modulation AM (pour Amplitude Modulation ou modulation d'amplitude) correspond à une modification de l'amplitude de l'onde porteuse par le signal information.

### <em>Qu’est-ce que m(t) ? (pas le développement, seulement sa signification et ces limites)</em>

- Signification : $m(t)$ est l'image du signal à transmettre.  

- Limites : Le signal original est transformé (opération de cadrage) pour que $m(t)$ se retrouve strictement borné entre les valeurs +1 et -1.  

### <em>Dessine un signal modulé en AM.</em>

Tu peux utiliser les schémas de la page globale 180 ou 183 pour ta réponse.

- Sur le diagramme temporel, on dessine une onde porteuse très rapide à l'intérieur d'une "enveloppe".  

- Cette enveloppe externe varie lentement en reproduisant la forme exacte du signal modulant $m(t)$.  

- Selon la page globale 183, l'amplitude globale de cette onde fluctue (par exemple entre $0$ et $2A$ pour la partie supérieure de l'enveloppe).  

### <em>Montre par les calculs, le contenu du spectre AM ?</em>

Voici la démonstration mathématique issue de la page globale 184 :

Si on prend un signal $m(t) = M.\cos(\Omega t)$, Le signal modulé s'écrit : $v(t) = A.\cos(\omega t) + A.M.\cos(\Omega t).\cos(\omega t)$ 

En utilisant la formule trigonométrique : 

$\cos(\alpha + \beta) + \cos(\alpha - \beta) = 2.\cos \alpha.\cos \beta$ 

On développe $v(t)$ pour obtenir le contenu spectral :

$v(t) = A.\cos(\omega t) + \frac{A.M}{2}.\cos(\omega + \Omega)t + \frac{A.M}{2}.\cos(\omega - \Omega)t$ 

(Cela montre bien la présence de la porteuse à la fréquence $\omega$, et de deux bandes latérales aux fréquences $\omega + \Omega$ et $\omega - \Omega$).  

### <em>Quel est le problème de la AM ?</em>

Le problème principal est que les bandes latérales (qui contiennent la véritable information) sont de puissances bien plus faibles que le signal à la fréquence de la porteuse (qui, elle, ne contient pas d'information). En conséquence, il y a un important gaspillage d'énergie dans la transmission.  

</div>

<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>10. Modulation AM sans porteuse. {Chapitre 13}</b></h2>

### <em>En quoi consiste la modulation ?</em>

<b>(Page 179) :</b> C'est le fait d'inscrire une information (issue d'une source) sur une porteuse sinusoïdale de fréquence $f_o$ émise par l'émetteur.

### <em>Qu’est-ce que la Am ?</em>

<b>(Page 180) :</b> C'est un type de modulation qui correspond à une modification de l'amplitude de l'onde porteuse par le signal information.

### <em>Qu’est-ce que m(t) ? (pas le développement, seulement sa signification et ces limites)</em>

<b>(Page 182) :</b> C'est l'image du signal à transmettre. Il a subi un cadrage pour être strictement borné entre les valeurs $+1$ et $-1$.

### <em>Dessine un signal modulé en AM.</em>

Le diagramme temporel à dessiner se trouve à la page globale 187. Il faut tracer trois graphiques superposés :

<b>La porteuse :</b> Une onde sinusoïdale rapide et d'amplitude constante.

<b>Le signal modulant $s(t)$ :</b> Une onde sinusoïdale lente qui tourne (ondule) autour de l'axe des 0V.

<b>La porteuse modulée DSB :</b> Le signal résultant. Contrairement à l'AM classique, l'enveloppe touche le zéro. L'astuce visuelle indispensable à dessiner est le saut de phase : à chaque fois que le signal modulant $s(t)$ traverse la ligne du 0, les "vagues" de la porteuse modulée s'inversent (déphasage de 180°).

### <em>Pourquoi de la AM sans porteuse ?</em>

La réponse est donnée au tout début de la section 13.3.2 (page globale 187) : C'est "pour ne pas perdre de puissance avec la porteuse, pour ne pas dépenser cette puissance". En effet, la porteuse en elle-même ne contient aucune information utile, l'enlever permet de faire des économies d'énergie à l'émission.

### <em>Montre par les calculs, le contenu du spectre AM SANS PORTEUSE ?</em>

La démonstration mathématique (page globale 187) est la suivante :

1. Pour retirer la porteuse, on supprime le "$1+$" de la formule de l'AM classique. L'équation de départ devient donc :

    $v(t) = A \cdot m(t) \cdot \cos(\omega t)$

2. On remplace le signal modulant $m(t)$ par son expression $M \cdot \cos(\Omega t)$ :

    $v(t) = A \cdot M \cdot \cos(\Omega t) \cdot \cos(\omega t)$

3. En appliquant la formule trigonométrique, on obtient le contenu spectral final :

    $v(t) = \frac{A \cdot M}{2}\cos(\omega + \Omega)t + \frac{A \cdot M}{2}\cos(\omega - \Omega)t$

Conclusion : L'équation finale montre qu'il n'y a plus de composante à la fréquence $\omega$ isolée. Il n'y a plus la présence de la porteuse dans le signal, uniquement les deux bandes latérales.

</div>

<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>11. Les Modulation FM et PM. {Chapitre 13}</b></h2>

### <em>En quoi consiste la modulation ?</em>



### <em>Qu’est-ce que la Fm ?</em>



### <em>Qu’est-ce que la PM (expliquer la différence).</em>



### <em>Dessine un signal modulé en FM.</em>



### <em>Comment obtient-on une modulation FM ?</em>



### <em>Quelle est l’allure d’un spectre FM (pas de calculs, expliquer la porteuse et les bandes latérales).</em>
