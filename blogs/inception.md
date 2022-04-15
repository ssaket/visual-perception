# Inception Network

- prior to the inception networks, most CNNs were just stacking convolutional layers deeper and deeper, hoping to get better performance.

## Inception v1

- Salient parts in the image can have extremely large variation in size. For instance, an image with a dog can be either of the following, as shown below. The area occupied by the dog is different in each image.

- Because of this huge variation in the location of the information, choosing the right kernel size for the convolution operation becomes tough. A larger kernel is preferred for information that is distributed more globally, and a smaller kernel is preferred for information that is distributed more locally.

- Very deep networks are prone to overfitting. It also hard to pass gradient updates through the entire network.

- Naively stacking large convolution operations is computationally expensive.

- Label Smoothing (A type of regularizing component added to the loss formula that prevents the network from becoming too confident about a class. Prevents over fitting).
