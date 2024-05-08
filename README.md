# Ex 06 EDGE-DETECTION
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

## Output:
```
NAME: SASIRAJKUMAR T J
REGISTER NUMBER: 212222230137
```

```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("light.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

### SOBEL EDGE DETECTOR

## SOBEL X AXIS
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
![Screenshot 2024-05-08 211607](https://github.com/SASIRAJ27/EDGE-DETECTION/assets/113497176/d52f6cd3-d5de-420e-8eb0-0de939ad9cf9)



## SOBEL Y AXIS
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
![Screenshot 2024-05-08 211646](https://github.com/SASIRAJ27/EDGE-DETECTION/assets/113497176/049cb2ff-0fcb-4faf-b833-91f0ecdcb4dc)


## SOBEL XY AXIS
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
![Screenshot 2024-05-08 211702](https://github.com/SASIRAJ27/EDGE-DETECTION/assets/113497176/ccb71b25-0962-4798-99fb-da7e3933d3c2)


### LAPLACIAN EDGE DETECTOR
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
![Screenshot 2024-05-08 211708](https://github.com/SASIRAJ27/EDGE-DETECTION/assets/113497176/a5225259-3762-4b22-b991-8469a924e5eb)


### CANNY EDGE DETECTOR
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
![Screenshot 2024-05-08 211713](https://github.com/SASIRAJ27/EDGE-DETECTION/assets/113497176/0147e4c2-0d9c-4fbe-b21d-ca77a84d28f8)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
