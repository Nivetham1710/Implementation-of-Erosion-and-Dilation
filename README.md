# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step1:
Import the necessary packages.
## Step2:
Create the Text using cv2.putText.
## Step3:
Create the structuring element.
## Step4:
Erode and Dilate the image.
## Step5:
End the Program.
 
## Program:
``` Python
 Developed by : Nivetha M
 Register number :212221240034

# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img1 = np.zeros((100,260), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'NIVETHA',(5,70), font, 2,(255),5,cv2.LINE_AA)
plt.imshow(img1,'gray')

# Create the structuring element

kernel=np.ones((5,5),np.uint8)
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
image_erode1=cv2.erode(img1, kernel)
plt.imshow(image_erode1, 'gray')

# Erode the image

image_erode1=cv2.erode(img1, kernel)
plt.imshow(image_erode1, 'gray')

# Dilate the image

image_dilate1 = cv2.dilate(img1, kernel)
plt.imshow(image_dilate1, 'gray')


```
## Output:

### Display the input Image
![d](https://github.com/Nivetham1710/Implementation-of-Erosion-and-Dilation/assets/94155183/ecd43646-171c-40a2-8719-8125951f6860)


### Display the Eroded Image
![e](https://github.com/Nivetham1710/Implementation-of-Erosion-and-Dilation/assets/94155183/ebaa5937-8559-4c3e-bb0e-6bfb28f01f79)


### Display the Dilated Image
![f](https://github.com/Nivetham1710/Implementation-of-Erosion-and-Dilation/assets/94155183/055a6963-fe41-42f0-b54f-ecd0d544da86)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
