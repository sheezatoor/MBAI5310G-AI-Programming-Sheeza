1. What does image classification mean? Explain with one example.
Image classification refers to labelling an image with a keyword based on pixel values and distribution probability in the model. Essentially, the input is an image with an array of pixel values in which darker pixels have lower values and lighter pixels have higher values. Using patterns learned through different classes/categories of pixel images such as shirts, shoes, bags, etc, the model probability distribution scores are achieved. The highest probability score classifies the image. For instance the image of a shirt that is 28 by 28 pixels can be presented by darker and lighter pixels with matrix numbers. Based on the statistical patterns in the pixel values compared to other classes, we can determine which class the image belongs to such as shirt. 


2. Why is using a Dense Network not always a suitable choice for images?
Although fully connected or dense neural networks can classify images, they ignore the local structure of the image. If the image is flattened, the model will see a vector of large numbers rather than an array which makes it difficult to know which pixels were next to one another in the original image. 


3. In a CNN, what is convolution, and what does a filter or kernel do?
CNN stands for convolutional neural network. It is used in image classification by looking for local patterns and combining them into high-level visual interpretations. Convolution refers to the main operation/task of CNN in which small matrices of filters go over the image and compute values at each position. The value correlates with patterns stored in the filter. Filters are responsible for pattern recognition as it detects certain aspects of the image by producing strong or weak responses creating a feature map. 


4. What is a feature map in a convolutional neural network?
A feature map is the output resulting from the filter processing an image. A CNN can use different filters to detect various aspects of an image such as edges, corners and textures. Each filter produces one feature map. 


5. Why is weight sharing used in CNNs? Explain.
Weight sharing refers to when one filter is reused over an image. The same detector is applied everywhere across the image. This helps to determine the same visual feature regardless of where it appears on the image. 


6. How does the ReLU activation function work? Write the ReLU output for the following values:
[-3, 0, 2, 5]
ReLu represents Rectified Linear Unit. It promotes non-linearity within the model and understanding of complex patterns through removing negative signals. It follows the following guidelines: negative value; replace with zero, positive value; keep it. 
For the following values, the ReLu output would be: [0, 0, 2, 5]


7. What is max pooling, and why is it used in CNNs?
Max pooling is a method in which a small window (2x2) moves over the feature map and reduces its spatial size by keeping the larger value in the window. In doing so, the feature map keeps the strongest signals. For instance, for the following values: [1, 3, 2, 0], max pooling would keep 3 because the strongest signal is three and its exact location may not matter. Max pooling can help to mitigate small shifts while recognizing the important feature and reducing computation. 


8. In the Fashion-MNIST code, why are images reshaped from 28 × 28 to 28 × 28 × 1?
Images are reshaped to this configuration because the image needs to be compatible with Conv2D. According to the Conv2D layer, inputs should be in the following format: height, width, channel. In this case, the 1 would represent the channel dimension meaning that it is a grayscale image. A color image on the other hand would have a channel dimension of 3. 


9. What is the difference between training data, validation data, and test data?
Training Data: used for updating model weights 
Validation Data: used to check generalizability beyond training examples in the model development stage
Test Data: used to test model performance on unseen data


10. What is overfitting? If training accuracy is high but validation accuracy is low, what does this indicate?
Overfitting refers to the model being highly dependent on training data and learns very specific details from the training data. This issue can make it very challenging for the model to process new and unseen data with the same level of accuracy. If training accuracy is high but validation low, it indicates overfitting. 

