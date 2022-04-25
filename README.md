# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read two images, Color image and Gray Scale image.
### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.
### Step3:
Display the histograms with their respective images.
### Step4:

Equalize the grayscale image.
### Step5:
Display the grayscale image.

## Program:
```python
# Developed By: Kumaravel V
# Register Number:212220230027
```
```python


# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('parrot.png')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()




# Display the histogram of gray scale image and any one channel histogram from color image

import cv2
import matplotlib.pyplot as plt
Color_image=cv2.imread('dog.jpg')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()



# Write the code to perform histogram equalization of the image. 
import cv2
Gray_image=cv2.imread('parrot.png',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()






```
## Output:
### Input Grayscale Image and Color Image


![Screenshot (101)](https://user-images.githubusercontent.com/75234946/165026204-4c113c34-d3a5-41dd-bd17-d5405a49e035.png)

### Histogram of Grayscale Image and any channel of Color Image
![Screenshot (102)](https://user-images.githubusercontent.com/75234946/165026020-13c6bde9-6e1e-4f3c-afe4-2677feffaac8.png)

### Histogram Equalization of Grayscale Image
![Screenshot (97)](https://user-images.githubusercontent.com/75234946/165025922-15a56ef6-7cbe-4232-8e92-aaa180dc41ae.png)
## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
