# Quantification of CellROX signal at engulfed fungal spores

## Overview

This pipeline quantifies the association between oxidative stress signals and fungal spores in fluorescence microscopy images through intensity-based colocalization analyses. The workflow combines macrophage segmentation masks generated using Cellpose with image-based analysis of CellROX and fungal spore channels to calculate colocalization metrics at both the macrophage and fungal spore levels.

## Microscopy Data Structure
The pipeline expects three-channel microscopy images with the following channel order:
| Channel | Description |
|----------|-------------|
| CH1 | CellROX |
| CH2 | Fungal spores |
| CH3 | Brightfield |

Macrophage boundaries are detected using the CellROX signal and segmented using Cellpose. The resulting segmentation masks, generated through the accompanying JIPipe workflow, are required as input for the colocalization analysis.

## Experimental Conditions
The pipeline has been developed and tested on:
#### timepoints:
- 1 h, 2 h, and 6 h post-infection
#### organisms:
- Aspergillus fumigatus wild type
- Aspergillus fumigatus ΔpksP
- Lichtheimia
#### macrophages:
- RAW macrophages
- Human monocyte-derived macrophages (hMDMs)
