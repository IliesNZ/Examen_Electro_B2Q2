<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>8. Le différenciateur. {Chapitre 12}</b></h2>

### <em>À quoi sert-il ?</em>

- Un différenciateur est un circuit électronique conçu pour réaliser l'opération mathématique de différentiation.

- Sa tension de sortie est directement proportionnelle à la vitesse instantanée de variation (c'est-à-dire la pente) de la tension appliquée à son entrée.

- Ses applications classiques sont la détection des fronts avant (montants) et arrière (descendants) d'une impulsion rectangulaire en les transformant en pics étroits, ou la production d'un signal de sortie rectangulaire à partir d'un signal d'entrée triangulaire.

### <em>Dessine le circuit de principe qui réalise cette fonction.</em>

### <em>Dessine les signaux sur un diagramme temporel.</em>

### <em>Explique le fonctionnement de ce circuit en revenant, au besoin, sur les rappels de début de chapitre.</em>

- Le rappel théorique (circuit RC de base) : Dans un circuit RC simple, lorsqu'un échelon de tension de valeur $V$ apparaît en entrée, le condensateur est initialement déchargé ($v_C = 0$). Par la loi de Kirchhoff ($v_R = v_{in} - v_C$), toute la tension se retrouve instantanément aux bornes de la résistance, faisant sauter la sortie à la valeur $V$ avant de décroître exponentiellement au fur et à mesure que le condensateur se charge.

- Le fonctionnement avec l'ampli-op : Grâce au concept de masse virtuelle sur l'entrée inverseuse (-), le courant provoqué par le signal d'entrée à travers le condensateur n'a pas d'autre choix que de traverser l'intégralité de la résistance de réaction $R$, générant ainsi la tension de sortie.

- Le courant traversant le condensateur est régi par la relation fondamentale : $i = C \frac{dv}{dt}$. La grandeur $\frac{dv}{dt}$ représente la pente de la tension d'entrée. Comme les fronts d'une onde rectangulaire sont extrêmement raides (pente quasi infinie), ils engendrent un courant subit et très intense pendant un très court instant, ce qui crée ces pics de tension très étroits en sortie.

- Avantage de l'AOP : Contrairement au simple circuit RC, l'ampli-op permet d'obtenir une source de pics à basse impédance, rendant la connexion de charges classiques bien plus facile.

### <em>Dessine le schéma d’amélioration du différenciateur.</em>

### <em>Dessine les signaux sur un diagramme temporel.</em>

### <em>Explique le fonctionnement de ce circuit.

## Pas le 1.5.3.</em>

</div>

<!-- TODO: finish this question -->

Vers [Question 9](../question-09/answer.md)
