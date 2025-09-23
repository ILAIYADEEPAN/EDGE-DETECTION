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
### ORIGINAL IMAGE
```
NAME : SANJEEV RAJ.S
REG NO : 212223220096



import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Shanks.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### ORIGINAL IMAGE
<img width="415" height="466" alt="Screenshot 2025-09-23 154814" src="https://github.com/user-attachments/assets/dd777b2c-d133-49e0-8d2b-3c3b4592b147" />



### SOBEL EDGE DETECTOR
<img width="478" height="478" alt="Screenshot 2025-09-23 154827" src="https://github.com/user-attachments/assets/3664fee9-1903-4900-80cc-98e6eeaa0dc9" />



### LAPLACIAN EDGE DETECTOR
<img width="402" height="471" alt="Screenshot 2025-09-23 154845" src="https://github.com/user-attachments/assets/a130982d-5cde-49cf-ab10-a73011821b37" />


### CANNY EDGE DETECTOR
<img width="395" height="481" alt="Screenshot 2025-09-23 154854" src="https://github.com/user-attachments/assets/00d2259f-23b4-45b4-bbff-056ac3b20beb" />



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
