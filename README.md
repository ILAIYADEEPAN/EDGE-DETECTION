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
NAME : ILAIYADEEPAN K
REG NO : 212223230080


import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Ilaiya.jpg')
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
<img width="289" height="405" alt="image" src="https://github.com/user-attachments/assets/322736db-a4c5-4764-b5e2-df51ff68d592" />




### SOBEL EDGE DETECTOR
<img width="287" height="413" alt="image" src="https://github.com/user-attachments/assets/0056aee6-687f-4f34-a5f1-96cde484304b" />




### LAPLACIAN EDGE DETECTOR
<img width="290" height="405" alt="image" src="https://github.com/user-attachments/assets/b676a995-8dab-4bd7-b883-d62e4134c443" />



### CANNY EDGE DETECTOR
<img width="288" height="406" alt="image" src="https://github.com/user-attachments/assets/63615009-ab33-475a-9a26-b5596c2c650a" />




## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
