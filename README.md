# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Read an image using imread() and Convert BGR and RGB to HSV and GRAY using:<br>
cv2.cvtColor(image,cv2.COLOR_RGB2HSV) <br>
cv2.cvtColor(image,cv2.COLOR_RGB2GRAY) <br>
cv2.cvtColor(image,cv2.COLOR_BGR2HSV) <br>
cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
<br>

### Step2:
Convert HSV to RGB and BGR using: <br>
cv2.cvtColor(image,cv2.COLOR_HSV2RGB) <br>
cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
<br>

### Step3:
Convert RGB and BGR to YCrCb using: <br>
cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb) <br>
cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
<br>

### Step4:
Split and Merge RGB Image using: <br>
blue = image[:,:,0] <br>
green = image[:,:,1] <br>
red = image[:,:,2] <br>
cv2.merge((blue,green,red))
<br>

### Step5:
 Split and merge HSV Image using: <br>
 hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV) <br>
 h, s, v = cv2.split(hsv) <br>
 cv2.merge((h,s,v))
<br>

## Program:
```python
# Developed By:J Vincent isaac jeyaraj
# Register Number:212220230060
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

RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB_YCrCb_IMAGE",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR_YCrCb_IMAGE",BGR_YCrCb)
cv2.waitKey(0)



# iv)Split and Merge RGB Image

blue = image[:,:,0]
cv2.imshow("blue",blue)
green = image[:,:,1]
cv2.imshow("green",green)
red = image[:,:,2]
cv2.imshow("red",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("merged",merged)
cv2.waitKey(0)



# v) Split and merge HSV Image

hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("ORIGINAL HSV_IMAGE",hsv)
h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow('merged',mergedhsv)
cv2.waitKey(0)



```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>|
![1](https://user-images.githubusercontent.com/75234588/162613522-7a6e2bfb-8708-4f0f-8243-5209ef6aaed2.png)
<br>

### ii) HSV to RGB and BGR
<br>
![2](https://user-images.githubusercontent.com/75234588/162610905-a41caf0b-48bb-4094-9e27-b0c7e7f61bf1.png)
<br>

### iii) RGB and BGR to YCrCb
<br>
![3](https://user-images.githubusercontent.com/75234588/162610909-81e5e2a3-c932-4c41-b08c-5305831b8f3a.png)
<br>

### iv) Split and merge RGB Image
<br>
![4](https://user-images.githubusercontent.com/75234588/162610914-59c29fe1-4661-4136-8441-ec55ccee7fef.png)
<br>

### v) Split and merge HSV Image
<br>
![5](https://user-images.githubusercontent.com/75234588/162613418-1388f2ed-da89-452d-aabd-ab12363dc7eb.png)
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
