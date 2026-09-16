# VIBE Applications v20260915

**Release Date**: September 2026

**Repository**: vibe applications

**Tag**: v20260915

## Release summary

This is a major release adding support for a few new applications (ChimeraX, VS Code) and adding major updates to some others such as Deep Learning-based image analysis tools in Fiji. This release also makes use of pixi instead of conda for multiple Python-based applications.

For details see the notes below.

## New applications

- **ChimeraX 1.12.1**
- **VS Code 1.130.0**
- **MATLAB r2026a**

## New versions of existing applications

- **Cellpose GUI 4.2.1.1**: This version supports cpsam_v2 models.
- **Cellpose GUI 3.1.1.3**: This version supports old style cellpose3 type of models.
- **Fiji base 20260611**: This new version now includes support for multiple deep learning-based image analysis tools such as SAMJ.
- **Fiji TrackMate 20260601**: This version of Fiji includes support for TrackMate8 and its deep learning extensions such as Trackmate-Cellpose.
- **napari base 0.7.0**: This version offers napari 0.7.0.
- **napari base 0.9.1**: This version offers napari 0.9.1.
- **napari StarDist 2024.8.6.1v2**: Technical improvements e.g. adding compatibility with Blackwell architecture.
- **QuPath extensions 0.6.0v2**: Technical improvements to make pre-installed extensions readily available to users.
- **IMOD collection 5.1.10**: Addition of subtools such as etomo and CLI.

## Modified in place

- **`napari/napari-microSAM-1.7.5`**: Update to pixi.
- **`firefox/firefox-base-latest`**: Improved default configuration by updating enterprise policies and adding managed bookmarks for the VIBE homepage and documentation.

## Archived

Superseded versions moved out of the active tree:

- `cellpose/cellpose-gui-4.0.8` → `archive/cellpose/`
- `fiji/fiji-base-2.17.0` → `archive/fiji/`
- `napari/napari-base-0.6.4` → `archive/napari/`
- `napari/napari-stardist-2024.8.6.1` → `archive/napari/`
- `qupath/qupath-extensions-0.6.0` → `archive/qupath/`


## Application catalogue

All applications currently in the active tree after this release, grouped by their `Category` label. Applications carrying several category labels are listed under the first one, with the full label set noted. "Provides" lists the `Application` label, i.e. the launchers the container exposes.

### segmentation

- **Cellpose GUI 4.2.1.1**: provides cellpose, jupyterlab
- **Cellpose GUI 3.1.1.3**: provides cellpose, jupyterlab
- **ilastik 1.4.1.post1**: provides ilastik
- **napari CAREamics 0.0.20**: provides napari, jupyterlab
- **napari Convpaint 0.8.2**: provides napari, jupyterlab, python
- **napari empanada 1.2**: provides napari
- **napari microSAM 1.7.5**: provides napari, jupyterlab
- **napari nnInteractive 1.0.6**: provides napari, jupyterlab
- **napari Spotiflow 0.4.4**: provides napari, jupyterlab, python
- **napari StarDist 2024.8.6.1_1**: provides napari, jupyterlab, python
- **QuPath extensions 0.6.0v2**: provides qupath

### image-processing

- **ChimeraX 1.12.1** *(also cryoEM, structural-biology)*: provides chimerax
- **Fiji base 20260611**: provides fiji
- **Fiji TrackMate 20260601**: provides fiji
- **IMOD collection 5.1.10** *(also cryoEM)*: provides imod, etomo, cli
- **Hlushchuk lab — laminitis 20250724**: provides jupyterlab, python
- **JupyterLab + vedo 2026.6.1**: provides jupyterlab, vedo, python
- **Meister lab — point analysis 20250702**: provides python, jupyterlab
- **Pertz lab — ARCOS 20250820**: provides jupyterlab, python
- **napari base 0.7.0**: provides napari, jupyterlab, python
- **napari base 0.9.1**: provides napari, jupyterlab, python

### denoising

- **Huygens 26.04.0-p2**: provides huygens
- **Meister lab — denoise 20250702**: provides python, jupyterlab
- **Noise2Void 1.0**: provides python, jupyterlab

### tracking

- **napari Trackastra 0.2.1**: provides napari, jupyterlab, python

### high-content

- **CellProfiler 4.2.8**: provides cellprofiler

### coding

- **VS Code 1.130.0**: provides vscode

### browser

- **Firefox (latest)**: provides firefox

## Versioning and Release Tagging

The vibe applications repository is bound to the same release tag as the vibe desktop repository. Because vibe applications is expected to change at a faster pace than vibe desktop, driven by new feature requests, application fixes, and updates, every new release published in either repository triggers an identical version tag in the other. This guarantees that a given tag always identifies a consistent, matched pair of desktop and application releases.

## Usage

This repository contains the Apptainer definition files used to build and deploy all application containers available in VIBE Desktop, running on OpenOnDemand.