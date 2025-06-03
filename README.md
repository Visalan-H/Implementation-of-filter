# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.

### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.

### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.

## Program:
### Developed By  :Visalan H
### Register Number:212223240183
</br>

### 1. Smoothing Filters

#### (i) Using Averaging Filter

```
kernel = np.ones((11, 11), np.float32) / 121
averaging_image = cv2.filter2D(image2, -1, kernel)
plt.figure(figsize=(10, 8))
plt.subplot(1, 2, 2)
plt.imshow(averaging_image)
plt.title("Averaging Filter Image")
plt.axis("off")
plt.show()
```

#### (ii) Using Weighted Averaging Filter
```
kernel1 = np.array([[1, 2, 1],
                    [2, 4, 2],
                    [1, 2, 1]]) / 16

weighted_average_image = cv2.filter2D(image2, -1, kernel1)
plt.figure(figsize=(10, 8))
plt.subplot(1, 2, 2)
plt.imshow(weighted_average_image)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()

```

#### (iii) Using Guassian Filter

```
gaussian_blur = cv2.GaussianBlur(image2, (11, 11), 0)
plt.figure(figsize=(10, 8))
plt.subplot(1, 2, 2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

#### (v) Using Median Filter
```
median_blur = cv2.medianBlur(image2, 11)
plt.figure(figsize=(10, 8))
plt.subplot(1, 2, 2)
plt.imshow(median_blur)
plt.title("Median Filter")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters
#### (i) Using Laplacian Linear Kernal

```
image1 = cv2.imread('ex5.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel3 = np.array([[0,1,0], [1, -4,1],[0,1,0]])
image5 =cv2.filter2D(image2, -1, kernel3)
plt.imshow(image5)
plt.title('Laplacian Kernel')
```
#### (ii) Using Laplacian Operator

```
laplacian = cv2.Laplacian(image2, cv2.CV_64F)
plt.figure(figsize=(10, 8))
plt.subplot(1, 2, 2)
plt.imshow(laplacian, cmap='gray')
plt.title("Laplacian Operator Image")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter

![image](https://github.com/user-attachments/assets/d375ddf7-bf4d-4f2e-b39f-b244378d1534)


ii)Using Weighted Averaging Filter

![image](https://github.com/user-attachments/assets/f0d6334e-ef56-4318-b8e6-4305a3478f69)


iii)Using Gaussian Filter

![image](https://github.com/user-attachments/assets/29c9341b-19b2-48ad-945a-d46866a8be4e)


iv) Using Median Filter

![image](https://github.com/user-attachments/assets/2ea07c87-7068-44f4-a1f6-fa203b1f4c42)


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernel

![image](https://github.com/user-attachments/assets/03064793-f8e2-4f4e-bc15-013d0141aa50)


ii) Using Laplacian Operator

![image](https://github.com/user-attachments/assets/a41d5b59-35a2-4a69-a839-f031e6b9f566)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
