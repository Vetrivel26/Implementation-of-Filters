# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.

### Step2:
Average filter

kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
Weighted average filter

kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
Gaussian Blur

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
Median filter

median=cv2.medianBlur(image2,13)
### Step3:
For performing sharpening on a image. Laplacian Kernel

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
Laplacian Operator

laplacian=cv2.Laplacian(image2,cv2.CV_64F)
### Step4
Display all the images with their respective filters.


## Program:
### Developed By   :Aavula Tharun
### Register Number:212221240003

~~~
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("image.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)

~~~

### 1. Smoothing Filters

i) Using Averaging Filter
```
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()




```
ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()





```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()





```

iv) Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()





```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()




```
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()





```

## OUTPUT:
### 1. Smoothing Filters

i) Using Averaging Filter

![ex  06-1](https://user-images.githubusercontent.com/93427201/168214918-79ed2077-4f9c-41e0-b937-de6f5209e744.png)

ii) Using Weighted Averaging Filter


![ex  06-2](https://user-images.githubusercontent.com/93427201/168214931-404dde51-73a0-4b00-a6f2-a5c5728093ff.png)


iii) Using Gaussian Filter

![ex 06-3](https://user-images.githubusercontent.com/93427201/168214939-e3227280-c5c4-40fb-81cf-34a7b5fe8bda.png)


iv) Using Median Filter

![ex 06-4](https://user-images.githubusercontent.com/93427201/168214945-f62f642f-9abc-4900-98aa-c6eb956943d0.png)


### 2. Sharpening Filters


i) Using Laplacian Kernal

![ex 06-5](https://user-images.githubusercontent.com/93427201/168214956-c883fd45-950d-48e0-879d-95106deb1489.png)


ii) Using Laplacian Operator

![ex 06-6](https://user-images.githubusercontent.com/93427201/168214970-ac748d4b-38b7-4902-b144-0c5eacc15394.png)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
