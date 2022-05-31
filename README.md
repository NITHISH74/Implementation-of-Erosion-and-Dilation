# Implementation-of-Erosion-and-Dilation:
## Aim:
To implement Erosion and Dilation using Python and OpenCV.
## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages.


### Step 2:
Create the text image.


### Step 3:
Create the structuring image for dilation/erosion.


### Step 4:
Apply erosion and dilation using cv2.erode and cv2.dilate.


### Step 5:
Display the images.

## Program:

``` 
Developer Name : NITHISHWAR S
Register number : 212221230071

import numpy as np 
import cv2
import matplotlib.pyplot as plt

img1=np.zeros((100,300),dtype= 'uint8') 
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'NITHISHWAR',(5,70),font,1.4,(355),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
plt.title("Original Image")
plt.axis('off')
# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
# Erode the image
image_erode = cv2.erode(img1,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,cmap='gray')
plt.axis('off')
# Dilate the image

image_dilate = cv2.dilate(img1,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,cmap='gray')
plt.axis('off')


```
## Output:

### Display the input Image
![image](https://user-images.githubusercontent.com/94164665/171099861-3c085985-7797-408a-babf-a9f3f3127ee7.png)
### Display the Eroded Image
![image](https://user-images.githubusercontent.com/94164665/171099837-6f4288f2-a742-46e6-ad7c-bc26fadae193.png)

### Display the Dilated Image
![image](https://user-images.githubusercontent.com/94164665/171099895-bc464958-3c7d-4023-84f3-fbab80db1f06.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
