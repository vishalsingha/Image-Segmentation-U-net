#  Image-Segmentation-U-net

##  Dataset
* <b>Source : </b> [https://www.robots.ox.ac.uk/~vgg/data/pets/](https://www.robots.ox.ac.uk/~vgg/data/pets/)
* <b>Discription:</b><br>
  Dataset Consist of colorder images and annonation correcponding to each  images. The annonations are 2D png images containing 1's, 2's, 3's where<br>
  1's : foreground<br>
  2's : boundary<br>
  3's : background
  
 ## Data preparation:
 All the images are resized to (256, 256, 3) dimention by using tf.data api to make datagenerator. And the annonation were also converted from (256, 256) to (256, 256, 3) images by using  pixel level one hot encoding.
  
## Model used:
U-net model having (None, 256, 256, 3) as input dim and (None 256, 256, 3) as output dimention.

## Results :

* Default train and test size (Segmentation_Unet.ipynb) :
  * train size: 2944
  * validation size : 736
  * test size : 3369
<p float="left">
<img src="https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/acc.png?raw=true" width="450" height="300">
<img src="https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/loss.png?raw=true" width="450" height="300">
</p>

* Custom train and test size (segmentation_Unet_final.ipynb) :
     * train size : 5621
     * validatio size : 1103
     * test size : 625
  
<p float="left">
<img src="https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet_final/acc1.png?raw=true" width="450" height="300" >
<img src="https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet_final/loss1.png?raw=true" width="450" height="300">
</p>

## Varification on test data (real vs predicted)

 * Default train and test size
    * Some good results:

      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/f1.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/f2.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/f3.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/f5.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/f8.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/f7.png?raw=true)
    * some bad results

      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/b1.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/b2.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/b3.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/b4.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/b5.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet/b6.png?raw=true)




 * Custom train and test size

      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet_final/l1.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet_final/l2.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet_final/l3.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet_final/l4.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet_final/l5.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet_final/l6.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet_final/l7.png?raw=true)
      ![image](https://github.com/vishalsingha/Image-Segmentation-U-net/blob/main/Images/Segmentation_unet_final/l8.png?raw=true)
      
      
## Conclusion:
 The accuracy of custom train test split increase the accuracy of prediction alot due to the increase of training data. If we increase the size of training set the model is expected to give better performance.







  





