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
img = cv2.imread("monty.jpeg")
img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

## 3. Display the image.

```python
plt.imshow(img)
plt.axis("off")
plt.show()
```

### Output

<img width="466" height="496" alt="image" src="https://github.com/user-attachments/assets/c74ed598-6fa1-42d9-9903-31cf524050d9" />


---

## 4. Draw a diagonal line.

```python
cv2.line(img, (0,0), (500,500), (255,0,0), 5)

plt.imshow(img)
plt.axis("off")
plt.show()
```

### Output

<img width="415" height="516" alt="image" src="https://github.com/user-attachments/assets/3a9da2b0-5619-4024-b7b4-3d20e86df02e" />


---

## 5. Draw a circle.

```python
cv2.circle(img, (350,250), 80, (0,255,0), 5)

plt.imshow(img)
plt.axis("off")
plt.show()
```

### Output

<img width="420" height="515" alt="image" src="https://github.com/user-attachments/assets/c9733f54-e63b-49d5-90b7-f57f1cc8a113" />


---

## 6. Draw a rectangle.

```python
cv2.rectangle(img, (80,100), (280,320), (255,255,0), 4)

plt.imshow(img)
plt.axis("off")
plt.show()
```

### Output

<img width="427" height="502" alt="image" src="https://github.com/user-attachments/assets/8eeb3e56-014c-430f-b130-76f5dbfa3e31" />


---

## 7. Add text to the image.

```python
cv2.putText(
    img,
    "monty",
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

<img width="411" height="502" alt="image" src="https://github.com/user-attachments/assets/838b6b2e-66e0-4080-ba1c-98d4c903022a" />


---

## 8. Convert the image to HSV.

```python
hsv = cv2.cvtColor(img, cv2.COLOR_RGB2HSV)

plt.imshow(hsv)
plt.axis("off")
plt.show()
```

### Output

<img width="452" height="510" alt="image" src="https://github.com/user-attachments/assets/5904392e-e223-4361-a4c6-cb69584482fd" />


---

## 9. Convert the image to Grayscale.

```python
gray = cv2.cvtColor(img, cv2.COLOR_RGB2GRAY)

plt.imshow(gray, cmap="gray")
plt.axis("off")
plt.show()
```

### Output

<img width="426" height="507" alt="image" src="https://github.com/user-attachments/assets/029ca800-8633-4308-b24b-30df4f62281a" />


---

## 10. Convert the image to YCrCb.

```python
ycrcb = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)

plt.imshow(ycrcb)
plt.axis("off")
plt.show()
```

### Output

<img width="418" height="505" alt="image" src="https://github.com/user-attachments/assets/e2861709-34f3-4a2d-a2d1-afefd218ae8c" />


---

## 11. Convert HSV back to RGB.

```python
rgb = cv2.cvtColor(hsv, cv2.COLOR_HSV2RGB)

plt.imshow(rgb)
plt.axis("off")
plt.show()
```

### Output
<img width="422" height="508" alt="image" src="https://github.com/user-attachments/assets/e4e7229c-4f32-47cb-be1e-98e7f2657b9a" />


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

<img width="412" height="508" alt="image" src="https://github.com/user-attachments/assets/25b0e594-932e-4911-aa77-bf4f7df25492" />


---

## 13. Resize the image.

```python
resized = cv2.resize(img, None, fx=0.5, fy=0.5)

plt.imshow(resized)
plt.axis("off")
plt.show()
```

### Output

<img width="582" height="512" alt="image" src="https://github.com/user-attachments/assets/c744594e-61d4-4350-94ca-c1ae601528a8" />


---

## 14. Crop the image.

```python
crop = img[100:450,100:400]

plt.imshow(crop)
plt.axis("off")
plt.show()
```

### Output

<img width="520" height="513" alt="image" src="https://github.com/user-attachments/assets/54f84f25-cf18-4487-ae45-beb854d1f548" />


---

## 15. Flip the image horizontally.

```python
horizontal = cv2.flip(img, 1)

plt.imshow(horizontal)
plt.axis("off")
plt.show()
```

### Output

<img width="415" height="501" alt="image" src="https://github.com/user-attachments/assets/6897f842-6325-4615-91d7-d608fa4ffdcd" />


---

## 16. Flip the image vertically.

```python
vertical = cv2.flip(img, 0)

plt.imshow(vertical)
plt.axis("off")
plt.show()
```

### Output

<img width="422" height="511" alt="image" src="https://github.com/user-attachments/assets/841a2e23-ba03-4996-ba36-33bdd19526f3" />


---

# Result

Thus, the image was successfully read, displayed, modified using various OpenCV drawing functions, converted into different color spaces, resized, cropped, and flipped successfully using Python and OpenCV.
