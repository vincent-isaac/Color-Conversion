# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Read an image using imread() and Convert BGR and RGB to HSV and GRAY using: cv2.cvtColor(image,cv2.COLOR_RGB2HSV) cv2.cvtColor(image,cv2.COLOR_RGB2GRAY) cv2.cvtColor(image,cv2.COLOR_BGR2HSV) cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
<br>

### Step2:
Convert HSV to RGB and BGR using: cv2.cvtColor(image,cv2.COLOR_HSV2RGB) cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
<br>

### Step3:
Convert RGB and BGR to YCrCb using: cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb) cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
<br>

### Step4:
Split and Merge RGB Image using: blue = image[:,:,0] green = image[:,:,1] red = image[:,:,2] cv2.merge((blue,green,red))
<br>

### Step5:
 Split and merge HSV Image using: hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV) h, s, v = cv2.split(hsv) cv2.merge((h,s,v))
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
<br>
![1](https://user-images.githubusercontent.com/75234588/162611385-6c8bc150-5206-407c-9c5b-bc7d0e41c5c1.png)
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
![5](https://user-images.githubusercontent.com/75234588/162610920-b92833e4-1295-4d05-880c-8577dd4a4bf7.png)
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
