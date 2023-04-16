## Plant Disease Detection Project

This is plant diease detection project and We have implemented deep learning model for that. 
This model could achive near about 99% accuracy trained over the 38 plant disease classes.

## Resources:

[Kaggle Data Source](https://www.kaggle.com/datasets/saroz014/plant-disease)

### Data Overview:
![Images Data](/docs/image_overview.png)

## Modelling:
### Neural Network Architecture:

    _________________________________________________________________
    Layer (type)                 Output Shape              Param #   
    =================================================================
    conv2d_1 (Conv2D)            (None, 128, 128, 32)      896       
    _________________________________________________________________
    activation_1 (Activation)    (None, 128, 128, 32)      0         
    _________________________________________________________________
    batch_normalization_1 (Batch (None, 128, 128, 32)      128       
    _________________________________________________________________
    max_pooling2d_1 (MaxPooling2 (None, 42, 42, 32)        0         
    _________________________________________________________________
    dropout_1 (Dropout)          (None, 42, 42, 32)        0         
    _________________________________________________________________
    conv2d_2 (Conv2D)            (None, 42, 42, 64)        18496     
    _________________________________________________________________
    activation_2 (Activation)    (None, 42, 42, 64)        0         
    _________________________________________________________________
    batch_normalization_2 (Batch (None, 42, 42, 64)        256       
    _________________________________________________________________
    conv2d_3 (Conv2D)            (None, 42, 42, 64)        36928     
    _________________________________________________________________
    activation_3 (Activation)    (None, 42, 42, 64)        0         
    _________________________________________________________________
    batch_normalization_3 (Batch (None, 42, 42, 64)        256       
    _________________________________________________________________
    max_pooling2d_2 (MaxPooling2 (None, 21, 21, 64)        0         
    _________________________________________________________________
    dropout_2 (Dropout)          (None, 21, 21, 64)        0         
    _________________________________________________________________
    conv2d_4 (Conv2D)            (None, 21, 21, 128)       73856     
    _________________________________________________________________
    activation_4 (Activation)    (None, 21, 21, 128)       0         
    _________________________________________________________________
    batch_normalization_4 (Batch (None, 21, 21, 128)       512       
    _________________________________________________________________
    conv2d_5 (Conv2D)            (None, 21, 21, 128)       147584    
    _________________________________________________________________
    activation_5 (Activation)    (None, 21, 21, 128)       0         
    _________________________________________________________________
    batch_normalization_5 (Batch (None, 21, 21, 128)       512       
    _________________________________________________________________
    max_pooling2d_3 (MaxPooling2 (None, 10, 10, 128)       0         
    _________________________________________________________________
    dropout_3 (Dropout)          (None, 10, 10, 128)       0         
    _________________________________________________________________
    flatten_1 (Flatten)          (None, 12800)             0         
    _________________________________________________________________
    dense_1 (Dense)              (None, 1024)              13108224  
    _________________________________________________________________
    activation_6 (Activation)    (None, 1024)              0         
    _________________________________________________________________
    batch_normalization_6 (Batch (None, 1024)              4096      
    _________________________________________________________________
    dropout_4 (Dropout)          (None, 1024)              0         
    _________________________________________________________________
    dense_2 (Dense)              (None, 38)                38950     
    _________________________________________________________________
    activation_7 (Activation)    (None, 38)                0         
    =================================================================
    Total params: 13,430,694
    Trainable params: 13,427,814
    Non-trainable params: 2,880
    _________________________________________________________________


Project Organization
------------

    ├── LICENSE
    ├── Makefile
    ├── README.md
    ├── docs
    │   ├── Makefile
    │   ├── commands.rst
    │   ├── conf.py
    │   ├── getting-started.rst
    │   ├── image_overview.png
    │   ├── index.rst
    │   └── make.bat
    ├── index.md
    ├── models
    ├── notebooks
    │   ├── Plant disease detection model - Final Model.ipynb
    │   └── Plant disease identification -  Sample Model.ipynb
    ├── references
    ├── reports
    │   └── figures
    ├── requirements.txt
    ├── setup.py
    ├── src
    │   ├── __init__.py
    │   ├── data
    │   │   ├── __init__.py
    │   │   └── make_dataset.py
    │   ├── features
    │   │   ├── __init__.py
    │   │   └── build_features.py
    │   ├── models
    │   │   ├── __init__.py
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   └── visualization
    │       ├── __init__.py
    │       └── visualize.py
    ├── test_environment.py
    └── tox.ini`
