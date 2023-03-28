# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:

# Step1: 

Import cv2 and save and image as filename.jpg

# Step2:
Use imread(filename, flags) to read the file.

# Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

# Step4: 
Split and merge the image using cv2.split and cv2.merge commands.

# Step5:
End the program and close the output image windows.

## Program:

Developed By: Gayathri A

Register Number: 212221230028

# Original Img :
```
import cv2
img=cv2.imread('mo.jpg')
cv2.imshow('Org_img',img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


# i) Convert BGR and RGB to HSV and GRAY
```
hsv_img=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

hsv_img1=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_img1)
cv2.waitKey(0)
cv2.destroyAllWindows()

gray_img=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

gray_img1=cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_img1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

# ii)Convert HSV to RGB and BGR
```
rgb_img=cv2.cvtColor(hsv_img,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV to RGB',rgb_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

bgr_img=cv2.cvtColor(hsv_img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to BGR',bgr_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```




# iii)Convert RGB and BGR to YCrCb
```
YCrCb_1 = cv2.cvtColor(rgb_img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('YCrCb_1',YCrCb_1)
cv2.waitKey(0)
cv2.destroyAllWindows()

YCrCb_2 = cv2.cvtColor(bgr_img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('YCrCb_2',YCrCb_2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```



# iv)Split and Merge RGB Image
```
blue = img[:,:,0]
green = img[:,:,1]
red = img[:,:,2]
cv2.merge((blue,green,red))
```



# v) Split and merge HSV Image
```
h, s, v = cv2.split(hsv_img)
cv2.merge((h,s,v))
```
## Output:
# Original img :

![output](dip%203.1.png)

### i) BGR and RGB to HSV and GRAY

![output](dip%203.2.png)
![output](dipp%203.3.png)
![output](./dip%203.4.png)
![output](./dip%203.5.png)

### ii) HSV to RGB and BGR

![output](./dip%203.7.png)
![output](./dip%203.8.png)

### iii) RGB and BGR to YCrCb

![output](./dip%203.9.png)
![output](./dip%203.10.png)

### iv) Split and merge RGB Image

![output](./dip%203.11.png)

### v) Split and merge HSV Image

![output](./dip%20%203.12.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
