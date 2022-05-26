# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Import the required modules.

</br> 

### Step2
</br>
Convert the image from BGR to RGB.

</br> 

### Step3
</br>
Apply the required filters for the image separately.

</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot

</br> 

### Step5
</br>
End the program.

</br> 

## Program:
### Developed By   :
### Register Number:
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("flower.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)

kernel1 = np.ones((11,11),np.float32)/121
avg_filter = cv2.filter2D(original_image,-1,kernel1)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(avg_filter)
plt.title("Filtered")
plt.axis("off")


```
ii) Using Weighted Averaging Filter
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("flower.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(weighted_filter)
plt.title("Filtered")
plt.axis("off")




```
iii) Using Gaussian Filter
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("flower.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Filtered")
plt.axis("off")




```

iv) Using Median Filter
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("flower.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
median = cv2.medianBlur(src=original_image,ksize = 11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Filtered")
plt.axis("off")




```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("flower.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Filtered")
plt.axis("off")




```
ii) Using Laplacian Operator
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("flower.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title("Filtered")
plt.axis("off")




```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
![1](https://user-images.githubusercontent.com/93427286/170527466-c6a620d5-6045-4e32-92d4-5de05eaf6efb.jpg)



ii) Using Weighted Averaging Filter
</br>
![2](https://user-images.githubusercontent.com/93427286/170527508-0ae182ac-b9b5-4023-8dab-55333d8df921.jpg)

</br>


iii) Using Gaussian Filter
</br>
![3](https://user-images.githubusercontent.com/93427286/170527591-8724a6e9-d555-4f80-9aee-948404e38190.jpg)

</br>


iv) Using Median Filter
</br>
![4](https://user-images.githubusercontent.com/93427286/170527631-a894050d-2d4d-44b6-9f21-b5c9e69c19d6.jpg)

</br>


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
![5](https://user-images.githubusercontent.com/93427286/170527704-88e945ae-dfbd-4967-9e3e-628369426a06.jpg)

</br>


ii) Using Laplacian Operator
</br>
![6](https://user-images.githubusercontent.com/93427286/170527748-0f7f3f26-e639-4d32-a388-1976ac3e2d82.jpg)

</br>


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
