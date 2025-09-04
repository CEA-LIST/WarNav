
# WarNav dataset

This repository constitutes the WarNav dataset, made of annotations of selected subsets of images provided by the open-source [DATTALION](https://dattalion.com/) multimedia repository. 
WarNav is specifically tailored to enable the development and benchmarking of semantic segmentation models for autonomous ground vehicles in unstructured, conflict-affected environments.



## Dataset contents

The following is provided in [Google Drive](https://drive.google.com/drive/folders/1H5tCksnuxfF5QYqGOAwvfgn6K0NOc4vL?usp=sharing):
 - 3 files providing the names of pictures selected from Dattalion. One file is given per dataset split (training, validation and test sets).
    - train_dataset_selection.txt (5354 image names)
    - validation_dataset_selection.txt (100 image names)
    - test_dataset_selection.txt (100 image names)
 - Validation and test annotation, in [Cityscape format](https://docs.cvat.ai/docs/manual/advanced/formats/format-cityscapes/)
    - Validation_annotation
    - Test_annotation

Among the 100 validation dataset images, 3 images do not contain any pixel of the classes of interest. Thus, annotation of validation set provides information for the 97 images which have at least 1 pixel of a class of interest.

The Test_annotation provides a single annotation for 90 images, and redundant annotations given by 3 different annotators for 10 additional images. For performance evaluation, the annotations of Annotator 2 are used.

Annotated classes of interest are the following:
* Overlay: Regions containing graphical overlays or annotations that were added post-capture. These pixels are excluded from both training and performance evaluation, as they do not correspond to real-world scene contents.
* Road: Surfaces intended for civilian vehicular traffic, typically paved with asphalt or similar materials.
* Drivable: Areas that are not formal roads but are deemed traversable by military 4x4 vehicles (e.g., dirt paths, open fields).
* Pedestrian: Humans. Accurate detection of this class is essential for tasks related to safe autonomous navigation.
* Vehicle: Civilian vehicles that are potentially operable. Obstacle avoidance algorithms would consider them as potentially non static obstacles. Damaged or abandoned car wrecks are excluded from this category.
* Background: All non-annotated regions are classified as background, encompassing areas where navigation is not feasible (e.g., buildings, vegetation, sky, rubble, or other obstacles).



## Licence

Data annotations are under Creative Commons Attribution Non Commercial 4.0 license.



## Citation

Associated paper can be read here (to be filled later).
