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
Erode the image and Dilate the image.

 
## Program:

``` 
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
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Erode the image
eroded_image = cv2.erode(image, kernel, iterations=1)

# Dilate the image
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Convert images from BGR to RGB for Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)

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
![image](https://github.com/user-attachments/assets/38f9f411-2dec-49f3-b7fe-4e204f91df32)


### Display the Eroded Image
![image](https://github.com/user-attachments/assets/c8774dcd-f2cc-4228-9095-93c5d0eaf0aa)


### Display the Dilated Image
![image](https://github.com/user-attachments/assets/5c92cc29-617d-4517-b95b-28db435bde83)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
