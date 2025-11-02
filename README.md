# EDGE-DETECTION
# Name:P.Senthil Arunachalam
# Reg No:212224240147
# Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

# Software Required:
Anaconda - Python 3.7

# Algorithm:
Step1:
Import all the necessary modules for the program.

Step2:
Load a image using imread() from cv2 module.

Step3:
Convert the image to grayscale

Step4:
Using Sobel operator from cv2,detect the edges of the image.

Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.


# Program:
```
# Name:P.Senthil Arunachalam
# Reg No:212224240147
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('/content/birds.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY
```
```
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
```
# SOBEL EDGE DETECTOR
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
```
# LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
```
# CANNY EDGE DETECTOR
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  

```

## Output:

# ORIGINAL IMAGE

<img width="473" height="281" alt="Screenshot 2025-11-02 125510" src="https://github.com/user-attachments/assets/18028ee1-fe41-43c6-8430-20f0efddc3fb" />

### SOBEL EDGE DETECTOR

<img width="471" height="275" alt="Screenshot 2025-11-02 125522" src="https://github.com/user-attachments/assets/751cc7cc-fe69-4502-92a0-392d0e958965" />


### LAPLACIAN EDGE DETECTOR
<img width="479" height="292" alt="Screenshot 2025-11-02 125535" src="https://github.com/user-attachments/assets/dc97d834-78e7-4a6c-a863-e8257ddd30c2" />


### CANNY EDGE DETECTOR

<img width="464" height="277" alt="Screenshot 2025-11-02 125543" src="https://github.com/user-attachments/assets/062006d9-520f-4b1c-8eb2-13345763bca7" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
