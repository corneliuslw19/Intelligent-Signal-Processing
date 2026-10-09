# Intelligent Signal Processing

## Overview
This repository contains a collection of signal processing projects developed as part of university coursework.
The projects demonstrate practical applications of computer vision, lossless audio compression, and multimedia processing using Python and supporting libraries.
Each project focuses on implementing signal processing techniques and evaluating their effectiveness through practical experiments.

## Project Components
### 1. Vehicle Detection Using OpenCV (Exercise 1.1)
Developed a Python-based vehicle detection system using OpenCV to identify moving vehicles in recorded traffic footage.
The implementation uses MOG2 background subtraction, Gaussian blur, morphological filtering, and contour analysis to detect moving
objects within a selected Region of Interest (ROI).
Detected vehicles are visualised using bounding boxes.

**Key techniques:** OpenCV, background subtraction, image preprocessing, contour detection, and ROI selection.

### 2. Vehicle Counting and Traffic Flow Analysis (Exercise 1.2)
Developed a vehicle counting system that extends the computer vision techniques used in Exercise 1.1.
The implementation uses centroid-based object tracking and a virtual counting line to estimate the number of vehicles
travelling in a specified direction.
It also calculates estimated traffic flow rates in cars per minute and compares results across two traffic videos.

**Key techniques:** Vehicle detection, centroid tracking, directional counting, and traffic flow estimation.

### 3. Lossless Audio Compression Using Rice Coding (Exercise 2)
Implemented a lossless audio compression and decompression system using Differential
Pulse Code Modulation (DPCM), ZigZag mapping, and Rice coding.
The implementation compares Rice parameters K=2 and K=4, evaluates compression efficiency
across WAV audio samples, and verifies lossless reconstruction.
The experiments demonstrate how compression performance varies depending on the audio characteristics
and selected coding parameters.

**Key techniques:** DPCM, ZigZag encoding, Rice coding, compression analysis, and lossless verification.

### 4. Video Format Validation and Conversion (Exercise 3)
Developed a Python-based multimedia processing workflow using FFmpeg and FFprobe.
The implementation inspects video properties, validates file formats, and converts non-compliant videos into a consistent MP4 format.
The workflow generates validation reports and stores converted media separately from the original files.

**Key technologies:** Python, FFmpeg, FFprobe, and Jupyter Notebook.
Technologies Used
- Python
- OpenCV
- NumPy
- SciPy
- Matplotlib
- Jupyter Notebook
- FFmpeg and FFprobe

## Repository Structure
Intelligent-Signal-Processing/
├── exercise-1-computer-vision/
│   ├── ex1.1/
│   │   ├── README.md
│   │   └── vehicle_detection.ipynb
│   ├── ex1.2/
│   │   ├── README.md
│   │   └── vehicle_counting.ipynb
│   └── requirements.txt
├── exercise-2-rice-coding/
│   ├── .gitignore
│   ├── README.md
│   ├── requirements.txt
│   └── rice_coding.ipynb
├── exercise-3-media-processing/
│   ├── .gitignore
│   ├── README.md
│   ├── requirements.txt
│   ├── video_format_conversion.ipynb
│   └── reports/
│       └── format_report.txt
└── README.md

## Running the Projects
Each project contains its own implementation and setup instructions.
To run an exercise:
1. Download or clone the repository.
2. Navigate to the relevant project folder.
3. Refer to the project's README for installation and setup instructions.
4. Install the required Python libraries or other dependencies.
5. Provide compatible input audio or video files where necessary.
6. Run the notebook according to the instructions.

Some projects require additional software, such as FFmpeg.

## Dataset and Media Availability
The original traffic videos, audio samples, and other media used in some exercises were supplied for university coursework.
These media files are not redistributed in this public repository because permission for public redistribution has not been established.
Users who wish to reproduce the experiments should provide their own appropriately licensed media files and adjust file paths or
processing parameters where necessary.
Relevant implementation code and experimental results are retained to demonstrate the functionality of the projects.

## Conclusion
This repository demonstrates practical experience in implementing and evaluating signal processing techniques across
computer vision, audio compression, and multimedia applications.
The projects provided hands-on experience in Python programming, algorithm implementation, data analysis, media processing,
and interpreting experimental results.