# Scaling and background subtraction

## Introduction

## Reciprocal space grid

```
mdx2.design_grid miller_index.h5 --supercell 3 3 3 --dmin 1.25
```
--> grid.nxs

## Integration

```
mdx2.integrate images.nxs coarse_grid.nxs
```
--> integrated.nxs

## Correcting

```
mdx2.correct coarse_integrated.nxs corrections.nxs --background bkg_filtered.nxs
```
--> intensity.nxs

## Scaling

```
mdx2.scaling_model images.nxs --absorption --thickness --background
```
--> scales.nxs
```
mdx2.refine_scales intensity.nxs scales.nxs
```
--> scales.nxs (overwrite or add?)

## Inspect scaling model
