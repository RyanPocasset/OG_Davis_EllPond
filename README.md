# Long Pond & AWC Tree Models

Interactive 3D viewer for 34 field-mapped trees (4, 9 and 18 Nov 2026) at Long Pond–Ell Pond, Hopkinton, RI, and an Atlantic white cedar site in the Westerly area. Each tree is matched to its crown in the 2022 USGS LiDAR. Leaf-off orthophotos can be draped under the point cloud.

The page loads its data from `data/` and `img/`, so serve it through GitHub Pages or any web server. It won't run from a double-clicked local file.

Views: **Tree 3D**, **Map** and **Site 3D**. Link straight to a tree with `#tree-12`, or to a view with `#map-longpond`, `#map-awc`, `#site-longpond` or `#site-awc`.

## Data

- **LiDAR**: USGS 3DEP Rhode Island Statewide 2022 (`RI_Statewide_1_D22`), flown 29 Mar 2022, leaf-off, ~19 pts/m². Public domain.
- **Orthophotos**: RIDOT 3-inch leaf-off imagery, April 2022 and March 2026, via RIGIS (maps.edc.uri.edu/rigis).
- **Coordinates**: NAD83(2011) / UTM zone 19N. GPS waypoints were shifted 1.28 m from the GPS's ITRF frame into NAD83(2011) before matching.
- **three.js** r128 (MIT licence), vendored in `vendor/`.

## Files

| Path | Contents |
|---|---|
| `index.html` | The viewer |
| `data/meta.json` | Metrics and match notes for all 34 trees |
| `data/tree_NN.json` | Per-tree point scene, crown envelope and ground mesh |
| `data/site3d_*.json` | Decimated site point clouds with GPS pins |
| `data/maps.json` | Map extents, crown outlines and GPS points |
| `img/` | Canopy height maps and leaf-off orthophotos |
