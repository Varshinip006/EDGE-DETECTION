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
## Program:
### ORIGINAL IMAGE:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('pigeon.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR:
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR:
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR:
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### ORIGINAL IMAGE:
<img width="240" height="363" alt="Screenshot 2025-10-15 115755" src="https://github.com/user-attachments/assets/436841a2-5855-414d-9a91-a6efada6b00a" />

### SOBEL EDGE DETECTOR:
<img width="234" height="362" alt="Screenshot 2025-10-15 115833" src="https://github.com/user-attachments/assets/0d6eb89e-dc41-4bd3-9f42-8d744b5fa2a3" />



### LAPLACIAN EDGE DETECTOR:
<img width="242" height="364" alt="Screenshot 2025-10-15 115900" src="https://github.com/user-attachments/assets/2cf883d5-22da-4e34-84c4-e7107401f50e" />



### CANNY EDGE DETECTOR:
<img width="250" height="370" alt="Screenshot 2025-10-15 115927" src="https://github.com/user-attachments/assets/e655e709-3453-4a30-b378-191bacf1d6a4" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
