# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>  Import the necessary packages


### Step2:
<br> Create the Text using cv2.putText

### Step3:
<br> Create the structuring element


### Step4:
<br> Erode the image

### Step5:
<br>  Dilate the image

 
## Program:

 Python
import cv2
import numpy as np
from matplotlib import pyplot as plt
imput_image='pic.png'
color_image=cv2.imread(imput_image)
gray_image=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)
edges=cv2.Canny(gray_image,100,200)
kernel_size=5
kernel=np.ones((kernel_size,kernel_size),np.uint8)
erosion=cv2.erode(edges,kernel,iterations=1)
dilation=cv2.dilate(edges,kernel,iterations=1)
plt.figure(figsize=(15,10))
plt.subplot(2,3,1)
plt.imshow(cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')
plt.subplot(2,3,2)
plt.imshow(gray_image,cmap='gray')
plt.title('black and white image')
plt.axis('on')
plt.subplot(2,3,3)
plt.imshow(edges,cmap='gray')
plt.title('edge segmentation')
plt.axis('on')
plt.subplot(2,3,4)
plt.imshow(edges,cmap='gray')
plt.title('erosion')
plt.axis('on')
plt.subplot(2,3,5)
plt.imshow(edges,cmap='gray')
plt.title('dilation')
plt.axis('on')


## Output:
![WhatsApp Image 2024-04-12 at 10 16 08_8299a7cd](https://github.com/manojMKJ/erosion--dilation/assets/120717614/0824ebb8-85fe-450c-aae3-bf31511a6f01)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
