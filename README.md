# Antarctic fracture Detection_With_U-Net

Using neural networks to detect fracture patterns, in collaboration with Cameron Chen (Google), Jonathan Kingslake (Coulmbia University), and Pierre Gentine (Columbia University).

## File descriptions:
Input images and the corresponding labeled images are in the format of .tif. The filenames of the labeled images ends with "_mask.tif". The imput image is a grey-valued image with one channel. labeled images contains only two grey values corresponding to two two classes (fracture: 255 and non fractutre: 0).

data_trainset_20190717: training data

data_testset_random_20190812: testing data

data_ross: extra testing data

Fracture_epoch50_LR1.4_D0.95_M0.2_example.ipynb: example code for training and testing UNet

## Motivation
The availability of remote-sensing data is rapidly expanding. New strategies which take advantage of the most recent algorithms and approaches are needed to interpret large remote-sensing data sets. In order to identify fracture locations from satellite imagery across Antarctica, we develop a neural network model for fracture recognition. Ice fractures result in the collapse of Antartctica ice-shelves, which is expected to destabilize glacier flows into the ocean and accelerate glabal sea-level rise. The outcome of this research will provide a thorough map of fracture distribution across Antarctica, which is important for evaluating the impact of ice fractures on the future sea-level.
