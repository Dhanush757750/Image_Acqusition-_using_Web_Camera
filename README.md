
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera
<br>

### Step 2:
Use cv2.imread to read the video or image.
<br>

### Step 3:
Use cv2.imwrite to save the image.
<br>

### Step 4:
Use cv2.imshow to show the video.
<br>

### Step 5:
End the program and close the output video window by pressing 'q'.
<br>

## Program:
### Developed By: C.DHANUSH
### Register No:212224040066

## i) Write the frame as JPG file
```
import cv2
viedoCaptureObject=cv2.VideoCapture(0)

ret,frame=viedoCaptureObject.read()
cv2.imwrite("webcam_img.jpg",frame)

viedoCaptureObject.release()
cv2.destroyAllWindows()
```
## ii) Display the video
```
import numpy as np
import cv2

cap = cv2.VideoCapture(0)
ret, frame = cap.read()

cv2.imshow('captured_frame', frame)

cv2.waitKey(10000)


cap.release()
cv2.destroyAllWindows()
```
## iii) Display the video by resizing the window
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)

ret,frame=cap.read()
width=int(cap.get(3))
height=int(cap.get(4))
image=np.zeros(frame.shape,np.uint8)
smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
image[:height//2, :width//2]=smaller_frame
image[height//2:, :width//2]=smaller_frame
image[:height//2, width//2:]=smaller_frame
image[height//2:, width//2:]=smaller_frame

cv2.imshow('212224240155_Harika',image)

cv2.waitKey(5000)  

image_dict = {'captured_image1': image}
cv2.imwrite('captured_image1.jpg', image)

cap.release()
cv2.destroyAllWindows()
```
## iv) Rotate and display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)

ret,frame=cap.read()
width=int(cap.get(3))
height=int(cap.get(4))
image=np.zeros(frame.shape,np.uint8)
smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
image[:height//2, :width//2]=smaller_frame
image[height//2:, :width//2]=smaller_frame
image[:height//2, width//2:]=smaller_frame
image[height//2:, width//2:]=smaller_frame

cv2.imshow('212224240155_Harika',image)

cv2.waitKey(5000)  

image_dict = {'captured_image1': image}
cv2.imwrite('captured_image1.jpg', image)

cap.release()
cv2.destroyAllWindows()

```
## Output

### i) Write the frame as JPG image
![IMAGE1](https://github.com/user-attachments/assets/41478f19-85d5-4242-8459-f68290c5c79d)
</br>

### ii) Display the video
![IMAGE1](https://github.com/user-attachments/assets/bd6f1e13-d26f-4864-b2c3-3cd08262ad5a)
</br>

### iii) Display the video by resizing the window
![IMAGE3](https://github.com/user-attachments/assets/284b950e-ce01-4304-9461-8f9da444fcb2)
</br>

### iv) Rotate and display the video
![IMAGE4](https://github.com/user-attachments/assets/acd308d2-6ed4-4e44-af02-e3bf6cce8025)
</br>

## Result:
Thus the image is accessed from webcamera and displayed using openCV.
