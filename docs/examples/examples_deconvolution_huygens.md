# Deconvolution with Huygens Pro

## Overview
 
In this tutorial we will show you how to restore an image using deconvolution methods with the commercial tool [Huygens Profesional](https://svi.nl/Huygens-Professional) from Scientific Volume Imaging ([SVI](https://svi.nl/HomePage)). As dataset, we will be using a 3D stack image example that consist of Actin filaments of HeLa cell stained with a fluorescent probe and acquired with a confocal microscopy. This dataset has kindly being provided by Dr. Diego Morone from the Università della Svizzera italiana.


## Login
In order to use Huygens remote manager, you need to have a valid license. If you have a license and an active account, please introduce it in this step. If you need one license or want to test Huygens for restoration and deconvolution of your image dataset, please get in touch with the [MIC](https://www.mic.unibe.ch/) for support or [Yury Belyaev](mailto:info.mic@unibe.ch). After login, Huygens will check your system and if it finds a GPU it will need a few minutes to initialize the cards.

![huygens_full_workflow](../assets/images/huygens_login_screenshot.png) 

## Open dataset
VIBE, as a service hosted by UBELIX, uses similar [data storage scheme](https://hpc-unibe-ch.github.io/storage/) and offers connectivity for their user to the Research Storage by default. Read more about [data transfer and storage documentation](../how-to-guides/data-management.md) or get in touch with the [ Dienstleistungen der Informatikdienste](https://intern.unibe.ch/dienstleistungen/informatik/dienstleistungen_der_informatikdienste/dienstleistungen___ressourcen/research_storage/index_ger.html) to request a Research Storage quota for your project. 


The dataset that we are going to use for this workflow is currently living somewhere at the `$HOME` directory of the current UBELIX session in use. Let's open the dataset by just drag and drop our image to the main application windows. Huygens is a very versatile software with a wide range of functionalities that won't be covered in this workflow. Feel free to look at the official documentation and watch the multiples tutorials and learning material in the [SVI website](https://svi.nl/HomePage). 

![open_dataset](../assets/images/huygens_open_dataset.png)


## Adjust microscopy settings
Make sure that the metadata from your image is correct. To check the metadata, right click on the image and select "Microscopic Parameters". It will display the microscopy parameters stored in the current image. Check them carefully and modify any missing parameter accordingly and accept the changes.

![open_dataset](../assets/images/huygens_set_microscopy_paramteres.png)

## Launch the Deconvolution Wizard
Click on the deconvolution wizard to start the deconvolution operation on your image. Navigate the wizard and change the parameters accordingly. For this image we will use the default settings. The deconvolution calculation for this image is fairly quick. However depending of the size of your image, number of channels, size of stack, etc, the deconvolution time may take longer. If you have doubt about how to  deconvolve your images please get in touch with the MIC for technical support.

![open_dataset](../assets/images/huygens_deconvolution_wizard.png)

## Quick 2D visualization
Once finished, the deconvolution wizard will display the resulting deconvolved image next to the original image to visualize the changes, thus helping the user to decide if the deconvolution operation was successful or if you need to modify your parameters and re-run it again. 

![quick_2d_visualization](../assets/images/huygens_quick_2d_visualizazton.png)


## 3D visualization
We can explore further the resulting image via 3D visualization. In the main window, select the two images and click on the tab "Visualization". Go to "Visualization 3D" and select "Twint MIP". This will display the [maximum intensity projection](https://svi.nl/MaxIntensityProjection) (MIP) of the two images in a new window. Sync the vies and readjust contrast or any other parameter to inspect in detail your image. 

![32_visualization](../assets/images/huygens_3d_visulization.png)

## Full workflow

The complete workflow from beginning to end can be visualized here:

<video controls loop muted autoplay>
 <source src="../assets/videos/huygens_workflow_video.mp4" type="video/mp4">
</video>


### Acknowledgment

- Dr. Yury Beliaev: For his valuable technical expertise on image restoration and deconvolution.
- Dr. Diego Morone: For kindly providing the dataset.
