# Data exploration

## Introduction

mdx2

nexus format

nexpy

## Using mdx2 command line tools

Listing available commands

Getting help

## Import image stacks using mdx2

Import crystal diffraction images

```
mdx2.import_images ../dials/imported.expt
```

Import background images

```
mdx2.import_images ../dials/background.expt --outfile bkg_images.nxs
```

## Import diffraction geometry using mdx2

Unit cell and space group symmetry

```
mdx2.import_crystal ../dials/scaled.expt
```

```
mdx2.import_corrections ../dials/scaled.expt --sampling 20 20 2
```

Miller indices

```
mdx2.import_miller_index ../dials/scaled.expt --sampling 10 10 1
```

## Explore nexus data files in nexpy

```
nexpy
```

## Masking Bragg peaks with mdx2

```
mdx2.find_peaks images.nxs --threshold 20
```

```
mdx2.mask_peaks peaks.nxs miller_index.nxs
```
--> outlier_mask.nxs and peak_mask.nxs

Apply masks using the command line

## Image processing with mdx2

Background scattering (visualize binned down)

```
mdx2.downsample_images bkg_images.nxs --bin 20 20 2 --threshold 200 --outfile bkg_filtered.nxs
```

Diffuse scattering (visualize binned down)

```
mdx2.downsample_images images.nxs --bin 20 20 2 --outfile filtered.nxs
```
