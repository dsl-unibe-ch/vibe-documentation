# Cell segmentation and tracking 

# outline/content

- **Intro**: description what we want to achieve, what the dataset consist and what operations and tools we use.

In this simple workflow, we will be showing how to use microSAM (link plus source) in combination with Trackmate Fiji (link plus source) plugin to track cell migration. The dataset consist of fluorescent images of  MDA-MB-231 cells expressing and labeled against ERK activity and live recorded  using a widefield fluorescence microscope [1, 2].

- **open and visualize** dataset -> Napari (base)
- **split channels** and save them in separate files -> Fiji
- reopen the channel containing the cell nucleus staining (DAPI) with **Napari micro-SAM**
- Adjust the setting for **automatic segmentation.**
- **segment** the cells.
- **save the resulting mask** (annotation) as an image
- in fiji, **merge the resulting mask** with the original 2 channels image .
- 

### Resources 
1. https://zenodo.org/records/5205955
2. https://www.nature.com/articles/s41592-022-01507-1 