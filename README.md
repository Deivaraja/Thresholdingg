# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:

Load the necessary packages.

### Step2:

Read the Image and convert to grayscale.


### Step3:

Use Global thresholding to segment the image.

### Step4:

Use Adaptive thresholding to segment the image.

### Step5:

Use Otsu's method to segment the image and display the results.

## Program


# Load the necessary packages
```
import cv2
import matplotlib.pyplot as plt
```




# Read the Image and convert to grayscale
```
image=cv2.imread('pic.jpeg')
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```
# Original image
```
plt.subplot(2,2,1)
plt.imshow(cv2.cvtColor(image,cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

# Use Global thresholding to segment the image
```
_,global_thresholded = cv2.threshold(gray_img, 127, 255, cv2.THRESH_BINARY)
```



# Use Adaptive thresholding to segment the image
```
adaptive_thresholded = cv2.adaptiveThreshold(gray_img, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
```



# Use Otsu's method to segment the image 
```
_,otsu_thresholded = cv2.threshold(gray_img, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```



# Global Thresholding

```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
# Adaptive Thresholding
```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
# Otsu's Method
```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
# Show the plot
```
plt.tight_layout()
plt.show()
```
## Output

### Original Image
<img width="245" height="166" alt="image" src="https://github.com/user-attachments/assets/5d28fe90-37b5-415b-a620-d0c1864bce44" />


### Global Thresholding
<img width="245" height="166" alt="image" src="https://github.com/user-attachments/assets/561eaeb5-a83e-4dd2-bedf-e8994df0e466" />


### Adaptive Thresholding
<img width="245" height="166" alt="image" src="https://github.com/user-attachments/assets/575fb780-afb2-41c2-bb86-6498fe8b40c9" />



### Optimum Global Thesholding using Otsu's Method
<img width="245" height="166" alt="image" src="https://github.com/user-attachments/assets/66b2fd33-1ca0-4945-9714-5691c15fbd14" />




## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
