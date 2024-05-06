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
```python
# Developed By: Kothai K
# Register Number: 212222240051
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cat1.jpg")
color_image = cv2.imread("cat2.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```python
import numpy as np
import cv2
Gray_image = cv2.imread("cat1.jpg")
Color_image = cv2.imread("cat2.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
```python
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
```python
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
```python
import cv2
gray_image = cv2.imread("cat1.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/KothaiKumar/Histogram-of-an-images/assets/121215739/0999e2d6-53d4-490d-a73b-d9c8d4bb0b9b)

### Input Grayscale Image and Color Image

![image](https://github.com/KothaiKumar/Histogram-of-an-images/assets/121215739/b3d21d66-6989-48f8-8c91-1d29132eac03)
![image](https://github.com/KothaiKumar/Histogram-of-an-images/assets/121215739/e3d6dba3-2c24-4f09-a4f7-2c5649026885)


### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/KothaiKumar/Histogram-of-an-images/assets/121215739/b483b449-081e-46ca-aee8-3eb1fbf2a51a)
![image](https://github.com/KothaiKumar/Histogram-of-an-images/assets/121215739/6d1859e8-4ee9-44b2-9513-88d1d6453c62)
### Histogram Equalization of Grayscale Image.
![image](https://github.com/KothaiKumar/Histogram-of-an-images/assets/121215739/799b937f-0ace-488d-9ebc-9f6636530f83)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
