# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the necessary libraries and read the original image and save it as a image variable.
### Step 2:
Translate the image.
### Step 3:
Scale the image.
### Step 4:
Shear the image.
### Step 5:
Reflect of the image.
### Step 6:
Rotate the image

## Program:
```
Developed By: Aakash S
Register Number: 212221240001
```
## i)Original Image:
```python
# To show the original image and to find the shape of the image
import cv2
import numpy as np
img = cv2.imread('cat.jpg',-1)
original = cv2.cvtColor(img , cv2.COLOR_BGR2RGB)
cv2.imshow('input',original)
cv2.waitKey(0)
cv2.destroyAllWindows()
original.shape
row, col, dim =original.shape
```
## ii)Image Translation
```python
translation = np.float32([[1,0,100],[0,1,150],[0,0,1]])
translated_image = cv2.warpPerspective(original,translation,(col,row))
cv2.imshow('translated_image',translated_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## iii)Image shearing
```python
shear_x = np.float32([[1,0.7,0],[0,1,0],[0,0,1]])
shear_y = np.float32([[1,0,0],[0.3,1,0],[0,0,1]])
sheared_x= cv2.warpPerspective(original,shear_x,(col,row))
sheared_y = cv2.warpPerspective(original,shear_y,(col,row))
cv2.imshow('shear_x',sheared_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('shear_y',sheared_y)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## iv)Image Reflection
```python
ref_x = np.float32([[1,0,0],[0,-1,row],[0,0,1]])
ref_y = np.float32([[-1,0,col],[0,1,0],[0,0,1]])
reflect_x= cv2.warpPerspective(original,ref_x,(col,row))
reflect_y = cv2.warpPerspective(original,ref_y,(col,row))
cv2.imshow('reflected_x',reflect_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('reflected_y',reflect_y)
cv2.waitKey(0)
cv2.destroyAllWindows()
```



## v)Image Rotation
```python
angle = np.radians(15)
mat_rotate = np.float32([[np.cos(angle),-
(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotate_img =cv2.warpPerspective(original,mat_rotate,(col,row))
cv2.imshow('rotated',rotate_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## vi)Image Cropping
```python
cropped_img=img[10:500,25:600] 
cv2.imshow('after_cropping',cropped_img);
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:

### original image
![input](https://github.com/JEEVAABI/IMAGETRANSFORMATION/assets/93427098/ec614892-dd85-4a1d-89ab-ca9ee13a1959)


### i)Image Translation
![trans](https://github.com/JEEVAABI/IMAGETRANSFORMATION/assets/93427098/629194bc-c782-4e26-995c-c86669183d6a)



### ii)Image shearing
![sheary](https://github.com/JEEVAABI/IMAGETRANSFORMATION/assets/93427098/cee05763-c9aa-4d4c-a056-1fc4bdf12827)
![shearx](https://github.com/JEEVAABI/IMAGETRANSFORMATION/assets/93427098/bfd29aa0-61ee-4f07-80e7-4e456a9c27b8)


### iii)Image Reflection
![refy](https://github.com/JEEVAABI/IMAGETRANSFORMATION/assets/93427098/1cdd38da-9f86-470b-831a-ff9c492f44d2)
![refx](https://github.com/JEEVAABI/IMAGETRANSFORMATION/assets/93427098/79be5f86-1eb6-4726-8aff-dd49b9d252aa)



### iv)Image Rotation
![rotate](https://github.com/JEEVAABI/IMAGETRANSFORMATION/assets/93427098/efdd2bb0-1089-49c1-8aa3-f43d9e15c7c4)



### v)Image Cropping
![crop](https://github.com/JEEVAABI/IMAGETRANSFORMATION/assets/93427098/fe03a6fb-1208-448b-8f3e-e4aeda8854a5)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
