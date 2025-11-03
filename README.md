# Implementation-of-Erosion-and-Dilation
## NAME : SANJAY V
## REG NO : 212223230188
## DATE : 3/11/25
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages
### Step2:
Create the text using cv2.put Text
### Step3:
create the structuting element
### Step4:
Erodde the image
### Step5:
Dilate the image

 
## Program:
```
Name : SANJAY V
Reg no : 212223230188

```
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
def load_image():
    blank_image = np.zeros((600,600))
    font = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_image,text='SANJU',org=(50,300),fontFace=font,fontScale = 5,color=(255,255,255),thickness=15,lineType=cv2.LINE_AA)
    return blank_image
def display_img(img):
    fig = plt.figure(figsize=(12,10))
    ax=fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    plt.show()
img=load_image()
display_img(img)
kernel=np.ones((5,5),dtype=np.uint8)
erosion = cv2.erode(img,kernel,iterations = 2)
display_img(erosion)
dilution=cv2.dilate(img,kernel,iterations=2)
display_img(dilution)

```
## Output:

### Display the input Image
<img width="801" height="764" alt="image" src="https://github.com/user-attachments/assets/9e3a7ec3-35a2-42ec-a70c-90f8752cdbe0" />


### Display the Eroded Image
<img width="805" height="769" alt="image" src="https://github.com/user-attachments/assets/95e1d167-9f13-4cd8-aaeb-e1697a7ec7d2" />


### Display the Dilated Image
<img width="804" height="775" alt="image" src="https://github.com/user-attachments/assets/c34067e2-d76b-4db5-8be6-249de6b7a260" />



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
