# budget-resnet
Built a ResNet architecture with size constraint of 5 million parameters, based on the ResNet18 architecture. The architecture was changed by eliminating the last of the four residual layers and increasing the number of residual blocks in each remanining layer. In our model, the first and last layers now contain 3 blocks, while the middle layer contains five blocks.

We created a custom offline data augmentation pipeline consisting of translations, rotations, scale changes, and hue and saturation variations. A custom learning rate schedule was also put in place to improve model performance and robustness. The optimizer of choice was a vanilla SGD algorithm with momentum. The learning rate starts large and decays by one degree of magnitude at every milestone. Three milestone were selected in total.

Achieved 95.67 percent test accuracy on the CIFAR10 dataset.
