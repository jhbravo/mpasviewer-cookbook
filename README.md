# MPAS-Viewer Cookbook

<img src="thumbnails/thumbnail.png" alt="thumbnail" width="300"/>

[![nightly-build](https://github.com/ProjectPythia/cookbook-template/actions/workflows/nightly-build.yaml/badge.svg)](https://github.com/ProjectPythia/cookbook-template/actions/workflows/nightly-build.yaml)
[![Binder](https://binder.projectpythia.org/badge_logo.svg)](https://binder.projectpythia.org/v2/gh/ProjectPythia/cookbook-template/main?labpath=notebooks)
[![DOI](https://zenodo.org/badge/475509405.svg)](https://zenodo.org/badge/latestdoi/475509405)


This **"Pythia Cookbook"** was started during the **Project Pythia June 15-18 2026 in Boulder, CO at the NCAR Mesa Lab**. 

This **MPAS-Viewer Cookbook** aims to provide a comprehensive guide for utilizing MPAS-Viewer, a lightweight and efficient Python-based visualization tool designed specifically for MPAS data. Unlike common approaches that rely on triangulation or iterative polygon construction, MPAS-Viewer operates directly on the native mesh, treating each model cell as the fundamental plotting unit. This approach avoids computationally expensive preprocessing steps and significantly reduces rendering time.

## Motivation

The development of this Pythia cookbook is motivated by the need to make MPAS-Viewer accessible, reproducible, and easy to adopt within the scientific community. By combining clear explanations with practical, executable examples, this cookbook provides users with a guided pathway to rapidly visualize, explore, and analyze MPAS-A outputs. It emphasizes simplicity, performance, and interactivity, enabling workflows that support animations, time exploration, and efficient data interrogation.

## Authors


| Name      | Affiliation |
| ----------- | ----------- |
| [Jorge Bravo](https://github.com/jhbravo)                 | Stevens Institute of Technology |      |
| [Name](https://github.com/user) | Affiliation  |
| []()              |  |
| []()              |  |
| []()              |  |
| []()              |  |

### Contributors

<a href="https://github.com/ProjectPythia/mpasviewer-cookbook/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ProjectPythia/mpasviewer-cookbook" />
</a>

## Structure

This practical development manual serves as an example of how to collect, manage, and present various MPAS-A data.

### Foundations

The **Model for Prediction Across Scales Atmosphere (MPAS-A)** is an advanced atmospheric model designed to represent weather systems across both regional and global scales. Its defining feature is the use of an unstructured, variable-resolution mesh, often described as a honeycomb-like grid, which allows high resolution in regions of interest while maintaining coarser resolution elsewhere. This design enables MPAS-A to efficiently capture fine-scale phenomena such as convection and storms without sacrificing the ability to simulate large-scale atmospheric dynamics.

Despite these advantages, the unstructured nature of the MPAS mesh introduces challenges for data visualization and analysis. Although MPAS-A outputs are stored in NetCDF format, they cannot be treated like conventional gridded raster data. Proper handling of the data requires knowledge of the mesh connectivity, including vertices, edges, and cell centroids, which complicates otherwise straightforward visualization tasks. As a result, rapid inspection and exploratory analysis of MPAS-A outputs can become time-consuming and technically demanding.

### Example workflows

Several notebooks with the following structure can be found in the notebooks directory:

## Running the Notebooks

You can either run the notebooks in the Cookbook using [Binder](https://binder.projectpythia.org/) or on your local machine.

### Running on Binder

The simplest way to interact with a Jupyter Notebook is through
[Binder](https://binder.projectpythia.org/), which enables "one click"
execution in the cloud. Simply navigate your mouse to
the top right corner of the book chapter you are viewing and click
on the rocket ship icon (see screenshots [here](https://foundations.projectpythia.org/preamble/how-to-use/#running-pythia-foundations-examples)),
and a text box will appear. Type or paste the Pythia Binder link
(`https://binder.projectpythia.org`) and click "Launch".
After a few moments you should be presented with a
notebook that you can interact with. You’ll be able to execute code
and even change the example programs. At first the code cells
have no output, until you execute them by pressing
{kbd}`Shift`\+{kbd}`Enter`. Complete details on how to interact with
a live Jupyter notebook are described in the Pythia Foundations chapter [Getting Started with
Jupyter](https://foundations.projectpythia.org/foundations/getting-started-jupyter).

Note, not all Cookbook chapters are executable. If you do not see
the rocket ship icon, such as on this page, you are not viewing an
executable book chapter.


### Running on Your Own Machine

If you are interested in running this material locally on your computer, you will need to follow this workflow:

(Replace "cookbook-example" with the title of your cookbooks)

1. Clone the `https://github.com/ProjectPythia/cookbook-example` repository:

   ```bash
    git clone https://github.com/ProjectPythia/cookbook-example.git
   ```

1. Move into the `cookbook-example` directory
   ```bash
   cd cookbook-example
   ```
1. Create and activate your conda environment from the `environment.yml` file
   ```bash
   conda env create -f environment.yml
   conda activate cookbook-example
   ```
1. Move into the `notebooks` directory and start up Jupyterlab
   ```bash
   cd notebooks/
   jupyter lab
   ```
