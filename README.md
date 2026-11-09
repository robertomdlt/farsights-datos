# farsights-datos

Datos públicos que usa la app [FarSights](https://robertomdlt.github.io/farsights-legal/) para no depender
de servidores saturados. Se sirven a la app a través de [jsDelivr](https://www.jsdelivr.com/).

## `peaks/v1/`

Cumbres y volcanes con nombre de OpenStreetMap, en cuadrículas de 1° × 1°.

- `index.json`: versión, fecha de generación y lista de cuadrículas cubiertas.
- `<lat>_<lon>.json`: esquina suroeste de la cuadrícula en grados enteros (`40_-4` = 40–41° N, 4–3° O).
  Lista de cumbres con claves cortas: `i` id del nodo OSM, `n` nombre, `a` latitud, `o` longitud,
  `l` nombres en otros idiomas (opcional), `e` altitud en m (opcional), `p` prominencia en m (opcional).
  Una cuadrícula cubierta sin cumbres es `[]`.

Se generan con `scripts/build-peak-tiles.mjs` del repositorio de la app.

## Licencia

Los datos son © colaboradores de OpenStreetMap y están disponibles bajo la
[Open Database License (ODbL)](https://opendatacommons.org/licenses/odbl/). Ver https://www.openstreetmap.org/copyright.
