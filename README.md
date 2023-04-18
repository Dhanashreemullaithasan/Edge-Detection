# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.

### Step2:
Read the image and convert the bgr image to gray scale image.

### Step3:
Use any filters for smoothing the image to reduse the noise.

### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step5:
Display the filtered image using plot and imshow.
 
## Program:

``` Python

# SOBEL EDGE DETECTOR

## Sobel X:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("nat.jfif")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel-X")
plt.xticks([])
plt.yticks([])
plt.show()

## Sobel Y:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("nat.jfif")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel-Y")
plt.xticks([])
plt.yticks([])
plt.show()

## Sobel XY:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("nat.jfif")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelxy=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel-XY")
plt.xticks([])
plt.yticks([])
plt.show()

# LAPLACIAN EDGE DETECTOR

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("nat.jfif")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='Blues')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap='Blues')
plt.title("Laplacian")
plt.xticks([])
plt.yticks([])
plt.show()


# CANNY EDGE DETECTOR

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("nat.jfif")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
canny_edges = cv2.Canny(image, 120, 150)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(canny_edges,cmap='gray')
plt.title("Canny_edges")
plt.xticks([])
plt.yticks([])
plt.show()


```
## Output:
### SOBEL EDGE DETECTOR
## Sobel X:

![im1 dip7](https://user-images.githubusercontent.com/94165415/232846784-095c5796-8e1c-43de-8bf8-2f20d2788d36.jpg)

## Sobel Y:
![im2 dip7](https://user-images.githubusercontent.com/94165415/232849890-cdc85c18-c212-4a56-b9b7-8ea06ec877c9.jpg)

## Sobel XY:
![im3 dip7](https://user-images.githubusercontent.com/94165415/232856208-d93ab4ff-4589-48f2-87a1-92c0bb5fbeda.jpg)


### LAPLACIAN EDGE DETECTOR

![im4 dip](https://user-images.githubusercontent.com/94165415/232856521-e495127a-6531-475e-9df4-6dcb640631e3.jpg)


### CANNY EDGE DETECTOR

![im5 dip7](https://user-images.githubusercontent.com/94165415/232856612-d4cd1c4f-a64b-4561-9bdd-f396bc61976b.jpg)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
