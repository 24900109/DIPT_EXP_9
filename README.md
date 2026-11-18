# Implementation of Erosion and Dilation Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program

## Developed By

**Name: KIRUTHIKA N** 

**Register No: 212224230127** 
## Output

### Original Image

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("lotus.jpg")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()
```
<img width="658" height="405" alt="1" src="https://github.com/user-attachments/assets/ce2b4050-61c0-4776-b4ec-87c178ee79c9" />

### Erosion

```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
erosion = cv2.erode(img, kernel, iterations=1)
plt.imshow(erosion, cmap="gray")
plt.title("Image Erosion")
plt.axis("off")
plt.show()
```
<img width="662" height="417" alt="2" src="https://github.com/user-attachments/assets/d65db241-e731-46f4-b509-97b79f0d07ca" />


### Dilation

```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
dilation = cv2.dilate(img, kernel, iterations=1)
plt.imshow(dilation, cmap="gray")
plt.title("Image Dilation")
plt.axis("off")
plt.show()
```
<img width="665" height="410" alt="3" src="https://github.com/user-attachments/assets/1d101266-3e3a-49b4-a5d5-706f14f9a384" />


## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
