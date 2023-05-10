# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>Import the necessary packages.


### Step2:
<br>Create the Text using cv2.putText.

### Step3:
<br>Create the structuring element.

### Step4:
<br>Erode and Dilate the image.



### Step5:
<br>End Program.

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL


# Create the Text using cv2.putText
cv2.putText(img1,'Kavinraja.D' ,(5,70),font,3.3,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')



# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Erode the image
img_erode=cv2.erode(img1,kernel1)
plt.imshow(img_erode,cmap='gray')




# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
plt.imshow(img_dilate,cmap='gray')




```
## Output:

### Display the input Image
![OUTPUT](./images/10(1).jpg)

### Display the Eroded Image
![OUTPUT](./images/10(2).jpg)

### Display the Dilated Image
![OUTPUT](./images/10(3).jpg)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.