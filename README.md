# Implementation-of-Erosion-and-Dilation
### NAME : V RAKSHA DHARANIKA
### REG NO: 212223230167
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
Step 1: Import the necessary libraries like OpenCV and NumPy.
Step 2: Create a blank image and draw text on it using cv2.putText().
Step 3: Create a structuring element using cv2.getStructuringElement().
Step 4: Apply erosion to the image using cv2.erode().
Step 5: Apply dilation to the image using cv2.dilate().
Step 6: Display the input, eroded, and dilated images.


## Program:

``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'L yagnesh' ,(5,70),font,4,(255),2,cv2.LINE_AA)


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
![image](https://github.com/user-attachments/assets/d2c451de-4d51-4fd5-aa5e-41a35748f271)


### Display the Eroded Image
![image](https://github.com/user-attachments/assets/18844b08-ea3c-47d6-92df-f25a5382c66e)

### Display the Dilated Image
![image](https://github.com/user-attachments/assets/8499c5f0-ddf4-46ce-b301-c8a1a9a1998c)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
