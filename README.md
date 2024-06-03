**Pruning Basics with PyTorch**
===============================

**Introduction**
---------------
This repository contains basic experiments with various pruning methods in PyTorch. It demonstrates how to apply different pruning techniques to a simple LeNet architecture. 

**About LeNet Architecture**
----------------------------
The LeNet architecture is a classic convolutional neural network (CNN) architecture that was introduced by Yann LeCun et al. in 1998. The architecture consists of a series of convolutional layers followed by fully connected layers. There the layers of the architecture used in this repository: 
* Convolutional Layers:
  * self.conv1: Takes a single input channel (e.g., grayscale image) and applies 6 filters, each with a 5x5 kernel. This layer extracts basic features like edges and patterns.
  * self.conv2: Takes the output of conv1 (6 channels) and applies 16 filters with a 5x5 kernel, further extracting more complex features.

* Pooling Layers:
  * F.max_pool2d: After each convolutional layer, max pooling is applied with a 2x2 window. This downsamples the feature maps, reducing the spatial dimensions and making the network more robust to small shifts in the input.

* Fully Connected Layers:
  * self.fc1: A fully connected layer with 120 neurons, taking the flattened output of the convolutional layers. This layer starts to learn high-level relationships between the features.
  * self.fc2: Another fully connected layer with 84 neurons, further processing the information.
  * self.fc3: The final fully connected layer with 10 neurons (for 10-digit classes), producing the output probabilities for each digit.
 
**Requirements**
----------------
* Python 3.6 or above
* PyTorch
* NumPy
* torch.nn.utils.prune

**Experiments**
---------------
Weight Pruning: Pruning individual weights based on their magnitude or importance.
Global Pruning: Pruning weights globally across the entire model.
Iterative Pruning: Gradually pruning the model over multiple iterations.
Random Unstructured Pruning: Randomly pruning a certain percentage of parameters.
L1 Unstructured Pruning: Pruning based on norm magnitudes of parameters.

**Contributions**
-----------------
Contributions to this repository are welcome. If you have any ideas for additional pruning experiments or improvements to the existing code, please open an issue or submit a pull request.


