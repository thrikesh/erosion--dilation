# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the Text using cv2.putText

### Step4:
Create the structuring element

### Step5:
Erode the image and Erode the image.

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Create a blank image
image = np.zeros((300, 600, 3), dtype="uint8")


# Create the Text using cv2.putText
# Step 2: Create the text using cv2.putText
text = "THRIKESWAR"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)


# Create the structuring element
# Step 3: Create a structuring element (5x5 rectangular)
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))


# Erode the image
# Step 4: Erode the image
eroded_image = cv2.erode(image, kernel, iterations=1)


# Dilate the image
# Step 5: Dilate the image
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Plot the original, eroded, and dilated images using Matplotlib
plt.figure(figsize=(10, 5))

plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

plt.figure(figsize=(10, 5))
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")

plt.figure(figsize=(10, 5))
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")
```

## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/3924eaf8-21ec-4ebc-ba14-8800d2d34c9d)


### Display the Eroded Image
![image](https://github.com/user-attachments/assets/f54bdd0e-16a0-422a-a790-99cce3a9be78)


### Display the Dilated Image
![image](https://github.com/user-attachments/assets/6b44ee23-16bf-4da0-844d-7604d00bd470)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
