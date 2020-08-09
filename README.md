# Traffic Light Classification
Image Classification using self-defined CNN model in Tensorflow 2.2 (Keras Sequential)

## Running Instructions

1. Install Tensorflow 2.2 for python 3.n:
```
pip3 install tensorflow==2.2

or

pip3 install tensorflow-gpu==2.2  #with GPU support
```
2. Install Jupyter Notebook:
```
pip3 install jupyter
```

3. Under the Project Directory, run Jupyter Notebook:
```
jupyter notebook Traffic_Light_Classifier_cnn_tf2.ipynb
```
## Dataset

This traffic light dataset consists of 1484 number of color images in 3 categories - red, yellow, and green. As with most human-sourced data, the data is not evenly distributed among the types. There are:

904 red traffic light images
536 green traffic light images
44 yellow traffic light images

Note: All images come from this MIT self-driving car course and are licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.

## CNN Architecture

```
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d (Conv2D)              (None, 32, 32, 16)        1216      
_________________________________________________________________
max_pooling2d (MaxPooling2D) (None, 16, 16, 16)        0         
_________________________________________________________________
conv2d_1 (Conv2D)            (None, 16, 16, 32)        12832     
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 8, 8, 32)          0         
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 8, 8, 32)          25632     
_________________________________________________________________
max_pooling2d_2 (MaxPooling2 (None, 4, 4, 32)          0         
_________________________________________________________________
conv2d_3 (Conv2D)            (None, 4, 4, 32)          25632     
_________________________________________________________________
max_pooling2d_3 (MaxPooling2 (None, 2, 2, 32)          0         
_________________________________________________________________
flatten (Flatten)            (None, 128)               0         
_________________________________________________________________
dense (Dense)                (None, 256)               33024     
_________________________________________________________________
dense_1 (Dense)              (None, 3)                 771       
=================================================================
Total params: 99,107
Trainable params: 99,107
Non-trainable params: 0
_________________________________________________________________
```

Feel Free to adjust this architecture or any parameters!

## Performance

```
Training Acc: 0.9967 in 10 epoches
Validation Acc: 1.0
Testing ACC: 0.9899, misclassified 3/297

Guaranteed not misclassifying 'red' as 'green'
```
