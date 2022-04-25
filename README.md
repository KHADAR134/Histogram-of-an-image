# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread().
<br>

### Step2:
Print the image using imshow().
<br>

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.
<br>

### Step4:
cv2.equalize() is used to transform the gray image to equalized form.
<br>

### Step5:
The Histogram of gray scale image and color image is shown.
<br>

## Program:
```python
# Developed By:
# Register Number:
# Developed By:SHAIK KHADAR BASHA
# Register Number: 212220230045

import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

import cv2
import matplotlib.pyplot as plt 
#gray scale and color image  


gray_image = cv2.imread("gray.jpg")
color_image = cv2.imread("tata.jpg")
#plotting the gray image in graph
plt.imshow(gray_image)
plt.show()
#plotting the color image in graph
plt.imshow(color_image)
plt.show()



# Write your code to find the histogram of gray scale image and color image channels.
gray=cv2.imread("gray.jpg")
color=cv2.imread("tata.jpg")
gray=cv2.resize(gray,(500,400))
color=cv2.resize(color,(500,400))

cv2.imshow("GRAY IMAGE ",gray)
cv2.imshow("COLOR IMAGE ",color)

cv2.waitKey(0)


# Display the histogram of gray scale image and any one channel histogram from color image

gray_hist=cv2.calcHist([gray],[0],None,[256],[0,255])
color_hist=cv2.calcHist([color],[2],None,[256],[0,255])
plt.figure()
plt.title("GRAY IMAGE")
plt.xlabel("GRAYSCALE VALUE")
plt.ylabel("PIXEL COUNT")
plt.stem(gray_hist)
plt.show()

plt.figure()
plt.title("COLOR IMAGE")
plt.xlabel("COLORSCALE VALUE")
plt.ylabel("PIXEL COUNT")
plt.stem(color_hist)
plt.show()





# Write the code to perform histogram equalization of the image. 

import cv2
Gray_image=cv2.imread('gray.jpg',0)
equalize=cv2.equalizeHist(Gray_image)
#resizing image 
Gray_image= cv2.resize(Gray_image, (270,190))
equalize= cv2.resize(equalize, (270,190))

#output
cv2.imshow('GRAY IMAGE',Gray_image)
cv2.imshow('EQUALIZED IMAGE',equalize)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
<br>
<br>
![DIP(41)](https://user-images.githubusercontent.com/75235233/165124011-b9e5d36d-b3ec-4982-8497-e18c415d6bfa.png)
<br>
<br>

### Histogram of Grayscale Image and any channel of Color Image
<br>
<br>
![DIP(42)](https://user-images.githubusercontent.com/75235233/165124055-840bc7b4-b550-4c7e-95c5-0fc637f3887d.png)
<br>
<br>

### Histogram Equalization of Grayscale Image
<br>
<br>
![DIP(43)](https://user-images.githubusercontent.com/75235233/165124242-074a6aec-fed7-432d-960d-f18b1d00a183.png)
<br>
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
