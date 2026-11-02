# Edge-Detection
# edge-detection-opencv
# Name: ABINAYA A
# Reg no:212224230004

## Aim

To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

---

## Software Required

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (cv2)  
- NumPy  
- Matplotlib  

---

## ⚙️ Algorithm

### Step 1:
Import all the necessary modules for the program.

### Step 2:
Load an image using `cv2.imread()`.

### Step 3:
Convert the image to grayscale.

### Step 4:
Apply **Sobel operator** using OpenCV to detect edges.

### Step 5:
Apply **Prewitt operator** using custom kernels.

### Step 6:
Apply **Roberts operator** using custom kernels.

### Step 7:
Apply **Laplacian operator** using OpenCV.

### Step 8:
Apply **Canny edge detector** using OpenCV.

### Step 9:
Display all edge-detected images for comparison.

---

## Developed By

  ## Name: Abinaya A
  ### Register No: 212224230004

---

## Output
## Original Image:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('strawberry.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## OUTPUT:
<img width="587" height="350" alt="image" src="https://github.com/user-attachments/assets/e6b2e517-49b5-4c42-a2f8-5c40e0295f23" />





### Sobel Edge Detector:
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
## OUTPUT:
<img width="593" height="347" alt="image" src="https://github.com/user-attachments/assets/1dacf07b-22c7-4e80-9dfa-3c6a8e4f4edc" />



### Laplacian Edge Detector:
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
## OUTPUT:
<img width="615" height="345" alt="image" src="https://github.com/user-attachments/assets/44aaec08-a098-4d81-a5e6-075ffc0679f6" />





### Canny Edge Detector:
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## OUTPUT:
<img width="596" height="337" alt="image" src="https://github.com/user-attachments/assets/7afac2ca-f276-46f1-bc9d-de296034b27d" />



## Result

Thus, edges are successfully detected using Sobel, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
