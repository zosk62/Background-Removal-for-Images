# Background-Removal-for-Images


This project demonstrates methods to automatically remove backgrounds from images using image processing techniques and the Remove.bg API.

## Overview

The project utilizes Python and OpenCV for image processing to achieve background removal. It includes two main methods:
1. **bg_rm_01**: Uses image processing techniques such as Gaussian blur, edge detection, and contour detection to isolate foreground objects and remove backgrounds.
2. **bg_rm_02**: Utilizes the Remove.bg API to remove backgrounds from images automatically using a cloud-based service.

## Requirements

- Python 3.x
- OpenCV (`pip install opencv-python`)
- Requests library (`pip install requests`)

## Getting Started

1. **API Setup**:
   - Obtain an API key from [Remove.bg](https://www.remove.bg/api) and update `api_key` in the script.


3. **Usage**:
   - Place your images to be processed in the `profile_image` directory.
   - Run the script:
     ```
     python bg_removal.py
     ```
   - Processed images with removed backgrounds will be saved in the `profile_image/bg_rm` directory.

## Methodology

### bg_rm_01
This method employs:
- Gaussian Blur to reduce noise.
- Edge detection using Canny algorithm.
- Contour detection to identify the main object.
- Mask creation and blending to remove the background.

### bg_rm_02
This method utilizes:
- The Remove.bg API for automated background removal.
- Images are processed via a POST request with the provided API key.

## Output

Processed images will have their backgrounds removed and saved with the original filename appended with `_rm.png` (for method 1) or `_removebg.png` (for method 2).

