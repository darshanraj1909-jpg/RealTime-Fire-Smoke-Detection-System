# Real-Time Fire and Smoke Detection System using YOLOv8 & TFLite

An end-to-end Computer Vision pipeline designed to detect fire and smoke in real-time. This project features a custom-trained YOLOv8 model optimized for both high-performance local desktop deployment and lightweight edge-device environments (like the Raspberry Pi) using TensorFlow Lite (TFLite).

## 🚀 Key Features
- **Custom-Trained Architecture:** Fine-tuned YOLOv8 nano model trained on specialized fire and smoke datasets, achieving robust bounding-box accuracy.
- **Cross-Platform Local Desktop App:** Python desktop client powered by OpenCV for low-latency, real-time live webcam tracking.
- **Edge-Optimized Deployment:** Model exported to `.tflite` format, drastically minimizing computational overhead for smooth frame rates on ARM-based architectures (e.g., Raspberry Pi).
- **Graceful Resource Handling:** Implements stable hardware release pipelines to prevent camera or memory locking upon application exit.

## 🛠️ Tech Stack & Dependencies
- **Language:** Python
- **Frameworks & Core ML:** Ultralytics YOLOv8, PyTorch (CPU optimized environment)
- **Computer Vision Framework:** OpenCV (Open Source Computer Vision Library)
- **Target Runtime Engine:** TensorFlow Lite (TFLite) / LiteRT

---

## 💻 Local Desktop Setup & Installation
### 1. Clone the Repository
```bash
git clone https://github.com/darshanraj1909-jpg/RealTime-Fire-Smoke-System.git
cd RealTime-Fire-Smoke-System
pip install ultralytics opencv-python
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
├── app.py             # Local Desktop Client application 
├── pi_app.py          # Embedded Raspberry Pi deployment client
├── best.pt            # PyTorch custom-trained target weights
└── best.tflite        # Exported lightweight TFLite model
python app.py

