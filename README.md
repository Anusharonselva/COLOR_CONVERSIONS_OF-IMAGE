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
color_image=cv2.imread('rose.jpg',1)
cv2.imshow('212222230054_JEEVITHA',color_image)
cv2.waitKey(0)
```
Output:
![Screenshot (402)](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/0fe4ffbe-3dbe-44d4-8ff2-d645b8878c60)
### ii)Write the image
```
import cv2
img = cv2.imread('waterb.jpg', 1)
new_img = cv2.imwrite('rose.jpg', img)
cv2.imshow('212222230054_JEEVITHA', img)
cv2.waitKey(0)
```
Output:
![Screenshot (403)](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/b53b493d-d937-4079-b3c7-9238ac0334d7)

### iii)Shape of the Image
```

import cv2
img = cv2.imread('rose.jpg', 1)
print(img.shape)

```
Output:
![Screenshot (404)](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/2de31b38-85bc-409b-ab25-c39863d093ed)


### iv)Access rows and columns
```
import cv2
import random
img = cv2.imread('rose.jpg', 1)
for i in range(100):
    for j in range(img.shape[1]):
        img[i][j] = [random.randint(0, 255), random.randint(0, 255), random.randint(0, 255)]
cv2.imshow('part image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
Output:
![Screenshot (405)](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/633e2ba5-5b10-498c-8fab-736e60b0c5f3)

### v)Cut and paste portion of image
```

import cv2
img = cv2.imread('rose.jpg', 1)
tag = img[200:400, 200:400]
img[100:300,100:300] = tag
cv2.imshow('212222230054_jeevitha', img)
cv2.waitKey(0)

```
Output:
![Screenshot (406)](https://github.com/Anusharonselva/COLOR_CONVERSIONS_OF-IMAGE/assets/119405600/a2ee3b04-87b1-4694-b989-5cfe2b4a46f8)

### vi) BGR and RGB to HSV and GRAY
```
```

### vii) HSV to RGB and BGR
<br>
<br>

### viii) RGB and BGR to YCrCb
<br>
<br>

### ix) Split and merge RGB Image
<br>
<br>

### x) Split and merge HSV Image
<br>
<br>




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







