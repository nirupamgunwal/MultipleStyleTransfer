# Table of contents
1. [Introduction](#introduction)
2. [Stats for Nerds](#paragraph2)
3. [How to Use??](#paragraph3)
3. [Documentation and Working](#paragraph4)
4. [References](#paragraph5)

## Introduction <a name="introduction"></a>
The objective of this module is to provide a method for transferring style of an artist or a particular painting to your images. So, what the user provides as input is his image and the particular image/images who's style he wants to be applied on his image.

What the user receives as output? <br />
The user receives his image painted in the style of his particular artist. So, the output image is user's image as it was painted by the artist.

## Stats for the nerds. <a name="paragraph2"></a>
Model Used: VGG-Net 16
![alt text](https://neurohive.io/wp-content/uploads/2018/11/vgg16-1-e1542731207177.png)
Optimizer: L-BFGS
Content Loss:
![alt text](https://latex.codecogs.com/svg.latex?L_{content}%20=%20\frac{1}{2}%20\sum_{i,j}%20(F_{ij}^l%20-%20P_{ij}^l)^2)
Style Loss:
Gram's Matrix: 
![alt text](https://latex.codecogs.com/svg.latex?G_{ij}^l = \sum_{k} F_{ik}^l F_{jk}^l )
Error Term:
![alt text](https://latex.codecogs.com/svg.latex?E_{l} = \frac{1}{4 N_{l}^2 M_{l}^2} \sum_{i,j} (G_{ij}^l - A_{ij}^l)^2 )
Loss Term: 
![alt text](https://latex.codecogs.com/svg.latex?L_{style} = \sum_{l =0}^l E_{l} )

Combined Loss:
![alt text](https://latex.codecogs.com/svg.latex?L_{total} = \alpha L_{content} + \beta L_{style})
## How to Use?? <a name="paragraph3"></a>
Provide your image path in block 3 variable "content_image_path". 
<br />
Provide your artists style image in block 4 variable "style_image_path".

Run every block and your output images will be saved in the path provided by you in result.save().
## Proper Documentation of the Work <a name="paragraph4"></a>
[Report Link](https://drive.google.com/file/d/0B1tMHssfdVfKZUx5Y00xN3V6UnJsd3FTUlp6RmhuVlU3dEZZ/view?usp=sharing)

## References <a name="paragraph5"></a>
1. [CS231n CNN's Module](http://cs231n.github.io/convolutional-networks/) 
2. [Keras Documentation](https://keras.io/)