# 📱 Mobile Camera Streaming using OpenCV
## Overview

This project allows you to use your **mobile phone camera as a webcam for your laptop** using **Python and OpenCV**.
The video is streamed from the mobile device to the laptop over the **local network** using an IP camera application.

This can be useful for **computer vision projects, remote monitoring, or testing OpenCV applications** without needing an external webcam.

---

## 🚀 Features

* Stream **live video from mobile camera to laptop**
* Simple implementation using **Python and OpenCV**
* Works over **Wi-Fi local network**
* Can be extended for **Computer Vision applications**

---

## 🛠 Tools & Libraries

* **Python 3**
* **OpenCV**
* **IP Webcam mobile application**
* Local Wi-Fi network

---

## 📦 Installation

Install the required library:

```bash
pip install opencv-python
```

---

## ▶ How to Run

1. Install the **IP Webcam** app on your mobile phone.
2. Connect both **mobile and laptop to the same Wi-Fi network**.
3. Open the app and start the camera server.
4. The app will display an **IP address**, for example:

```
http://192.168.1.5:8080
```

5. Use the video stream URL in the Python code:

```
http://192.168.1.5:8080/video
```

6. Run the Python script and the mobile camera stream will appear on your laptop.

---

## 💻 Example Code

```python
import cv2

url = "http://192.168.1.5:8080/video"

cap = cv2.VideoCapture(url)

while True:
    ret, frame = cap.read()
    if not ret:
        break

    cv2.imshow("Mobile Camera Stream", frame)

    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
```

Press **Q** to exit the video window.

---

## 📊 Possible Extensions

This project can be extended to include:

* Face Detection
* Object Detection
* Motion Detection
* Security camera system
* Real-time image processing

---

## 📄 License

This project is open-source and free to use.


