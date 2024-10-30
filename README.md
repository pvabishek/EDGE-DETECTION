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
## program:
## DEVELOPED BY:ABISHEK PV
## REGISTER NUMBER: 212222230003
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('download.jpeg')  # Replace with your image path
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## SOBEL EDGE DETECTOR:
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
## LAPLACIAN EDGE DETECTOR:
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
## CANNY EDGE DETECTOR:
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```


## Output:
### ORIGINAL IMAGE:
![download](https://github.com/user-attachments/assets/ba93fc40-e8f4-42e3-8505-984e9b82a2cf)

### SOBEL EDGE DETECTOR
![download](https://github.com/user-attachments/assets/50dc310a-cd1a-4340-821f-ee976d12e266)


### LAPLACIAN EDGE DETECTOR
![download](https://github.com/user-attachments/assets/22ab1bc4-595e-4cf9-963f-5fc2ad8685e1)



### CANNY EDGE DETECTOR
![download](https://github.com/user-attachments/assets/39a01514-3456-4e5c-8fcc-93e2131ebb1a)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
