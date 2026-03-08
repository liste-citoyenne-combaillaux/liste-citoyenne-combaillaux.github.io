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

.collectif-page ul {
  list-style-type: none;
}

.collectif-page ul li::before {
  content: "▪";
  color: #28a745;
  font-weight: bold;
  margin-right: 0.5em;
}

.collectif-page ul ul li::before {
  content: "-";
  color: #28a745;
  font-weight: bold;
  margin-right: 0.5em;
}

.candidates-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
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
  cursor: pointer;
}

.candidate-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 6px 18px rgba(0,0,0,0.18);
}

.candidate-card.active {
  box-shadow: 0 0 0 3px #4a9eff, 0 6px 18px rgba(0,0,0,0.18);
  transform: translateY(-4px);
}

.candidate-card img {
  width: 100%;
  aspect-ratio: 3 / 4;
  object-fit: cover;
  object-position: top;
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

/* Bio panel */
#bio-panel {
  display: none;
  background: #f0f7ff;
  border: 2px solid #4a9eff;
  border-radius: 10px;
  padding: 1.5rem 2rem;
  margin-top: 1.2rem;
  position: relative;
  animation: fadeIn 0.25s ease;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-8px); }
  to   { opacity: 1; transform: translateY(0); }
}

#bio-panel .bio-header {
  display: flex;
  align-items: center;
  gap: 1.2rem;
  margin-bottom: 1rem;
}

#bio-panel .bio-photo {
  width: 90px;
  height: 120px;
  object-fit: cover;
  object-position: top;
  border-radius: 8px;
  flex-shrink: 0;
  box-shadow: 0 2px 8px rgba(0,0,0,0.15);
}

#bio-panel .bio-title h3 {
  margin: 0 0 0.25rem 0 !important;
  padding-left: 0;
  border-left: none;
  font-size: 1.1rem;
  color: #1976d2;
}

#bio-panel .bio-title .bio-meta {
  font-size: 0.8rem;
  color: #555;
}

#bio-panel .bio-title .bio-location {
  font-size: 0.78rem;
  color: #4a9eff;
  font-style: italic;
}

#bio-panel .bio-text {
  font-size: 0.9rem;
  line-height: 1.65;
  color: #333;
  white-space: pre-line;
}

#bio-panel .bio-close {
  position: absolute;
  top: 0.7rem;
  right: 0.9rem;
  background: none;
  border: none;
  font-size: 1.3rem;
  cursor: pointer;
  color: #888;
  line-height: 1;
}

#bio-panel .bio-close:hover {
  color: #333;
}
</style>


<div class="collectif-page" markdown="1">

## Notre liste électorale

<div class="candidates-grid" id="candidates-grid">

  <div class="candidate-card" data-id="1" onclick="showBio(1)">
    <div class="candidate-number">1</div>
    <img src="/assets/img/equipe/1.png" alt="Jean-Louis Couture" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Jean-Louis <strong>Couture</strong></span>
      <span class="candidate-role">Tête de liste</span>
      <span class="candidate-details">67 ans · Ingénieur agronome</span>
      <span class="candidate-location">Les Hauts de la Fontaine</span>
    </div>
  </div>

  <div class="candidate-card" data-id="2" onclick="showBio(2)">
    <div class="candidate-number">2</div>
    <img src="/assets/img/equipe/2.png" alt="Véronique Granit" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Véronique <strong>Granit</strong></span>
      <span class="candidate-details">43 ans · Orthophoniste</span>
      <span class="candidate-location">Quartier les Pins d'Alep</span>
    </div>
  </div>

  <div class="candidate-card" data-id="3" onclick="showBio(3)">
    <div class="candidate-number">3</div>
    <img src="/assets/img/equipe/3.png" alt="Petru Valicov" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Petru <strong>Valicov</strong></span>
      <span class="candidate-details">39 ans · Enseignant-chercheur en informatique</span>
      <span class="candidate-location">Les Sajolles</span>
    </div>
  </div>

  <div class="candidate-card" data-id="4" onclick="showBio(4)">
    <div class="candidate-number">4</div>
    <img src="/assets/img/equipe/4.png" alt="Marie-Claude Monleau" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Marie-Claude <strong>Monleau</strong></span>
      <span class="candidate-details">69 ans · Informaticienne et chef d'entreprise retraitée</span>
      <span class="candidate-location">Les Sajolles</span>
    </div>
  </div>

  <div class="candidate-card" data-id="5" onclick="showBio(5)">
    <div class="candidate-number">5</div>
    <img src="/assets/img/equipe/5.png" alt="Daniel Guiral" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Daniel <strong>Guiral</strong></span>
      <span class="candidate-details">74 ans · Directeur de recherche hydrobiologiste retraité (IRD)</span>
      <span class="candidate-location">Quartier du Patus</span>
    </div>
  </div>

  <div class="candidate-card" data-id="6" onclick="showBio(6)">
    <div class="candidate-number">6</div>
    <img src="/assets/img/equipe/6.png" alt="Isabelle Soulairol" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Isabelle <strong>Soulairol</strong></span>
      <span class="candidate-details">63 ans · Responsable projets informatiques retraitée</span>
      <span class="candidate-location">Secteur Drailles</span>
    </div>
  </div>

  <div class="candidate-card" data-id="7" onclick="showBio(7)">
    <div class="candidate-number">7</div>
    <img src="/assets/img/equipe/7.png" alt="Ludwig Forte" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Ludwig <strong>Forte</strong></span>
      <span class="candidate-details">34 ans · Consultant systèmes d'information</span>
      <span class="candidate-location">Secteur Branquedieu</span>
    </div>
  </div>

  <div class="candidate-card" data-id="8" onclick="showBio(8)">
    <div class="candidate-number">8</div>
    <img src="/assets/img/equipe/8.png" alt="Hélène Ilbert" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Hélène <strong>Ilbert</strong></span>
      <span class="candidate-details">72 ans · Chercheuse en économie politique</span>
      <span class="candidate-location">Plaine du Mas de Gentil</span>
    </div>
  </div>

  <div class="candidate-card" data-id="9" onclick="showBio(9)">
    <div class="candidate-number">9</div>
    <img src="/assets/img/equipe/9.png" alt="Olivier Hoibian" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Olivier <strong>Hoibian</strong></span>
      <span class="candidate-details">70 ans · Historien et sociologue retraité</span>
      <span class="candidate-location">Quartier des Sajolles</span>
    </div>
  </div>

  <div class="candidate-card" data-id="10" onclick="showBio(10)">
    <div class="candidate-number">10</div>
    <img src="/assets/img/equipe/10.png" alt="Claire Balavoine" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Claire <strong>Balavoine</strong></span>
      <span class="candidate-details">67 ans · Professeure des écoles retraitée</span>
      <span class="candidate-location">Les Sajolles</span>
    </div>
  </div>

  <div class="candidate-card" data-id="11" onclick="showBio(11)">
    <div class="candidate-number">11</div>
    <img src="/assets/img/equipe/11.png" alt="Christian Combes" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Christian <strong>Combes</strong></span>
      <span class="candidate-details">74 ans · Professeur des écoles retraité</span>
      <span class="candidate-location">Plaine du Mas de Gentil</span>
    </div>
  </div>

  <div class="candidate-card" data-id="12" onclick="showBio(12)">
    <div class="candidate-number">12</div>
    <img src="/assets/img/equipe/12.png" alt="Coraline Alberti" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Coraline <strong>Alberti</strong></span>
      <span class="candidate-details">36 ans · Médecin addictologue</span>
      <span class="candidate-location">Les Sajolles</span>
    </div>
  </div>

  <div class="candidate-card" data-id="13" onclick="showBio(13)">
    <div class="candidate-number">13</div>
    <img src="/assets/img/equipe/13.png" alt="Clément Rodriguez-Soulairol" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Clément <strong>Rodriguez-Soulairol</strong></span>
      <span class="candidate-details">19 ans · Étudiant en droit</span>
      <span class="candidate-location">Secteur Drailles</span>
    </div>
  </div>

  <div class="candidate-card" data-id="14" onclick="showBio(14)">
    <div class="candidate-number">14</div>
    <img src="/assets/img/equipe/14.png" alt="Claudine Ménard" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Claudine <strong>Ménard</strong></span>
      <span class="candidate-details">54 ans · Enseignante-chercheuse en biochimie</span>
      <span class="candidate-location">Les Servants</span>
    </div>
  </div>

  <div class="candidate-card" data-id="15" onclick="showBio(15)">
    <div class="candidate-number">15</div>
    <img src="/assets/img/equipe/15.png" alt="Michel Vanneste" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Michel <strong>Vanneste</strong></span>
      <span class="candidate-details">57 ans · Chirurgien-orthopédiste</span>
      <span class="candidate-location">Les Servants</span>
    </div>
  </div>

  <div class="candidate-card" data-id="16" onclick="showBio(16)">
    <div class="candidate-number">16</div>
    <img src="/assets/img/equipe/16.png" alt="Danièle Guigou" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Danièle <strong>Guigou</strong></span>
      <span class="candidate-details">68 ans · Peintre-sculptrice</span>
      <span class="candidate-location">Les Sajolles</span>
    </div>
  </div>

  <div class="candidate-card" data-id="17" onclick="showBio(17)">
    <div class="candidate-number">17</div>
    <img src="/assets/img/equipe/17.png" alt="Jean-Marie Crapez" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Jean-Marie <strong>Crapez</strong></span>
      <span class="candidate-details">67 ans · Professeur spécialisé déficients auditifs retraité</span>
      <span class="candidate-location">Secteur Route de Grabels</span>
    </div>
  </div>

  <div class="candidate-card" data-id="18" onclick="showBio(18)">
    <div class="candidate-number">18</div>
    <img src="/assets/img/equipe/18.png" alt="Laurence Tubiana" loading="lazy" style="object-fit: contain; background: #f0f0f0;">
    <div class="candidate-info">
      <span class="candidate-name">Laurence <strong>Tubiana</strong></span>
      <span class="candidate-details">Directrice, Fondation Européenne pour le Climat</span>
      <span class="candidate-location">Plaine du Mas de Gentil</span>
    </div>
  </div>

  <div class="candidate-card" data-id="19" onclick="showBio(19)">
    <div class="candidate-number">19</div>
    <img src="/assets/img/equipe/19.png" alt="François Lerin" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">François <strong>Lerin</strong></span>
      <span class="candidate-details">Chercheur médiateur en agroenvironnement</span>
      <span class="candidate-location">Plaine du Mas de Gentil</span>
    </div>
  </div>

  <div class="candidate-card" data-id="20" onclick="showBio(20)">
    <div class="candidate-number">20</div>
    <img src="/assets/img/equipe/20.png" alt="Léane Freyburger-Giouve" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Léane <strong>Freyburger-Giouve</strong></span>
      <span class="candidate-details">18 ans · Étudiante en droit</span>
      <span class="candidate-location">Les Sajolles</span>
    </div>
  </div>

  <div class="candidate-card" data-id="21" onclick="showBio(21)">
    <div class="candidate-number">21</div>
    <img src="/assets/img/equipe/21.png" alt="Claude Hammecker" loading="lazy">
    <div class="candidate-info">
      <span class="candidate-name">Claude <strong>Hammecker</strong></span>
      <span class="candidate-details">61 ans · Directeur de recherche science du sol (IRD)</span>
      <span class="candidate-location">Quartier du Patus</span>
    </div>
  </div>

</div>

<div id="bio-panel">
  <button class="bio-close" onclick="closeBio()" title="Fermer">✕</button>
  <div class="bio-header">
    <img class="bio-photo" id="bio-photo" src="" alt="">
    <div class="bio-title">
      <h3 id="bio-name"></h3>
      <div class="bio-meta" id="bio-meta"></div>
      <div class="bio-location" id="bio-location"></div>
    </div>
  </div>
  <div class="bio-text" id="bio-text"></div>
</div>

Une équipe motivée pour proposer un projet municipal **alternatif** à ce qui est en place depuis de nombreuses années sur Combaillaux. **Ce collectif se veut pluriel et dynamique** :

* Femmes et hommes de **différentes générations**
* Habitant **différents lieux dits de Combaillaux** que ce soit dans la plaine, les
versants ou les hauteurs de la commune
* Portés par des **savoir-faire variés** : expériences dans le culturel, le social, l'éducation, l'agriculture, la santé, les sports, la gestion, l'informatique, les sciences ou l'écologie.
* **Déjà investis sur le terrain** : actifs dans les associations, l'animation locale et les échanges de savoir-faire
* Désireux de **construire ensemble** l'avenir de Combaillaux
* Avec **un mode de fonctionnement horizontal** : pas de maire qui décide seul, mais une équipe qui construit et porte les projets collectivement



## Le comité de soutien

* Carine **Biro** - commerçante produits de bien-être/naturopathie
* Claudine **Carillo**, psychologue libérale
* Cégolène **Colonna-Leroul** - 56 ans, consultante formatrice, les Sajolles
* Sébastien **Freyburger** - 48 ans, cadre fonction publique territoriale (Région), les Sajolles
* Ezéchiel **Meireles** - 36 ans, cadre fonction publique (ARS), quartier les Pins d'Alep
* Pierre **Pobeda** - 66 ans, artisan paysagiste JEV retraité, allée des Amandiers
* Jean-Bernard **Rodriguez** - 62 ans, dirigeant SSII retraité, secteur Drailles 

Contactez-nous dès maintenant (<a href="mailto:contact@combaillaux-autrement.fr">contact@combaillaux-autrement.fr</a>) pour partager vos idées et/ou rejoindre l'aventure.

</div>
</div>

<script>
var bios = {
  1: {
    name: "Jean-Louis Couture",
    meta: "67 ans · Ingénieur agronome · Tête de liste",
    location: "Les Hauts de la Fontaine",
    photo: "/assets/img/equipe/1.png",
    text: "Installé à Combaillaux depuis 2016, je viens d'une famille d'ouvriers-paysans, ce qui a déterminé mon parcours d'ingénieur agronome. J'ai surtout travaillé dans le domaine du développement rural, du foncier et de la gestion de l'eau essentiellement avec des organisations paysannes, des organismes agricoles, des ONG, des bailleurs de fonds ou même aux Nations Unies.\n\nFort de toute cette expérience je souhaite apporter ma contribution à notre commune en participant à des propositions d'orientations novatrices fondées sur l'intérêt général qui représente bien plus que la simple somme des intérêts particuliers.\n\nPenser global et agir local fondent mes engagements. Pour moi, il n'y a pas de gestion durable et socialement équitable sans institutions fondées et animées par les principes de la gestion démocratique et éthique du bien commun."
  },
  2: {
    name: "Véronique Granit",
    meta: "43 ans · Orthophoniste",
    location: "Quartier les Pins d'Alep",
    photo: "/assets/img/equipe/2.png",
    text: "Je suis orthophoniste auprès d'enfants et d'adultes avec autisme depuis 17 ans et formatrice dans le même domaine.\n\nLa communication, sous toutes ses formes, est au cœur de mon quotidien que ce soit pour permettre à certains de pouvoir s'exprimer ou pour transmettre des connaissances à d'autres.\n\nIntégrer la liste de Combaillaux Autrement est pour moi l'occasion de développer une autre forme de communication à travers une réflexion sur des projets qui rassemblent pour plus de partage, d'échanges et d'inclusion."
  },
  3: {
    name: "Petru Valicov",
    meta: "39 ans · Enseignant-chercheur en informatique",
    location: "Les Sajolles",
    photo: "/assets/img/equipe/3.png",
    text: "Convaincu que la démocratie locale se nourrit d'information claire et accessible, je vais œuvrer pour plus de transparence dans les décisions municipales et pour moderniser nos outils numériques — à commencer par un site web digne de ce nom et un vrai portail citoyen numérique.\n\nDans la vie, j'aime optimiser : mes algorithmes, mes dépenses, mes itinéraires à vélo, mon jardin. C'est cette même logique que j'aimerais apporter à la commune : mieux utiliser les ressources, réduire les gaspillages financiers et énergétiques.\n\nRejoindre cette liste, c'est pour moi l'occasion de mettre mon expertise au service du collectif, avec rigueur et engagement."
  },
  4: {
    name: "Marie-Claude Monleau",
    meta: "69 ans · Informaticienne et chef d'entreprise retraitée",
    location: "Les Sajolles",
    photo: "/assets/img/equipe/4.png",
    text: "Arrivée à Combaillaux il y a 31 ans, j'ai vu au fil du temps notre village perdre son identité rurale face à l'urbanisation de la métropole.\n\nDepuis 6 ans mobilisée pour la défense de notre commune, de son environnement et de ses habitants, rejoindre Combaillaux Autrement est la suite logique de mon engagement associatif. Les valeurs portées par ce collectif, concertation et écoute, souci du bien vivre pour toutes les générations, mais aussi transparence et rigueur dans la gestion, sont les moteurs de ma motivation à participer à une démarche originale pour vivre à Combaillaux, autrement."
  },
  5: {
    name: "Daniel Guiral",
    meta: "74 ans · Directeur de recherche hydrobiologiste retraité (IRD)",
    location: "Quartier du Patus",
    photo: "/assets/img/equipe/5.png",
    text: "Installé à Combaillaux depuis plus de 30 ans, ancien directeur de recherche en écologie et microbiologie environnementale, j'ai été adjoint au maire de Combaillaux en charge de l'environnement, puis président de l'Association Départementale des Anciens Maires et Adjoints de l'Hérault (ADAMA 34).\n\nAujourd'hui retraité, je reste très impliqué dans la vie associative aux échelles locale, régionale — en tant que représentant des associations environnementales (FNE, WWF, LPO et Surfrider) d'Occitanie, PACA et Corse — et nationale, pour la préservation de la qualité des eaux et de la biodiversité des écosystèmes aquatiques et marins.\n\nNotre commune est aujourd'hui confrontée à des enjeux majeurs qui nécessitent des décisions claires et des actions ambitieuses. Au sein de Combaillaux Autrement, je souhaite mettre mon expérience et mes compétences au service de notre village afin que Combaillaux conserve son attractivité, fidèle à son histoire, ainsi qu'à sa richesse et diversité paysagère.\n\n« Hâte-toi de transmettre ta part de merveilleux, de rébellion, de bienveillance » — René Char"
  },
  6: {
    name: "Isabelle Soulairol",
    meta: "63 ans · Responsable projets informatiques retraitée",
    location: "Secteur Drailles",
    photo: "/assets/img/equipe/6.png",
    text: "Manager Informatique retraitée, ancienne conseillère municipale, je suis impliquée depuis longtemps dans le monde associatif dans les domaines de la culture, du sport, de l'éducation, de la nature et du développement durable.\n\nUne nouvelle fois, je me mets au service de ma commune, dans un contexte qui oblige à la rigueur et aussi à la créativité et parce que je crois profondément en la force du collectif."
  },
  7: {
    name: "Ludwig Forte",
    meta: "34 ans · Consultant systèmes d'information",
    location: "Secteur Branquedieu",
    photo: "/assets/img/equipe/7.png",
    text: "Consultant en conduite du changement et systèmes d'information, jeune papa amoureux de la nature, j'ai trouvé mon équilibre personnel entre le temps que je consacre à mon entourage et au sens que je donne à mes missions pour la protection de l'enfance auprès des collectivités publiques.\n\nOriginaire de Montpellier et depuis plus de 18 ans pensionnaire intermittent de Combaillaux, j'ai toujours rêvé d'y construire ma vie de famille. Maintenant habitant du village, j'ai décidé de m'investir pour le futur de ma commune qui représente pour moi un cadre de vie exceptionnel !"
  },
  8: {
    name: "Hélène Ilbert",
    meta: "72 ans · Chercheuse en économie politique",
    location: "Plaine du Mas de Gentil",
    photo: "/assets/img/equipe/8.png",
    text: "Chercheuse en économie politique internationale, je travaille aujourd'hui sur les pratiques des paysans herboristes et des cueilleurs. J'habite à Combaillaux depuis 1991 et j'ai été conseillère municipale, élue d'opposition après 2014.\n\nAujourd'hui, les valeurs de solidarité, équité et transparence qui animent l'équipe de « Combaillaux Autrement » me motivent pour participer à nouveau à la vie de la commune. Sensible aux transformations rapides de notre territoire coupé par de nombreux axes routiers et des aménagements consécutifs qui ferment les chances de continuité biologique et bloquent les cheminements et les rencontres, je me bats avec eux, avec vous pour tisser des liens et agir."
  },
  9: {
    name: "Olivier Hoibian",
    meta: "70 ans · Historien et sociologue retraité",
    location: "Quartier des Sajolles",
    photo: "/assets/img/equipe/9.png",
    text: "Avec mon épouse, je réside à Combaillaux depuis 24 ans. Historien et sociologue émérite, je conserve des liens avec la recherche universitaire. Ancien conseiller municipal, j'ai présidé pendant plus de 10 ans l'association « Ensemble à Combaillaux » qui a informé régulièrement la population du village sur les mesures nécessaires pour préserver notre cadre de vie.\n\nLa dynamique au sein de la liste Combaillaux Autrement m'a convaincu de la possibilité de rendre la gestion de la commune plus transparente et démocratique en associant davantage les habitants. Je suis donc très heureux de pouvoir mettre mes compétences et mon expérience au service de l'intérêt général pour la réalisation de notre programme."
  },
  10: {
    name: "Claire Balavoine",
    meta: "67 ans · Professeure des écoles retraitée",
    location: "Les Sajolles",
    photo: "/assets/img/equipe/10.png",
    text: "Institutrice à la retraite, installée à Combaillaux il y a un peu plus de 30 ans, tombée sous le charme de ce village tranquille riche en histoire niché entre les vignes et la garrigue.\n\nL'envie d'être utile, de travailler avec une équipe motivée et solidaire à l'amélioration de notre environnement et à la qualité de vie pour tous sont mes principales raisons de m'investir ces prochaines années pour notre village."
  },
  11: {
    name: "Christian Combes",
    meta: "74 ans · Professeur des écoles retraité",
    location: "Plaine du Mas de Gentil",
    photo: "/assets/img/equipe/11.png",
    text: "Après plus de quarante années au service de l'Éducation nationale, où j'ai exercé des fonctions d'enseignant, de conseiller d'orientation, de directeur de CIO et de chef d'établissement, je suis aujourd'hui retraité et souhaite mettre mon expérience au service de notre commune.\n\nParallèlement à mon activité professionnelle, j'ai conduit pendant une dizaine d'années une activité de maraîchage biologique, expérience qui a renforcé ma conviction de la nécessité d'une agriculture respectueuse de l'environnement et ancrée dans les territoires.\n\nProfondément attaché à l'éducation et à l'éducation populaire, je crois au rôle essentiel de la vie associative pour renforcer le lien social. Je souhaite aujourd'hui contribuer à un projet municipal fondé sur l'écoute, le dialogue et la coopération, au service d'une commune solidaire, dynamique et durable."
  },
  12: {
    name: "Coraline Alberti",
    meta: "36 ans · Médecin addictologue",
    location: "Les Sajolles",
    photo: "/assets/img/equipe/12.png",
    text: "Dans mon métier, l'écoute, le soutien et l'accompagnement de l'autre guident chacune de mes interventions. Au fil de ma pratique, une chose m'apparaît essentielle : le lien est fondamental à l'équilibre de chacun. Se sentir ancré, appartenir à une communauté — cela ne va pas toujours de soi, et l'environnement dans lequel on grandit façonne profondément notre trajectoire.\n\nC'est pourquoi je crois que la commune doit être un lieu de ressources, un espace où chaque habitant se sent en sécurité, soutenu, écouté, mais aussi où l'on peut rire et partager. Aujourd'hui, j'ai à cœur de m'engager avec Combaillaux Autrement pour le renouveau de cette commune, dans laquelle j'ai grandi et où je vois mon fils grandir à son tour, pour faire de Combaillaux un village où chacun trouve sa place."
  },
  13: {
    name: "Clément Rodriguez-Soulairol",
    meta: "19 ans · Étudiant en droit",
    location: "Secteur Drailles",
    photo: "/assets/img/equipe/13.png",
    text: "J'ai bientôt 19 ans. Je suis étudiant en droit à la faculté de Montpellier. J'ai toujours vécu à Combaillaux. J'aime mon village. J'y ai appris à lire, à compter, à jouer au tennis, à faire du vélo... J'ai arpenté sa garrigue avec le Club Nature, j'ai participé aux opérations de nettoyage des bords de la Mosson. J'y ai mes amis, mes racines.\n\nParce que je crois que chacun peut apporter à la collectivité, que je préfère m'impliquer que supporter ou subir, je souhaite être acteur, m'impliquer et m'engager dans la vie de ma commune.\n\nJe pense pouvoir apporter la vision des jeunes de la commune, notamment leurs aspirations, besoins, attentes et souhaits, au sein d'une équipe portée par l'intérêt général dans une démarche participative où chacun peut donner son avis et apporter sa pierre à l'édifice."
  },
  14: {
    name: "Claudine Ménard",
    meta: "54 ans · Enseignante-chercheuse en biochimie",
    location: "Les Servants",
    photo: "/assets/img/equipe/14.png",
    text: "Enseignante-chercheuse en biologie à la Faculté des Sciences, mon métier consiste à étudier le vivant et à transmettre des connaissances scientifiques. Cet engagement m'amène naturellement à m'intéresser aux questions d'environnement, de santé et de qualité de vie au quotidien.\n\nJ'apprécie particulièrement les démarches fondées sur l'observation, le dialogue et le bon sens. Comprendre avant d'agir, expliquer les choix et avancer collectivement me semblent essentiels pour construire des projets utiles et durables. Je souhaite contribuer à une réflexion locale sur la biodiversité, l'alimentation de proximité et la sensibilisation à l'environnement, dans une approche à la fois scientifique et accessible à tous.\n\nRejoindre Combaillaux Autrement, c'est pour moi participer à une dynamique collective au service du village, en apportant mon expérience d'enseignante et de chercheuse, avec sérieux, écoute et esprit d'équipe."
  },
  15: {
    name: "Michel Vanneste",
    meta: "57 ans · Chirurgien-orthopédiste",
    location: "Les Servants",
    photo: "/assets/img/equipe/15.png",
    text: "Vit à Combaillaux depuis 12 ans.\n\nNon en phase avec les projets urbanistiques de la municipalité (tout béton sans réflexion) et sa gouvernance qui me paraît autocratique.\n\nAprès plus de 3 mandats exercés par l'équipe en place, Combaillaux mérite un renouveau, pour valoriser son patrimoine et protéger la merveilleuse nature qui l'entoure, en intégrant davantage ses habitants dans les prises de décisions."
  },
  16: {
    name: "Danièle Guigou",
    meta: "68 ans · Peintre-sculptrice",
    location: "Les Sajolles",
    photo: "/assets/img/equipe/16.png",
    text: "J'habite à Combaillaux depuis plus de 10 ans. Je suis très concernée par le vivant : la cause animale, les graines reproductibles, les arbres…\n\nMes zones d'intérêt :\n— Résilience alimentaire via nos potagers, les échanges avec les agriculteurs, préservation d'une production locale.\n— Agriculture respectueuse des sols et des riverains, bio de préférence.\n— Préservation de nos ressources en eau, restauration des puits, haies, qualité des sols.\n\nJ'espère trouver des chemins nouveaux pour que ces idées puissent prendre pleinement forme dans le concret, en concertation avec les personnes concernées et au sein de notre collectif."
  },
  17: {
    name: "Jean-Marie Crapez",
    meta: "67 ans · Professeur spécialisé déficients auditifs retraité",
    location: "Secteur Route de Grabels",
    photo: "/assets/img/equipe/17.png",
    text: "Professeur spécialisé pour déficients auditifs, aide à la communication en LSF (Langue des signes française), expert auprès des tribunaux, retraité.\n\nArrivé à Combaillaux en 1995, je me suis très vite investi dans la vie du village. Dès 1996, j'ai rejoint l'APE, où j'ai eu le plaisir de participer activement pendant les dix années de prime jeunesse de mes deux garçons.\n\nAttiré depuis toujours par l'entraide et l'humain, j'ai orienté toute ma carrière dans ce sens : d'abord comme professeur d'histoire spécialisé, puis comme interprète en langue des signes française (LSF) auprès d'adolescents et d'adultes sourds. Cet engagement m'a également conduit à m'impliquer dans plusieurs associations œuvrant pour les personnes en situation de handicap.\n\nAujourd'hui, c'est avec un grand plaisir que je rejoins la belle équipe intergénérationnelle et motivée de « Combaillaux Autrement »."
  },
  18: {
    name: "Laurence Tubiana",
    meta: "Directrice, Fondation Européenne pour le Climat",
    location: "Plaine du Mas de Gentil",
    photo: "/assets/img/equipe/18.png",
    text: "Laurence Tubiana habite Combaillaux depuis 1991 et vient régulièrement s'y ressourcer.\n\nÉconomiste et diplomate française, elle est professeure-associée, directrice de la chaire « développement durable » de Sciences Po, doyenne de « l'école du climat » à Sciences Po-Paris et titulaire de la chaire « démocratie et climat » à l'École normale supérieure de Paris.\n\nElle dirige la Fondation Européenne pour le Climat depuis 2017 et siège au Haut Conseil pour le Climat.\n\nElle est connue pour son engagement lors de l'accord de Paris signé le 12 décembre 2015, où elle négocie en tant que représentante spéciale du ministre des Affaires étrangères dans le cadre de la COP 21.\n\nRejoindre la liste de « Combaillaux Autrement » aujourd'hui, c'est affirmer que la bataille est autant pour le climat que pour la démocratie."
  },
  19: {
    name: "François Lerin",
    meta: "Chercheur médiateur en agroenvironnement",
    location: "Plaine du Mas de Gentil",
    photo: "/assets/img/equipe/19.png",
    text: "Combaillaulenc depuis plus de 35 ans, un peu à l'écart du village, au Mas de Gentil. Économiste, je fais des sciences sociales appliquées et impliquées, sur l'agri-environnement et les stratégies de transition à partir d'une ONG.\n\nJ'ai été membre du Conseil Municipal de notre village, tête de liste d'une opposition en 2014. J'aime la garrigue et le milieu méditerranéen de ce petit coin encore un peu rural, proche de la Métropole.\n\nJe rejoins avec plaisir et enthousiasme cette liste et suis prêt à donner mon temps, mon énergie et mes compétences pour cette élection et après… Mais je garde toujours un chapeau."
  },
  20: {
    name: "Léane Freyburger-Giouve",
    meta: "18 ans · Étudiante en droit",
    location: "Les Sajolles",
    photo: "/assets/img/equipe/20.png",
    text: "Étudiante en deuxième année de droit, j'ai choisi de rejoindre le collectif Combaillaux Autrement et de m'engager sur cette liste afin de contribuer au développement de notre commune.\n\nAprès plusieurs discussions avec des personnes investies dans ce projet depuis ses débuts, j'ai pris la décision d'intégrer à mon tour cette nouvelle dynamique, engagée à porter collectivement de nouveaux projets pour Combaillaux.\n\nMotivée à m'impliquer pour l'avenir de notre village, je suis convaincue que renouveau et évolutions sont possibles. Rejoindre Combaillaux Autrement c'est pour moi défendre des projets concrets tout en participant à une dynamique citoyenne tournée vers l'avenir de notre village."
  },
  21: {
    name: "Claude Hammecker",
    meta: "61 ans · Directeur de recherche science du sol (IRD)",
    location: "Quartier du Patus",
    photo: "/assets/img/equipe/21.png",
    text: "Directeur de recherche en science du sol à l'IRD (Institut de Recherche pour le Développement), installé à Combaillaux au Quartier du Patus.\n\nMes travaux portent sur la physique des sols, la gestion de l'eau en milieu semi-aride et les enjeux liés à la dégradation des terres. Cette expertise scientifique me sensibilise aux défis environnementaux auxquels notre commune est confrontée.\n\nRejoindre Combaillaux Autrement, c'est pour moi mettre ces compétences au service d'un projet collectif qui place la préservation de notre environnement et la participation citoyenne au cœur de la gestion municipale."
  }
};

var currentId = null;

function showBio(id) {
  if (currentId === id) {
    closeBio();
    return;
  }

  var bio = bios[id];
  if (!bio) return;

  var cards = document.querySelectorAll('.candidate-card');
  cards.forEach(function(c) { c.classList.remove('active'); });
  var activeCard = document.querySelector('.candidate-card[data-id="' + id + '"]');
  if (activeCard) activeCard.classList.add('active');

  document.getElementById('bio-photo').src = bio.photo;
  document.getElementById('bio-photo').alt = bio.name;
  document.getElementById('bio-name').textContent = bio.name;
  document.getElementById('bio-meta').textContent = bio.meta;
  document.getElementById('bio-location').textContent = bio.location;
  document.getElementById('bio-text').textContent = bio.text;

  var panel = document.getElementById('bio-panel');
  panel.style.display = 'block';

  setTimeout(function() {
    panel.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
  }, 50);

  currentId = id;
}

function closeBio() {
  document.getElementById('bio-panel').style.display = 'none';
  var cards = document.querySelectorAll('.candidate-card');
  cards.forEach(function(c) { c.classList.remove('active'); });
  currentId = null;
}
</script>