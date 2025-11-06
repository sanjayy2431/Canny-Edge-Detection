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

<img width="301" height="230" alt="image" src="https://github.com/user-attachments/assets/83b69e19-22d4-4aab-bcef-9b2b8be5aa9e" />


Canny (Balanced Thresholds: 50-100):
<img width="332" height="230" alt="image" src="https://github.com/user-attachments/assets/02fdb8c6-6a96-48ad-841e-366a293cb866" />


Canny (High Thresholds: 100-200):
<img width="397" height="292" alt="image" src="https://github.com/user-attachments/assets/3c9a2734-7420-47ba-97ab-3b6df46b0145" />

Result:
Thus , the edges are detected by Canny edge detection and also implemented with different parameter settings.
