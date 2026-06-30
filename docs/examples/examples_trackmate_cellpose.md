# Cell tracking using Trackmate + Cellpose

## Overview

In this example, we will try to track cells from a challenging dataset. This data sample consist of collective cell migration from Glioblastoma-astrocytoma [^1]. The sample here was imaged using bright-field microscopy and expose complex shape and changes in contrast along the time series. This example is from the Trackmate Fiji Plugin and you can read more about the original workflow [here](https://imagej.net/plugins/trackmate/detectors/trackmate-cellpose#tracking-cells-stained-for-cytoplam-with-cellpose).

Our final goal is to successfully segment and track these cells. First we will try to use the default segmentation selector from Trackmate and asses the quality of the segmentation. Then, we will train our custom deep learning model using cellpose and SAM[^2][^3][^4][^5]. Finally we will use oru custom model to run the segmentation step within trackmate and further run the tracking of the cells.

Let's get started.


## Open and visualize the dataset

### Download the dataset

- Launch your VIBE session.
- Open the browser and download the dataset for this tutorial from zenodo using this [link](https://doi.org/10.5281/zenodo.5863317).
- Create a folder for this project and save your dataset there.
- Try to decompress your dataset using the peaZip utility. You will find it in the VIBE desktop menu under `Applications > VIBE > VIBE Applications > peaZip`.

### Visualize the dataset

- Open the Fiji-Trackmate application via: `Applications > VIBE > VIBE Applications > fiji > fiji (fiji-trackmate-20260601) [VIBE]`
- Drag and drop the file named `Glioblastoma_brightfield.tif` to the fiji application.
- Explore the image: look at the bit depth, image size, dimensions, etc.

<video controls loop muted autoplay>
 <source src="../assets/videos/preview_glioblastoma.webm" type="video/webm">
</video>


## Running Trackmate on samples


## Pick sample images for training


## Open training images and interact with cellpose


## Correct annotations and train the custom model


## Export model


## Re-run Trackmate with custom model and asses results



## Export video of tracks

















[^1]: Guillaume Jacquemet, Joanna W. Pylvänäinen, & Jean-Yves Tinevez. (2022). Tracking Glioblastoma-astrocytoma cells imaged in brightfield with TrackMate-Cellpose [Data set]. Zenodo. [https://doi.org/10.5281/zenodo.5863317](https://doi.org/10.5281/zenodo.5863317)

[^2]: Pachitariu, M., Rariden, M., & Stringer, C. (2025). Cellpose-SAM: superhuman generalization for cellular segmentation. bioRxiv.

[^3]: Stringer, C., Wang, T., Michaelos, M., & Pachitariu, M. (2021). Cellpose: a generalist algorithm for cellular segmentation. Nature methods, 18(1), 100-106.

[^4]: Pachitariu, M. & Stringer, C. (2022). Cellpose 2.0: how to train your own model. Nature methods, 1-8.

[^5]: Stringer, C. & Pachitariu, M. (2025). Cellpose3: one-click image restoration for improved segmentation. Nature Methods.