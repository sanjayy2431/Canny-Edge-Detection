# Canny-Edge-Detection

# Aim:
To perform Canny edge detection algorithm and obtain the edges with different parameter settings.

# Software Required:
Anaconda - Python 3.7

# Algorithm:
Step1:
To perform edge detection using Canny edge detectors.

Step2:
For performing edge detection on a image.

Canny : canny_edges=cv2.Canny(gray,50,150)

For different parameters :

i) Low thresholds (detects more edges, including noise) : canny_edges1 = cv2.Canny(blurred, 30, 80)

ii) Balanced thresholds (good trade-off) : canny_edges2 = cv2.Canny(blurred, 50, 100)

iii)High thresholds (detects only strong edges) : canny_edges3 = cv2.Canny(blurred, 100, 200)

Step3:
Display all the images with their respective edge detected images.

# Program :
```
Name : Sanjay V
Reg No: 212223230188
```
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread('wb.jpg') 
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
blurred = cv2.GaussianBlur(gray, (5, 5), 1.4)
canny_edges = cv2.Canny(gray, 50, 150)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.title('Original Image')
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()
plt.figure(figsize=(8,8))
plt.subplot(1, 2, 2)
plt.title('Canny Edge Detection')
plt.imshow(canny_edges, cmap='gray')
plt.axis('off')
plt.show()
# Apply Canny with different threshold settings
# Low thresholds (detects more edges, including noise)
canny_edges1 = cv2.Canny(blurred, 30, 80)
plt.figure(figsize=(8, 8))
plt.subplot(2, 2, 2)
plt.title('Canny (Low Thresholds: 30-80)')
plt.imshow(canny_edges1, cmap='gray')
plt.axis('off')

plt.show()
# Balanced thresholds (good trade-off)
canny_edges2= cv2.Canny(blurred, 50, 100)
plt.figure(figsize=(8, 8))
plt.subplot(2, 2, 3)
plt.title('Canny (Balanced Thresholds: 50-100)')
plt.imshow(canny_edges2, cmap='gray')
plt.axis('off')

plt.show()
# High thresholds (detects only strong edges)
canny_edges3 = cv2.Canny(blurred, 100, 200)
plt.figure(figsize=(8,8))
plt.subplot(2, 2, 4)
plt.title('Canny (High Thresholds: 100-200)')
plt.imshow(canny_edges3, cmap='gray')
plt.axis('off')

plt.tight_layout()
plt.show()
```
# Output:
Original Image:


Canny Edge Detection:
 
https://private-user-images.githubusercontent.com/209225820/437760558-5a6a54cd-cdbf-4c69-ba2f-c68f1dc42bd5.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NjI0NDE0MTYsIm5iZiI6MTc2MjQ0MTExNiwicGF0aCI6Ii8yMDkyMjU4MjAvNDM3NzYwNTU4LTVhNmE1NGNkLWNkYmYtNGM2OS1iYTJmLWM2OGYxZGM0MmJkNS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUxMTA2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MTEwNlQxNDU4MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0zMzUzNTM2NTJhNjQ5N2JmN2QxMTBiN2ExNzhlN2E3MDhmYzk1MDgwNWZlNjcyMmYzN2VjZjkxNTRmMjE3NDcxJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.7Sh-zaYOkXwEAPwxu-bDsn2u04Nh1WpMtB57WY5LTPE

Canny (Low Thresholds: 30-80):
download

Canny (Balanced Thresholds: 50-100):
download

Canny (High Thresholds: 100-200):
download

Result:
Thus , the edges are detected by Canny edge detection and also implemented with different parameter settings.
