# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required modules.
</br>
</br> 

### Step2:
Convert the image from BGR to RGB.
</br>
</br> 

### Step3:
Apply the required filters for the image separately.
</br>
</br> 

### Step4:
Plot the original and filtered image by using matplotlib.pyplot.
</br>
</br> 

### Step5:
End the program.
</br>
</br> 

## Program:
### Developed By   : Manoj Guna Sundar Tella.
### Register Number: 212221240026.
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("car.jpeg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)

kernel1 = np.ones((11,11),np.float32)/121
avg_filter = cv2.filter2D(original_image,-1,kernel1)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(avg_filter)
plt.title("Filtered")
plt.axis("off")




```
ii) Using Weighted Averaging Filter
```
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(weighted_filter)
plt.title("Filtered")
plt.axis("off")





```
iii) Using Gaussian Filter
```
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Filtered")
plt.axis("off")





```

iv) Using Median Filter
```

median = cv2.medianBlur(src=original_image,ksize = 11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Filtered")
plt.axis("off")





```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```

kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Filtered")
plt.axis("off")





```
ii) Using Laplacian Operator
```

laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title("Filtered")
plt.axis("off")


```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
![par1](https://user-images.githubusercontent.com/94883876/168250196-f2f2e3d1-7481-4782-9790-ef9323efa1b3.png)

</br>
</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter
![par2](https://user-images.githubusercontent.com/94883876/168250439-13fec6b8-f8a5-483b-9f76-89f03f1e125e.png)

</br>
</br>
</br>
</br>
</br>

iii) Using Gaussian Filter
![par3](https://user-images.githubusercontent.com/94883876/168250487-56e28a8e-7fa9-4f08-bde1-0b4dc609cca4.png)

</br>
</br>
</br>
</br>
</br>

iv) Using Median Filter
![par4](https://user-images.githubusercontent.com/94883876/168250553-8a382092-1f84-4344-ba02-70a1771ab4a6.png)

</br>
</br>
</br>
</br>
</br>

### 2. Sharpening Filters
i) Using Laplacian Kernal
![par5](https://user-images.githubusercontent.com/94883876/168250892-bf679e78-5e95-4d0d-b954-4b303e9041f9.png)


</br>
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator
![par6](https://user-images.githubusercontent.com/94883876/168250643-4b4d0494-115c-4a7e-ad77-8fed6fce31e3.png)

</br>
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
