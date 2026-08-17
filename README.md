# Video Capture and Frame Processing using OpenCV

# Program Developed By

**Name:** Chintala aman monty

**Register Number:** 212224040054

## AIM
Write a Python program using OpenCV to perform basic webcam operations including:

- Capture an image from the webcam.
- Display the captured image.
- Display live webcam video.
- Resize live video frames.
- Rotate live video frames.

---

## Software Required
- Anaconda (Python 3.7 or above)
- Jupyter Notebook
- OpenCV (`cv2`)
- Matplotlib
- IPython

---

## Algorithm

### Step 1
Import the required libraries.

### Step 2
Initialize the webcam using `cv2.VideoCapture()`.

### Step 3
Capture a single frame from the webcam.

### Step 4
Save the captured frame as an image.

### Step 5
Read and display the captured image.

### Step 6
Display the live webcam feed.

### Step 7
Resize the webcam frames and display them.

### Step 8
Rotate the webcam frames and display them.

### Step 9
Release the webcam resource after execution.

---

# Ex. No. 02

## 1. Import the required libraries.

```python
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
```

---

## 2. Capture a single frame from the webcam.

```python
cap = cv2.VideoCapture(0)

ret, frame = cap.read()

if ret:
    cv2.imwrite("captured_frame.jpg", frame)

cap.release()
```

---

## 3. Read the captured image.

```python
captured_image = cv2.imread("captured_frame.jpg")
```

---

## 4. Display the captured image.

```python
plt.imshow(captured_image[:, :, ::-1])
plt.title("Captured Frame")
plt.axis("off")
plt.show()
```

### Output

<img width="684" height="488" alt="Screenshot 2026-08-17 140148" src="https://github.com/user-attachments/assets/15c70839-e050-4718-814c-e0dab5def20e" />




---

## 5. Display live webcam video.

```python
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()

    if not ret:
        break

    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)

    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis("off")
    plt.show()

    time.sleep(0.05)

cap.release()
```

### Output

<img width="706" height="480" alt="Screenshot 2026-08-17 140202" src="https://github.com/user-attachments/assets/76a4cb46-b953-426c-b5aa-8e4228228180" />


---

## 6. Resize the live webcam frames.

```python
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()

    if not ret:
        break

    resized_frame = cv2.resize(frame, (100, 150))

    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)

    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis("off")
    plt.show()

    time.sleep(0.05)

cap.release()
```

### Output

<img width="371" height="501" alt="Screenshot 2026-08-17 140208" src="https://github.com/user-attachments/assets/bdb6f658-a39a-45fe-8096-cc65c5a2da59" />



---

## 7. Rotate the live webcam frames.

```python
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()

    if not ret:
        break

    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)

    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)

    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis("off")
    plt.show()

    time.sleep(0.05)

cap.release()
```

### Output

<img width="415" height="496" alt="Screenshot 2026-08-17 140215" src="https://github.com/user-attachments/assets/b8c72f3e-a6e4-425a-948a-bb12f6bed4c8" />


---

# Output

1. Successfully captured an image from the webcam.
2. Displayed the captured image.
3. Displayed live webcam video.
4. Resized the webcam frames.
5. Rotated the webcam frames by 90° clockwise.

---

# Result

Thus, the webcam was successfully accessed using OpenCV. A single image was captured and displayed, while live video frames were processed by resizing and rotating them successfully using Python and OpenCV.
