# Data Reduction Workshop for the 2022 Erice International School of Crystallography

These materials were developed for the [2022 Erice School on Diffuse Scattering](https://crystalerice.org/2022/programme_ds.php).

## Overview

The workshop is 1.5 hours and is divided into 6 self-guided tutorials.

We will introduce modern diffuse scattering data reduction techniques using three open-source python packages:

1. [dials](https://dials.github.io/) for Bragg peak indexing and geometry refinement
2. [mdx2](https://github.com/ando-Lab/mdx2) for image processing and reciprocal space reconstruction
3. [nexpy](https://nexpy.github.io/nexpy/) for visualization

The tutorials are:

- [0_introduction](tutorials/0_Indexing_and_geometry_refinement.md)
- [1_dials_indexing](1_dials_indexing.ipynb)
- [2_mdx2_geometry](2_mdx2_geometry.ipynb)
- [3_mdx2_data](3_mdx2_data.ipynb)
- [4_mdx2_integration](4_mdx2_integration.ipynb)
- [5_mdx2_merging](5_mdx2_merging.ipynb)
- [6_mdx2_python](6_mdx2_python.ipynb)

## Requirements

The exercises are designed to run on a laptop computer.

If you will bring your own laptop, please do the following *before* you travel:

1. Verify that your computer has at least 10 Gb free disk space.
2. Install the Erice-2022 python environment for macromolecular crystallography (Link: <INSERT LINK HERE>)
3. Follow the *Installation* instructions below.

## Installation on OSX / linux

Open a terminal window and add the Erice python environment to the path (Instructions here: <INSERT LINK HERE>).

Install `mdx2`

```bash
git clone https://github.com/ando-Lab/mdx2
cd mdx2
pip install -e .
```

Download the tutorials and the diffraction data. The code below places these in a subdirectory of your `Documents` folder -- you can change the location if needed.

```bash
cd ~/Documents
git clone https://github.com/ando-Lab/erice-2022-data-reduction
cd erice-2022-data-reduction
mkdir data
cd data
curl https://zenodo.org/api/records/<RECORD>
```

## Getting started

Open a terminal window and make sure Erice python environment is on path (see above):

```bash
cd ~/Documents/erice-2022-data-reduction
jupyter lab
```

In the left panel, navigate to the "tutorials" directory and double-click `0_Indexing_and_geometry_refinement.ipynb`
