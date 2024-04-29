# mechanical-parts-classification-resnet18

Welcome to the ResNet18 Mechanical Parts Classification project! This project focuses on implementing an image classification model based on the ResNet18 architecture using TensorFlow.

### Key Features:
* Implements the ResNet18 architecture for image classification tasks.
* Custom child classes derived from TensorFlow's Model and Layer classes.
* Includes data preprocessing and augmentation techniques to enhance model performance.
* Evaluates model performance using standard metrics.

## Brief Overview of ResNet18 Architecture

Residual Networks or ResNets is a type of convolutional neural network (NN) architecture developed by Microsoft Research. It was introduced to address challenges with training deeper NN effectively. It was shown that traditional deep NNs suffer from the vanishing gradient problem. Gradients become increasingly small as they propagete through the layers during training, resulting in bad performance outcomes. In simpler terms the inital input signal is getting lost (or dampened) while it travels through the layers. 

To address this issue, researchers introduced skip connections, also known as residual connections [1]. These connections allow the network to learn __residual functions__, which respresent the difference between the input and output of a particular layer. Learning the residuals instead of directly learning the desired mapping allows the network to focus on the "harder" parts of the task, hence making it easier to train deeper networks.

ResNet18 is one of the smaller types of ResNet architecture. As the name implies it consists of a total of 18 layers, including convolutional layers, pooling layers and fully connected layers. ResNet18 architecture is illustrated in the figure below [2].

![image](https://github.com/peksikeksi/mechanical-parts-classification-resnet18/assets/81853083/9dd531ae-c433-4315-b8ed-14aff74970aa)

*ResNet-18 architecture* [2]

The architecture starts with a few convolutional layers followed by a series of residual blocks. Each residual block contains two convolutional layers with batch normalization and ReLU activation, along with a skip connection that adds the input to the output of the block. The final layers include global average pooling and a fully connected layer for classification. Despite relatively shallow depth, ResNet18 often outperformes many deeper architectures. 

## TODOs:
* Experiment with different architectures or ensemble methods and compare performance.
* Explore deployment options.
* For yet unclear reasons, model is unable to learn when tensor values are normalized. This should be further explored. 

## Dataset

The project utilizes a dataset [3] consists of images of mechanical parts created using a CAD software. There is a total of four classes: 'bolt', 'locatingpin', 'nut', and 'washer'. The dataset is divided into training and validation sets for model training and evaluation.

## Note:

This project serves as a learning exercise to demonstrate competency in machine learning fundamentals and software development practices. Feedback and contributions are welcome 😁


## References and Cool links

[1] [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385)

[2] [Image Link](https://www.researchgate.net/figure/ResNet-18-architecture-20-The-numbers-added-to-the-end-of-ResNet-represent-the_fig2_349241995>)

[3] [Images of mechanical parts (Bolt,Nut, Washer,Pin)](https://www.kaggle.com/datasets/manikantanrnair/images-of-mechanical-parts-boltnut-washerpin)

[4] [Understanding ResNet Architecture: A Deep Dive into Residual Neural Network](https://medium.com/@ibtedaazeem/understanding-resnet-architecture-a-deep-dive-into-residual-neural-network-2c792e6537a9)

[5] [Residual Networks (ResNet) – Deep Learning](https://www.geeksforgeeks.org/residual-networks-resnet-deep-learning/)

[6] [ResNet (actually) explained in under 10 minutes](https://www.youtube.com/watch?v=o_3mboe1jYI)

[7] [Neuralearn](https://www.youtube.com/channel/UC4vLiApNM0VEYE-WQCjcscA)
