# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import packages.
### Step2:
Assign image and create a matrix ofones.

### Step3:
Put text in that image.

### Step4:
Do erosion on the image.

### Step5:
Do dilation and display the results.

 
## Program:

``` Python
# Import the necessary packages
# Create the Text using cv2.putText

import cv2
import numpy as np
import matplotlib.pyplot as plt


img = np.zeros((100,440),dtype = 'uint8')
cimg = cv2.cv2.Color(img,)
font = cv2.FONT_HERSHEY_SIMPLEX 
cv2.putText(img," Archana.J",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img,'coolwarm')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image

#erosion
eimg = cv2.erode(img,kernel)
plt.imshow(eimg,'coolwarm')
plt.title("Erorded Output")


# Dilate the image

#dilation
dimg = cv2.dilate(img,kernel)
plt.imshow(dimg,'coolwarm')
plt.title("Dilated Output")



```
## Output:

### Display the input Image
 ![image](https://user-images.githubusercontent.com/93427594/235286099-51d64695-2aa7-4408-8c4a-6e714c11f511.png)


### Display the Eroded Image

![image](https://user-images.githubusercontent.com/93427594/235286119-63fc6004-d510-42ce-9f28-6c00047d72ef.png)

### Display the Dilated Image
![image](https://user-images.githubusercontent.com/93427594/235285894-27807724-9bb7-4d5a-bf85-27df6e8773e5.png)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
