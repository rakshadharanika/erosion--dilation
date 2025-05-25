# Implementation-of-Erosion-and-Dilation
### NAME : V RAKSHA DHARANIKA
### REG NO: 212223230167
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
Algorithm:
Step 1: Import the necessary libraries like OpenCV and NumPy.
Step 2: Create a blank image and draw text on it using cv2.putText().
Step 3: Create a structuring element using cv2.getStructuringElement().
Step 4: Apply erosion to the image using cv2.erode().
Step 5: Apply dilation to the image using cv2.dilate().
Step 6: Display the input, eroded, and dilated images.


## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np

# Create a black image
image = np.zeros((200, 600), dtype="uint8")

# Create the text using cv2.putText
cv2.putText(image, 'OpenCV', (50, 100), cv2.FONT_HERSHEY_SIMPLEX, 3, (255), 10)

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Erode the image
eroded = cv2.erode(image, kernel, iterations=1)

# Dilate the image
dilated = cv2.dilate(image, kernel, iterations=1)

# Output: Display the input Image
cv2.imshow("Original Image", image)

# Display the Eroded Image
cv2.imshow("Eroded Image", eroded)

# Display the Dilated Image
cv2.imshow("Dilated Image", dilated)

# Wait for a key press and close the image windows
cv2.waitKey(0)
cv2.destroyAllWindows()



```
## Output:

### Display the input Image
<br>
<br>
<br>
<br>
<br>
<br>

### Display the Eroded Image
<br>
<br>
<br>
<br>
<br>
<br>

### Display the Dilated Image
<br>
<br>
<br>
<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
