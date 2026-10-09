# Video Format Validation and Conversion Using FFmpeg

## Overview
This project implements a video format validation and conversion workflow using Python and FFmpeg.
The system processes video files, examines their format properties, identifies files that do not meet 
the required specifications, and converts them into a consistent MP4 format.

The project demonstrates practical media processing techniques, automated file validation, and video conversion.

## Features
- Discovers video files from an input directory.
- Inspects video format properties using FFmpeg tools.
- Checks files against predefined format requirements.
- Converts non-compliant videos into MP4 format.
- Saves converted videos in a separate output directory.
- Generates a text report documenting validation results.

## Technologies Used
- Python
- FFmpeg and FFprobe
- Jupyter Notebook
- Python standard library utilities

## Project Structure
```text
exercise-3-media-processing/
├── README.md
├── requirements.txt
├── .gitignore
├── video_format_conversion.ipynb
├── input/                  # Original videos (not included)
├── output/                 # Generated videos (not included)
└── reports/
    └── format_report.txt
```

## How It Works
1. **Video Discovery:** The notebook searches the input directory for supported video files.
2. **Format Inspection:** Video properties are extracted using FFmpeg tools.
3. **Validation:** The extracted properties are compared against predefined format requirements.
4. **Conversion:** Videos requiring conversion are processed using FFmpeg.
5. **Output Generation:** Converted videos are saved to the output directory.
6. **Reporting:** Validation results are recorded in a text report.

## Installation
Install Python, Jupyter Notebook, and FFmpeg.
Ensure FFmpeg and FFprobe are accessible through your system's PATH.
Install the Python dependencies:

```bash
pip install -r requirements.txt
```

## Running the Project
1. Download or clone the repository.
2. Open the `exercise-3-media-processing` folder in VS Code or Jupyter.
3. Place your own video files inside the `input/` directory.
4. Open `video_format_conversion.ipynb`.
5. Run the notebook cells in order.
6. Review the converted videos in `output/` and the generated report in `reports/`.

**Note:** The original videos were supplied for university coursework and are not redistributed in 
this public repository. Users should provide their own appropriately licensed videos to reproduce the workflow.

## Results

The notebook demonstrates an automated workflow for inspecting video properties, identifying format compliance, 
converting non-compliant videos, and generating a validation report.

The generated `format_report.txt` provides a record of the validation results.

## Limitations

- FFmpeg must be installed separately.
- Video conversion can be time-consuming for large files.
- Conversion may increase file size or reduce quality depending on the encoding settings.
- The validation rules are predefined rather than automatically adapted to different use cases.

## Conclusion

This project demonstrates how Python and FFmpeg can be combined to automate video format inspection, 
conversion, and reporting. The workflow provides a foundation for larger media processing applications.