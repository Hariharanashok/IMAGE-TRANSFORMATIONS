# Ex-4-IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:

Import the necessary libraries and read the original image and save it as a image variable.

## Step2:

Translate the image using a function warpPerpective()

## Step3:

Scale the image by multiplying the rows and columns with a float value.

## Step4:

Shear the image in both the rows and columns.

## Step5:

Find the reflection of the image.

Developed By: Hariharan A
Register Number: 212222100012
## Program:
```python
i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("/content/BIRD.webp")
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

ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/color.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```


iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/BIRD.webp")
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



iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/color.jpg")
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

v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/color.jpg")
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

vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/BIRD.webp")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation
![image](https://github.com/KothaiKumar/IMAGE-TRANSFORMATIONS/assets/121215739/b8bad49c-ccb9-474f-b3ab-bd5ee5e02c6f)

### ii) Image Scaling
![image](https://github.com/KothaiKumar/IMAGE-TRANSFORMATIONS/assets/121215739/1b375b1b-25ed-4668-9836-4302c54c136e)

### iii)Image shearing
![image](https://github.com/KothaiKumar/IMAGE-TRANSFORMATIONS/assets/121215739/f4c0f7cc-1ef1-41a5-a9e3-ed3c70262e23)
![image](https://github.com/KothaiKumar/IMAGE-TRANSFORMATIONS/assets/121215739/6fb5abba-6d89-40a5-94ff-3ea16a514fda)

### iv)Image Reflection
![image](https://github.com/KothaiKumar/IMAGE-TRANSFORMATIONS/assets/121215739/f84b7751-ac12-4962-9227-84a548f9e7f3)
![image](https://github.com/KothaiKumar/IMAGE-TRANSFORMATIONS/assets/121215739/80fbda47-c800-4f04-95a9-c47efe823333)


### v)Image Rotation
![image](https://github.com/KothaiKumar/IMAGE-TRANSFORMATIONS/assets/121215739/172d6638-e301-4f72-9054-302ad5689fcb)
![image](https://github.com/KothaiKumar/IMAGE-TRANSFORMATIONS/assets/121215739/ebdfff3a-5b17-4ce3-bb0e-4c0d961a262f)


### vi)Image Cropping
![image](https://github.com/KothaiKumar/IMAGE-TRANSFORMATIONS/assets/121215739/db45cdf5-1b63-42fd-8ef5-33cfb2c458ff)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
