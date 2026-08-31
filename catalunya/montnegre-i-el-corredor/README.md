# Rutes del Parc Natural del Montnegre i el Corredor

JSON curats de les rutes senyalitzades oficials (Diputació de Barcelona / Xarxa de Parcs Naturals).

## Contingut

- `index.json` — Índex de totes les rutes
- Un fitxer `.json` per cada ruta amb la mateixa estructura que les del Montseny

## Estructura de cada ruta

- Metadades curades (nom, descripció, dificultat, punt d’inici, distància, durada…) en català
- `category`: GR | PR-C | SL-C
- `track`: preparat per rebre polyline (actualment buit; cal generar-la des d’OSM amb la mateixa metodologia del Montseny)
- `source`: OpenStreetMap (ODbL) + `relation_id` quan es coneix
- `image`: `imgs/<id-de-la-ruta>.webp`

## Tracks

Les geometries s’han d’extreure d’OpenStreetMap (llicència ODbL – gratuïta i compatible amb ús comercial amb atribució).  
Relacions conegudes:

- GR 5 → relation/379910
- PR-C 216 → relation/11977618

Per a la resta, cerca per `ref=SL-C XX` o `ref=PR-C XXX` + `route=hiking`.

## Ús

Copia els JSON a la carpeta de rutes del projecte i genera les polylines amb el mateix script/mètode que es va fer per al Montseny.
