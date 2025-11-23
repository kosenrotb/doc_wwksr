# Guide des rôles et événements

Version lisible pour GitHub Pages. Utilisez les sections déroulantes pour afficher/masquer les détails.

## Villageois

<details>
<summary>🏃‍♂️ Fuyard</summary>

- Aucune commande, toujours actif.
- Dès qu'il prend ≥ 0,5 cœur de dégâts, il gagne Vitesse 10 s.
- Marche autant de fois que nécessaire dans la partie.
</details>

<details>
<summary>🎃 Jack O'Lantern</summary>

- Commande : `/ww observer <joueur>` (dès la nuit 2, une nuit sur deux).
- Halo de la cible + message global (loup/neutralité).
- Recharge automatique : une nuit sur deux.
</details>

<details>
<summary>🎯 Chasseur de Têtes</summary>

- Commandes : `/ww hhtraque <joueur>`, `/ww hhbuff`, `/ww hhprotect <joueur>`.
- Marque une cible pour deux nuits (dès la nuit 2).
- Si elle meurt à temps : 1 action bonus à dépenser en buff perso ou protection.
</details>

<details>
<summary>🧪 Sorcière Noire</summary>

- Commande : `/ww potiondeath <joueur>` retire 2,5 cœurs.
- Sauvetage automatique unique d'un joueur mourant.
- Potion de mort utilisable une seule fois.
</details>

<details>
<summary>🪦 Veilleur des Tombes</summary>

- Aucune commande.
- À chaque mort, indique immédiatement la direction du meurtre.
</details>

<details>
<summary>🔔 Fantôme du Clocher</summary>

- Sans armure : invisibilité passive + carillons périodiques.
- Commande mort : `/ww ghosthaunt` (délai configurable).
- Perd l’invisibilité s’il remet une armure.
</details>

<details>
<summary>🧸 Tom Pouce</summary>

- Sous 7 cœurs : perd 3 cœurs max, rapetisse pour la durée configurée.
- Après retour à taille normale : commande `/ww tompouce` avec recharge pour rétrécir à nouveau.
</details>

<details>
<summary>🗡️ Chevalier à l'Épée Rouillée</summary>

- Aucune commande.
- À sa mort : purge tous les effets de son tueur, applique Faiblesse pendant `poison_duration`, restitue ensuite les anciens bonus.
</details>

<details>
<summary>🎁 Père Noël</summary>

- Commande : `/ww perenoel <joueur>` (jour 2 puis 1 fois tous les 2 jours).
- Cible vivante à < 50 blocs, unique par joueur, pas d’auto-cible.
- Cadeau livré début de nuit : pomme d’or, +1 cœur, ou Speed/Force/Résistance 1 min (message à la cible).
</details>

## Rôles neutres / solos

<details>
<summary>🩸 Jack l'Éventreur</summary>

- Commande : `/ww jackbleed <joueur>` (hémorragie).
- Pouvoir récupéré après chaque kill ; après le premier meurtre : Force + Speed la nuit, Weakness le jour.
</details>

<details>
<summary>🪦 Revenant</summary>

- Aucune commande.
- Première mort annulée : résurrection immédiate avec Force + Résistance permanentes.
</details>

<details>
<summary>👻 Banshee</summary>

- Commandes : `/ww scream` (cri + vol) et `/ww bansheewand` (orbe aveuglante).
- Si aucune mort la nuit du cri : pouvoir perdu ; sinon recharge la nuit suivante.
</details>

<details>
<summary>⚖️ L'Opportuniste</summary>

- Commande : `/ww opportunite <solo|lg|village>` (fenêtre de 1 min après la 2ᵉ vraie mort).
- Tant qu’il n’a pas choisi : solo neutre + Résistance I permanente.
- Choix : Solo (Force jour, Résistance nuit) ; Loup (bonus loup, perte de la résistance de base) ; Village (aura obscure, no-fall nocturne).
</details>

## Loups-garous

<details>
<summary>😈 Croque-Mitaine</summary>

- Commande : `/ww terror <joueur>` (et éventuellement talisman clic droit).
- Une fois par nuit sur un non-loup : purge des effets, Lenteur + Faiblesse pendant la durée configurée ; pas deux nuits de suite sur la même cible.
</details>

<details>
<summary>🩸 Ombre Sanglante</summary>

- Commande : `/ww sanglant` (fenêtre 15 s après lever du jour, une seule fois).
- Subit Lenteur + Faiblesse toute la journée, gagne Force + Résistance la nuit suivante.
</details>

<details>
<summary>🎭 Marionnettiste</summary>

- Commande : `/ww control <joueur>` (nombre d’utilisations/nuit configuré).
- Inverse totalement les déplacements d’une cible non-loup pendant quelques secondes.
</details>

## Événements

<details>
<summary>🏅 Pluie d'honneur</summary>

- À intervalles aléatoires, annonce à chaque joueur son honneur actuel dans le chat.
</details>

<details>
<summary>🎄 Papa Noël (event)</summary>

- Tir périodique ; chaque joueur reçoit un cadeau distinct (items, effets, cœurs, restitution de pouvoir) via une loottable pondérée.
</details>

<details>
<summary>🏗️ Structure custom</summary>

- Au lancement de la partie, pose `custom_structure.nbt` au point (0,0) si présent dans `plugins/MoreRoleKSR/structures/`.
</details>
