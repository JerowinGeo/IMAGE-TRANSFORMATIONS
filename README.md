# IMAGE TRANSFORMATION


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:
```python
Developed By: Jerowin Geo J A
Register Number:212223100016
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
