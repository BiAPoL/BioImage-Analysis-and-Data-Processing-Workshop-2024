# Bio-Image Analysis with napari

In this workshop, we will explore ways to analyze and visualize microscopy images with [napari](https://napari.org/stable/), an nD viewer open-source software.

We explore some napari plugins as an interactive and convenient way of performing these analysis, especially the [napari-assistant](https://github.com/haesleinhuepf/napari-assistant?tab=readme-ov-file#napari-assistant), [napari-apoc](https://github.com/haesleinhuepf/napari-accelerated-pixel-and-object-classification?tab=readme-ov-file#napari-accelerated-pixel-and-object-classification-apoc) and [napari-flim-phasor-plotter](https://github.com/zoccoler/napari-flim-phasor-plotter?tab=readme-ov-file#napari-flim-phasor-plotter) plugins.

We will also perform feature extraction using [napari-skimage-regionprops](https://github.com/haesleinhuepf/napari-skimage-regionprops), plot features against each other, and perform a multichannel analysis, where we measure summary statistics of objects in one channel relative to objects in another channel.

Finally, we will analyze higher dimensional FLIM data with the [napari-flim-phasor-plotter plugin](https://github.com/zoccoler/napari-flim-phasor-plotter/tree/main?tab=readme-ov-file#napari-flim-phasor-plotter).

Some [Jupyter](https://jupyter.org/) notebooks will be used to illustrate and reproduce the examples.

For this, we will be using different 3 environments. Please follow the instructions below.

## Getting started with Miniforge and Python 

If you are attending this course in presence, most of these environments will be already set up for you. Skip to [Third environment: napari-flim-phasor-env](#third-environment-napari-flim-phasor-env) to update the last environment.

Please follow the instructions from the blog post written by [Mara Lampert](https://biapol.github.io/blog/mara_lampert/readme.html) and and updated by [Stefan Hahmann](https://biapol.github.io/blog/stefan_hahmann/readme.html) and Mara Lampert again [here](https://biapol.github.io/blog/mara_lampert/getting_started_with_miniforge_and_python/readme.html) under [CC BY 4.0 License](https://creativecommons.org/licenses/by/4.0/legalcode) to install Miniforge on your computer.


## First environment: napari-intro-env 

Clone this repository to your computer (go to the repository page on GitHub [here](https://github.com/BiAPoL/BioImage-Analysis-and-Data-Processing-Workshop-2024), click the green button <span style="color:green">**Code**</span> and choose one option to clone it, the most straight-forward being downloading it as a `.zip` file). After that, open a terminal, navigate to where you cloned the repository locally in your computer and create a conda environment by running:

`mamba env create -f environment.yml`

or

`mamba env create -f https://github.com/BiAPoL/BioImage-Analysis-and-Data-Processing-Workshop-2024/raw/main/environment.yml`

After successful installation, activate your environment with:

`mamba activate napari-intro-env`

## Second environemnt: devbio-napari

Open a terminal and type (or copy the line below):

`mamba create --name devbio-napari python=3.9 devbio-napari pyqt -c conda-forge -c pytorch`

Hit `ENTER` to answer yes when asked to install packages.
Activate your environment with:

`mamba activate devbio-napari`

## Third environment: napari-flim-phasor-env

Open a terminal and type (or copy the line below):

`mamba create -n napari-flim-phasor-env python=3.9 napari pyqt git`

Hit `ENTER` to answer yes when asked to install packages.

Activate your environment with:

`mamba activate napari-flim-phasor-env`

Then install [napari-flim-phasor-plotter](https://github.com/zoccoler/napari-flim-phasor-plotter/tree/main?tab=readme-ov-file#napari-flim-phasor-plotter) with pip:

`pip install napari-flim-phasor-plotter`

Finally, include the `devbio-napari` bundle package with:

`mamba install -c conda-forge devbio-napari=0.10.0 scikit-image=0.24.0`
