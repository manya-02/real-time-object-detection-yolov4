
# 🧠 Real-Time Object Detection using YOLOv4 + OpenCV (Local Version)

This project implements **real-time object detection using YOLOv4** and **OpenCV**, running completely locally via your webcam. It includes a utility script to **auto-download YOLOv4 weights** and displays detection results in a live OpenCV window.

---

## 🔍 Features

- ✅ Real-time object detection using YOLOv4 (Darknet)
- 🧠 Uses OpenCV's DNN module (no Darknet compilation or Flask needed)
- 🔁 Auto-downloads `yolov4.weights` if not present
- 💻 Runs entirely locally using your webcam
- 🚫 No web deployment, no Flask, no external servers

---

## 🗂️ Project Structure

```
Object-Detection/
├── app.py                # Main object detection script (local OpenCV)
├── coco.names            # COCO class labels
├── yolov4.cfg            # YOLOv4 model configuration
├── yolov4.weights        # YOLOv4 pre-trained weights (auto-downloaded)
├── download_weights.py   # Script to auto-download yolov4.weights
├── requirements.txt      # Python dependencies
├── .gitignore            # Prevents large/binary files from being tracked
└── README.md             # Project documentation (this file)
```

---

## ⚙️ Installation (Local)

### 1. Clone the repository

```bash
git clone https://github.com/Mayank-01x/Object-Detection.git
cd Object-Detection
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Download YOLOv4 weights (if not already present)

```bash
python download_weights.py
```

### 4. Run the object detection app

```bash
python app.py
```

> 💡 The window will automatically close when you press `q` or manually close it.

---

## 🎥 Camera Input Options

You can modify `cv2.VideoCapture()` in `app.py` to use different sources:

```python
# Use default webcam
cv2.VideoCapture(0)

# IP camera (replace with your IP)
cv2.VideoCapture("http://your-ip-address:port/video")

# Pre-recorded video file
cv2.VideoCapture("your_video.mp4")
```

---

## 🙋 Author

**Manya Aggarwal**  
GitHub: [@manya-02]((https://github.com/manya-02/real-time-object-detection-yolov4))

---

## 📄 License

This project is licensed under the **MIT License**.
