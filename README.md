# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Create a blank image.

### Step2:
Create a structuring element (5x5 rectangular)

### Step3:
Erode the image.

### Step4:
Dilate the image.

### Step5:
End the program.
 
## Program:

``` Python
# Developed By: SAI DARSHINI R S
# Register No: 212223230178


import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'SAI DARSHINI' ,(5,70),font,3,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')


```
## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/d099074b-699c-4632-83c1-130af3fee2dd)



### Display the Eroded Image
![image](https://github.com/user-attachments/assets/ff3b2890-2497-4e59-a89c-699f953fe8ef)


### Display the Dilated Image
![image](https://github.com/user-attachments/assets/efa3207a-4dda-4ed2-9a22-d6596a83c383)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
