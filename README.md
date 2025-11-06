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
<img width="301" height="230" alt="image" src="https://github.com/user-attachments/assets/a75573ac-9c36-4339-ba2f-9c6e2e92cdc9" />


Canny Edge Detection:
 
<img width="301" height="230" alt="image" src="https://github.com/user-attachments/assets/9744f75e-4334-4dcb-ba66-2b66db1ee9ca" />


Canny (Low Thresholds: 30-80):
https://private-user-images.githubusercontent.com/209225820/437760861-9bae14a2-8078-4320-9bdb-981a7f6904ff.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NjI0NDE0MTYsIm5iZiI6MTc2MjQ0MTExNiwicGF0aCI6Ii8yMDkyMjU4MjAvNDM3NzYwODYxLTliYWUxNGEyLTgwNzgtNDMyMC05YmRiLTk4MWE3ZjY5MDRmZi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUxMTA2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MTEwNlQxNDU4MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1mZmUwNDM1MThjMjFlNmQxZTk1NTdjYjI2ZDgyM2VlZTg1ZGRlMTM5YWZiZWNkZTNmNTBmZTVhNTdhMjEwMzk4JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.u5fTC2a2mcuZOeyBNYEh4j69ST95kJfWXXf3hs9K_P0

Canny (Balanced Thresholds: 50-100):


Canny (High Thresholds: 100-200):


Result:
Thus , the edges are detected by Canny edge detection and also implemented with different parameter settings.
