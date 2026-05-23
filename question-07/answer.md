<div style="border:1px solid #444;padding:12px;margin:12px 0;border-radius:6px;">
<h2><b>7. Générateur d’échelons à comparateur mémoire (montage 2). {Chapitre 12}</b></h2>

### <em>À quoi sert-il ?</em>

Selon la section 12.5 (page globale 173), un différenciateur sert à réaliser l'opération mathématique de différentiation. Sa tension de sortie est directement proportionnelle à la vitesse instantanée de variation de la tension d'entrée (la pente). Ses applications classiques sont :

- La détection des fronts avant et arrière d'une impulsion rectangulaire (création de pics).

- La production d'une sortie rectangulaire à partir d'une entrée triangulaire.

### <em>Dessine le circuit qui réalise cette fonction.</em>

Le schéma de principe à amplificateur opérationnel se trouve à la page globale 174 (figure a). Il ressemble à un intégrateur, mais les composants sont inversés :

- Le signal d'entrée ( $v_{in}$ ) traverse un condensateur $C$ en série.

- Une résistance $R$ est placée dans la boucle de contre-réaction (entre la sortie et l'entrée inverseuse).

- L'entrée non inverseuse (+) est reliée à la masse.

### <em>Dessine les signaux sur un diagramme temporel.</em>

Les signaux sont illustrés à la page globale 174 (figure b) :

- <b>En haut ( $v_{in}$ ) :</b> On trace une impulsion rectangulaire (un signal qui passe subitement d'un niveau bas à un niveau haut, y reste un moment, puis redescend).

- <b>En bas ( $v_{out}$ ) :</b> La sortie est normalement à 0V. Lors du front montant de l'entrée (quand la tension grimpe brusquement), on observe un pic (pointe) négatif très étroit. Lors du front descendant, on observe un pic positif très étroit.

### <em>Explique le fonctionnement de ce circuit en revenant, au besoin, sur les rappels de début de chapitre.</em>

L'explication est donnée à la section 12.5.2 (page globale 174) :

Grâce à la masse virtuelle, l'entrée inverseuse de l'ampli op est maintenue à 0V. Le signal d'entrée force un courant à travers le condensateur. Ce courant répond à la formule mathématique fondamentale des condensateurs : $i = C \frac{dv}{dt}$ (où $\frac{dv}{dt}$ représente la pente du signal d'entrée).

La masse virtuelle oblige l'intégralité de ce courant à traverser la résistance de réaction $R$, ce qui crée la tension de sortie. Puisque les fronts d'une impulsion rectangulaire sont presque verticaux (pente infiniment grande), ils génèrent un courant bref et très intense, ce qui se traduit en sortie par l'apparition de pics de tension très étroits.

</div>

<!-- TODO: find images for this question -->

Vers [Question 8](../question-08/answer.md)
