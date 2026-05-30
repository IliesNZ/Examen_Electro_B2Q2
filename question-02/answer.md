<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>2. Conversion du sinusoïdal au carré {Chapitre 12}</b></h2>

### <em>Dessine le circuit qui réalise cette fonction.</em>

Le circuit qui réalise cette fonction s'appelle un comparateur (ou détecteur de passage par zéro). Selon la page 148, il s'agit simplement d'un amplificateur opérationnel connecté sans résistance de réaction.

<figure style="width: 50%; margin: 0 auto;">

  ![](../assets/page-148.png)
</figure>

- Pour un comparateur non inversé : L'entrée inverseuse (-) est reliée à la masse (le point de référence à 0V), et le signal d'entrée ($v_{in}$) est appliqué à l'entrée non inverseuse (+).

- Pour un comparateur inversé : L'entrée non inverseuse (+) est reliée à la masse, et le signal d'entrée ($v_{in}$) est appliqué sur l'entrée inverseuse (-).

### <em>Dessine les signaux sur un diagramme temporel.</em>

Les diagrammes temporels se trouvent à la page 149 (figures a et b).

<figure style="width: 50%; margin: 0 auto;">

  ![](../assets/page-149.png)
</figure>

- On y trace l'onde sinusoïdale d'entrée qui ondule autour de l'axe de 0V.

- On y trace superposée l'onde de sortie : c'est un signal rectangulaire franc, qui alterne entre une tension maximale ($+V_{sat}$) et une tension minimale ($-V_{sat}$).

- Le point crucial sur le diagramme est que le basculement vertical du signal de sortie se produit exactement à l'instant où la sinusoïde d'entrée coupe l'axe horizontal (le point zéro). Dans le cas d'un comparateur inversé, l'onde de sortie est déphasée de 180° par rapport à l'entrée.

### <em>Explique le fonctionnement de ce circuit en revenant au besoin sur les rappels de début de chapitre.</em>

- L'immense gain et la saturation (Rappel) : En l'absence de contre-réaction négative, le gain très élevé de l'AOP fait que la tension de sortie ne peut pas rester dans des valeurs intermédiaires. Dès que la tension d'entrée diffère de la tension de référence, la sortie "sature" instantanément aux limites de l'alimentation (+Vsat ou -Vsat). C'est ce phénomène qui explique pourquoi le signal de sortie est parfaitement plat et rectangulaire.

- ​La réaction positive : Contrairement à un simple détecteur de passage par zéro (qui bascule dès que le signal croise 0V en boucle ouverte), ce circuit utilise une réaction positive (la résistance R2 ramène une partie du signal sur l'entrée non inverseuse). Cela crée un effet d'hystérésis, définissant deux seuils distincts de basculement au lieu d'un seul.

- ​Le mécanisme de conversion : La bascule de Schmitt transforme l'onde sinusoïdale en signal carré en exploitant ces deux seuils. Quand la sinusoïde d'entrée monte et dépasse le Point de Déclenchement Supérieur (PDS), l'AOP sature brutalement à -Vsat. Lorsque l'alternance redescend et franchit le Point de Déclenchement Inférieur (PDI), la sortie retourne instantanément saturer à +Vsat.

C'est donc la combinaison du gain infini de l'AOP (qui garantit des états hauts et bas très stricts) et de la réaction positive (qui fixe les seuils PDS et PDI) qui permet cette conversion propre et périodique du sinusoïdal au rectangulaire.

</div>

Vers [Question 3](../question-03/answer.md)
