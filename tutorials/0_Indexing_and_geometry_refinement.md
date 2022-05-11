# Indexing and geometry refinement

## Introduction

This is based on the DIALS tutorial: [Processing in Detail](https://dials.github.io/documentation/tutorials/processing_in_detail_betalactamase.html)

## Tutorial data

Download `insulin_1_1.tar` from Zenodo [doi: 10.5281/zenodo.6536805](https://dx.doi.org/10.5281/zenodo.6536805).

The tar archive will expand to a directory called `images` with subfolders `insulin_2_1`, `insulin_2_bkg`, and `metrology`.

Place the `images` directory in `erice-2022-data-reduction/data/`

Create a new directory for dials processing: `erice-2022-data-reduction/data/dials`.

## Import

Open a terminal window and cd to the `erice-2022-data-reduction/data/dials` directory.

```
dials.import ../images/insulin_2_1
```

Also import the background images (will be used later in the tutorial)
```
dials.import ../images/insulin_2_bkg output.experiments=background.expt
```

```
dials.show imported.expt
```

```
dials.show background.expt
```

```
dials.image_viewer imported.expt
```

## Masking



## Find Spots

```
dials.find_spots imported.expt
```

## Indexing

```
dials.index imported.expt strong.refl space_group=199
```

## Refinement

```
dials.refine indexed.expt indexed.refl
```

## Integration

```
dials.integrate refined.expt refined.refl
```

## Scaling

```
dials.scale integrated.expt integrated.refl
```

```
dials.scale scaled.expt scaled.refl d_min=1.26
```

## Report

```
dials.report scaled.expt scaled.refl
```
