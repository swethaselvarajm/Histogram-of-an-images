## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
# Developed By: SWETHA S
# Register Number: 212222230155

## Grayscale image and Color image:
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cat.jpg")
color_image = cv2.imread("bird.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Histogram of Grayscale image:
```
import numpy as np
import cv2
Gray_image = cv2.imread("DOG1.jpeg")
Color_image = cv2.imread("BIRD.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```

## Histogram of Color image:
```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```

## Histogram equalization of Grayscale image:
```

import cv2
gray_image = cv2.imread("BIRD.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image:

![Screenshot 2024-03-21 224759](https://github.com/swethaselvarajm/Histogram-of-an-images/assets/119525603/aff5d068-7fc3-459f-a411-99366974aa90)

![Screenshot 2024-03-21 224805](https://github.com/swethaselvarajm/Histogram-of-an-images/assets/119525603/a499c188-e826-4a10-8f8f-0f0959ef58c1)

### Histogram of Grayscale Image and any channel of Color Image:

![Screenshot 2024-03-21 230222](https://github.com/swethaselvarajm/Histogram-of-an-images/assets/119525603/d5530c73-6b3e-42e9-ab54-b3a6a6f8cf15)

![Screenshot 2024-03-21 230340](https://github.com/swethaselvarajm/Histogram-of-an-images/assets/119525603/55959a0b-9c5b-417d-b103-e1f444dd5f4d)

### Histogram Equalization of Grayscale Image:

![Screenshot 2024-03-21 230448](https://github.com/swethaselvarajm/Histogram-of-an-images/assets/119525603/a09d250b-b180-41ca-8f75-c7096451c383)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
