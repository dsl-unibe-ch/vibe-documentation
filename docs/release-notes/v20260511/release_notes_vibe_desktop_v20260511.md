# VIBE Desktop 20260615 — First Public Release

**Release Date**: June 2026
**Repository**: vibe desktop
**Tag**: v20260615

We are excited to announce the first official release of VIBE Desktop, a web based virtual research workstation that provides seamless access to scientific software, image analysis tools, interactive computing environments, and high performance computing resources through a unified desktop experience.

Developed by the Data Science Lab (DSL) and the Microscopy Imaging Center (MIC) at the University of Bern, VIBE Desktop enables researchers to launch powerful analysis applications directly from their browser while leveraging the computational capabilities of the UBELIX HPC infrastructure.

## Browser Based Research Environment

VIBE Desktop delivers a complete Linux desktop environment accessible through a web browser, eliminating the need for complex local software installations while providing a consistent user experience across devices and operating systems.

Key benefits include:

- No local installation required
- Persistent research environment
- Access from any modern web browser
- Centralized software management
- Integration with institutional computing resources

## HPC Powered Scientific Computing

Researchers can seamlessly utilize the computational resources of the University of Bern HPC infrastructure directly from the desktop environment.

Features include:

- GPU enabled applications
- Large memory compute resources
- Centralized data storage
- Interactive and batch processing workflows
- Scalable analysis pipelines

## Versioning and Release Tagging

Starting with this release, the vibe desktop and vibe applications repositories are bound by a shared release tag. Although the two repositories may develop at a different pace, since the vibe applications repository is expected to change more frequently to accommodate new feature requests, application fixes, and updates, every new release published in either repository triggers an identical version tag in the other. This ensures that a given tag always identifies a consistent, matched pair of desktop and application releases.

This first joint release is tagged v20260615 in both the vibe desktop and vibe applications repositories.

## Usage

This repository contains all relevant information to create the containerized desktop running on OpenOnDemand. It also contains scripts to build and deploy the application containers defined in the vibe applications repository.

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

VIBE Desktop is designed for researchers working in:

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

This first public release establishes the foundation of the VIBE ecosystem. Future releases will continue to expand the application catalog, improve user experience, introduce additional GPU enabled workflows, and provide deeper integration with reproducible scientific computing practices. Each future release will keep the vibe desktop and vibe applications repositories aligned under the same version tag.

VIBE Desktop v20260615 brings modern scientific computing, advanced image analysis, and HPC powered research workflows together in a single browser accessible platform, enabling researchers to focus on science rather than software installation and infrastructure management.

## License

BSD 3 Clause

Developed by the Data Science Lab (DSL) and Microscopy Imaging Center (MIC), University of Bern.