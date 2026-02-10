# Cell segmentation and tracking 

## Overview

In this example, we demonstrate how to use **microSAM**[^1] with napari in combination with the **TrackMate**[^2] Fiji plugin to track cell migration. The dataset consists of time-lapse fluorescence images of MDA-MB-231 cells expressing an ERK activity reporter, acquired using a widefield fluorescence microscope[^3].

We use the DAPI staining channel as a reference for cell tracking. microSAM is employed to segment the cell nuclei, and the resulting labeled nuclei are subsequently used as input for tracking cell trajectories with TrackMate in Fiji. Between these steps, several preprocessing operations are performed, including splitting and merging image channels.


## Visualize and split channels

We will launch the standard Fiji program to visualize and split the channels of the image. Go to the Applications menu on the top left of the window and navigate to **VIBE -> VIBE applications -> fiji** and click on the Fiji-base application. this will launch the application. A terminal window will show that the launching of the application is in process. Wait few seconds until the Application GUI appears. 

!!! note
    place screenshot of application menu, highlighting Fiji location

The image that we are going to use is in a folder located at the desktop of the current session in use. Drag and drop the image to visualize it in Fiji.

!!! note
    place screenshot/video of the raw image displaying cell in motion.

In Fiji, go to **Image -> Colors -> Split Channels** to separate each of the two channels of the image and save them.


## Launch napari and micro-SAM

We will open the DAPI channel with napari and use the napari-microSAM plugin to segment the nuclei. Let's find Napari by navigating again the applications menu on **VIBE -> VIBE applications -> napari** and click on **napari-microSAM-1.6.2**. Open the second  image that contains the stained nuclei (DAPI) and launch the plugin by going to **Plugins -> Segment anything for Microscopy -> Annotator 3D**.


## Adjust setting and segment the cells.

!!! note
    place screenshot/video of setting being adjusted in microSAM.

## **export the resulting mask** (annotation) as an image

## in fiji, **merge the resulting mask** with the original 2 channels image

## Track cells with trackmate

## adjust trackmate settings

## visualize results

## Full workflow

The complete workflow from beginning to end can be visualized here:

<video controls loop muted autoplay>
 <source src="../assets/videos/usam_trackmate_tutorial_60fps_crf55.webm" type="video/webm">
</video>



### Acknowledge

### Resources 

[^1]: Archit, A., Freckmann, L., Nair, S. et al. Segment Anything for Microscopy. Nat Methods 22, 579–591 (2025). [https://doi.org/10.1038/s41592-024-02580-4](https://doi.org/10.1038/s41592-024-02580-4)
[^2]: Ershov, D., Phan, MS., Pylvänäinen, J.W. et al. TrackMate 7: integrating state-of-the-art segmentation algorithms into tracking pipelines. Nat Methods 19, 829–832 (2022). [https://doi.org/10.1038/s41592-022-01507-1](https://doi.org/10.1038/s41592-022-01507-1)
[^3]: Jean-Yves Tinevez, & Joanna W. Pylvänäinen. (2021). Cell migration with ERK signalling [Data set]. Zenodo. [https://doi.org/10.5281/zenodo.5205955](https://doi.org/10.5281/zenodo.5205955)