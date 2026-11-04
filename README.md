# Edge-Detection

# **Name:** KAMLESH P


# **Register Number:** 212225240067 

## Aim

To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required

- Anaconda - Python 3.7
- OpenCV
- NumPy
- Matplotlib

## Algorithm

### Step 1
Import all the necessary modules for the program.

### Step 2
Load an image using the `cv2.imread()` function.

### Step 3
Convert the image into grayscale using `cv2.cvtColor()`.

### Step 4
Use the Sobel operator from OpenCV to detect the edges of the image in the horizontal and vertical directions.

### Step 5
Use the Laplacian operator to detect edges based on second-order derivatives.

### Step 6
Use the Canny operator to detect edges in the image.

### Step 7
Display the edge-detected images using Matplotlib.

## Program

**Developed By:** SHRIVARSHAN P G

**Register Number:** 212225240146

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('sv.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')

laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output

### Input Image 


<img width="353" height="470" alt="Screenshot 2026-11-04 114738" src="https://github.com/user-attachments/assets/b9999db0-5589-46ac-b89f-ec2737cd2515" />


### 1. Sobel Edge Detector

<img width="344" height="471" alt="Screenshot 2026-11-04 114756" src="https://github.com/user-attachments/assets/2db2a1e9-8207-4119-826b-2f0718fbb0fc" />

### 2. Laplacian Edge Detector

<img width="336" height="470" alt="Screenshot 2026-11-04 114816" src="https://github.com/user-attachments/assets/82533c02-babe-4fbc-b598-fac8faa4aa77" />



### 3. Canny Edge Detector

<img width="353" height="469" alt="Screenshot 2026-11-04 114841" src="https://github.com/user-attachments/assets/ec432d33-6fd9-439d-afa3-09268c1cabe3" />


## Result

Thus, the edges of the image were detected successfully using Sobel, Laplacian, and Canny edge detectors with OpenCV and Python.
