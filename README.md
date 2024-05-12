
# Super Resolution Image Generation using SRGAN


SRGAN (Super-Resolution Generative Adversarial Network) is a deep learning technique used to generate high-resolution images from low-resolution inputs. It comprises a generator network, which upscales low-res images, and a discriminator network, trained to distinguish real high-res images from generated ones. Through adversarial training, SRGAN aims to produce realistic high-res images, employing perceptual loss and adversarial loss functions. It's effective for tasks like enhancing image quality in medical imaging or improving details in low-quality surveillance footage.


## Project Goal


1. Develop and implement a system for Super Resolution Image      Generation using SRGAN.
2. Generate high-quality, realistic high-resolution images from low-resolution inputs.
3. Address limitations of traditional super-resolution techniques through deep learning and adversarial training.
4. Achieve state-of-the-art performance in super-resolution tasks across diverse domains.
5. Provide an efficient solution for enhancing image resolution while preserving vital visual details.
## Methodology/ Working Procedure
![](https://github.com/Nur-RMSU/DIP-LAB/blob/main/Images/Picture2.jpg?raw=true)
##  Architecture of SRGAN:
The Super Resolution GAN contains two parts Generator and Discriminator where generator produces some data based on the probability distribution and discriminator tries to guess weather data coming from input dataset or generator.  Generator than tries to optimize the generated data so that it can fool the discriminator.
![](https://github.com/Nur-RMSU/DIP-LAB/blob/main/Images/SRGAN-660x442-removebg-preview.png?raw=true)

## About Generator and Discriminator:
1. Total 16 residual blocks were used in Generator Network
2. Within the residual block, two convolutional layers are used, with small 3×3 kernels and 64 feature maps followed by batch-normalization layers and ParametricReLU.
3. In Discriminator Network, there are eight convolutional layers with of 3×3 filter kernels, increasing by a factor of 2 from 64 to 512 kernels. 
4. Strided convolutions are used to reduce the image resolution each time the number of features is doubled.
![](https://github.com/Nur-RMSU/DIP-LAB/blob/main/Images/Architecture-of-SRGAN-network-diagram-of-generator-and-discriminator-with%20(1).jpg?raw=true)

## Loss Function
1. The SRGAN uses perceptual loss function
2. perpetual loss = content loss + adversarial loss
![](https://github.com/Nur-RMSU/DIP-LAB/blob/main/Images/loss.png?raw=true)

## Dataset
Dataset
In our project, we used a image dataset from Kaggle by Matteo Castrignano
The dataset can be found here: mirflickr (kaggle.com)
1. Size: The dataset contains 25000 images. During our work we use just 2000 random images for simplicity due to limitation of Hardware resource. 
2. Features: The dataset includes a variety of type of image including clouds, sea, lake, river, night, tree, flower, dog, bird, car, people, baby, female, male, portrait
Data Preprocessing

During the project we use two type of Image Low Resolution and High Resolution. We convert our original Image to two different size and save into two different folders.  
1. 32x32 format as Low Resolution
2. 128x128 format as High Resolution


## Result
![](https://github.com/Nur-RMSU/DIP-LAB/blob/main/Images/5.png?raw=true)
![](https://github.com/Nur-RMSU/DIP-LAB/blob/main/Images/50.png?raw=true)
![](https://github.com/Nur-RMSU/DIP-LAB/blob/main/Images/150.png?raw=true)
## Limitations
1. Computational Complexity
2. Model Size
3. Overfitting
4. Artifact Generation
5. Subjective Evaluation

## Reference
[1] Tensorlayer. (n.d.). GitHub - tensorlayer/SRGAN: Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network. GitHub. https://github.com/tensorlayer/SRGAN
[2] A super resolution algorithm based on attention mechanism and SRGAN network. (2021). IEEE Journals & Magazine | IEEE Xplore. https://ieeexplore.ieee.org/abstract/document/9496642
[3] https://www.geeksforgeeks.org/super-resolution-gan-srgan/
