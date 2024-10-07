# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the Text using cv2.putText
### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation



 
## Program:
```
Name : Vikash s
Register no : 212222240115
```

#### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

#### Read and show the Original image
``` Python
image = cv2.imread("fingerprint.png")
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```



#### Use Opening operation
```py

opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```


#### Use Closing Operation
```py


closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")


```
## Output:

### Display the Original Image

![image](https://github.com/user-attachments/assets/34ad87e0-c6cf-4085-9025-16a32dc420e4)


### Display the result of Opening

![image](https://github.com/user-attachments/assets/705ea6d0-3f5d-4012-b631-e7eb49c06c75)


### Display the result of Closing

![image](https://github.com/user-attachments/assets/36fccd7c-4c08-47d4-a1e3-2a4c051fc9f4)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
