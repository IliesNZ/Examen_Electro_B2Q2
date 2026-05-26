<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>6. Générateur d’échelons (montage 1). {Chapitre 12}</b></h2>

### <em>À quoi sert-il ?</em>

Ce montage sert à obtenir des échelons parfaits (avec des pentes verticales et non plus obliques comme dans le montage précédent). Selon le cours (page globale 172), il est concrètement utilisé pour les oscilloscopes échantillonneurs, pour tracer des réseaux de caractéristiques courant-tension des transistors, ou encore pour échelonner le courant de base ou de grille.

### <em>Dessine le circuit qui réalise cette fonction.</em>

Le schéma complet se trouve à la page globale 171. Il est composé de plusieurs blocs en cascade :

![](../assets/page-171-part-1.png)

1. Un premier amplificateur opérationnel monté en suiveur de tension (adaptateur d'impédance) qui reçoit l'entrée $v_{in}$.

2. Un condensateur $C_1$ en série.

3. Un jeu de deux diodes $D_1$ (reliée à la masse) et $D_2$ (en série vers la suite du circuit).

4. Un second amplificateur opérationnel monté en intégrateur avec un condensateur $C_2$ dans sa boucle de contre-réaction (et un interrupteur de remise à zéro $B$ en parallèle avec $C_2$).

### <em>Dessine les signaux sur un diagramme temporel.</em>

![](../assets/page-171-part-2.png)

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

Vers [Question 7](../question-07/answer.md)
