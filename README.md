# LOOMI

Prototype web d'un **réseau social de quartier** — facilite les rencontres entre voisins, le partage d'événements locaux et l'entraide via petites annonces.

Concept et maquette interactive développés en autonomie : design produit + intégration front-end de A à Z.

[![HTML5](https://img.shields.io/badge/HTML-5-E34F26?logo=html5&logoColor=white)](#)
[![CSS3](https://img.shields.io/badge/CSS-3-1572B6?logo=css3&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-F7DF1E?logo=javascript&logoColor=black)](#)
[![No framework](https://img.shields.io/badge/no_framework-clean-success)](#)

**Démo live** : https://maximegarin.github.io/LOOMI/

---

## Concept

LOOMI veut recréer une couche de lien social hyperlocal à l'échelle d'un quartier :

- Rencontres 1-to-1 entre voisins (profils, intérêts partagés, propositions d'activités)
- Événements de quartier (apéros, ateliers, marchés, vide-greniers)
- Petites annonces d'entraide (services, prêt, dons)
- Messagerie privée entre voisins

Cible : les habitants d'un même quartier qui veulent retisser du lien sans passer par les groupes Facebook ou WhatsApp.

---

## Stack

| Couche | Choix | Pourquoi |
| --- | --- | --- |
| HTML | HTML5 sémantique | Accessibilité, SEO friendly |
| CSS | CSS3 vanilla, variable d'accent (`--orange`) | Maintenable sans build step, pas de tooling à apprendre |
| JS | JavaScript vanilla (DOM API native) | Aucune dépendance, démarrage instantané |
| Fonts | Nunito | Lisibilité chaleureuse cohérente avec le ton communautaire |
| Build | Aucun | Site statique 100% déployable tel quel |

Volontairement sans framework : ce prototype valide les principes UX/UI avant d'investir dans une stack lourde.

---

## Fonctionnalités présentes

- **Navigation responsive** : barre horizontale desktop + menu burger mobile
- **Section Hero** avec CTA d'inscription
- **Carte de profil voisin** (rencontre 1-to-1) avec actions suggérées
- **Cards d'événements** locaux
- **Liste de petites annonces** avec verbatim utilisateur
- **Sidebar messagerie** dépliable, fermeture au clic externe
- **Footer** avec liens réseaux sociaux et mentions

Le menu burger et la sidebar messagerie sont les seules interactions JS — tout le reste est statique pour valider la maquette visuelle.

---

## Captures d'écran

*(Placeholders — à remplacer par captures réelles)*

| Desktop | Mobile (menu ouvert) | Messagerie |
| --- | --- | --- |
| ![Desktop](docs/screenshots/desktop.png) | ![Mobile](docs/screenshots/mobile.png) | ![Sidebar](docs/screenshots/messagerie.png) |

---

## Lancement local

Aucune dépendance, aucun build. Ouvrir `index.html` directement dans le navigateur fonctionne. Pour une expérience plus propre avec live reload :

```bash
# Avec Python (préinstallé sur Windows 10+ via Microsoft Store)
python -m http.server 8000

# Avec Node
npx serve

# Avec VS Code
# → Extension "Live Server" → clic droit index.html → "Open with Live Server"
```

Puis ouvrir `http://localhost:8000`.

---

## Structure du projet

```
.
├── index.html              Document principal, toutes les sections
├── style.css               Design system + responsive (breakpoint 768px)
├── script.js               Toggle menu burger + sidebar messagerie
└── assets/
    └── images/             SVG + JPG (logo, illustrations, profils, événements)
```

---

## Limitations actuelles (assumées)

Ce projet est un **prototype design** — pas une app production-ready. Voir Roadmap pour la suite envisagée.

- Pas de backend, donc aucune persistance des données
- Pas de système d'authentification réel
- Les contenus (profils, événements, annonces) sont statiques dans le HTML
- Le breakpoint responsive est unique (768px) — à raffiner pour les tablettes et grands desktops

---

## Roadmap

Si le concept était poussé en produit :

- [ ] Refonte mobile-first stricte avec breakpoints plus fins (320px / 768px / 1024px / 1440px)
- [ ] Migration vers un framework léger (Astro ou Next.js) pour les pages dynamiques
- [ ] Backend Node.js / PostgreSQL avec auth + géolocalisation au quartier
- [ ] Système de messagerie temps réel (WebSocket)
- [ ] Notifications push pour nouveaux événements / annonces du quartier
- [ ] Application mobile React Native

---



---

## Auteur

**Maxime Garin** — [github.com/maximegarin](https://github.com/maximegarin)

Projet réalisé en autonomie au début de ma formation Titre Pro Développeur Web à l'AFEC Bayonne (2024–2026), en exploitant mon double profil designer + développeur.
