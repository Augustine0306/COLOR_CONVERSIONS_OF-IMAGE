# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

## Program:
#### Developed By: Augustine.J
#### Register Number: 212222240015


## Output:

### i) Read and display the image

```python
    import cv2
    image=cv2.imread('cat.jpg',1)
    image=cv2.resize(image,(300,300))
    cv2.imshow('augus',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```

![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/9b153cd0-f6e7-47f6-964e-093926185a68)

![Screenshot 2024-03-01 085201](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/8263e587-6f93-48eb-ac5b-ac7382a95a91)

### ii)Write the image

```python
    import cv2
    image=cv2.imread('cat.jpg',0)
    cv2.imwrite('demos.jpg',image)
```
![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/d1698d91-ddf8-4c0a-a5d3-1b584fd15de5)


### iii)Shape of the Image

```python
    import cv2
    image=cv2.imread('cat.jpg',1)
    print(image.shape)
```
![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/6c2ef511-16ad-4de7-b710-4cd1e0f8aa37)



### iv)Access rows and columns

```python
import random
    import cv2
    image=cv2.imread('cat.jpg',1)
    image=cv2.resize(image,(500,500))
    for i in range (250,500):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/d5925713-06dc-4b87-9ee7-7d5b6b2bf2ab)


![Screenshot 2024-03-01 085842](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/2945d785-332b-4dd1-9567-59dc6512dd6b)



### v)Cut and paste portion of image

```python
  import cv2
  image=cv2.imread('cat.jpg',1)
  image=cv2.resize(image,(300,300))
  tag =image[150:200,110:160]
  image[110:160,150:200] = tag
  cv2.imshow('yogi',image)
  cv2.waitKey(0)
  cv2.destroyAllWindows()
```

![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/2037562e-42e2-4997-b707-20ac50951005)


![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/d1829bb7-cce0-41c5-ab4e-423faf032e03)


### vi) BGR and RGB to HSV and GRAY

```python
import cv2
img = cv2.imread('cat.jpg',1)
img = cv2.resize(img,(200,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-03-01 090222](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/bf071e2b-4ff0-41db-8d0e-56dc86e26dad)

![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/c2a8726e-c70e-4dc6-99db-9a44d5639a2d)


### vii) HSV to RGB and BGR

```python
import cv2
img = cv2.imread('cat.jpg')
img = cv2.resize(img,(200,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/becd66c7-afe4-4551-a6d5-4730bb228ce5)


![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/067a8d65-6c23-48d3-98e9-4fcaacf25fa6)



### viii) RGB and BGR to YCrCb

```python
import cv2
img = cv2.imread('cat.jpg')
img = cv2.resize(img,(200,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/74e259da-8e8d-4597-978b-68cea728874f)

![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/fd38854e-aa84-4189-9839-6e621a57e175)


### ix) Split and merge RGB Image
```python
import cv2
img = cv2.imread('cat.jpg',1)
img = cv2.resize(img,(200,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/5abd9b51-3d90-45ea-bb8d-c5381b3045b0)

![Screenshot 2024-03-01 091312](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/b231ec66-7a33-4a50-a075-dba06eb60e01)


### x) Split and merge HSV Image
```python
import cv2
img = cv2.imread("cat.jpg",1)
img = cv2.resize(img,(200,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/e5b7f841-b9c9-45f8-9888-f386b32f16c3)

![image](https://github.com/Augustine0306/COLOR_CONVERSIONS_OF-IMAGE/assets/119404460/28654725-336d-4d76-a4c5-e54da2684b70)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.






