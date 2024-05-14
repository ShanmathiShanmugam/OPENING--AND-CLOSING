# EXP-10 OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages
### Step2:
Give the input text using cv2.putText()
### Step3:
Perform opening operation and closing operations.
### Step4:
Display the result.

## Program:

### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```python
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Euphoria',(5,70), font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1)
plt.axis("off")
```
### Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
### Use Opening operation
```python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```
### Use Closing Operation
```python
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:

### Display the input Image
<br>
<img src="https://github.com/Jenishajustin/OPENING--AND-CLOSING/assets/119405070/d82f5eee-d2d2-4063-b643-a1bb8bd5a528" height=100 width=400>

<br>

### Display the result of Opening
<br>
<img src="https://github.com/Jenishajustin/OPENING--AND-CLOSING/assets/119405070/ef5d7ed9-f366-423b-bcea-796a11fbf308" height=100 width=400>

<br>

### Display the result of Closing
<br>
<img src="https://github.com/Jenishajustin/OPENING--AND-CLOSING/assets/119405070/3d64d0d2-c89d-446e-bbac-78f6c39a1564" height=100 width=400>

<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
