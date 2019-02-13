# Neural-Style-Transfer

This is a Tensorflow implementation of styling images using VGG-19 model.

## Some Examples

| Content Image                                                | Style Image                                                    | Generated Image                                                                        |
|:------------------------------------------------------------:|:--------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| ![Macau](resources/Content%20Images/ContentMacau.jpg)        | ![Starry Night](resources/Style%20Images/StyleStarryNight.jpg) | ![MacauStarryNight](resources/Generated%20Images/Generated_MacauStarryNight.png)       |
| ![Star Wars](resources/Content%20Images/ContentStarWars.jpg) | ![Feneck](resources/Style%20Images/StyleFeneck.jpg)            | ![StarWarsFeneck](resources/Generated%20Images/Generated_StarWarsFeneck.png)           |
| ![Star Wars](resources/Content%20Images/ContentStarWars.jpg) | ![Starry Night](resources/Style%20Images/StyleStarryNight.jpg) | ![StarWarsStarryNight](resources/Generated%20Images/Generated_StarWarsStarryNight.png) |

## Hyperparamter Tuning

### Style Strength

| Alpha | Beta |   Result                                                          |
|:-----:|:----:|:-----------------------------------------------------------------:|
| 0.025 |   5  | ![Generated_11](resources/alpha%20beta%20tuning/Generated_11.png) |
|   1   |  500 | ![Generated_12](resources/alpha%20beta%20tuning/Generated_12.png) |
|   5   |  100 | ![Generated_13](resources/alpha%20beta%20tuning/Generated_13.png) |
|   10  |  40  | ![Generated_14](resources/alpha%20beta%20tuning/Generated_14.png) |
|  7.5  |  100 | ![Generated_15](resources/alpha%20beta%20tuning/Generated_15.png) |
|   10  | 5000 | ![Generated_16](resources/alpha%20beta%20tuning/Generated_16.png) |

### Content Formula

Here, 

J<sub>content</sub> is the content loss function  
C and G represent content and generated image respectively  
a(C)and a(G) are the activations from the chosen layer when image is passed to the model  
n<sub>H</sub>, n<sub>W</sub>, n<sub>C</sub> are the height, weight and number of channels of the image respectively

|                Formula Used           |                           Generated Image(Run only upto 100 iterations)   |
|:-------------------------------------:|:-------------------------------------------------------------------------:|
|  ![First](resources/CodeCogsEqn1.png) |  ![GeneratedFirst](resources/Content%20formula%20tuning/Generated_21.png) |
| ![Second](resources/CodeCogsEqn2.png) | ![GeneratedSecond](resources/Content%20formula%20tuning/Generated_22.png) |
|  ![Third](resources/CodeCogsEqn3.png) |  ![GeneratedThird](resources/Content%20formula%20tuning/Generated_23.png) |

## References:

1. [A Neural Algorithm of Artistic Style](https://arxiv.org/abs/1508.06576)
2. [Convolutional Neural Networks](https://www.coursera.org/learn/convolutional-neural-networks/) by deeplearning.ai on coursera
3. [NeuralArt Github Repository](https://github.com/ckmarkoh/neuralart_tensorflow)
