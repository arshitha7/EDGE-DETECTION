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

## Code :

## Original:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread("C:/Users/admin/Downloads/Digital images/ex_6_image.jpg")
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

```
## SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
## LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
## CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output:

## Original:

![image](https://github.com/user-attachments/assets/5b4448f4-e2ce-41b8-a76f-66ea2d42335c)


### SOBEL EDGE DETECTOR:
![image](https://github.com/user-attachments/assets/d126359e-42e2-41a1-8422-cf8fa6ebb5cb)



### LAPLACIAN EDGE DETECTOR:

![Screenshot 2025-04-24 134544](https://github.com/user-attachments/assets/9a9e96fc-1f8d-4d0f-9e96-c4506a7e6278)


### CANNY EDGE DETECTOR
![Screenshot 2025-04-24 134554](https://github.com/user-attachments/assets/f6565d42-ef7b-4623-a8fd-edf33333c2a9)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
