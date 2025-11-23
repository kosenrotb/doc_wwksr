---
layout: default
title: Guide des rôles et événements
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

<div class="page">
  <div class="hero">
    <h1>MoreRoleKSR · Guide joueur</h1>
    <p>Rôles, commandes et événements de l’addon Werewolf. Cliquez sur une carte pour ouvrir/fermer les détails.</p>
    <div class="grid" aria-label="badges">
      <span class="pill">✔️ Compatibilité Werewolf 1.13.1</span>
      <span class="pill">🧭 Commandes in-game /ww</span>
      <span class="pill">🎲 Événements aléatoires intégrés</span>
    </div>
  </div>

  <h2>Villageois</h2>
  <div class="panel">
    <details>
      <summary>🏃‍♂️ Fuyard <span class="tag">passif</span></summary>
      <ul>
        <li>Aucune commande.</li>
        <li>À chaque coup ≥ 0,5 cœur, gagne Vitesse 10 s (répétable).</li>
      </ul>
    </details>
    <details>
      <summary>🎃 Jack O'Lantern <span class="tag">/ww observer</span></summary>
      <ul>
        <li>Dès la nuit 2, utilisable une nuit sur deux.</li>
        <li>Fait luire la cible et annonce publiquement l’aura (loup/neutralité).</li>
      </ul>
    </details>
    <details>
      <summary>🎯 Chasseur de Têtes <span class="tag">/ww hhtraque</span></summary>
      <ul>
        <li>Marque une cible pour deux nuits (dès la nuit 2).</li>
        <li>Si elle meurt à temps : gagne une action bonus (`/ww hhbuff` ou `/ww hhprotect`).</li>
      </ul>
    </details>
    <details>
      <summary>🧪 Sorcière Noire <span class="tag">/ww potiondeath</span></summary>
      <ul>
        <li>Potion de mort : retire 2,5 cœurs à la cible.</li>
        <li>Dispose d’un unique sauvetage automatique d’un joueur mourant.</li>
      </ul>
    </details>
    <details>
      <summary>🪦 Veilleur des Tombes <span class="tag">passif</span></summary>
      <ul>
        <li>À chaque mort, indique instantanément la direction du meurtre.</li>
      </ul>
    </details>
    <details>
      <summary>🔔 Fantôme du Clocher <span class="tag">/ww ghosthaunt</span></summary>
      <ul>
        <li>Sans armure : invisibilité passive + carillons périodiques.</li>
        <li>Une fois mort : peut hanter via `/ww ghosthaunt` (cooldown). </li>
      </ul>
    </details>
    <details>
      <summary>🧸 Tom Pouce <span class="tag">/ww tompouce</span></summary>
      <ul>
        <li>Sous 7 cœurs : perd 3 cœurs max, rapetisse pour la durée configurée.</li>
        <li>Débloque ensuite la commande pour rétrécir à nouveau (avec recharge).</li>
      </ul>
    </details>
    <details>
      <summary>🗡️ Chevalier à l'Épée Rouillée <span class="tag">passif</span></summary>
      <ul>
        <li>À sa mort : purge les effets de son tueur, applique Faiblesse pendant `poison_duration`.</li>
        <li>Restitue ensuite les anciens bonus de la cible.</li>
      </ul>
    </details>
    <details>
      <summary>🎁 Père Noël <span class="tag">/ww perenoel</span></summary>
      <ul>
        <li>Dès le jour 2, une fois tous les deux jours.</li>
        <li>Cible vivante à &lt; 50 blocs, unique par joueur, pas d’auto-cible.</li>
        <li>Cadeau début de nuit : pomme d’or, +1 cœur, ou Speed/Force/Résistance 1 min (message chat à la cible).</li>
      </ul>
    </details>
  </div>

  <h2>Rôles neutres / solos</h2>
  <div class="panel">
    <details>
      <summary>🩸 Jack l'Éventreur <span class="tag">/ww jackbleed</span></summary>
      <ul>
        <li>Inflige une hémorragie ; pouvoir récupéré après chaque kill.</li>
        <li>Après le premier meurtre : Force + Speed la nuit, Weakness le jour.</li>
      </ul>
    </details>
    <details>
      <summary>🪦 Revenant <span class="tag">passif</span></summary>
      <ul>
        <li>Première mort annulée : résurrection immédiate avec Force + Résistance permanentes.</li>
      </ul>
    </details>
    <details>
      <summary>👻 Banshee <span class="tag">/ww scream /ww bansheewand</span></summary>
      <ul>
        <li>Cri nocturne : Vol + Résistance jusqu’à l’aube.</li>
        <li>Si aucune mort la nuit du cri : pouvoir perdu ; sinon recharge la nuit suivante.</li>
        <li>En vol : bâton qui aveugle une cible en ligne droite (cooldown configurable).</li>
      </ul>
    </details>
    <details>
      <summary>⚖️ L'Opportuniste <span class="tag">/ww opportunite</span></summary>
      <ul>
        <li>Fenêtre de 1 min après la seconde vraie mort pour choisir son camp.</li>
        <li>Tant qu’il n’a pas choisi : solo neutre + Résistance I permanente.</li>
        <li>Choix : Solo (Force jour, Résistance nuit) ; Loup (bonus loup) ; Village (aura obscure, no-fall nocturne).</li>
      </ul>
    </details>
  </div>

  <h2>Loups-garous</h2>
  <div class="panel">
    <details>
      <summary>😈 Croque-Mitaine <span class="tag">/ww terror</span></summary>
      <ul>
        <li>Une fois par nuit sur un non-loup : purge des effets, Lenteur + Faiblesse pendant la durée configurée.</li>
        <li>Pas deux nuits de suite sur la même cible.</li>
      </ul>
    </details>
    <details>
      <summary>🩸 Ombre Sanglante <span class="tag">/ww sanglant</span></summary>
      <ul>
        <li>Fenêtre de 15 s après le lever du jour (une seule utilisation).</li>
        <li>Journée : Lenteur + Faiblesse ; nuit suivante : Force + Résistance.</li>
      </ul>
    </details>
    <details>
      <summary>🎭 Marionnettiste <span class="tag">/ww control</span></summary>
      <ul>
        <li>Inverse totalement les déplacements d’une cible non-loup pendant quelques secondes.</li>
        <li>Nombre d’utilisations par nuit configurable.</li>
      </ul>
    </details>
  </div>

  <h2>Événements</h2>
  <div class="panel">
    <details>
      <summary>🏅 Pluie d'honneur</summary>
      <ul>
        <li>À intervalles aléatoires, annonce à chaque joueur son honneur actuel dans le chat.</li>
      </ul>
    </details>
    <details>
      <summary>🎄 Papa Noël (event)</summary>
      <ul>
        <li>Tir périodique ; chaque joueur reçoit un cadeau distinct via une loottable pondérée (items, effets, cœurs, restitution de pouvoir).</li>
      </ul>
    </details>
    <details>
      <summary>🏗️ Structure custom</summary>
      <ul>
        <li>Au lancement de la partie, pose `custom_structure.nbt` au point (0,0) si présent dans `plugins/MoreRoleKSR/structures/`.</li>
      </ul>
    </details>
  </div>
</div>
