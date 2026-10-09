# Vehicle Detection Using OpenCV

## Overview
This project implements a vehicle detection system using Python and OpenCV.
The system processes traffic video footage to identify moving vehicles within a 
selected Region of Interest (ROI). It uses background subtraction, image processing, and contour 
detection to locate moving objects and display bounding boxes around detected vehicles.
The project demonstrates fundamental computer vision techniques for automated traffic monitoring.

## Features
- Video processing using OpenCV
- Region of Interest (ROI) selection
- Moving object detection using MOG2 background subtraction
- Gaussian blur and morphological filtering
- Contour-based vehicle detection
- Bounding box visualisation
- Processing and analysis of two traffic videos

## Technologies Used
- Python
- OpenCV
- NumPy
- Matplotlib
- Jupyter Notebook

## Project Structure
```text
vehicle-detection/
├── README.md
└── vehicle_detection.ipynb
```

The original traffic videos are not included in this repository.

## How It Works
1. **Video Loading:** Reads traffic footage and extracts an initial frame for visual inspection.
2. **ROI Selection:** Defines the road area used for vehicle detection.
3. **Frame Preprocessing:** Applies Gaussian blur to reduce image noise.
4. **Background Subtraction:** Uses the MOG2 algorithm to identify moving foreground objects.
5. **Morphological Filtering:** Applies image processing operations to remove noise and improve detection.
6. **Contour Detection:** Identifies moving objects and filters them based on size and shape.
7. **Vehicle Visualisation:** Draws bounding boxes around detected moving objects in the traffic footage.

## Installation
Install the required Python libraries:

```bash
pip install opencv-python numpy matplotlib notebook
```

## Running the Project
1. Download or clone the repository.
2. Obtain compatible traffic video footage that you have permission to use.
3. Place the video files in the project directory.
4. If using different filenames, update the video file paths in `vehicle_detection.ipynb`. The original implementation references:
   - `Traffic_Laramie_1.mp4`
   - `Traffic_Laramie_2.mp4`
5. Launch Jupyter Notebook:

```bash
jupyter notebook
```

6. Open `vehicle_detection.ipynb`.
7. Execute the notebook cells in order.

**Note:** The ROI coordinates and detection parameters were configured for the original traffic footage. 
When using different videos, these settings may require adjustment to achieve suitable detection results.

## Results
The notebook demonstrates:

- Extraction and visualisation of traffic video frames.
- Selection of a Region of Interest for vehicle detection.
- Identification of candidate moving vehicles using background subtraction and contour analysis.
- Visualisation of detected objects using bounding boxes.

The implementation provides a basic demonstration of automated vehicle detection through computer vision.

## Limitations
- Detection accuracy may be affected by lighting conditions, shadows, and background movement.
- Overlapping vehicles may result in inaccurate detections.
- The system relies on predefined ROI coordinates and detection thresholds.
- Different traffic footage may require parameter adjustments.
- The implementation focuses on identifying moving objects rather than performing advanced vehicle classification.

## Dataset Availability
The original traffic videos were supplied for university coursework and are not redistributed in this public repository.
Users who wish to reproduce the implementation should provide their own appropriately licensed traffic footage and adjust 
the video paths and processing parameters where necessary.

## Conclusion
This project demonstrates the application of OpenCV for detecting moving vehicles in traffic footage.

By combining background subtraction, image preprocessing, and contour analysis, the implementation provides a foundation 
for automated traffic monitoring and more advanced computer vision applications.