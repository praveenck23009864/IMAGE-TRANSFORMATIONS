# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import numpy module as np and pandas as pd.

### Step2:
Assign the values to variables in the program.

### Step3:
Get the values from the user appropriately.

### Step4:
Continue the program by implementing the codes of required topics.

### Step5:
Thus the program is executed in google collab.

## Program:
```
Developed By:HARINI V
Register Number:212222230044
```
i)Image Translation:
```python
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Function to display images in Colab
def show_image(image):
    plt.figure(figsize=(6, 6))
    plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
    plt.axis('off')
    plt.show()

# Load an image from URL or file path
image_url = 'dipt.jpeg'  
image = cv2.imread(image_url)

# Define translation matrix
tx = 50  # Translation along x-axis
ty = 30  # Translation along y-axis
translation_matrix = np.float32([[1, 0, tx], [0, 1, ty]])  # Create translation matrix

# Apply translation to the image
translated_image = cv2.warpAffine(image, translation_matrix, (image.shape[1], image.shape[0]))

# Display original and translated images
print("Original Image:")
show_image(image)
print("Translated Image:")
show_image(translated_image)
```



ii) Image Scaling
```python
#Install OpenCV library if not already installed
!pip install opencv-python-headless

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Function to display images in Colab
def show_image(image):
    plt.figure(figsize=(6, 6))
    plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
    plt.axis('off')
    plt.show()

# Load an image from URL or file path
image_url = 'dipt.jpeg'  # Replace with your image URL or file path
image = cv2.imread(image_url)

# Define scale factors
scale_x = 1.5  # Scaling factor along x-axis
scale_y = 1.5  # Scaling factor along y-axis

# Apply scaling to the image
scaled_image = cv2.resize(image, None, fx=scale_x, fy=scale_y, interpolation=cv2.INTER_LINEAR)

# Display original and scaled images
print("Original image:")
show_image(image)
print("Scaled Image:")
show_image(scaled_image)
```


iii)Image shearing:
```python
# Install OpenCV library if not already installed
!pip install opencv-python-headless

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Function to display images in Colab
def show_image(image):
    plt.figure(figsize=(6, 6))
    plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
    plt.axis('off')
    plt.show()

# Load an image from URL or file path
image_url = 'dipt.jpeg'  # Replace with your image URL or file path
image = cv2.imread(image_url)

# Define shear parameters
shear_factor_x = 0.5  # Shear factor along x-axis
shear_factor_y = 0.2  # Shear factor along y-axis

# Define shear matrix
shear_matrix = np.float32([[1, shear_factor_x, 0], [shear_factor_y, 1, 0]])

# Apply shear to the image
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))

# Display original and sheared images
print("Original Image:")
show_image(image)
print("Sheared Image:")
show_image(sheared_image)
```



iv)Image Reflection
```python
# Install OpenCV library if not already installed
!pip install opencv-python-headless

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Function to display images in Colab
def show_image(image):
    plt.figure(figsize=(6, 6))
    plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
    plt.axis('off')
    plt.show()

# Load an image from URL or file path
image_url = 'dipt.jpeg'  # Replace with your image URL or file path
image = cv2.imread(image_url)

# Reflect the image horizontally
reflected_image_horizontal = cv2.flip(image, 1)

# Reflect the image vertically
reflected_image_vertical = cv2.flip(image, 0)

# Reflect the image both horizontally and vertically
reflected_image_both = cv2.flip(image, -1)

# Display original and reflected images
print("Original Image:")
show_image(image)
print("Reflected Horizontally:")
show_image(reflected_image_horizontal)
print("Reflected Vertically:")
show_image(reflected_image_vertical)
print("Reflected Both:")
show_image(reflected_image_both)

```



v)Image Rotation:
```python


# Install OpenCV library if not already installed
!pip install opencv-python-headless

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Function to display images in Colab
def show_image(image):
    plt.figure(figsize=(6, 6))
    plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
    plt.axis('off')
    plt.show()

# Load an image from URL or file path
image_url = 'dipt.jpeg'  # Replace with your image URL or file path
image = cv2.imread(image_url)

# Define rotation angle in degrees
angle = 45

# Get image height and width
height, width = image.shape[:2]

# Calculate rotation matrix
rotation_matrix = cv2.getRotationMatrix2D((width / 2, height / 2), angle, 1)

# Perform image rotation
rotated_image = cv2.warpAffine(image, rotation_matrix, (width, height))

# Display original and rotated images
print("Original Image:")
show_image(image)
print("Rotated Image:")
show_image(rotated_image)
```





vi)Image Cropping:
```python
# Install OpenCV library if not already installed
!pip install opencv-python-headless

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Function to display images in Colab
def show_image(image):
    plt.figure(figsize=(6, 6))
    plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
    plt.axis('off')
    plt.show()

# Load an image from URL or file path
image_url = 'dipt.jpeg'  # Replace with your image URL or file path
image = cv2.imread(image_url)

# Define cropping coordinates (x, y, width, height)
x = 100  # Starting x-coordinate
y = 50   # Starting y-coordinate
width = 200  # Width of the cropped region
height = 150  # Height of the cropped region

# Perform image cropping
cropped_image = image[y:y+height, x:x+width]

# Display original and cropped images
print("Original Image:")
show_image(image)
print("Cropped Image:")
show_image(cropped_image)








```
## Output:
### i)Image Translation

![image](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/93df1e32-885e-4036-ad7a-21d020c575f3)


![image](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/c99cc97c-e193-46e1-8965-23650d69bd37)



### ii) Image Scaling

![image](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/a33fb3fd-43f2-4a2b-a974-6998ac357f43)


![image](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/611533f9-72ec-47b7-b9d8-98a77983d280)




### iii)Image shearing

![Screenshot 2024-03-13 093255](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/c3b59bf5-c787-4655-a151-6c9cada54657)


![image](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/4e0aab53-9b65-4d15-b96c-e11feb0af9ff)




### iv)Image Reflection

![image](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/a56ef4b1-d0b8-480d-a993-15bbe0c33ebc)


![image](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/93419cb8-27af-4a21-80ec-1272472ecc57)

![image](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/1190bf82-7d77-4e76-881b-c39a7a673879)

![image](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/1a121df9-204e-40ad-aac1-a3862e9de57f)





### v)Image Rotation

![image](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/aa2cb0dc-928c-4bd3-9039-33b1885c499e)


![image](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/2f2deb92-ff07-48eb-a0d6-5059cd6096e1)




### vi)Image Cropping

![image](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/443c3038-6fc7-4477-9396-16036d70728a)


![image](https://github.com/harini1006/IMAGE-TRANSFORMATIONS/assets/113497405/06c7f973-67a4-48cf-a807-478aed37cfed)






## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
