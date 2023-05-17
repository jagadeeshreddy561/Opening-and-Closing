# OPENING AND CLOSING

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Use Opening operation.
### Step 5:
Use Closing Operation.

## PROGRAM:
```
/*
Developed by   : Jagadeeshreddy561
Register Number: 212222240062
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Kavya',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()

```
## OUTPUT:

### Display the input Image
![download](https://github.com/jagadeeshreddy561/Opening-and-Closing/assets/120623104/4be602a5-4a9e-439f-93c1-10f45ce06ec7)

### Display the result of Opening
![download](https://github.com/jagadeeshreddy561/Opening-and-Closing/assets/120623104/720ea63d-6d6a-4a12-ac0b-14e3ce753e16)


### Display the result of Closing
![download](https://github.com/jagadeeshreddy561/Opening-and-Closing/assets/120623104/9cd9d909-393a-45fb-8b40-3bba0d1f0131)


## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
