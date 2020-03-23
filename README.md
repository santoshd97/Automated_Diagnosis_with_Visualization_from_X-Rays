# Automated-Diagnosis-with-Visualization-from-X-Rays
In this work, we aimed to assess the performance of various deep learning techniques to automatically detect the presence of 14 different disease classes in chest radiographs and visualize the areas indicating the presence of these diseases in the X-Ray.

<h2>Dataset:</h2>
The dataset has 3 classes for each of the 14 labels. The competition of this dataset suggested many ways of dealing with the uncertain labels (-1). Since the dataset is collected from a credible source, we prefer replacing the (-1) values with (0) for simplicity. Moreover, as this dataset belongs to a competition, we sampled validation and testing data from the training data and downscaled the images to 128 x 128 pixels.

<h2>Multi-label Classification Problem:</h2>
Various current state-of-the art models such as DenseNet-121, MobileNet-V2, Inception-V3, VGG-16 were trained on the CheXpert dataset. Common parameters used on all these models for training are learning rate = 0.0002, batch size = 64, optimizer = Adam and since it is a multi-label classification, binary cross entropy is used as the loss function. Moreover, these models were trained on 30,000 training samples and 5000 validation samples.

<h2>Result:<h2>
5000 test images for multi-label classification task.
