# IMAGE TRANSFORMATION


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using a function warpPerpective()

### Step3:
Scale the image by multiplying the rows and columns with a float value.

### Step4:
Shear the image in both the rows and columns.

### Step5:
Find the reflection of the image.

### step 6:
Rotate the image using angle function.


## Program:
```python
Developed By: Jerowin Geo J A
Register Number:212223100016
```

## i)Image Translation

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("vijay.png")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

## ii) Image Scaling

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("vijay.png")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```


## iii)Image shearing

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("vijay.png")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```


### iv)Image Reflection

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("vijay.png")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```


### v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("vijay.png")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()

angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(input_image,M,(int(cols),int(rows)))

plt.imshow(rotated_img)
plt.show()
```



### vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("vijay.png")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()
```

## Output:
###Orginal Image

![image](https://github.com/user-attachments/assets/714f7eeb-9a86-4800-a018-2d8d49adb66a)


### i)Image Translation

![image](https://github.com/user-attachments/assets/906b7378-ba3b-4a61-9dc2-8a89ecd7e1da)




### ii) Image Scaling

![image](https://github.com/user-attachments/assets/eb445e52-4b26-4ba8-b40b-da05b417411b)






### iii)Image shearing


![image](https://github.com/user-attachments/assets/d656b24a-f228-4fd4-b636-e68efe773e33)


### iv)Image Reflection

![image](https://github.com/user-attachments/assets/bc8839fa-6281-4c56-90f2-0092c1e1001a)




### v)Image Rotation

![image](https://github.com/user-attachments/assets/fb6bc5bd-bcdd-45a5-9d96-309db75040bd)




### vi)Image Cropping

![image](https://github.com/user-attachments/assets/9376851d-c010-49cb-a540-1aecdb619ff5)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
