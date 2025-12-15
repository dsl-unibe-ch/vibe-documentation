# Cell segmentation and tracking 

## Overview

In this example we will be showing how to use **microSAM**[^1] with napari in combination with **Trackmate**[^2] Fiji plugin to track cell migration. The dataset consist of fluorescent images of MDA-MB-231 cells expressing and labeled against ERK activity and live recorded using a widefield fluorescence microscope[^3].

## **open and visualize** 
dataset -> Napari (base)
## **split channels** 
and save them in separate files -> Fiji
## reopen the channel containing the cell nucleus staining (DAPI) with **Napari micro-SAM**
## Adjust the setting for **automatic segmentation.**
## **segment** the cells.
## **save the resulting mask** (annotation) as an image
## in fiji, **merge the resulting mask** with the original 2 channels image .
- 

### Acknowledge

### Resources 

[^1]: Archit, A., Freckmann, L., Nair, S. et al. Segment Anything for Microscopy. Nat Methods 22, 579–591 (2025). [https://doi.org/10.1038/s41592-024-02580-4](https://doi.org/10.1038/s41592-024-02580-4)
[^2]: Ershov, D., Phan, MS., Pylvänäinen, J.W. et al. TrackMate 7: integrating state-of-the-art segmentation algorithms into tracking pipelines. Nat Methods 19, 829–832 (2022). [https://doi.org/10.1038/s41592-022-01507-1](https://doi.org/10.1038/s41592-022-01507-1)
[^3]: Jean-Yves Tinevez, & Joanna W. Pylvänäinen. (2021). Cell migration with ERK signalling [Data set]. Zenodo. [https://doi.org/10.5281/zenodo.5205955](https://doi.org/10.5281/zenodo.5205955)