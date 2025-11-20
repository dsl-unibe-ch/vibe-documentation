# Cell segmentation and tracking 

# outline/content

- **Intro**: description what we want to achieve, what the dataset consist and what operations and tools we use.
- **open and visualize** dataset -> Napari (base)
- **split channels** and save them in separate files -> Fiji
- reopen the channel containing the cell nucleus staining (DAPI) with **Napari micro-SAM**
- Adjust the setting for **automatic segmentation.**
- **segment** the cells.
- **save the resulting mask** (annotation) as an image
- in fiji, **merge the resulting mask** with the original 2 channels image .
- 

