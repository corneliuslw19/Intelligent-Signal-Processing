# Vehicle Counting and Traffic Flow Analysis Using OpenCV

## Overview
This project implements a vehicle counting and traffic flow analysis system using Python and OpenCV.
The system processes traffic video footage to detect moving vehicles, track their positions, and count 
vehicles crossing a virtual counting line in a specified direction.
It analyses two traffic videos and calculates the estimated total vehicle count and average traffic flow rate in cars per minute.
The project demonstrates how computer vision techniques can be applied to basic traffic monitoring and analysis.

## Features
- Video processing using OpenCV
- Region of Interest (ROI) selection
- Moving object detection using MOG2 background subtraction
- Gaussian blur and morphological filtering
- Vehicle detection using contour analysis
- Centroid-based object tracking
- Directional vehicle counting using a virtual line
- Traffic flow calculation in cars per minute
- Comparison of traffic flow across two videos

## Technologies Used
- Python
- OpenCV
- NumPy
- Matplotlib
- Jupyter Notebook

## Project Structure
```text
vehicle-counting/
├── README.md
└── vehicle_counting.ipynb
```

The original traffic videos are not included in this repository.

## How It Works
1. **Video Loading:** Reads traffic footage and extracts an initial frame.
2. **ROI Selection:** Defines the road area used for processing.
3. **Background Subtraction:** Uses MOG2 to identify moving objects.
4. **Image Processing:** Applies Gaussian blur, thresholding, and morphological operations to reduce noise.
5. **Vehicle Detection:** Identifies moving objects using contours and minimum-area filtering.
6. **Object Tracking:** Assigns temporary tracking IDs based on centroid positions.
7. **Vehicle Counting:** Counts tracked objects crossing a virtual horizontal line in the upward direction.
8. **Traffic Flow Analysis:** Calculates the estimated number of vehicles per minute and compares the two videos.

## Installation
Install the required Python libraries:

```bash
pip install opencv-python numpy matplotlib notebook
```

## Running the Project
1. Download or clone the repository.
2. Obtain compatible traffic footage that you have permission to use.
3. Place the video files in the project directory.
4. If using different filenames, update the video paths in `vehicle_counting.ipynb`. The original implementation references:
   - `Traffic_Laramie_1.mp4`
   - `Traffic_Laramie_2.mp4`
5. Launch Jupyter Notebook:

```bash
jupyter notebook
```

6. Open `vehicle_counting.ipynb`.
7. Execute the notebook cells in order.

**Note:** The ROI coordinates, virtual counting line, tracking thresholds, and detection parameters 
were configured for the original traffic footage. When using different videos, these settings may require adjustment. 
The counting direction may also need to be changed depending on the camera perspective.

## Results
The notebook generates:
- Total estimated vehicle count for each video.
- Estimated traffic flow rate in cars per minute.
- A comparison table displaying the results of both traffic videos.

Traffic flow values are rounded down to whole numbers for presentation.
The results demonstrate how moving-object detection and centroid-based tracking can be combined to estimate traffic flow.

## Limitations
- Detection accuracy may be affected by shadows, lighting changes, and background movement.
- Overlapping vehicles may result in inaccurate detections or tracking.
- Centroid-based tracking may incorrectly associate vehicles moving close together.
- Counting accuracy depends on the selected ROI, counting line, and detection thresholds.
- The original counting direction assumes that upward movement in the video corresponds to traffic travelling towards downtown.
- The estimated counts have not been independently validated against manually counted vehicles.

## Dataset Availability
The original traffic videos were supplied for university coursework and are not redistributed in this public repository.

Users who wish to reproduce the implementation should provide their own appropriately licensed traffic footage and adjust 
the video paths, ROI coordinates, counting line, and processing parameters where necessary.

## Conclusion
This project demonstrates how computer vision techniques can be used to estimate directional vehicle counts 
and traffic flow from video footage.

By combining background subtraction, contour detection, centroid tracking, and virtual line-crossing detection, 
the system provides a basic approach to automated traffic analysis.