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
Developed By: SRIRAM S S
Register Number: 212222230150
```
```python
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

![Screenshot 2024-04-18 081943](https://github.com/Augustine0306/Histogram-of-an-images/assets/119404460/55fa6553-3d13-490a-8c92-a52a0664d2d8)


### Histogram of Grayscale Image and any channel of Color Image
## Grayscale Image

![image](https://github.com/Augustine0306/Histogram-of-an-images/assets/119404460/5f80a875-7088-4817-869b-2d86b139b425)
![image](https://github.com/Augustine0306/Histogram-of-an-images/assets/119404460/07cb8a4f-1255-42a5-bd2a-d9a2ce67fde8)

## Color Image
![image](https://github.com/Augustine0306/Histogram-of-an-images/assets/119404460/6e76a2e1-59dc-490f-a8eb-866be423b025)
![image](https://github.com/Augustine0306/Histogram-of-an-images/assets/119404460/a6d3c736-7d93-49bf-85b5-4d1b16250174)


### Histogram Equalization of Grayscale Image.

![image](https://github.com/Augustine0306/Histogram-of-an-images/assets/119404460/c3f4fcc1-8d5a-423d-9ff3-87d185352a4c)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
