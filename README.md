# EX. NO: 10
# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import all the necessary modules and libraries.

### Step2:
Create a blank image. Then Add text on the image using cv2.putText.

### Step3:
Create a simple square kernel (3x3). Display the input image.

### Step4:
Opening is erosion followed by dilation. Display the result of Opening.

### Step5:
Closing is dilation followed by erosion.

 
## Program:
Developed by: NAME - NANDIKA S
REGISTER NO - 212224230175

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Create the Text using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, '212224230175', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')

# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
```
## Output:

### Display the input Image with text
<img width="530" height="562" alt="image" src="https://github.com/user-attachments/assets/d307d577-968c-45af-8e50-9702e1a35839" />

### Display the result of Opening Operation
<img width="517" height="554" alt="image" src="https://github.com/user-attachments/assets/f8b666c7-096d-4efd-869f-4b1d6a101713" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
