# Cell segmentation and tracking 

## Overview

In this example, we demonstrate how to use **microSAM**[^1] with napari in combination with the **TrackMate**[^2] Fiji plugin to track cell migration. The dataset consists of time-lapse fluorescence images of MDA-MB-231 cells expressing an ERK activity reporter, acquired using a widefield fluorescence microscope[^3].

We use the DAPI staining channel as a reference for cell tracking. microSAM is employed to segment the cell nuclei, and the resulting labeled nuclei are subsequently used as input for tracking cell trajectories with TrackMate in Fiji. Between these steps, several preprocessing operations are performed, including splitting and merging image channels.


## Visualize and split channels

We will launch the standard Fiji program to visualize and split the channels of the image. Go to the Applications menu on the top left of the window and navigate to **VIBE -> VIBE applications -> fiji** and click on the Fiji-base application. this will launch the application. A terminal window will show that the launching of the application is in process. Wait few seconds until the Application GUI appears. 

![](../assets/images/fiji_menu.png) 

The image that we are going to use is in a folder located at the desktop of the current session in use. Drag and drop the image to visualize it in Fiji.

<video controls loop muted autoplay>
 <source src="../assets/videos/display_cells_in_motion.webm" type="video/webm">
</video>

In Fiji, go to **Image -> Colors -> Split Channels** to separate each the channels. Save each channel separately. We will use in the next step the channel containing the nuclei staining for segmentation.


## Launch napari and micro-SAM

Let's open napari and use the napari-microSAM plugin to segment the nuclei. Find Napari by navigating again the applications menu on **VIBE -> VIBE applications -> napari** and click on **napari-microSAM-1.6.2**. Open the second  image that contains the stained nuclei (DAPI) and launch the plugin by going to **Plugins -> Segment anything for Microscopy -> Annotator 3D**.


## Adjust setting and segment the cells.

microSAM has number of settings that can be tuned for optimal segmentation. In addition, microSAM needs to compute image embeddings in order to make predictions. For our example we will use default settings, which yields to acceptable results for our example. Feel free to explore and experiment with further parameters for your own images and find deeper explanation on what are these parameters and how to use them in the official [microSAM documentation](https://computational-cell-analytics.github.io/micro-sam/micro_sam.html). 

So let's dive slowly into the basic configuration needed to make our segmentation.

- **Select the image layer you want ot segment**. In our case, is taken by default since is the only image we have open.
- **Select the model "light Microscopy"**
- **Compute embeddings**. Open the "Embeddings Settings" menu and adjust the settings as shown below accordingly.
    - **Select model size: "base"**.
    - **Select device: cuda.**
    - **Click on "Compute Embeddings"**. Wait a few moments until the computations ends.

![](../assets/images/microSAM_settings.png) 

Once adjusted the basic settings, go to the menu for automatic segmentation and **select "apply to volume"** and finally **click on the "Automatic Segmentation"** button. This step may take few minutes to complete. You can follow the progress using the activity progress bar from napari at the button right corner of the window. 

<video controls loop muted autoplay>
 <source src="../assets/videos/segmentation_progress.webm" type="video/webm">
</video>

## Merge annotation label with the image

Save the layer "auto_segmentation". This image containing the mask with the segmentation of the cells that we are going to need for our next step using Trackmate. Use Fiji and open the individual channels previously saved as well as the mask with the labels generated using microSAM. 

From Fiji, combine the three images by navigating to **Image -> Color -> Merge Channels** and saved it.

## Track cells with trackmate

With our last image opened in Fiji, launch TrackMate by navigating to **Plugins -> Tracking -> TrackMate**.

![](../assets/images/trackmate_in_fiji.png)

## Adjust trackmate settings

Navigate the Trackmate wizard to adjust the settings for basic object tracking. 

- TrackMate can read some metadata and adjust some images settings for you, for instance the calibration settings in this examples are taking by default from the image. 
- click next and use "mask detector", then select the channel that contain the mask. In our case is the channel 3, which is already detected. Click pthe preview button to check the contours of the segmentation.
- click next to see a first preview of the objects detected. 
- click next and select the tracker. There are a number of trackers that you can potentially use. Let's use the default "LAP tracker" and continue to the next step.
- in the LAP tracker settings, use the default 20 µm as a "frame to frame linking distance" and "track segment splitting" and click next.
- the tracking lines for each object detected will appear now as displayed bellow.

![](../assets/images/tracking_lines.png)

## Visualize results

What we observe above are the trajectories linked to each ROI that has been detected and tracked based on our simple parameters. The color represent the index of the tracks. Noted that despite having a pretty descent detection and tracking results with the default settings, this results can be further tuned by applying filters, using a different tracker algorithm, adjusting the linking distance. However, this goues beyound the scope of this demostration and for the propose of this demonstration this should suffice. 

As a last step, lets try to adjust the visualization of the tracks by adjusting the draw tracks layout. This will help to visualoze less corwed draws and focus better on the trajectories of single spots or cells.

- In the present window, select "edit settings". 
- In the "Track" section go to "track display mode" and select the option "show tracks backward in time".
- Optionally, you can change the "track display max", which will result in the length of the draw track display in the animation. in this case is 10 time-points length distance. Close the windows and click next.
- Select the option "Capture overlay" to create a new image with the track overlay on the original image with the current display settings.
- Click "Execute" and accept the options. A new image will be created that capture the draw tracks. You can export this image for presentation, etc.

<video controls loop muted autoplay>
 <source src="../assets/videos/visualize_tracks.webm" type="video/webm">
</video>

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