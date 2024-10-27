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
Load the image using cv2.imread()
### Step3:
Create a structuring element (5x5 rectangular)
### Step4:
Use Opening operation
### Step5:
Use Closing operation
## Program:
#### Developed by : SRINITHI V
#### Register.No  : 212222110046
### Import the necessary packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the structuring element
```python
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
```
### Read and display the original image
```python
image = cv2.imread("happyfish.png")
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(10, 5))
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
plt.tight_layout()
plt.show()
```
### Output:
![image](https://github.com/user-attachments/assets/91ef3d9d-d090-4260-bf1d-1340c7db9cd0)

### Use Opening operation
```python
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(10, 5))
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
plt.tight_layout()
plt.show()
```
### Output:
![image](https://github.com/user-attachments/assets/ab709796-73e7-49bf-8200-7cbd6c9bb984)

### Use Closing Operation
```python
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(10, 5))
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")
plt.tight_layout()
plt.show()
```
### Output:
![image](https://github.com/user-attachments/assets/44691d3d-5587-4d22-9f0c-313eab7cf083)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
