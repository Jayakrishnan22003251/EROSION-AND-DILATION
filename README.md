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


### Import the necessary packages
```import cv2
import numpy as np
from google.colab.patches import cv2_imshow
```


### Create the Text using cv2.putText
```
img1 = np.zeros((100, 400), dtype="uint8")
font = cv2.FONT_HERSHEY_PLAIN
cv2.putText(img1, "JAYAKRISHNAN", (5, 70), font, 2, 255, 5, cv2.LINE_AA)
cv2_imshow(img1)

```


### Create the structuring element
```
kernel = np.ones((5, 5), np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS, (7, 7))

```


### Erode the image
```
image_erode = cv2.erode(img1, kernel)
cv2_imshow(image_erode)
```



# Dilate the image

```
image_dilate = cv2.dilate(img1, kernel1)
cv2_imshow(image_dilate)

```
## Output:

### Display the input Image
![image](https://github.com/Jayakrishnan22003251/EROSION-AND-DILATION/assets/120232371/41835801-f231-48a7-be6e-12d8d349366e)


### Display the Eroded Image
![image](https://github.com/Jayakrishnan22003251/EROSION-AND-DILATION/assets/120232371/2ca0b442-f451-4d9c-ad62-a29e5ec327f7)


### Display the Dilated Image
![image](https://github.com/Jayakrishnan22003251/EROSION-AND-DILATION/assets/120232371/d826ee78-f267-4579-9e5a-9739f00d4853)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
