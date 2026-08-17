# Image Processing using OpenCV


# Program Developed By

**Name:** Chintala aman monty

**Register Number:** 212224040054


## AIM
Write a Python program using OpenCV to perform basic image processing operations including:

- Read and display an image.
- Draw basic shapes and text.
- Perform color space conversions.
- Access and modify pixel values.
- Resize and crop an image.
- Flip an image horizontally and vertically.

---

## Software Required
- Anaconda (Python 3.7 or above)
- Jupyter Notebook
- OpenCV (`cv2`)
- Matplotlib

---

## Algorithm

### Step 1
Import the required libraries (`cv2`, `matplotlib.pyplot`).

### Step 2
Read the image from the local directory and display it.

### Step 3
Draw graphical objects such as:
- Line
- Circle
- Rectangle
- Text

### Step 4
Convert the image into different color spaces:
- RGB
- HSV
- Grayscale
- YCrCb

### Step 5
Modify pixel values by changing a selected region.

### Step 6
Resize the image.

### Step 7
Crop a Region of Interest (ROI).

### Step 8
Flip the image horizontally and vertically.

---

# Ex. No. 01

## 1. Import the required libraries.

```python
import cv2
import matplotlib.pyplot as plt
```

---

## 2. Read the image.

```python
img = cv2.imread("Joel_John_Jobinse_Photo.jpg")
img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

## 3. Display the image.

```python
plt.imshow(img)
plt.axis("off")
plt.show()
```

### Output

<img width="620" height="631" alt="image" src="https://github.com/user-attachments/assets/c9bcc4be-c786-4d2e-ad1f-9ba43fb3b5bd" />


---

## 4. Draw a diagonal line.

```python
cv2.line(img, (0,0), (500,500), (255,0,0), 5)

plt.imshow(img)
plt.axis("off")
plt.show()
```

### Output

<img width="562" height="528" alt="image" src="https://github.com/user-attachments/assets/d9551f38-710e-4da7-8c7a-a0c0cca20503" />


---

## 5. Draw a circle.

```python
cv2.circle(img, (350,250), 80, (0,255,0), 5)

plt.imshow(img)
plt.axis("off")
plt.show()
```

### Output

<img width="581" height="546" alt="image" src="https://github.com/user-attachments/assets/c18d87fa-0146-4b81-922f-b0fe89a12af8" />


---

## 6. Draw a rectangle.

```python
cv2.rectangle(img, (80,100), (280,320), (255,255,0), 4)

plt.imshow(img)
plt.axis("off")
plt.show()
```

### Output

<img width="568" height="532" alt="image" src="https://github.com/user-attachments/assets/00ac1808-3be8-4add-b396-c3b357b47c5d" />


---

## 7. Add text to the image.

```python
cv2.putText(
    img,
    "Joel John Jobinse",
    (50,50),
    cv2.FONT_HERSHEY_SIMPLEX,
    1,
    (255,0,255),
    2
)

plt.imshow(img)
plt.axis("off")
plt.show()
```

### Output

<img width="553" height="518" alt="image" src="https://github.com/user-attachments/assets/560514ef-1650-452c-8ca1-2563f5067705" />


---

## 8. Convert the image to HSV.

```python
hsv = cv2.cvtColor(img, cv2.COLOR_RGB2HSV)

plt.imshow(hsv)
plt.axis("off")
plt.show()
```

### Output

<img width="846" height="572" alt="image" src="https://github.com/user-attachments/assets/e19faefb-ec45-4047-9d9b-6160f61fa6e5" />


---

## 9. Convert the image to Grayscale.

```python
gray = cv2.cvtColor(img, cv2.COLOR_RGB2GRAY)

plt.imshow(gray, cmap="gray")
plt.axis("off")
plt.show()
```

### Output

<img width="902" height="587" alt="image" src="https://github.com/user-attachments/assets/060cc742-3ce7-46d9-9c7b-2a1057a72080" />


---

## 10. Convert the image to YCrCb.

```python
ycrcb = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)

plt.imshow(ycrcb)
plt.axis("off")
plt.show()
```

### Output

<img width="887" height="581" alt="image" src="https://github.com/user-attachments/assets/8222087f-6800-4f2c-a568-17bfe55431ae" />


---

## 11. Convert HSV back to RGB.

```python
rgb = cv2.cvtColor(hsv, cv2.COLOR_HSV2RGB)

plt.imshow(rgb)
plt.axis("off")
plt.show()
```

### Output
<img width="941" height="580" alt="image" src="https://github.com/user-attachments/assets/f239f7d1-a803-4e4c-a1ba-c191a14d2599" />


---

## 12. Access and modify pixel values.

```python
modified = img.copy()

modified[100:180,100:180] = [255,255,255]

plt.imshow(modified)
plt.axis("off")
plt.show()
```

### Output

<img width="702" height="533" alt="image" src="https://github.com/user-attachments/assets/4fced4ad-a6e5-431f-a8e9-876a46d0dc80" />


---

## 13. Resize the image.

```python
resized = cv2.resize(img, None, fx=0.5, fy=0.5)

plt.imshow(resized)
plt.axis("off")
plt.show()
```

### Output

<img width="750" height="532" alt="image" src="https://github.com/user-attachments/assets/c382ce94-632a-4b9a-8b16-d7e7102a5e5a" />


---

## 14. Crop the image.

```python
crop = img[100:450,100:400]

plt.imshow(crop)
plt.axis("off")
plt.show()
```

### Output

<img width="663" height="540" alt="image" src="https://github.com/user-attachments/assets/048da9b6-008a-40c8-9a9a-7fd8744220b8" />


---

## 15. Flip the image horizontally.

```python
horizontal = cv2.flip(img, 1)

plt.imshow(horizontal)
plt.axis("off")
plt.show()
```

### Output

<img width="563" height="527" alt="image" src="https://github.com/user-attachments/assets/e47004b0-6b22-45bc-bc45-5d028b49c755" />


---

## 16. Flip the image vertically.

```python
vertical = cv2.flip(img, 0)

plt.imshow(vertical)
plt.axis("off")
plt.show()
```

### Output

<img width="902" height="545" alt="image" src="https://github.com/user-attachments/assets/d371f1ce-0d6c-458b-850e-840fa48053e7" />


---

# Result

Thus, the image was successfully read, displayed, modified using various OpenCV drawing functions, converted into different color spaces, resized, cropped, and flipped successfully using Python and OpenCV.
