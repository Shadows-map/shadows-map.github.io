# Shadows Map

Carte interactive des zones à l'ombre et au soleil créées par le relief, partout dans le monde, à n'importe quelle date et heure.

## Fonctions

- Choix de la date (calendrier, curseur sur l'année, −1 j / +1 j, Aujourd'hui) et de l'heure (curseur sur la journée). Lecture animée de la journée ou de l'année.
- Ombres portées par le relief et versants dos au soleil, calculées en direct sur la carte graphique (WebGL). Deux rendus : ombre nette ou nuancé.
- Effet de nuit progressif suivant la hauteur du soleil : crépuscules civil (0 à −6°), nautique (−6 à −12°) et astronomique (−12 à −18°). La durée de la transition dépend donc de la latitude et de la saison.
- Lieu suivi : recherche par nom, position GPS ou clic sur la carte. L'app affiche le soleil ou l'ombre à l'heure choisie, l'altitude, la durée de soleil direct sur la journée (relief compris) et les heures d'aube, de lever, de coucher et de crépuscule. Les heures sont données dans le fuseau du lieu.
- Favoris : ★ pour enregistrer un lieu. Un appui va au lieu, un appui long le renomme, un glisser change l'ordre et ✕ le supprime. Ils sont enregistrés dans le navigateur.
- Fonds de carte : OpenTopoMap, OpenStreetMap, satellite Esri, et cartes officielles de France (IGN), Suisse (swisstopo), Autriche (basemap.at), Allemagne et Europe (BKG TopPlusOpen), Espagne (IGN), Belgique (NGI), Norvège (Kartverket), États-Unis (USGS) et Japon (GSI).

## Utilisation

L'app tient dans une seule page statique, sans compilation ni clé d'API. Ouvre `index.html` via un serveur web, par exemple GitHub Pages ou `python -m http.server`.

## Limites

- Ni les bâtiments ni la végétation ne sont pris en compte.
- Le relief a une résolution d'environ 10 à 30 m par pixel selon le zoom. Les ombres sont prises en compte jusqu'à environ 12 km.
- La position du soleil est calculée au centre de la vue (précision d'environ 0,1°).

## Sources de données

- Relief : [Terrain Tiles](https://registry.opendata.aws/terrain-tiles/) (AWS Open Data, Mapzen), format Terrarium.
- Géocodage : [Open-Meteo](https://open-meteo.com/) (recherche, fuseau horaire) et [Nominatim](https://nominatim.org/) / OpenStreetMap (nom d'un point).
- Fonds de carte : voir les attributions affichées sur la carte.
- Carte : [Leaflet](https://leafletjs.com/).
