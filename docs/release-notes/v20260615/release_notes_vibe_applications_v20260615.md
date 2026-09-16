# VIBE Applications v20260615 — First Public Release

**Release Date**: May 2026

**Repository**: vibe applications

**Tag**: v20260615

We are excited to announce the first official release of the VIBE Applications repository, containing the full catalog of Apptainer container definitions that power the VIBE Desktop virtual research workstation.

Developed by the Data Science Lab (DSL) and the Microscopy Imaging Center (MIC) at the University of Bern, this repository provides the scientific software, image analysis tools, and interactive computing environments that researchers launch through VIBE Desktop, leveraging the computational capabilities of the UBELIX HPC infrastructure.

## Versioning and Release Tagging

The vibe applications repository is bound to the same release tag as the vibe desktop repository. Because vibe applications is expected to change at a faster pace than vibe desktop, driven by new feature requests, application fixes, and updates, every new release published in either repository triggers an identical version tag in the other. This guarantees that a given tag always identifies a consistent, matched pair of desktop and application releases.

This first joint release is tagged v20260615 in both the vibe applications and vibe desktop repositories.

## Usage

This repository contains the Apptainer definition files used to build and deploy all application containers available in VIBE Desktop, running on OpenOnDemand.

## Application Catalog

The first public release ships the following applications and versions.

### General Tools

| Application | Version      |
| ----------- | ------------ |
| Firefox     | base, latest |

### Image Analysis and Segmentation

| Application  | Version          |
| ------------ | ---------------- |
| Cellpose     | GUI 4.0.8        |
| Fiji         | base 2.17.0      |
| CellProfiler | base 4.2.8       |
| ilastik      | base 1.4.1.post1 |
| QuPath       | extensions 0.6.0 |
| IMOD         | base 5.1.10      |

### Napari Plugins

| Application          | Version    |
| --------------------- | ---------- |
| napari               | base 0.6.4 |
| napari nninteractive | 1.0.6      |
| napari trackastra    | 0.2.1      |
| napari convpaint     | 0.8.2      |
| napari spotiflow     | 0.4.4      |
| napari empanada      | 1.2        |
| napari careamics     | 0.0.20     |
| napari stardist      | 2024.8.6.1 |
| napari microSAM      | 1.7.5      |

### Deconvolution

| Application | Version         |
| ----------- | --------------- |
| Huygens     | base 26.04.0 p2 |

### Python and Denoising

| Application | Version |
| ----------- | ------- |
| Python n2v  | 1.0     |

### JupyterLab Environments

| Application     | Version  |
| --------------- | -------- |
| jupyterlab vedo | 2026.6.1 |

### Research Lab Environments

Customized JupyterLab images contributed by individual research labs, bundling lab specific dependencies and workflows alongside the shared VIBE base environment.

| Application              | Version  |
| ------------------------- | -------- |
| hlushchuklab laminitis   | 20250724 |
| pertzlab ARCOS           | 20250820 |
| meisterlab denoise       | 20250702 |
| meisterlab pointanalysis | 20250702 |

## Infrastructure Repositories

| Repository        | Role                                                        |
| ------------------ | ----------------------------------------------------------- |
| vibe desktop      | Open OnDemand app: form, submit, and session scripts       |
| vibe applications | Apptainer definition files for all application containers  |
| vibe utilities    | Autobuild scripts for UBELIX; logo assets                  |

## Documentation

Full user documentation is available at vibe documentation, covering:

- Quick start guide
- Resource allocation guidance
- Data management
- Worked examples (cell tracking, deconvolution with Huygens)
- Launching applications from the terminal
- Known limitations and FAQ

## Target Users

VIBE Applications is designed for researchers working in:

- Biomedical sciences
- Cell biology
- Microscopy
- Bioimage analysis
- Structural biology
- Digital pathology
- Computational biology
- Data science
- Machine learning
- Scientific visualization

## Looking Ahead

This first public release establishes the foundation of the VIBE application catalog. Future releases will continue to expand the number of available applications, update existing containers, and introduce additional GPU enabled workflows. Each future release will keep the vibe applications and vibe desktop repositories aligned under the same version tag.

## License

BSD 3 Clause

Developed by the Data Science Lab (DSL) and Microscopy Imaging Center (MIC), University of Bern.