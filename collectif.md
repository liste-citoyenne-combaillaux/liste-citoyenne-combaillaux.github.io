---
layout: page
title: Qui sommes-nous ?
---

<style>
h3 {
  margin-left: 1.5rem !important;
  padding-left: 1rem;
  border-left: 3px solid #4a9eff;
}

h3 + ul,
h3 + ol,
h3 + p + ul {
  margin-left: 2rem;
}

.info-box {
  background-color: #e3f2fd;
  border: 2px solid #4a9eff;
  border-radius: 8px;
  padding: 1.5rem;
  margin: 2rem 0;
}

.info-box h2 {
  margin-top: 0;
  color: #1976d2;
}


/* Cache les puces noires par défaut pour laisser place aux emojis */
.collectif-page ul {
  list-style-type: none;
}


.collectif-page ul li::before {
  content: "▪";
  color: #28a745; /* green color */
  font-weight: bold;
  margin-right: 0.5em;
}

/* Sublists with green dash */
.collectif-page ul ul li::before {
  content: "-";
  color: #28a745; /* green color */
  font-weight: bold;
  margin-right: 0.5em;
}

.candidates-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); /* 160px → 220px */
  gap: 1.2rem;
  margin-top: 1rem;
}


.candidate-card {
  position: relative;
  border-radius: 10px;
  overflow: hidden;
  background: #fff;
  box-shadow: 0 2px 8px rgba(0,0,0,0.12);
  transition: transform 0.2s, box-shadow 0.2s;
  cursor: default;
}

.candidate-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 6px 18px rgba(0,0,0,0.18);
}


.candidate-card img {
  width: 100%;
  aspect-ratio: 3 / 4; /* carré 1/1 → portrait 3/4, plus naturel pour des visages */
  object-fit: cover;
  object-position: top; /* cadre sur le haut (visage) plutôt que le centre */
  display: block;
}

.candidate-number {
  position: absolute;
  top: 8px;
  left: 8px;
  background: #4a9eff;
  color: #fff;
  font-weight: bold;
  font-size: 0.8rem;
  width: 24px;
  height: 24px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1;
}

.candidate-info {
  padding: 0.6rem 0.7rem;
  display: flex;
  flex-direction: column;
  gap: 0.15rem;
}

.candidate-name {
  font-size: 0.85rem;
  line-height: 1.2;
}

.candidate-role {
  font-size: 0.72rem;
  color: #fff;
  background: #1976d2;
  border-radius: 4px;
  padding: 1px 5px;
  align-self: flex-start;
  font-weight: bold;
}

.candidate-details {
  font-size: 0.72rem;
  color: #555;
}

.candidate-location {
  font-size: 0.68rem;
  color: #4a9eff;
  font-style: italic;
}
</style>


<div class="collectif-page" markdown="1">

## Notre liste électorale

<div class="candidates-grid">
  <div class="candidate-card">
    <div class="candidate-number">1</div>
    <img src="/assets/img/equipe/1.png" alt="Jean-Louis Couture" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Jean-Louis <strong>Couture</strong></span>
      <span class="candidate-role">Tête de liste</span>
      <span class="candidate-details">67 ans · Ingénieur agronome</span>
      <span class="candidate-location">Les Hauts de la Fontaine</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">2</div>
    <img src="/assets/img/equipe/2.png" alt="Véronique Granit" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Véronique <strong>Granit</strong></span>
      <span class="candidate-details">43 ans · Orthophoniste</span>
      <span class="candidate-location">Quartier les Pins d'Alep</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">3</div>
    <img src="/assets/img/equipe/3.png" alt="Petru Valicov" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Petru <strong>Valicov</strong></span>
      <span class="candidate-details">39 ans · Enseignant-chercheur en informatique</span>
      <span class="candidate-location">Les Sajolles</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">4</div>
    <img src="/assets/img/equipe/4.png" alt="Marie-Claude Monleau" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Marie-Claude <strong>Monleau</strong></span>
      <span class="candidate-details">69 ans · Informaticienne et chef d'entreprise retraitée</span>
      <span class="candidate-location">Les Sajolles</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">5</div>
    <img src="/assets/img/equipe/5.png" alt="Daniel Guiral" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Daniel <strong>Guiral</strong></span>
      <span class="candidate-details">74 ans · Directeur de recherche hydrobiologiste retraité (IRD)</span>
      <span class="candidate-location">Quartier du Patus</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">6</div>
    <img src="/assets/img/equipe/6.png" alt="Isabelle Soulairol" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Isabelle <strong>Soulairol</strong></span>
      <span class="candidate-details">63 ans · Responsable projets informatiques retraitée</span>
      <span class="candidate-location">Secteur Drailles</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">7</div>
    <img src="/assets/img/equipe/7.png" alt="Ludwig Forte" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Ludwig <strong>Forte</strong></span>
      <span class="candidate-details">34 ans · Consultant systèmes d'information</span>
      <span class="candidate-location">Secteur Branquedieu</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">8</div>
    <img src="/assets/img/equipe/8.png" alt="Hélène Ilbert" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Hélène <strong>Ilbert</strong></span>
      <span class="candidate-details">72 ans · Chercheuse en économie politique</span>
      <span class="candidate-location">Plaine du Mas de Gentil</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">9</div>
    <img src="/assets/img/equipe/9.png" alt="Olivier Hoibian" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Olivier <strong>Hoibian</strong></span>
      <span class="candidate-details">70 ans · Historien et sociologue retraité</span>
      <span class="candidate-location">Quartier des Sajolles</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">10</div>
    <img src="/assets/img/equipe/10.png" alt="Claire Balavoine" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Claire <strong>Balavoine</strong></span>
      <span class="candidate-details">67 ans · Professeure des écoles retraitée</span>
      <span class="candidate-location">Les Sajolles</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">11</div>
    <img src="/assets/img/equipe/11.png" alt="Christian Combes" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Christian <strong>Combes</strong></span>
      <span class="candidate-details">74 ans · Professeur des écoles retraité</span>
      <span class="candidate-location">Plaine du Mas de Gentil</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">12</div>
    <img src="/assets/img/equipe/12.png" alt="Coraline Alberti" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Coraline <strong>Alberti</strong></span>
      <span class="candidate-details">36 ans · Médecin addictologue</span>
      <span class="candidate-location">Les Sajolles</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">13</div>
    <img src="/assets/img/equipe/13.png" alt="Clément Rodriguez-Soulairol" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Clément <strong>Rodriguez-Soulairol</strong></span>
      <span class="candidate-details">19 ans · Étudiant en droit</span>
      <span class="candidate-location">Secteur Drailles</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">14</div>
    <img src="/assets/img/equipe/14.png" alt="Claudine Ménard" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Claudine <strong>Ménard</strong></span>
      <span class="candidate-details">54 ans · Enseignante-chercheuse en biochimie</span>
      <span class="candidate-location">Les Servants</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">15</div>
    <img src="/assets/img/equipe/15.png" alt="Michel Vanneste" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Michel <strong>Vanneste</strong></span>
      <span class="candidate-details">57 ans · Chirurgien-orthopédiste</span>
      <span class="candidate-location">Les Servants</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">16</div>
    <img src="/assets/img/equipe/16.png" alt="Danièle Guigou" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Danièle <strong>Guigou</strong></span>
      <span class="candidate-details">68 ans · Peintre-sculptrice</span>
      <span class="candidate-location">Les Sajolles</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">17</div>
    <img src="/assets/img/equipe/17.png" alt="Jean-Marie Crapez" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Jean-Marie <strong>Crapez</strong></span>
      <span class="candidate-details">67 ans · Professeur spécialisé déficients auditifs retraité</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">18</div>
    <img src="/assets/img/equipe/18.png" alt="Laurence Tubiana" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Laurence <strong>Tubiana</strong></span>
      <span class="candidate-details">Directrice, Fondation Européenne pour le Climat</span>
      <span class="candidate-location">Plaine du Mas de Gentil</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">19</div>
    <img src="/assets/img/equipe/19.png" alt="François Lerin" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">François <strong>Lerin</strong></span>
      <span class="candidate-details">Chercheur médiateur en agroenvironnement</span>
      <span class="candidate-location">Plaine du Mas de Gentil</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">20</div>
    <img src="/assets/img/equipe/20.png" alt="Léane Freyburger-Giouve" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Léane <strong>Freyburger-Giouve</strong></span>
      <span class="candidate-details">18 ans · Étudiante en droit</span>
      <span class="candidate-location">Les Sajolles</span>
    </div>
  </div>

  <div class="candidate-card">
    <div class="candidate-number">21</div>
    <img src="/assets/img/equipe/21.png" alt="Claude Hammecker" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Claude <strong>Hammecker</strong></span>
      <span class="candidate-details">61 ans · Directeur de recherche science du sol (IRD)</span>
      <span class="candidate-location">Quartier du Patus</span>
    </div>
  </div>
</div>


Une équipe motivée pour proposer un projet municipal **alternatif** à ce qui est en place depuis de nombreuses années sur Combaillaux. **Ce collectif se veut pluriel et dynamique** :

* Femmes et hommes de **différentes générations**
* Habitant **différents lieux dits de Combaillaux** que ce soit dans la plaine, les
versants ou les hauteurs de la commune
* Portés par des **savoir-faire variés** : expériences dans le culturel, le social, l'éducation, l'agriculture, la santé, les sports, la gestion, l'informatique, les sciences ou l'écologie.
* **Déjà investis sur le terrain** : actifs dans les associations, l'animation locale et les échanges de savoir-faire
* Désireux de **construire ensemble** l'avenir de Combaillaux
* Avec **un mode de fonctionnement horizontal** : pas de maire qui décide seul, mais une équipe qui construit et porte les projets collectivement


<div class="info-box" markdown="0">

## Le comité de soutien

* Carine **Biro** - commerçante produits de bien-être/naturopathie
* Claudine **Carillo**, psychologue libérale
* Cégolène **Colonna-Leroul** - 56 ans, consultante formatrice, les Sajolles
* Sébastien **Freyburger** - 48 ans, cadre fonction publique territoriale (Région), les Sajolles
* Ezéchiel **Meireles** - 36 ans, cadre fonction publique (ARS), quartier les Pins d'Alep
* Pierre **Pobeda** - 66 ans, artisan paysagiste JEV retraité, allée des Amandiers
* Jean-Bernard **Rodriguez** - 62 ans, dirigeant SSII retraité, secteur Drailles 
</div>

Contactez-nous dès maintenant (<a href="mailto:contact@combaillaux-autrement.fr">contact@combaillaux-autrement.fr</a>) pour partager vos idées et/ou rejoindre l'aventure.


</div>