# VIBE Desktop 20260915

**Release Date**: September 2026

**Repository**: vibe desktop

**Tag**: v20260915

## Release summary

This release brings both infrastructure and application improvements: 

### Concurrent Connections

This release adds a fix for an issue preventing sessions from starting with many concurrent connections as typically experienced during courses or demos. Failures are caught upon launch and new sessions are automatically retried.

### Archived containers

When releasing new versions of the vibe-applications, old containers, are copied to an archive to preserve the option to access them (building is managed by the scripts of vibe-utilities). Even if no changes were made to the build files, new builds might slightly differ from the previous ones as e.g. linux package versions are not pinned. This release gives access to that archive by offering a VIBE archive entry in the VIBE menu.

### Warning message

The new release allows to display a warning message at session launch for important information such as maintenances of UBELIX that disrupt access to VIBE.

### New features

- peaZip: An application for unzipping.
- evince: A document viewer for PDF and other formats.
- The VIBE icon is now used to represent VIBE on OnDemand.


## Browser Based Research Environment

VIBE Desktop delivers a complete Linux desktop environment accessible through a web browser, eliminating the need for complex local software installations while providing a consistent user experience across devices and operating systems.

Key benefits include:

* No local installation required
* Persistent research environment
* Access from any modern web browser
* Centralized software management
* Integration with institutional computing resources

## HPC Powered Scientific Computing

Researchers can seamlessly utilize the computational resources of the University of Bern HPC infrastructure directly from the desktop environment.

Features include:

* GPU enabled applications
* Large memory compute resources
* Centralized data storage
* Interactive and batch processing workflows
* Scalable analysis pipelines

## Versioning and Release Tagging

Starting with this release, the vibe desktop and vibe applications repositories are bound by a shared release tag. Although the two repositories may develop at a different pace, since the vibe applications repository is expected to change more frequently to accommodate new feature requests, application fixes, and updates, every new release published in either repository triggers an identical version tag in the other. This ensures that a given tag always identifies a consistent, matched pair of desktop and application releases.

This first joint release is tagged v20260915 in both the vibe desktop and vibe applications repositories.

## Usage

This repository contains all relevant information to create the containerized desktop running on OpenOnDemand. It also contains scripts to build and deploy the application containers defined in the vibe applications repository.

## Infrastructure Repositories

| Repository | Role |
|---|---|
| vibe desktop | Open OnDemand app: form, submit, and session scripts |
| vibe applications | Apptainer definition files for all application containers |
| vibe utilities | Autobuild scripts for UBELIX; logo assets |

## Documentation

Full user documentation is available at vibe documentation, covering:

* Quick start guide
* Resource allocation guidance
* Data management
* Worked examples (cell tracking, deconvolution with Huygens)
* Launching applications from the terminal
* Known limitations and FAQ

## Target Users

VIBE Desktop is designed for researchers working in:

* Biomedical sciences
* Cell biology
* Microscopy
* Bioimage analysis
* Structural biology
* Digital pathology
* Computational biology
* Data science
* Machine learning
* Scientific visualization


## License

BSD 3 Clause

Developed by the Data Science Lab (DSL) and Microscopy Imaging Center (MIC), University of Bern.