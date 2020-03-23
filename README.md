# Automated-Diagnosis-with-Visualization-from-X-Rays
In this work, we aimed to assess the performance of various deep learning techniques to automatically detect the presence of 14 different disease classes in chest radiographs and visualize the areas indicating the presence of these diseases in the X-Ray. Detailed decription is included in "project report.pdf" in this repository.

<h2>Dataset:</h2>
ChexPert dataset is used in this project. The dataset has 3 classes for each of the 14 labels. The competition of this dataset suggested many ways of dealing with the uncertain labels (-1). Since the dataset is collected from a credible source, we prefer replacing the (-1) values with (0) for simplicity. Moreover, as this dataset belongs to a competition, we sampled validation and testing data from the training data and downscaled the images to 128 x 128 pixels.

<h2>Multi-label Classification Problem:</h2>
Various current state-of-the art models such as DenseNet-121, MobileNet-V2, Inception-V3, VGG-16 were trained on the CheXpert dataset. Common parameters used on all these models for training are learning rate = 0.0002, batch size = 64, optimizer = Adam and since it is a multi-label classification, binary cross entropy is used as the loss function. Moreover, these models were trained on 30,000 training samples and 5000 validation samples.

<h2>Visualization:</h2>
For a given test image, we predict all the possible classes out of the 14 classes based on the trained VGG-16 model and visualize the areas most indicative of each of the predicted classes in the form of a heatmap using Grad-CAM technique. Following table shows the predicted probabilities for the given test image:<br>
![class probabilities](https://github.com/santoshd97/Automated-Diagnosis-with-Visualization-from-X-Rays/blob/master/Class%20probailities.png)

The Grad-CAMs are generated only for the positive classes, because we want to visualize the regions where pathologies are present.


<h2>Result:</h2>
5000 test images were used for multi-label classification task. Below table shows overall accuracies of various deep learning models:<br>
![Accuracy table](https://github.com/santoshd97/Automated-Diagnosis-with-Visualization-from-X-Rays/blob/master/Accuracy.png)
