# Transfer-Learning-with-TensorFlow

In traditional supervised learning algorithms, we were always given a particular dataset and particular domain in which the data is labelled. We used this data to train a model and apply it on the same domain and measure whether the model performed well. For example, if we had a model to predict pedestrians during the day time, the same model would not predict pedestrians properly during night times. Though we are trying to solve the same problem, their domains are different and so one model cannot be used in the other domain though they are similar. For these types of problems, we use something called “Transfer Learning”

# What is Transfer Learning?

Transfer learning is using a pre-trained network(pre-trained on a larger dataset) on your data. In the figure below, you can see that there was a model which was trained on a huge image dataset (ImageNet) which is used on a new data with new classes and weights updated.

![1_mA1sUreCxnl-65ljlaXEcA](https://github.com/HiteshRam666/Transfer-Learning-with-TensorFlow-Feature-Extraction/assets/116026459/ae80fd5f-b142-4054-b722-d49e0e3dc9d9)

## When do you apply Transfer Learning?
- When there is huge amount of similar data in another domain, but less data in current domain
  
- Have enough data for training, but don’t have enough computational resources to train it.

## How does Transfer Learning Work?

As we have discussed about Convolution Neural Network, we know that CNN’s extract important features from an image. So, the neural network has learned to detect an object or classify an image. This has been stored in the form of weights throughout the neural network. We can use these weights on any data to classify images. This is the whole idea behind transfer learning. When you have new data and you use a pre-trained network, you just have to update the weights and fine-tune to model to make it work.

Generally, the first layers in a CNN try to extract the generalized features from every image. Only in the last few layers, the model tries to distinguish between different classes. So when we apply transfer learning, we have 2 options

- Freeze the weights and bias on initial few layers and train only the last few layers- dense and fully connected and their respective activation functions. In this case you don’t need to re-train the whole model again.
  
- Re-train the whole network, initializing from the learned weights and bias. While we do this, we keep the learning rate very low so that we don’t deviate from the original weights drastically.<img width="1324" alt="04-different-kinds-of-transfer-learning" src="https://github.com/HiteshRam666/Transfer-Learning-with-TensorFlow-Feature-Extraction/assets/116026459/fb736c46-0a67-4ad7-8b8d-cea4ec43a17a">
