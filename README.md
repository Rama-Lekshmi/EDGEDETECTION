# EXP-7 EDGE DETECTION

## Aim:

To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:

Anaconda - Python 3.7 .

## Algorithm:

### Step 1:

Import the required packages for further process.

### Step 2:

Read the image and convert the bgr image to gray scale image.

### Step 3:

Use any filters for smoothing the image to reduse the noise.

### Step 4:

Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step 5:

Display the filtered image using plot and imshow.
 
 
## Program:

```python 
## Developed by:Rama E.K.Lekshmi
## Register no:212222240082
# Import the packages and load the image, Convert to grayscale and remove noise:

import cv2
import matplotlib.pyplot as plt
image = cv2.imread("carss.jpg")
plt.imshow(image)
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)

```

```python

# SOBEL EDGE DETECTOR:

# SOBEL-X:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("carss.jpg")
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

```

```python

# SOBEL-Y:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("carss.jpg")
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

```

```python

# SOBEL-XY:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("carss.jpg")
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

```

```python

# LAPLACIAN EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("carss.jpg")
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

```

```python 

# CANNY EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("carss.jpg")
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

### INPUT IMAGE:

![DI7 1](https://github.com/Javith-farkhan/Edge-Detection/assets/94296805/6046e47d-95d2-4fd1-ad3c-109be0fec995)


### SOBEL EDGE DETECTOR:

### SOBEL-X:

![Di7 2](https://github.com/Javith-farkhan/Edge-Detection/assets/94296805/67806391-0c83-465d-8ee6-3a6d482ebe31)


### SOBEL-Y:

![Di7 3](https://github.com/Javith-farkhan/Edge-Detection/assets/94296805/a12cf668-ca37-4958-acca-eac59be047cf)


### SOBEL-XY:

![Di7 4](https://github.com/Javith-farkhan/Edge-Detection/assets/94296805/efc71567-1bd3-48ac-9bf2-ae51f519ccf7)



### LAPLACIAN EDGE DETECTOR:

![Di7 5](https://github.com/Javith-farkhan/Edge-Detection/assets/94296805/28b76459-b220-4be9-a9ae-6416342aae5e)


### CANNY EDGE DETECTOR:

![DI7 6](https://github.com/Javith-farkhan/Edge-Detection/assets/94296805/2484ac6d-d18c-4993-921b-7ffcd394c119)


## Result:

Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.


