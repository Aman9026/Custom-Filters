# ImageProcessing

![](https://miro.medium.com/max/1400/1*VeUwoUU7wb2T-NDciUuo7w.jpeg)


***You are always welcome to optimize or improve any resource in this repository by following [these](https://github.com/Aman9026/ImageProcessing/blob/master/CONTRIBUTING.md) instructions.***

---

**Images:** 2-D representation of the visible light spectrum
```
Human visual system(eye & visual cortex) is incredibly good at image processing
```

**Color Spaces:** different method to store image in computer (eg, RGB, HSV, CMYK)


**OpenCV:** Open source Computer Vision Software for image processing, OpenCV default color space is RGB, but stores color in BGR format, to improve processing of image operation


**HSV:** hue, saturation and value/brightness , is a color space that attempts to represent colors the way humans perceive it, in CV we use for color segmentation



## Installation

Install OpenCV by Anaconda:
 ```conda install opencv```

Install by python installer pip:
 ```pip install opencv-python```

## Adding filters
We can add inbuilt filters or create custom filters by ourself, We'll incorporate both here.

***Original Image:***
![ogimage](https://github.com/Aman9026/ImageProcessing/blob/master/Data/Images/billu.jpeg)

**Now let's add filters to it.**

Import module opencv
```
>>> import cv2
```

OpenCV load image from storage and convert into numpy array:
```
>>> photo = cv2.imread('imagename.jpg')

```
**We don't need to load numpy module, opencv call its internal property.**

Convert image into gray image:

```>>> gray_image = cv2.cvtColor(photo , cv2.COLOR_BGR2GRAY)```

Show image, but we have use waitKey()  and destroyAllWindows() with imshow(), otherwise program will hang up

```
>>> cv2.imshow('image title', photo)
>>> cv2.waitKey()
>>> cv2.destroyAllWindows()
```

**waitkey():** used to hold windows for some time interval, and also wait for any key input from keyword, so listen key and then go to next statement

**destroyAllWindows():** close any window, open by imshow()

![grayfilter](https://github.com/Aman9026/ImageProcessing/blob/master/Data/Images/grayscale.jpeg)

A very faster alternative of adding filter by inbuilt functions is by doing it manually in an optimized way. 
We can convert the image to gray while reading only by a simple trick given below.
```
>>> grey_photo = cv2.imread('image.jpg' , 0)

```
