# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:S.ANUSHARON
### Register Number: 212222240010

### i) Read and display the image
```
import cv2
color_image=cv2.imread('dog.jpg',1)
cv2.imshow('212222240010 S.ANUSHARON',color_image)
cv2.waitKey(0)
```
Output:
![WhatsApp Image 2024-02-28 at 7 12 30 AM](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/9059a528-45e8-4d6a-8e4b-ab56a16e05e8)

### ii)Write the image
```
import cv2
img = cv2.imread('dog.jpg', 1)
new_img = cv2.imwrite('rose.jpg', img)
cv2.imshow('212222240010_S.ANUSHARON', img)
cv2.waitKey(0)
```
Output:
![WhatsApp Image 2024-02-28 at 7 11 38 AM](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/306e9d5a-3383-4614-af07-4c70f39daf1f)


### iii)Shape of the Image
```

import cv2
img = cv2.imread('dog.jpg', 1)
print(img.shape)

```
Output:
![WhatsApp Image 2024-02-28 at 7 11 30 AM](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/9d94285b-8da7-4e85-bf3e-ae69836d6d4f)


### iv)Access rows and columns
```
import cv2
import random
img = cv2.imread('dog.jpg', 1)
for i in range(100):
    for j in range(img.shape[1]):
        img[i][j] = [random.randint(0, 255), random.randint(0, 255), random.randint(0, 255)]
cv2.imshow('part image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
Output:
![WhatsApp Image 2024-02-28 at 7 12 23 AM](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/141bcc26-1d84-4975-9c80-2d8dfba6a77a)


### v)Cut and paste portion of image
```

import cv2
img = cv2.imread('dog.jpg', 1)
tag = img[200:400, 200:400]
img[100:300,100:300] = tag
cv2.imshow('212222240010', img)
cv2.waitKey(0)

```
Output:
![WhatsApp Image 2024-02-28 at 7 12 17 AM](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/2f73c230-9e6b-480b-8a0d-9f51701ab566)

### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('dog.jpeg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
Output:
![WhatsApp Image 2024-02-28 at 7 12 12 AM](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/fefdce02-7843-4100-954b-288f6e3078af)

### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('dog.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
Output:
![WhatsApp Image 2024-02-28 at 7 12 05 AM](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/eb94f0af-a72a-481a-9bab-2fd60a083240)

### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('dog.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
Output:
![WhatsApp Image 2024-02-28 at 7 11 58 AM](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/304c9f50-6d2c-4aed-a4d4-028a810ed175)


### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('dog.jpg',1)
img = cv2.resize(img,(300,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
Output:
![WhatsApp Image 2024-02-28 at 7 11 52 AM](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/af0eb1a5-ca2e-4fa2-9b3d-57476e58e6b1)


### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("dog.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
Output:

![WhatsApp Image 2024-02-28 at 7 11 46 AM](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/ca694af7-cfb8-4b0c-baac-e41c7045d4a4)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







