## Introduction

L’objectif de ce travail est d’identifier les solutions envisageables pour mettre en place une récupération d’énergie au sein de notre projet innovant. Dans ce contexte, la problématique centrale est la suivante : quelle quantité d’énergie peut raisonnablement être récupérée sur un robot quadrupède de type SOLO12, et cette énergie est‑elle suffisamment significative pour permettre une économie d’énergie mesurable ?

Afin de répondre à cette question, nous commencerons par présenter la plateforme étudiée (SOLO12 v1.1) ainsi que ses éléments d’alimentation et de gestion d’énergie. Nous analyserons ensuite les différents mécanismes de récupération d’énergie envisageables et nous proposerons une estimation quantitative de l’énergie potentiellement récupérable dans plusieurs scénarios représentatifs.


## Présentation de la plateforme SOLO12

### Versions du robot

Il existe plusieurs versions du robot SOLO12 :

* **Version v1 [1]** : version filaire, utilisant des câbles pour l’alimentation ainsi qu’un câble Ethernet pour la communication.

<div align="center">
  <img src="https://github.com/user-attachments/assets/4f6b29cd-44ef-4dce-b253-45e27c0d25ec" alt="solo12_1" width="400" />
  <p><em>Figure 1: Solo 12 v1 [1]</em></p>
</div>

* **Version v1.1 [2]** : version autonome intégrant des batteries embarquées et un module de communication sans fil.

<div align="center">
  <img src="https://github.com/user-attachments/assets/9748497b-bdaf-49c2-8d02-88c3a711cd9a" alt="solo12_1.1" width="400" />
  <p><em>Figure 2: Solo 12 v1.1 [2]</em></p>
</div>

Dans le cadre de cette étude, nous nous intéressons exclusivement à la version v1.1, plus représentative d’un usage autonome.


### Système d’alimentation


La version SOLO12 v1.1 est équipée de deux batteries LiPo SLS X‑Cube 850 mAh (3S1P, 11,1 V) câblées en série. Ces batteries offrent un bon compromis entre densité énergétique, capacité de décharge et masse embarquée.
<table style="width: 100%; text-align: center;">
  <tr>
    <td>
      <img width="300" alt="image" src="https://github.com/user-attachments/assets/c42f2e39-89f4-45bc-880a-0cada2a469f6" />
      <p><em>Figure 1: Solo 12 v1 [1]</em></p>
    </td>
    <td>
      <img width="500" alt="image" src="https://github.com/user-attachments/assets/c5002ee4-2484-46f4-bdff-d000e6b4fc35" />
      <p><em>Figure 2: Cablage [3]</em></p>
    </td>
  </tr>
</table>

Le robot intègre également une Power Management Board, développée par Thomas Flayols (LAAS‑CNRS). Cette carte assure :

* la sécurité des batteries (arrêt d’urgence, coupure d’alimentation),
* la limitation des appels de courant,
* la mesure en temps réel de la tension batterie et du courant consommé,
* la communication avec la carte maître via une interface SPI.

<div align="center">
  <img width="351" height="233" alt="image" src="https://github.com/user-attachments/assets/5828880d-b50c-47ac-9b9a-6aaced3c23a5" />
  <p><em>Figure 2: PMB [4]</em></p>
</div>

Cette architecture permet un suivi de la consommation énergétique du robot, condition indispensable pour évaluer une éventuelle récupération d’énergie.

## Impact de la masse sur la récupération d’énergie

Un facteur clé dans la mise en œuvre d’une solution de récupération d’énergie est la masse totale du robot. Plus le robot est lourd, plus l’énergie nécessaire pour marcher, sauter, se redresser ou accélérer/décélérer augmente, car chaque patte doit fournir davantage de force et donc de couple.

Le robot SOLO12 v1.0 a une masse d’environ 2,5 kg. La version v1.1 annonce un surpoids d’environ 300 g, principalement dû à l’intégration des batteries et de l’électronique d’autonomie, portant la masse totale à environ 2,8 kg.

Il est donc crucial que toute solution de récupération d’énergie :

* n’ajoute qu’une masse supplémentaire très limitée,
* ne nécessite pas de moteurs plus puissants,
* ne devienne pas contre‑productive en augmentant la consommation globale d’énergie.


## Moyens de récupération d’énergie envisageables

La solution principalement envisagée est la régénération d’énergie par les moteurs, c’est‑à‑dire le fonctionnement des moteurs électriques en mode générateur lorsque le mouvement est imposé au robot.

Ce principe est couramment utilisé dans les véhicules électriques et les trottinettes électriques, notamment lors du freinage ou des descentes. Nous avons d’ailleurs pu expérimenter ce mécanisme lors d’un précédent bureau d’étude (BE trottinette).

Un moteur électrique peut fonctionner en générateur lorsque :

* le robot freine ou décélère,
* il descend une pente,
* il subit un impact ou une contrainte mécanique externe.


## Estimation de l’énergie récupérable

L’énergie récupérable provient de l’énergie mécanique extraite du système :

* **Énergie potentielle de pesanteur** : $$E_p = m g \Delta h$$

* **Énergie cinétique :** $$E_k = \tfrac{1}{2} m v^2$$

### Capacité énergétique de la batterie

Chaque batterie possède une tension nominale de 11,1 V et une capacité de 0,85 Ah, soit :

$$E = 11,1 \times 0,85 \approx 9,44 \, \text{Wh}$$


Les deux batteries étant câblées en série, l’énergie totale disponible est d’environ :

$$E_{tot} \approx 18,9 , \text{Wh} \approx 68,040 , \text{J}$$

## Scénarios de récupération d’énergie

### 1. Chute verticale

Considérons une descente verticale de 1 m pour un robot de masse 2,8 kg :

$$E_p = 2,8 \times 9,81 \times 1 \approx 27,5 , \text{J}$$

Cela représente environ 0,04 % de l’énergie totale de la batterie, dans l’hypothèse irréaliste d’un rendement de 100 %. En pratique, les rendements sont très inférieurs, rendant cette récupération négligeable.

### 2. Freinage depuis la vitesse maximale

Pour un freinage complet depuis une vitesse maximale de 1,5 m/s :

$$E_k = \tfrac{1}{2} \times 2,8 \times 1,5^2 \approx 3,15 , \text{J}$$

Cela correspond à environ 0,005 % de la capacité totale de la batterie (pour un rendement de 1). Un freinage isolé récupère donc une quantité d’énergie très faible. Cependant, en pratique, la locomotion du robot implique de nombreux micro‑freinages, fréquents mais difficiles à quantifier.

### 3. Descente contrôlée sur une pente

Le cas le plus favorable est celui d’une descente contrôlée, où le robot doit freiner en continu.

Pour une pente d’angle ( \theta ), une vitesse de descente ( v ), la puissance théoriquement récupérable est :

$$P \approx m g v \sin(\theta) - P_{pertes}$$

Pour une pente de 10 % et une vitesse de 1 m/s :

$$P \approx 2,8 \times 9,81 \times 1 \times 0,10 \approx 2,75 , \text{W}$$

En tenant compte des pertes, la puissance récupérable est de l’ordre de quelques watts.

Pour une descente de 10 minutes (600 s) avec une puissance moyenne récupérée de 1 W :

$$E \approx 600 , \text{J}$$

Cela représente environ 0,9 % de la capacité totale de la batterie pour un rendement idéal, soit environ 0,4 % avec un rendement réaliste. La récupération d’énergie devient alors légèrement plus intéressante, mais uniquement pour des descentes longues et continues.

### Estimation plus réaliste à partir des mesures embarquées

Pour obtenir une estimation plus pertinente de l’énergie potentiellement récupérable, il serait judicieux d’exploiter directement les mesures de tension et de courant fournies par la power management board. Ces données permettent d’accéder à la puissance instantanée consommée.

Une analyse temporelle des profils de courant et de tension (en particulier lors des phases de décélération, d’impact ou de descente contrôlée) permettrait : d’identifier les périodes où les moteurs fonctionnent en génératrice, et d’estimer l’énergie réellement récupérée par intégration de la puissance négative,

Cette approche offrirait une vision beaucoup plus réaliste que les calculs purement analytiques.


## Autres formes de récupération d’énergie

### Récupération thermique

La récupération d’énergie par gradient de température apparaît peu envisageable dans le cadre du robot SOLO12. Les environnements dans lesquels le robot est susceptible d’être déployé ne présentent généralement pas de gradients thermiques suffisamment élevés et exploitables. De plus, la puissance récupérable par des dispositifs thermoélectriques resterait négligeable face à la consommation des actionneurs.

### Récupération vibratoire (piézoélectrique ou électromagnétique)

De la même manière, les solutions de récupération d’énergie par vibrations, qu’elles soient piézoélectriques ou électromagnétiques, ne semblent pas pertinentes. Les niveaux d’énergie récupérables sont très faibles et largement insuffisants par rapport aux besoins énergétiques du robot. Ces technologies sont davantage adaptées à des capteurs basse consommation qu’à des systèmes de locomotion active.

### Évaluation de la récupération solaire

Le robot SOLO12 est équipé d’actionneurs électriques assurant le mouvement de ses articulations, lesquels consomment une quantité d’énergie significative. Il est indiqué dans la littérature que, pour une vitesse de déplacement de 1,5 m/s (vitesse maximale du robot), la puissance moyenne consommée se situe entre 5,5 W et 17,7 W sur une durée de 5 s, selon le coefficient de pondération de la consommation énergétique utilisé dans la fonction de récompense lors de l’apprentissage de la locomotion.

Les dimensions du robot sont d’environ 42 cm de longueur et 33 cm de largeur. Cependant, l’ensemble de la surface supérieure n’est pas exploitable pour l’intégration de panneaux solaires. On considère uniquement la surface dorsale réellement disponible.

En supposant que seule une zone représentant environ 80 % de la longueur et 33 % de la largeur soit exploitable, la surface disponible est :

<div align="center">
  <img width="689" height="322" alt="image" src="https://github.com/user-attachments/assets/03b31302-88d1-4a2b-9f52-7708004456b0" />
  <p><em>Figure 2: PMB [4]</em></p>
</div>

<div align="center">
  <img width="488" height="334" alt="image" src="https://github.com/user-attachments/assets/d43ba965-63d0-41c4-9bf2-cc80ab5c63f9" />
  <p><em>Figure 2: PMB [4]</em></p>
</div>

$$S = (0,8 	\times 42) \times (0,33 \times 33) = 33,6 \times 11 = 369,6 , {cm}^2 = 0,03696 , {m}^2$$

Après analyse de plusieurs panneaux photovoltaïques monocristallins grand public utilisant des cellules à haut rendement (jusqu’à environ 23 % annoncés), il apparaît que les modules correspondants restent relativement lourds. À titre d’exemple, un panneau de 50 W pèse environ 1,1 kg, soit plus d’un tiers de la masse totale du robot.

Pour un robot léger comme le SOLO12, une telle masse additionnelle est incompatible avec les contraintes mécaniques et énergétiques. Par ailleurs, même dans des conditions d’ensoleillement optimales, la récupération solaire ne permettrait pas de couvrir l’intégralité de la consommation énergétique du robot, mais tout au plus d’en réduire marginalement la demande.

## Conclusion

Cette étude montre que la récupération d’énergie sur un robot quadrupède léger comme le SOLO12 reste globalement limitée. Les scénarios de chute ou de freinage ponctuel apportent une contribution négligeable, tandis que la régénération devient pertinente uniquement lors de descentes prolongées.

Ainsi, la récupération d’énergie ne peut pas être considérée comme une source majeure d’autonomie supplémentaire, mais plutôt comme un complément marginal, potentiellement intéressant dans des contextes d’utilisation spécifiques.

## Source

1. Open Dynamic Robot Initiative, *SOLO12 v1 – Mechanical Design*, GitHub.
2. Open Dynamic Robot Initiative, *SOLO12 v1.1 – Mechanical Design*, GitHub.
3. SLS, *SLS X‑Cube LiPo Battery 850 mAh – Technical Specifications*.
4. Open Dynamic Robot Initiative, *Power Management Board*, GitHub.
