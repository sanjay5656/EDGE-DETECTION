# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
```
Developed by : Sanjay S
Register no  : 212221243002
```

### Convert image to grayscale and remove noise:
```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("sanjay.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

### Sobel Edge Detector:
#### SOBEL X AXIS: 
```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```

#### SOBEL Y AXIS:
```python 
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```

#### SOBEL XY AXIS: 
```python 
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```

### laplacian edge Detector:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```

### Canny Edge Detector:
```python 
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR :
#### SOBEL X AXIS :
![out_1](https://github.com/sanjay5656/EDGE-DETECTION/assets/115128955/49751076-d5c3-4a2d-b962-4b1585db6b9e)

#### SOBEL Y AXIS :
![out_2](https://github.com/sanjay5656/EDGE-DETECTION/assets/115128955/3106fbc3-72bd-404e-813e-4ac6f7fdca7c)

#### SOBEL XY AXIS :
![out_3](https://github.com/sanjay5656/EDGE-DETECTION/assets/115128955/b76dcade-358f-48ae-8da5-dfb41894e512)

### LAPLACIAN EDGE DETECTOR :
![out_4](https://github.com/sanjay5656/EDGE-DETECTION/assets/115128955/220dd336-b37f-4d42-b085-c8764d29b8be)

### CANNY EDGE DETECTOR :
![out_5](https://github.com/sanjay5656/EDGE-DETECTION/assets/115128955/b5073429-d69c-4cf8-a18a-01fbb9b184ac)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
