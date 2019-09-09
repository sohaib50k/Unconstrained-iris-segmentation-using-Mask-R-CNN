# Iris segmentation using Mask-R-CNN
Unconstrained iris segmentation using Mask R-CNN

This repository borrows heavily from the Matterport implementation of mask r-cnn. 

The code uploaded is kept similar to the matterport implementation for ease of upgrading the implementation.

The matterport implementation can be found here: https://github.com/matterport/Mask_RCNN so all the packages need to be installed.

For starters the implementation uses Keras and Tensorflow, other needed packages include numpy, opencv, matplotlib among others.

# Training process 
We use ground truths by Hofbauer et al. for the NotreDame 0405, Casia v3, IITD and Ubiris v2 datasets.
The iris datasets need to be in specific formats for the trainDataset file.
Folder format:

* Train
  * iris -> Iris images here
  * mask -> Mask images here
  

Likewise for validation and testing datasets.

Download the MS COCO trained weights (from the matterport implementation) to speed up the training process otherwise the model can be trained from scratch.

You can use the trained model with the inferFolder script.

# Testing process
Download the pre-trained models from the given google drive link or train your own model on your dataset by following the instructions above.

Put all test images in a folder and your models in the weights folder. Change the weights location and the location to the folder where you want to infer images.

The inferFolder script will save the segmented images in a new folder called segmented with the same filenames as the input file names.

If you use this repository consider citing our paper and the [ matterport implementation ](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

``` @inproceedings{ahmad2018unconstrained,
  title={Unconstrained Iris Segmentation Using Convolutional Neural Networks},
  author={Ahmad, Sohaib and Fuller, Benjamin},
  booktitle={Asian Conference on Computer Vision},
  pages={450--466},
  year={2018},
  organization={Springer}
}
```
