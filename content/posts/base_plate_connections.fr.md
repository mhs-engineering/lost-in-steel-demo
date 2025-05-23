---
title: "Ancrages en pleine masse : Un guide conceptuel"
date: 2025-05-18T23:27:03+02:00
draft: false
cover:
  image: img/cover/base_plate_cover.jpg
  thumbnail: img/thumbs/base_plate_thumbnail.jpg
tags: ["acier", "structures", "supports", "platine"]
categories: ["Structures en acier"]
author: ["MHS"]

---

Dans cet article, nous explorons les **notions fondamentales** des liaisons acier-béton, en mettant particulièrement l’accent sur les **pieds de poteaux**. En comprenant la mécanique sous-jacente et les principes de base qui régissent ces connexions, nous pouvons aborder les normes de conception applicables avec plus de clarté et de confiance.

## Les pieds de poteux : Comment fonctionnent-ils?

Au fond, indépendamment des hypothèses que nous choisissons pour modéliser notre structure, l’objectif reste toujours le même : garantir que chaque élément structurel réponde tant aux critères d’aptitude au service qu’aux exigences de sécurité pendant toute sa durée de vie prévue.

>📌 Il ne s’agit pas de rechercher la complexité, mais d’aligner nos hypothèses de conception sur la réalité physique.

Supposons que nous ayons terminé notre analyse structurelle : notre modèle d’analyse par éléments finis (FEA) est finalisé, les vérifications des éléments sont faites, et nous avons sélectionné les sections appropriées pour toutes les poutres et poteaux. Les réactions aux appuis, tant les forces que les moments, ont été extraites. **L’attention se porte** alors **sur** une partie cruciale du système, mais souvent négligée : **les appuis** eux-mêmes.

Nous connaisons désormais la **descente de charges** que chaque appui doit **transmettre à la fondation** ou au mur auquel il est connecté. L’étape suivante consiste à **concevoir** cette **liaison d’interface** de manière cohérente avec les **hypothèses** formulées lors de la modélisation, en particulier les **conditions aux limites** (CL). En général, ces CL se classifient en deux **catégories** :

- **Encastré (fixe)** : Doit empêcher à la fois les translations et les rotations. Les six degrés de liberté (UX, UY, UZ, RX, RY, RZ) sont restreints, permettant un transfert complet des efforts et des moments.

- **Articulé** : Doit permettre, sans entrave importante, les rotations. Blocage des translations (UX, UY, UZ), mais sans transmission des moments.

>💡 Le comportement réel se situe entre ces deux extrêmes Aucun appui n’est jamais parfaitement articulé ni totalement rigide. 

En tant qu’ingénieurs.es, notre rôle est de **concevoir les composants** (platines, chevilles d'ancrage, fondations) afin d’obtenir une **réponse** réaliste **cohérente** avec les **hypothèses de modélisation**, tout en respectant les tolérances de construction, les contraintes économiques et les marges de sécurité requises.

## Les pieds de poteuax : Éléments Constitutifs

>💡 Quelle est la fonction attendue du support ? Doit-il uniquement transmettre des efforts axiaux ?
>Doit-il également résister à des moments fléchissants ? Faut-il ajouter des renforts pour améliorer sa performance ?

Ce sont quelques-unes des **questions clés qu’il convient de se poser** au moment de concevoir un appui acier-béton. Bien que les informations initiales, généralement les réactions d’appui issues de notre modèle d’analyse par éléments finis (FEA), constituent un point de départ, elles ne sont utiles que si nous comprenons comment doit fonctionner le système d’appui et de quoi il est constitué.

Il s’agit de déterminer quels composants sont essentiels pour garantir le comportement structurel recherché, et de concentrer nos efforts sur ceux qui contribuent réellement à la performance globale du système.

>📌 En **ingénierie**, la conception ne se résume pas à des calculs ; c’est un **exercice de jugement**. 

Notre tâche est de **diriger** le **flux des efforts** depuis le **poteau** en acier, à travers les éléments intermédiaires, comme la **platine** d’appui, les **chevilles d’ancrage**, le **mortier** (grout), jusqu’à leur destination finale : la **fondation en béton**.

Avant de passer au dimensionnement proprement dit, il est essentiel d’**identifier** les **éléments constitutifs** qu’un système d’appui acier-béton peut comporter. Ce n’est qu’à partir de là que nous pourrons décider lesquels sont pertinents **pour notre cas particulier**. Ce processus est souvent itératif : de nouvelles exigences peuvent émerger en cours de conception, et c’est tout à fait normal. Le dimensionnement structurel laisse toujours place à des ajustements pour rester en phase avec la physique et les contraintes de mise en œuvre.

La configuration des **pieds de poteau** en acier varient selon les sollicitations structurelles et les préférences de mise en œuvre, mais les **composants suivants** sont souvent présents :

![Fixed Connection.jpg](/img/posts/Fixed_Pinned_Connection.jpg)

- **Profilé** (Column Profile) : **Transmet** les **efforts internes** et/ou les moments à l’appui. La section du profilé est déjà conçue et vérifiée aux étapes précédentes.

- **Platine d’appui** (Base Plate) : Répartit les efforts du poteau sur une surface plus large et les transmet à la fondation.

- **Liaison poteau–platine** : Assure la liaison entre le profilé et la platine, selon la condition aux limites :

    - Pour les appuis encastrés → Cordons de *soudure d’angle* (fillet welds) : Généralement la section est reconstituée.

    - Pour les appuis articulés → *Boulons de fixation* (connection bolt)

- **Mortier** (Grouting) : Garantit la **mise à niveau de la structure**, une répartition homogène des appuis, et **transmet** les **efforts de compression** de la platine vers le béton.

- **Chevilles d'ancrage** (Anchor Bolts) : **Transmettent** les efforts de **traction** et de **cisaillement** à la fondation.

- **Fondation en béton** (Concrete Foundation) : **Reçoit** la **descente de charges** depuis l’ensemble du système d’appui.

- **Raidisseurs (optionnelles)** (Stiffeners) : Utilisés en présence de **fortes réactions en moment**.

- **Bêche d'ancrage (optionnel)** (Shear key) : Aide à résister aux **efforts tranchants élevés** transmis par la platine.

## Comment les systèmes de platines se comportent-ils sous charge ?

Considérons un **pied de poteau encastré**, soumis à des efforts et des moments selon les directions X, Y, Z, comme illustré ci-dessous :
![Fixed Base plate.jpg](/img/posts/Fixed_Base_plate.jpg)

Tout comme le relief d’un paysage façonne l’écoulement de l’eau, la configuration et la raideur d’une structure conditionnent la manière dont les charges sont transférées jusqu’au sol. À l’image de l’eau qui suit le chemin de moindre résistance, **les efforts se propagent par les chemins les plus raides et les plus continus**, que ce soit au sein des éléments structuraux ou à travers les composants de liaison.
>**Rigidité** : **propriété** intrinsèque d'un **matériau**, définie par son module de Young. Un matériau plus rigide résiste davantage à la déformation lorsqu'une force lui est appliquée.

>**Raideur** : **propriété de la structure** ou de l'objet dans son ensemble. Elle dépend à la fois de la rigidité du matériau et de la géométrie de la structure. Une structure peut présenter une raideur supérieure à celle d’un matériau rigide, si sa forme est conçue pour résister efficacement à la déformation. 

>💡 On peut considérer la **raideur** comme le **milieu de propagation des efforts**.

Pour qu’une **platine** fonctionne correctement, elle **doit être suffisamment raide** pour directionner les efforts là où on le souhaite. Les schémas ci-dessous illustrent comment la raideur de la platine influence le transfert des efforts vers le béton et les ancrages pour différents cas de chargement élémentaires.

![PLate Stiffness.jpg](/img/posts/Plate_Stiffness.jpg)
📍 Plus d'information sur la raideur des liaisons ici : [Insert link to blog entry] 

La platine joue le rôle de distributeur d’efforts : elle capte les efforts internes provenant du poteau et les transmet aux ancrages et au béton.

>💡 En résumé, la **platine** d’appui est un **nœud de transfert d’efforts**.

Comprendre la contribution de chaque interface est essentiel pour garantir que le système se comporte comme prévu, notamment en validant les hypothèses faites lors de la modélisation (connexion rigide, semi-rigide ou flexible).

Le tableau ci-dessous résume les interactions entre composants dans une liaison encastrée :

| **Interface** | **Transfert d’efforts** | **Remarques** |
| --- | --- | --- |
| Profilé-Platine | Traction, Compression, Cisaillement, Flexion, Torsion | Soudure d’angle pour liaisons encastrées. |
| Raidisseurs-Platine | Compression, Flexion | Augmente la surface effective de compression et le bras de levier z, améliorant la résistance de la platine. La résistance des raidisseurs n'est pas explicitement vérifiée dans l’EC3. |
| Platine-Béton | Compression, Cisaillement (par friction) | Le frottement est souvent négligé, car aucun glissement n’est supposé après la pose. |
| Platine-Chevilles | Traction, Cisaillement | La torsion est transmise par cisaillement aux chevilles. |
| Chevilles-Béton | Traction, Cisaillement | Par liaison chimique (chevilles chimiques ou tiges scellées) ou mécanique (chevilles à expansion).|
| Bêche-Béton | Cisaillement | La bêche favorise le transfert des efforts tranchants importants vers la fondation. |

Dans une liaison encastrée, l’**interface** principale est celle entre le **profilé** et la **platine**, où sont transférés les **efforts axiaux**, les efforts **tranchants** et les moments **fléchissants**. Cette liaison est en général assurée par des **cordons de soudure d’angle**, qui **garantissent** la continuité du **transfert des efforts et des moments**.

Depuis la platine, les efforts sont redistribués vers trois composants principaux : les chevilles ou tiges d’ancrage, la fondation en béton et éventuellement des raidisseurs qui viennent renforcer la capacité portante. Examinons chaque interface :

- L’interface **Platine–Béton** supporte principalement la compression, via un appui direct sur la fondation (souvent à travers un lit de mortier de nivellement). Bien que le frottement puisse théoriquement contribuer à la résistance au cisaillement, cet effet est généralement négligeable dans les assemblages encastrés et plus significatif dans les appuis simples.

- Si des **raidisseurs** sont présents, ils servent de **redistributeurs locaux des efforts**, notamment en cas de **forts moments fléchissants**. Ils augmentent à la fois la surface portante effective et le bras de levier z (cf. EN 1993 §6.2.8), améliorant ainsi la résistance à la flexion et la portance locale. Leur résistance n’est pas explicitement vérifiée dans les formules de l’EN 1993.

- L’interface **Platine–Chevilles** est cruciale pour le transfert de la **traction**, du **cisaillement**, et parfois de la **torsion**. En effet, dans une liaison encastrée, les chevilles ou tiges d'ancrage sont soumises à des efforts de traction ou de cisaillement selon les combinaisons de charges. La torsion est quant à elle répartie en cisaillement au sein du groupe de chevilles.

- L’interface **Chevilles–Béton** constitue le dernier maillon de la chaîne de transfert. Les efforts de **cisaillement** et de **traction** doivent y être transmis de manière fiable à la fondation.

- L’interface **Bêche–Béton** devient critique lorsque la connexion doit résister à de **grands efforts tranchants**. Dans ces cas, il est souvent difficile, voire impossible, de compter uniquement sur les chevilles, en raison de leur taille ou de leur coût. La bêche constitue alors une solution robuste, conçue pour transférer les efforts tranchants directement à la fondation.

## Modes de ruine principaux

La **résistance** de l’ensemble du système est **déterminée par la plus faible capacité portante parmi les composants individuels**. Chacun de ces éléments doit être vérifié séparément pour déterminer sa résistance propre.

>💡 Une liaison est aussi résistante que son maillon le plus faible.

### Platine

Comme évoqué précédemment, la **platine** d’appui doit présenter une **taille**, une **raideur** et une **résistance suffisantes** pour transmettre les charges appliquées à la fois à la fondation en béton et aux chevilles d’ancrage, sans excéder les capacités des matériaux ni les tolérances géométriques. Deux **modes de ruine principaux** gouvernent généralement son dimensionnement :

1. **Surface d'appui insuffisante** : Si la platine est trop petite, elle ne parvient pas à répartir efficacement les efforts de compression. Cela engendre des **contraintes d’appui excessives** sur le béton, susceptibles de dépasser la résistance admissible en compression définie dans l’EN 1992 et référencée dans l’EN 1993.
2. **Épaisseur insuffisante** : Si la platine est trop fine, elle peut ne pas résister aux moments fléchissants induits par les charges excentrées. Ce phénomène est particulièrement critique dans les liaisons encastrées, où la platine agit comme un encastrement en porte-à-faux (cantilever) entre les semelles du profilé et la surface du béton.

Le **dimensionnement précis** de la **surface de contact** et de l’**épaisseur de platine** est essentiel pour assurer un transfert fiable des efforts, et pour rester en **cohérence** avec les **hypothèses de conditions aux limites** utilisées dans les modèles par éléments finis.

### Chevilles / Tiges d'ancrage et Béton

Les schémas ci-dessous illustrent les modes de ruine les plus fréquents impliquant les chevilles d’ancrage et le béton, dans le cadre des assemblages par platine. Deux types de sollicitations principales doivent être considérées : les efforts de traction et les efforts de cisaillement, chacun affectant différemment les composants en acier et en béton, et devant être vérifié séparément.

![Tensile Failure Modes.jpg](/img/posts/Tensile_Failure_Modes.jpg)

Sous **efforts de traction**, les modes de ruine suivants peuvent se produire :

- **Acier (chevilles)** :

    - **Rupture (acier) cheville** (Steel break) : Se produit lorsque la **section transversale de la cheville** est **insuffisante** pour résister à l’effort appliqué.

    - **Rupture par extraction / glissement** (Pull-out) : Conséquence d'une **contrainte** limitée dans le béton exercée par l’**expansion** de la cheville ou d'une **adhérence inadéquate** dans le cas des chevilles chimiques.

- **Béton** :

    - **Rupture par cône de béton** (Concrete cone) : Mode de ruine dans lequel un cône de béton se détache si la profondeur d’ancrage est trop faible ou si les contraintes de traction dans le béton dépassent sa résistance. Ce mode concerne aussi bien les chevilles chimiques que mécaniques.

    - **Rupture par fendage** (Splitting) : Dans le cas d’ancrages mécaniques, conséquence d’une épaisseur de dalle insuffisante par rapport à la zone d’expansion qui peut engendrer une rupture localisée à proximité de la zone d’expansion de la cheville.

![Shear Failure Modes.jpg](/img/posts/Shear_Failure_Modes.jpg)

Sous **efforts de cisaillement**, le système peut échouer selon les mécanismes suivants :

- **Acier (chevilles)** :

    - - **Cisaillement pur** (Pure Shear) : Résulte d’une **section de cheville insuffisante** pour résister aux efforts de cisaillement.

    - **Flexion avec effet de levier** (Bending) : Dans le cas de **platines** posées **sans mortier** de calage (grouting), les chevilles peuvent se comporter comme des encastrements en porte-à-faux (cantilever), induisant des moments importants et une **possible plastification de l’acier**.

- **Béton** :

    - **Rupture par effet de levier** (Pry-out) : Apparaît en cas de **profondeur d’ancrage est insuffisante**, et qu’un morceau de béton est arraché par effet de levier.

    - **Rupture en bord de dalle** (Edge breakout) : Si les **chevilles** sont trop **proches du bord**, les efforts de cisaillement peuvent provoquer la rupture d’un coin de béton, du fait des effets de bras de levier.

📌 Pour en **savoir plus** sur les **types de chevilles** et les considérations de pose, consultez: [Manuel technique chevillage (Hilti France)](https://www.hilti.fr/medias/sys_master/documents/hd7/h4e/9497622642718/Manuel-technique-chevillage-2019-Fiche-technique-ASSET-DOC-LOC-10501008.pdf)

---

## Résumé

>💡 Que l’on dimensionne sa première platine ou que l’on affine un système d’ancrage complexe, un modèle conceptuel solide demeure notre outil de conception le plus précieux.

Le **dimensionnement des supports** par platine ne se limite pas à insérer des valeurs dans des formules : il s’agit de **comprendre** comment les **efforts** se transmettent à travers les **matériaux**, comment les **composants** interagissent entre eux, et où les **points faibles** peuvent apparaître.

En décomposant le système en ses éléments fondamentaux et en visualisant leur comportement sous différentes sollicitations, on prend des décisions de conception plus éclairées dès le départ.

- **En cas de doute, réaliser un diagramme de corps libre** : Représenter le cheminement des efforts du profilé à la fondation permet de clarifier le rôle de chaque composant.
- **Ne pas sous-estimer le comportement du béton** : Les modes de ruine du béton, cône de béton, effet de levier, rupture en bord de dalle, peuvent être aussi critiques que ceux de l’acier, surtout en cas d’ancrage peu profond ou d’espacement insuffisant.
- **Ne pas s'appuyer aveuglément sur les logiciels** : Des outils comme IDEA StatiCa ou Tekla Tedds sont d’excellents auxiliaires de calcul, mais ils doivent être complétés par un jugement d’ingénieur et une compréhension claire des hypothèses sous-jacentes. En cas d’incertitude, des vérifications manuelles ou des modèles simplifiés sont nécessaires.
- **Respecter les prescriptions normatives d'implantation** : Les distances aux bords, l’espacement des chevilles, les profondeurs d’ancrage et les épaisseurs minimales de platines ne sont pas arbitraires : elles garantissent la sécurité, la durabilité et la conformité réglementaire.

---

## Références

**EN 1993-1-8**:

European Committee for Standardization. (2005). *EN 1993-1-8: Eurocode 3 – Design of steel structures – Part 1-8: Design of joints*. Brussels: CEN.

**EN 1992** (general reference to EN 1992-1-1, most commonly used):

European Committee for Standardization. (2004). *EN 1992-1-1: Eurocode 2 – Design of concrete structures – Part 1-1: General rules and rules for buildings*. Brussels: CEN.

European Organization for Technical Approvals. (2013). ***ETAG 001**: Guideline for European Technical Approval of Metal Anchors for Use in Concrete – Part 1: Anchors in General* (Edition 1997, 1st amended 2006, 2nd amended 2013). EOTA.

Celigüeta, J. T., & Tecnun (Universidad de Navarra). (2022). *Diseño de estructuras de acero. Uniones*. [CC BY-NC-SA 3.0 ES]. [https://creativecommons.org/licenses/by-nc-sa/3.0/es/](https://creativecommons.org/licenses/by-nc-sa/3.0/es/)