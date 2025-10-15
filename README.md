# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1: Load the necessary packages.

### Step2: Read the Image and convert to grayscale.

### Step3: Use Global thresholding to segment the image.

### Step4: Use Adaptive thresholding to segment the image.

### Step5: Use Otsu's method to segment the image and display the results

## Program

# Load the necessary packages

```
import cv2
import matplotlib.pyplot as plt
```

# Read the Image and convert to grayscale

```
image=cv2.imread("C:\\Users\\admin\\OneDrive\\Desktop\\DIPT\\flwr1.jpeg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```

```
plt.subplot(2,2,1)
plt.imshow(cv2.cvtColor(image,cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

```
_,global_thresholded = cv2.threshold(gray_img, 127, 255, cv2.THRESH_BINARY)

adaptive_thresholded = cv2.adaptiveThreshold(gray_img, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)

_,otsu_thresholded = cv2.threshold(gray_img, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

```


# Use Global thresholding to segment the image

```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')

```


# Use Adaptive thresholding to segment the image

```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')

```

# Use Otsu's method to segment the image 

```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

```
## Output

### Original Image



<img width="743" height="313" alt="image" src="https://github.com/user-attachments/assets/d257390f-3e73-4e32-8e48-3fadbe8e143b" />


### Global Thresholding



<img width="831" height="285" alt="image" src="https://github.com/user-attachments/assets/40c098e4-372a-4d21-b210-b441d653a92b" />



### Adaptive Thresholding


<img width="752" height="312" alt="image" src="https://github.com/user-attachments/assets/89ca0fc4-f6f8-4a8e-b0c7-1c88245ef36e" />


### Optimum Global Thesholding using Otsu's Method


<img width="801" height="318" alt="image" src="https://github.com/user-attachments/assets/546b961e-83d4-4aa4-bcf5-b0fa9590ad59" />



## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
