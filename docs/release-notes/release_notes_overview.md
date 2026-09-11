# Release Notes Overview

VIBE Desktop adheres to the FAIR principles: the source code is freely available for reproducibility and reuse by other imaging platforms, the research community, and the general public.

This page summarizes the technical structure of the VIBE source code — repository locations, versioning scheme, and archival records.

## Repositories

VIBE Desktop is built on two main repositories:

- [**vibe-desktop**](https://github.com/dsl-unibe-ch/vibe-desktop) — the Open OnDemand app (form, submit, and session scripts)
- [**vibe-applications**](https://github.com/dsl-unibe-ch/vibe-applications) — Apptainer container definitions for all applications

## Versioning

Both repositories share the same release tag. Since vibe-applications changes more frequently — driven by new feature requests, application fixes, and updates — every release published in either repository triggers an identical version tag in the other. This guarantees that a given tag always identifies a consistent, matched pair of desktop and application releases.

## Archival (Zenodo)

| Repository | DOI |
| --- | --- |
| vibe-desktop | [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22096552.svg)](https://doi.org/10.5281/zenodo.22096552) |
| vibe-applications | [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22096511.svg)](https://doi.org/10.5281/zenodo.22096511) |