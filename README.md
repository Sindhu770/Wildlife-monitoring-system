# 🐾 Wildlife Monitoring System using Camera Traps

## 📌 Project Overview
The **Wildlife Monitoring System using Camera Traps** is a computer vision project that uses the YOLOv5 object detection model to identify wildlife in images captured by camera traps. This tool automates the detection process, making it efficient for researchers and conservationists.

## 🛠 Technologies Used
- Python
- Google Colab
- YOLOv5 (You Only Look Once version 5)
- PyTorch
- Matplotlib
- PIL (Python Imaging Library)

## 📂 Project Structure
- **Clone YOLOv5 Repository**: Downloads the detection model and codebase.
- **Install Requirements**: Installs the necessary Python libraries.
- **Load YOLOv5s Model**: Uses a lightweight, fast version of YOLOv5.
- **Upload Image**: Upload a camera trap image via Colab.
- **Detect Wildlife**: YOLOv5 identifies animals in the image.
- **Visualize and Save**: Shows and saves the result with bounding boxes.

## 🚀 How It Works

### Step 1: Clone YOLOv5 Repository
```bash
!git clone https://github.com/ultralytics/yolov5
```

### Step 2: Install Required Packages
```bash
!pip install -r requirements.txt
```

### Step 3: Import Libraries
```python
import torch
from matplotlib import pyplot as plt
import os
from PIL import Image
```

### Step 4: Load YOLOv5 Model
```python
model = torch.hub.load('ultralytics/yolov5', 'yolov5s')
```

### Step 5: Upload Image
```python
from google.colab import files
uploaded = files.upload()
```

### Step 6: Run Detection
```python
results = model(img_path)
results.print()
results.show()
results.save()
```

## 📷 Output
Detected images include bounding boxes around identified animals. Saved results are located in `yolov5/runs/detect/exp`.

## ✅ Advantages
- Seamless integration with Google Colab
- Fast and accurate detection with YOLOv5
- User-friendly for non-programmers

## 🔄 Future Improvements
- Batch image processing
- Real-time video detection
- Exporting results to CSV
- Training on custom wildlife datasets

## 🧑‍💻 Author
Developed as part of a wildlife conservation monitoring project using AI and open-source tools.
