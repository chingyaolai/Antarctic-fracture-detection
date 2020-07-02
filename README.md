# Antarctic fracture detection with U-Net
[![DOI](https://zenodo.org/badge/259829938.svg)](https://zenodo.org/badge/latestdoi/259829938)

We use **U-Net** to detect fracture locations from satellite imagery across Antarctica (125m-resolution MOA imagery (2009); [https://doi.org/10.7265/N5KP8037](https://doi.org/10.7265/N5KP8037)). Ice fractures result in the collapse of Antartctica ice-shelves, which can accelerate glacier flows into the ocean. We trained the U-Net with the labeled imagery, and applied the trained model to detect fracture across the Antarctic ice shelvse. In Fig. 1 the fracture/non-fracture locations are marked in white/black. 

The [Tensorflow U-Net](https://tf-unet.readthedocs.io/en/latest/installation.html) implementation was developed by Akeret et al. (2017) and available at [https://github.com/jakeret/tf_unet](https://github.com/jakeret/tf_unet). 

#### Fig. 1. Locations of the training/validation/testing data and continent-wide fracture predictions
![Frac](https://github.com/chingyaolai/Antarctic-fracture-detection/blob/master/images/dataloc.PNG)

<br/>

## File descriptions:
Input images and the corresponding labeled images are in the format of .tif. The filenames of the labeled images ends with "_mask.tif". The imput image is a grey-valued image with one channel. labeled images contains only two grey values corresponding to two two classes (fracture: 255 and non fractutre: 0).

- **data_trainset**: training data (26 1000x1000 pixel tiles, shown in blue in Fig. 1)

- **data_validset**: validation data (6 1000x1000 pixel tiles, shown in red in Fig. 1)

- **data_testset**: testing data (6 1000x1000 pixel tiles, shown in green in Fig. 1)

- **data_ross**: two extra images on the Ross ice shelf for visulization. One tile with fracture one without, the prediction of the fracture image is shown in Fig. 2.

- **Fracture_prediction_demo.ipynb**: example code for training and testing UNet
<br/>

#### Fig. 2. Model prediction
<img src="https://github.com/chingyaolai/Antarctic-fracture-detection/blob/master/images/test.png" width="800">
