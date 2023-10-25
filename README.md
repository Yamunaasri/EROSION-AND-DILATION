# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary libraries (OpenCV and NumPy).

### Step2:
Use cv2.putText to add the text to the img1 image at specific coordinates.

### Step3:
Define two kernels (kernel and kernel1) for morphological operations.

### Step4:
Display the eroded image using cv2.imshow.

### Step5:
Use cv2.waitKey(0) to wait for a key press indefinitely.
 
## Program:
```
DEVELOPED BY: YAMUNAASRI T S
REG NO: 212222240117
```
### Import the necessary packages
```
import cv2
import numpy as np
```
### Create the Text using cv2.putText
```
img1=np.zeros((100,400),dtype="uint8")
font=cv2.FONT_HERSHEY_PLAIN
cv2.putText(img1,"YAMUNAASRI T S",(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("image",img1)
cv2.waitKey(0)
```
### Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
### Erode the image
```
cv2.erode(img1, kernel)
image_erode = cv2.erode(img1,kernel1)
cv2.imshow("YAMUNAASRI T S",image_erode)
cv2.waitKey(0)
```
### Dilate the image
```
image_dilatel=cv2.dilate(img1,kernel1)
cv2.imshow("YAMUNAASRI T S",image_dilatel)
cv2.waitKey(0)
```
## Output:

### Display the input Image
![Screenshot 2023-10-25 160326](https://github.com/Yamunaasri/EROSION-AND-DILATION/assets/115707860/e9d36cc9-4b66-48ec-9ea3-ec742cbfd758)


### Display the Eroded Image
![Screenshot 2023-10-25 160334](https://github.com/Yamunaasri/EROSION-AND-DILATION/assets/115707860/11b017e3-1f14-4b6e-a552-9ba8561904aa)


### Display the Dilated Image
![Screenshot 2023-10-25 160348](https://github.com/Yamunaasri/EROSION-AND-DILATION/assets/115707860/af398885-ea98-4bc3-91d1-b960bce73739)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
