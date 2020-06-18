# Antarctic fracture detection with U-Net
[![DOI](https://zenodo.org/badge/259829938.svg)](https://zenodo.org/badge/latestdoi/259829938)

We use U-Net to detect fracture locations from satellite imagery across Antarctica (125m-resolution MOA imagery (2009); [https://doi.org/10.7265/N5KP8037](https://nsidc.org/data/NSIDC-0593)). Ice fractures result in the collapse of Antartctica ice-shelves, which is expected to destabilize glacier flows into the ocean and accelerate glabal sea-level rise. The outcome of this research will provide a thorough map of fracture distribution across Antarctica, which is important for evaluating the impact of ice fractures on the future sea-level.

## File descriptions:
Input images and the corresponding labeled images are in the format of .tif. The filenames of the labeled images ends with "_mask.tif". The imput image is a grey-valued image with one channel. labeled images contains only two grey values corresponding to two two classes (fracture: 255 and non fractutre: 0).

data_trainset_20190717: training data (6 1000x1000 pixel tiles )

data_tuneset_20190717: validation data

data_testset_random_20190812: testing data

data_ross: two extra images on the Ross ice shelf for visulization 

Fracture_epoch50_LR1.4_D0.95_M0.2_example.ipynb: example code for training and testing UNet


### Locations of the training/validation/testing data and continent-wide fracture predictions
![Frac](https://github.com/chingyaolai/Antarctic-fracture-detection/blob/master/images/dataloc.PNG)
