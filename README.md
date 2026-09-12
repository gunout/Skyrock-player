# 📻 Skyrock Paris – Interface HUD

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![jQuery](https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

> **Lecteur radio Skyrock avec interface HUD futuriste, webradios et carte complète des fréquences FM/DAB+ en France**

Interface web immersive pour écouter **Skyrock** et ses **7 webradios thématiques**, avec un design HUD cyberpunk, un visualiseur audio animé, un carrousel d'arrière-plan dynamique, et un recensement complet des **fréquences FM et DAB+** dans toute la France (métropole, Corse, Monaco, Espagne frontalière).

---

## 📋 Table des matières

- [Aperçu](#-aperçu)
- [Fonctionnalités](#-fonctionnalités)
- [Webradios](#-webradios)
- [Fréquences FM/DAB+](#-fréquences-fmdab)
- [Installation](#-installation)
- [Utilisation](#-utilisation)
- [Technologies](#-technologies)
- [Captures d'écran](#-captures-décran)
- [Contribuer](#-contribuer)
- [Licence](#-licence)

---

## 🎯 Aperçu

Cette interface HUD (Head-Up Display) au design **cyberpunk / futuriste** permet de :

- 🎧 **Écouter Skyrock** en direct (flux icecast 128 kbps)
- 🎵 **Basculer entre 7 webradios** thématiques (Rap & RnB, 100% Français, Klassiks, Urban, Hit US, PLM…)
- 📻 **Consulter la carte complète des fréquences** FM et DAB+ partout en France
- 🌈 **Profiter d'un carrousel d'arrière-plan** synchronisé avec la webradio active
- 🎨 **Visualiser le son** avec un visualiseur circulaire animé
- 🎛️ **Contrôler le volume** via un slider custom
- 🔗 **Accéder aux replays** via un panneau dédié avec redirection vers skyrock.fm/replay

---

## ✨ Fonctionnalités

### 🎵 Lecteur principal (HUD)
- **Bouton play/pause** central avec animations
- **Visualiseur circulaire** de 20 barres animées
- **Statut système** : `SYS.ONLINE`, `SYS.PAUSED`, `SYS.OFFLINE`, `SYS.ERROR`
- **Readout de données** : bitrate (KBS), fréquence FM, latence (MS) — simulés en temps réel
- **Contrôle du volume** avec fill visuel et icônes −/+

### 🎨 Design HUD cyberpunk
- **3 anneaux orbitaux** rotatifs autour du player
- **Scan line** animée sur le core player
- **Logo Skyrock** pulsant avec effet néon rouge
- **Décorations d'angle** (4 coins) façon interface militaire
- **Grille HUD** en arrière-plan
- **Palette de couleurs** :
  - 🔴 Rouge primaire `#ff3b3b`
  - 🟠 Orange secondaire `#ff9e00`
  - 🔵 Cyan DAB+ `#00f3ff`
  - ⚫ Fond sombre `#050505`

### 🌈 Carrousel d'arrière-plan (Slick)
- **Plein écran** en arrière-plan
- **Transition en fondu** synchronisée avec la webradio active
- **Filtres CSS** : brightness 30 %, contraste 115 %, saturation 120 %
- **Overlay radial** pour la lisibilité du HUD
- **Fallback** en dégradé si les images échouent

### 🎛️ Webradios (7 stations)
Carrousel horizontal en bas de l'écran :
- 🎤 **Skyrock** (station principale)
- 🎵 **Rap & RnB**
- 🇫🇷 **100% Français**
- 🎼 **Klassiks**
- 🌆 **Urban**
- 🇺🇸 **Hit US**
- 🎧 **PLM**

### 📻 Panneau "Stations FM"
- **Recherche par ville** ou département
- **Filtre par département** (dropdown)
- **Compteur dynamique** de villes
- **Liste triée alphabétiquement**
- **Badges DAB+** cyan pour les fréquences numériques
- **Bouton "Écouter"** sur chaque station FM
- **Compteur total** : nombre de villes et de départements

### 🎙️ Panneau "Replays"
- Redirection directe vers **skyrock.fm/replay**
- **Bouton animé** avec effet shine
- **Note de mise à jour automatique**

### 📊 Données FM/DAB+
- **~500 villes** recensées
- **~100 départements** couverts (métropole + Corse + Monaco + Espagne frontalière)
- **Deux types de fréquences** :
  - 📻 **FM** : fréquence classique (ex. 96.0 FM)
  - 📡 **DAB+** : radio numérique terrestre

---

## 🎵 Webradios

| ID | Nom | Description | Flux |
|----|-----|-------------|------|
| `skyrock` | 🎤 Skyrock | Station principale rap/RnB | `natio_mp3_128k` |
| `rap-rnb` | 🎵 Rap & RnB | 100% rap et RnB | `rap_rnb_aac_128k` |
| `francais` | 🇫🇷 100% Français | Rap français uniquement | `francais_aac_128k` |
| `klassiks` | 🎼 Klassiks | Classiques du rap | `klassiks_aac_128k` |
| `urban` | 🌆 Urban | Urban music | `urban_music_aac_128k` |
| `hit-us` | 🇺🇸 Hit US | Hits américains | `hit_us_aac_128k` |
| `plm` | 🎧 PLM | Pour La Musique | `plm_aac_128k` |

---

## 📻 Fréquences FM/DAB+

### Couverture géographique
| Zone | Départements couverts |
|------|----------------------|
| **Métropole** | 01 à 95 (hors 20 pour Paris intramuros) |
| **Corse** | 2A (Corse-du-Sud), 2B (Haute-Corse) |
| **Monaco** | MC |
| **Espagne frontalière** | ES (San Sebastián) |

### Exemples de fréquences

#### 🏙️ Grandes villes
| Ville | FM | DAB+ |
|-------|-----|------|
| **Paris** | 96.0 FM | ✅ |
| **Marseille** | 90.0 FM | ✅ |
| **Lyon** | 96.1 FM | — |
| **Toulouse** | 100.0 FM | — |
| **Nice** | 107.0 FM | — |
| **Nantes** | 102.9 FM | — |
| **Bordeaux** | 102.8 FM | — |
| **Lille** | 94.3 FM | — |
| **Strasbourg** | 96.0 FM | — |

#### 🏔️ Stations de ski / zones touristiques
| Ville | FM |
|-------|-----|
| Chamonix-Mont-Blanc | 93.5 FM |
| Les Deux Alpes | 106.0 FM |
| Val Thorens | — (DAB+) |
| Saint-Martin-de-Belleville | 93.0 FM |
| Vars | 88.3 FM |

#### 🏝️ Outre-mer / frontières
| Zone | FM |
|------|-----|
| Monaco | 102.1 FM |
| San Sebastián (ES) | 100.7 FM |

### Types de réception
- **FM analogique** : fréquences classiques (87.5 → 108.0 MHz)
- **DAB+ (Digital Audio Broadcasting)** : diffusion numérique, meilleure qualité audio

---

## 🚀 Installation

### Prérequis
- Un navigateur moderne (Chrome, Firefox, Edge, Safari)
- Une connexion internet (flux radio + polices + CDN)
- (Optionnel) Un serveur HTTP local

### Installation rapide

```bash
# 1. Cloner le dépôt
git clone https://github.com/votre-utilisateur/skyrock-hud-paris.git
cd skyrock-hud-paris

# 2. Ouvrir directement dans le navigateur
open index.html      # macOS
xdg-open index.html  # Linux
start index.html     # Windows
```

> ⚠️ **Important** : Certains navigateurs bloquent la lecture audio automatique sur `file://`. Un serveur local est recommandé.

### Avec serveur local

```bash
# Python 3
python3 -m http.server 8000

# Node.js (avec npx)
npx serve . -l 8000

# PHP
php -S localhost:8000
```

Puis ouvrir : **http://localhost:8000**

---

## 🎮 Utilisation

### 🎧 Écouter la radio
1. Cliquer sur le **bouton play** central (triangle rouge)
2. Le HUD passe en `SYS.ONLINE` et le visualiseur s'anime
3. Ajuster le **volume** via le slider en bas

### 🎵 Changer de webradio
1. Cliquer sur une **webradio** dans le carrousel du bas
2. L'arrière-plan change en fondu
3. La lecture continue automatiquement

### 📻 Consulter les fréquences
1. Cliquer sur **« Stations FM »** en haut à droite
2. Le panneau s'ouvre à droite
3. **Filtrer par département** via le dropdown
4. **Rechercher une ville** via la barre de recherche
5. Cliquer sur ▶️ pour écouter Skyrock depuis cette ville

### 🎙️ Accéder aux replays
1. Cliquer sur **« Replays »** (bouton orange)
2. Le panneau s'ouvre avec un bouton de redirection
3. Cliquer sur le bouton → ouverture de **skyrock.fm/replay**

---

## 🛠️ Technologies

| Technologie | Usage |
|-------------|-------|
| HTML5 | Structure sémantique |
| CSS3 | Design HUD, animations, grid, glassmorphism |
| JavaScript (Vanilla) | Contrôle audio, gestion des stations, simulation |
| [jQuery 3.6.0](https://jquery.com/) | Requis par Slick Carousel |
| [Slick Carousel 1.8.1](https://kenwheeler.github.io/slick/) | Carrousel d'arrière-plan plein écran |
| [Google Fonts](https://fonts.google.com/) | Orbitron + Share Tech Mono |
| HTML5 Audio API | Lecture des flux icecast |
| CDN jsDelivr | Slick Carousel + Fonts |

### Flux audio utilisés
- **Icecast Skyrock** : `https://icecast.skyrock.net/s/natio_mp3_128k`
- **Webradios** : flux AAC 128 kbps

---

## 📸 Captures d'écran

> *Ajoutez ici vos captures d'écran de l'interface*

```
📷 [Capture 1 : HUD principal avec anneaux orbitaux et visualiseur]
📷 [Capture 2 : Carrousel de webradios en bas de l'écran]
📷 [Capture 3 : Panneau "Stations FM" avec liste filtrée]
📷 [Capture 4 : Panneau "Replays" avec bouton de redirection]
```

---

## 🤝 Contribuer

Les contributions sont les bienvenues !

1. Fork le projet
2. Créer une branche (`git checkout -b feature/amelioration`)
3. Commit les changements (`git commit -m 'Ajout fonctionnalité X'`)
4. Push (`git push origin feature/amelioration`)
5. Ouvrir une Pull Request

### Idées d'amélioration
- [ ] Ajout d'une carte interactive Leaflet pour visualiser les fréquences
- [ ] Détection automatique de la ville de l'utilisateur (géolocalisation)
- [ ] Ajout d'un égaliseur audio (Web Audio API)
- [ ] Historique des morceaux (via API Skyrock)
- [ ] Mode clair / sombre
- [ ] PWA (Progressive Web App) avec mode hors-ligne
- [ ] Support des raccourcis clavier (espace = play/pause, ↑↓ = volume)
- [ ] Intégration des podcasts Skyrock avec lecteur intégré
- [ ] Mise à jour automatique des fréquences depuis l'API Skyrock
- [ ] Ajout des fréquences en Outre-mer (DOM-TOM)

---

## 📄 Licence

Ce projet est distribué sous licence **MIT**. Voir le fichier [LICENSE](LICENSE) pour plus d'informations.

### Fichier `LICENSE` (MIT)

```
MIT License

Copyright (c) 2026 Skyrock Paris – Interface HUD

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## ⚠️ Avertissement légal

Ce projet est un **lecteur non officiel** des flux publics de Skyrock. Il n'est **pas affilié, sponsorisé ou approuvé** par Skyrock ou ses ayants droit. Toutes les marques, logos et contenus audio restent la propriété de leurs détenteurs respectifs.

- Les flux audio sont publics et diffusés par Skyrock via Icecast.
- Ce projet ne stocke, ne redistribue ni ne modifie les flux.
- Les logos et images sont utilisés à titre illustratif uniquement.

---

## 🙏 Remerciements

- [Skyrock](https://skyrock.fm/) – Flux radio et webradios
- [Slick Carousel](https://kenwheeler.github.io/slick/) – Carrousel d'arrière-plan
- [jQuery](https://jquery.com/) – Bibliothèque JS
- [Google Fonts](https://fonts.google.com/) – Orbitron & Share Tech Mono
- [jsDelivr](https://www.jsdelivr.com/) – CDN

---

<p align="center">
  <strong>📻 SKYROCK · Interface HUD</strong><br>
  <em>Première radio rap & RnB de France</em><br>
  <code>SYS.ONLINE</code>
</p>


## LIENS 

    https://gunout.github.io/Skyrock-player/

## EXAMPLE

<img width="1803" height="786" alt="Screenshot 2026-09-12 at 01-42-31 Skyrock Paris - Interface HUD" src="https://github.com/user-attachments/assets/ed90b1b0-4f9a-4193-b910-1facef440766" />

<img width="1803" height="786" alt="Screenshot 2026-09-12 at 01-45-42 Skyrock Paris - Interface HUD" src="https://github.com/user-attachments/assets/eb18db47-3da8-45f4-ae4f-59d102f46078" />

<img width="1803" height="786" alt="Screenshot 2026-09-12 at 01-45-25 Skyrock Paris - Interface HUD" src="https://github.com/user-attachments/assets/527e4fa4-59d6-4898-80a3-3eed0bd77199" />

---

<div align="center">

### 🇫🇷 Gunout · 2026

![Made in France](https://img.shields.io/badge/Made_in-France-002395?style=flat-square&labelColor=FFFFFF&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA5MDAgNjAwIj48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjYwMCIgZmlsbD0iIzAwMjM5NSIvPjxyZWN0IHdpZHRoPSI5MDAiIGhlaWdodD0iNDAwIiB5PSIxMDAiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjIwMCIgeT0iNDAwIiBmaWxsPSIjZWQyOTM5Ii8+PC9zdmc+)
![GitHub](https://img.shields.io/badge/GitHub-gunout-181717?style=flat-square&logo=github&logoColor=white)
![Year](https://img.shields.io/badge/2026-ED2939?style=flat-square&labelColor=FFFFFF)

<sub>© 2026 <strong>gunout</strong> — Tous droits réservés.</sub>

</div>
