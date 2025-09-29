# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
### PROGRAM
```
NAME:P.Senthil Arunachalam
REG NO:212224240147
EXP:6.EDGE DETECTION

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('Tiger.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

#SOBEL EDGE DETECTOR
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')

#LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

#CANNY EDGE DETECTOR
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### ORIGINAL IMAGE

<img width="749" height="466" alt="original_image" src="https://github.com/user-attachments/assets/e15fd8ce-cff4-4bbc-8c61-8f168038752c" />

### SOBEL EDGE DETECTOR

<img width="686" height="474" alt="sobel_edge" src="https://github.com/user-attachments/assets/038f03cb-d527-4be6-accb-49d4a43e00e7" />

### LAPLACIAN EDGE DETECTOR

<img width="637" height="456" alt="Laplacian_edge" src="https://github.com/user-attachments/assets/d65472d8-996e-4b2d-937f-7b5badfcd768" />

### CANNY EDGE DETECTOR

<img width="684" height="460" alt="canny_edge" src="https://github.com/user-attachments/assets/0f6770f8-b781-46e4-8c67-c02ace25785f" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
