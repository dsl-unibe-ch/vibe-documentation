# Deconvolution with Huygens Pro


# outline/content

## Intro
Description what we want to achieve, what the dataset consist and what operations and tools we use. (TO BE DONE)
- **Login** In order to use Huygens remote manager, you need have an active license. If you have a license and an active account, please introduce it in this step. If you need one license or want to test Huygens for restauration and deconvolution of your image dataset, please get in touch with the [MIC](https://www.mic.unibe.ch/) for support or [Yury Belyaev](mailto:info.mic@unibe.ch). After login, Huygens will check your system and if it finds a GPU it will need a few minutes to initialize the cards.

![huygens_full_workflow](../assets/images/huygens_login_screenshot.png) 

## Open dataset
Let's open the dataset by just drag and drop our image to the main windows. Huygens is a very versatile software with a wide range of functionalities that won't be covered in this workflow. Feel free to look at the official documentation and watch the multiples tutorials and learning material in the [SVI website](https://svi.nl/HomePage). 

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
We can explore further the resulting image via 3D visualization. In the main window, select the two images and click on the tab "Visualization". Go to "Visulaization 3D" and select "Twint MIP". This will display the [maximum intensity projection](https://svi.nl/MaxIntensityProjection) (MIP) of the two images in a new window. Sync the vies and readjust contrast or any other parameter to inspect in detail your image. 

![32_visualization](../assets/images/huygens_3d_visulization.png)

The complete workflow can be visualized here:


![huygens_full_workflow](../assets/videos/huygens_full_workshop.webm)


### Acknowledgment

This workflow example was kindly provided by Yury Belyaev, and ...
