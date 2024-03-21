# Machine Learning with napari plugins

In this lecture, we will explore how to apply different machine learning algorithms to images using napari plugins. We will do supervised machine learning with [napari-apoc plugin](https://github.com/haesleinhuepf/napari-accelerated-pixel-and-object-classification?tab=readme-ov-file#napari-accelerated-pixel-and-object-classification-apoc) and unsupervised machine learning with [napari-clusters-plotter plugin](https://github.com/BiAPoL/napari-clusters-plotter?tab=readme-ov-file#napari-clusters-plotter). Finally, we will go slightly off-topic to analyze FLIM data with the [napari-flim-phasor-plotter plugin](https://github.com/zoccoler/napari-flim-phasor-plotter/tree/main?tab=readme-ov-file#napari-flim-phasor-plotter).

For this, we will need to create 2 new environments. Please follow the instructions below.

## First environemnt: devbio-napari

Open a terminal and type (or copy the line below):

`mamba create --name devbio-napari-env python=3.9 devbio-napari pyqt -c conda-forge -c pytorch`

Hit `ENTER` to answer yes when asked to install packages.
Activate your environment with:

`mamba activate devbio-napari`

## Second environment: napari-flim-phasor-env

Open a terminal and type (or copy the line below):

`mamba create -n napari-flim-phasor-env python=3.9 napari==0.4.17 napari-clusters-plotter git pyqt devbio-napari`

Hit `ENTER` to answer yes when asked to install packages.

Activate your environment with:

`mamba activate napari-flim-phasor-env`

Then install [napari-flim-phasor-plotter](https://github.com/zoccoler/napari-flim-phasor-plotter/tree/main?tab=readme-ov-file#napari-flim-phasor-plotter) with pip:

`pip install napari-flim-phasor-plotter`



