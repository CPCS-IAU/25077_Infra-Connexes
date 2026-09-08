# Corridor Bangui–Lisala — SIG en ligne

Visualiseur des couches SIG du mandat **CPCS 25077** (étude d'appui à la
mobilité et au transport dans la zone du corridor Bangui–Zongo–Akula–Lisala,
RDC).

Quinze couches réparties en six groupes thématiques, dont l'ordre de dessin se
réorganise par glisser-déposer, comme dans un SIG de bureau.

| Groupe | Couches |
|---|---|
| Corridor | emprise 500 m, phases du programme, axe RN6 / RN23 |
| Équipements de proximité (moins de 500 m) | santé, éducation, marchés et stockage, ports/bacs/aérodromes |
| Priorisation — eau potable | priorité par village |
| Priorisation — réhabilitation | formations sanitaires, villages scolaires |
| Relevé de terrain OKAPI | villages relevés |
| Contexte (rasters) | population 2030, productivité de l'aquifère, stockage souterrain, classe de sol |

## Sources

Relevé de terrain OKAPI (sept. 2026) · GRID3 COD Health Facilities v9.0 ·
OpenStreetMap et export national HOT OSM · Overture Maps · GHS-POP R2023A
(Copernicus / JRC) · MacDonald et al. 2012 (UNESCO IHP-WINS) · SoilGrids 2.0 ·
HydroRIVERS v1.0 · analyse CPCS 2026.

Chaque objet est cliquable : une structure de santé donne son niveau, son aire
de santé, sa population desservie, sa charge et son rang de réhabilitation ; un
village donne son relevé OKAPI, son rang de priorité pour l'eau et son rang
scolaire. Un clic hors objet lit la classe des rasters affichés, sans télécharger
de donnée supplémentaire : le navigateur relit la couleur du pixel.

## Mise à jour des données

Depuis le dossier du mandat, régénérer les GeoJSON puis recopier :

```
"C:\Program Files\QGIS 3.44.4\apps\Python312\python.exe" 04_scripts\27_export_web.py
"C:\Program Files\QGIS 3.44.4pps\Python312\python.exe" 04_scripts8_export_rasters_web.py
```

Le script écrit dans `Analyse_SIG_Corridor/05_sig_en_ligne/data/`. Copier ce
dossier ici, puis `git add data && git commit && git push`.

`index.html` est écrit à la main et n'est pas régénéré : le modifier
directement.

## Diffusion

Le site porte `robots.txt` et une balise `noindex` : accessible par lien, non
indexé par les moteurs.
