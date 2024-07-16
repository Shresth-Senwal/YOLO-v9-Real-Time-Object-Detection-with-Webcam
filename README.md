# YOLO v9 Real-Time Object Detection with Webcam

## Table of Contents

- [Introduction]
- [Features]
- [Installation]
- [Usage]
- [Customization]
- [Issues Faced]
- [License]
## Introduction

This project implements YOLO v9 for real-time object detection using a webcam. YOLO (You Only Look Once) is a state-of-the-art object detection algorithm known for its speed and accuracy. This project integrates YOLO v9 to perform real-time detection using a computer's webcam.

## Features

- **Real-Time Detection:** Seamless real-time detection with your webcam.
- **High Accuracy:** Utilizes YOLO v9 for precise object detection.
- **Easy Setup:** Simple to configure and run on any machine with a webcam.

## Installation

Follow these steps to set up the project:

1. **Clone the Repository**

    ```bash
    git clone https://github.com/yourusername/yolo-v9-webcam.git
    ```

2. **Install Dependencies**

    Ensure you have Python 3.7+ installed. Then, install the required packages:

    ```bash
    pip install -r requirements.txt
    ```

3. **Download YOLO v9 Weights**

    Download the pre-trained YOLO v9 weights from the official source and place them in the `weights` directory.

    ```bash
    mkdir weights
    cd weights
    # Download the weights file and place it in this directory
    ```

## Usage

To start real-time object detection with your webcam:

```bash
python detect.py --weights gelan-c.pt --conf 0.5 --source 0 --device 0
```

This will activate your webcam and start detecting objects in real-time. The detected objects will be highlighted with bounding boxes and labels.

## Customization

You can customize the detection parameters and configurations in the `config.py` file. Adjust settings such as detection threshold, input size, and more to fit your needs.

## Issues Faced

During the development of this project, I encountered the following issues:

1. **CUDA Compatibility:**
   - I had to reinstall CUDA to a version compatible with PyTorch, which was version 12.1. Ensure you check the compatibility between the CUDA and PyTorch versions you are using.

2. **Manual Upgrades:**
   - I had to manually upgrade the Ultralytics package to ensure compatibility with YOLO v9. You can upgrade it using:
     ```bash
     pip install --upgrade ultralytics
     ```

3. **Additional Installations:**
   - Despite installing all components from the `requirements.txt` file using `pip install -r requirements.txt`, I had to manually install some components. If you encounter missing dependencies, try installing them individually.

4. **OpenCV Reinstallation:**
   - I had to reinstall OpenCV to resolve compatibility issues. You can reinstall it using:
     ```bash
     pip install --upgrade opencv-python
     ```
## License

This project is licensed under the MIT License. See the [LICENSE] file for more details.

## Acknowledgements

- [YOLO v9 Official Repository] https://github.com/WongKinYiu/yolov9.git
- [OpenCV](https://opencv.org/)
