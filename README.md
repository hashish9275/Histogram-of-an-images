# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()
### Step2:
Print the image using imshow().
### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.
### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.
### Step5:
The Histogram of gray scale image and color image is shown.

## Program:
### Developed By: K.R.HASHISH VIDYA SAGAR
### Register Number: 212222230047
s://github.com/user-attachments/assets/631a15a0-35de-468e-8da1-ff690c5c23da)

### Histogram of Grayscale Image
```python
plt.title("Histogram of Grayscale Image")
plt.hist(gray_image.ravel(), bins=256, color='black', alpha=0.6)
plt.xlim(0, 255)
plt.tight_layout()
plt.show()
```
## Output:
![image](https://github.com/user-attachments/assets/1dbac238-fe86-4cdb-8ad2-eebe9fde40cc)

### Histogram Equalization of Grayscale Image.
```python
equalized_gray_image = cv2.equalizeHist(gray_image)
plt.title("Histogram of Equalized Grayscale Image")
plt.hist(equalized_gray_image.ravel(), bins=256, color='black', alpha=0.6)
plt.xlim(0, 255)
plt.title("Enhanced Grayscale Image")
plt.imshow(equalized_gray_image, cmap='gray')
plt.axis('off')
```
## Output:
![image](https://github.com/user-attachments/assets/0357dac5-9b2f-4d4d-af4f-e48a88ba1e4c)
![image](https://github.com/user-attachments/assets/5753d49a-18ca-48c9-8edb-654388b9d825)

### Input of color image
```python
color_image = cv2.imread('color_image.jpg')
plt.title("Input Color Image")
plt.imshow(cv2.cvtColor(color_image, cv2.COLOR_BGR2RGB))
plt.axis('off')
```
### Output:
![image](https://github.com/user-attachments/assets/486876b2-04e2-406c-916f-74421bf117b8)

### Histogram of Color Image
```python
hist_b = cv2.calcHist([color_image], [0], None, [256], [0, 256])
hist_g = cv2.calcHist([color_image], [1], None, [256], [0, 256])
hist_r = cv2.calcHist([color_image], [2], None, [256], [0, 256])
plt.title("Histogram of Input Color Image")
plt.plot(hist_b, color='blue', label='Blue channel')
plt.plot(hist_g, color='green', label='Green channel')
plt.plot(hist_r, color='red', label='Red channel')
plt.show()
```
### Output:
![image](https://github.com/user-attachments/assets/b128d11d-8e7e-46d9-bf56-d1a9d1f45612)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.

