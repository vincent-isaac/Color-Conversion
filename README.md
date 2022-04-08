# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:
```python
# Developed By:
# Register Number:
# i) Convert BGR and RGB to HSV and GRAY

import cv2
image=cv2.imread('1.jpg')
hsv_img = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_img)
hsv1_img = cv2.cvtColor(image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv1_img)
gray_img = cv2.cvtColor(image, cv2.COLOR_RGB2GRAY)
gray1_img = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
cv2.imshow('RGB2GRAY',gray_img)
cv2.imshow('BGR2GRAY',gray1_img )
cv2.waitKey(0)
cv2.destroyAllWindows



# ii)Convert HSV to RGB and BGR


import cv2
image=cv2.imread('1.jpg')
hsv_img = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_img)
hsv1_img = cv2.cvtColor(hsv_img, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB',hsv1_img)
hsv2_img = cv2.cvtColor(image, cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2GRAY',hsv2_img)
cv2.waitKey(0)
cv2.destroyAllWindows


# iii)Convert RGB and BGR to YCrCb




# iv)Split and Merge RGB Image




# v) Split and merge HSV Image




```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>
<br>

### ii) HSV to RGB and BGR
<br>
<br>

### iii) RGB and BGR to YCrCb
<br>
<br>

### iv) Split and merge RGB Image
<br>
<br>

### v) Split and merge HSV Image
<br>
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
