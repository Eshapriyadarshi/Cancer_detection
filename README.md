# Cancer_detection
In this project a cancer detection CNN model is used on the histopathologic dataset from kaggle. This works on google colab, the dataset is downloaded from kaggle directly on the colab using the Kaggle API.
## Deep Learning  Frameworks and  Python Libraries used:
- TensorFlow
- Keras
- Sklearn
- Numpy
- Pandas
- Matplotlib
- Seaborn
- scikitplot
## Dataset ##
The histopathologic dataset used is from kaggle which contains a total of 220025 training images and 57458 testing images. It contains a csv file of training images with labels 0 & 1 representing no tumor tissue and tumor tissue respectively. The training data has a non-uniform distribution of labels with 130908 positive label (1) and 89117 negative label (0). Too ensure a robust training on both the labels feature engineering is performed and a new training dataframe is created having 89000 samples of each label. Further 10% of this training set is split into validation set.
- Reference - https://www.kaggle.com/c/histopathologic-cancer-detection/data
## CNN Model ##
This model consists of 3 layers of SeparableConv layer of 32, 64 and 128 respectively which is followed by a fully connected layer then a sigmoid classifier. Every Conv layer is followed by a relu activation and batch normalizaion followed by maxpool layer. Dropout is also used to remove the overfitting of the model.
