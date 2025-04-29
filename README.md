# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```
# Developed By: Elamaran S E
# Register Number: 212222230036
```
### Input Grayscale Image and Color Image
```python
import cv2
import numpy as np
from matplotlib import pyplot as plt
image = cv2.imread('light.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('on')
```
```python
image1 = cv2.imread('dark.jpg')
gray_image1 = cv2.cvtColor(image1, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image1, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('on')
```
### Histogram of Grayscale Image and any channel of Color Image
```python
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original)
plt.title('Original Histogram')
plt.xlim([0, 256])
```
```python
hist_original1 = cv2.calcHist([gray_image1], [0], None, [256], [0, 256])
plt.plot(hist_original1)
plt.title('Original Histogram')
plt.xlim([0, 256])
```
### Histogram Equalization of Grayscale Image
```python
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('on')
```
```python
equalized_image1 = cv2.equalizeHist(gray_image1)
plt.imshow(equalized_image1, cmap='gray')
plt.title('Equalized Image')
plt.axis('on')
```
```python
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized)
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
```python
hist_equalized1 = cv2.calcHist([equalized_image1], [0], None, [256], [0, 256])
plt.plot(hist_equalized1)
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/c6a0c0e2-083f-4252-b80a-57965edd46ff)

![image](https://github.com/user-attachments/assets/e56ad634-6632-4fc5-9f7a-bb03d1dc350f)



### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/user-attachments/assets/7bc92de7-dada-4a81-bacc-ddf6b299f07a)

![image](https://github.com/user-attachments/assets/2a77eb75-7924-4c9f-9911-e8edb0763a66)




### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/642b9e61-eb9a-4077-8084-13ea25c4b294)

![image](https://github.com/user-attachments/assets/07cf20f2-8322-4f09-965c-ef8b2eae56ae)

![image](https://github.com/user-attachments/assets/33b02ae1-e8fb-4b09-b081-3b897f1cf1ce)

![image](https://github.com/user-attachments/assets/5c00d3be-c897-49f3-9461-d9877f1e566e)






## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
