# Face Anonymizer

## Overview
Face Anonymizer is a Python application that automatically detects and blurs faces in images, videos, or webcam feeds. It uses MediaPipe's face detection model to identify faces and OpenCV to apply blurring effects, ensuring privacy in visual content.

## Features
- Blur faces in static images
- Process video files to anonymize all faces
- Real-time face blurring in webcam feeds
- Simple command-line interface

## Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package installer)

### Setup
1. Clone this repository:
   ```
   git clone https://github.com/yourusername/face_anonimizer.git
   cd face_anonimizer
   ```

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

## Usage

### Webcam Mode (Default)
To blur faces in your webcam feed:
```
python main.py
```
Press any key to exit the webcam view.

### Image Mode
To blur faces in a single image:
```
python main.py --mode image --filePath data/testImg.png
```
The processed image will be saved to `output/output.png`.

### Video Mode
To blur faces in a video file:
```
python main.py --mode video --filePath data/testVideo.mp4
```
The processed video will be saved to `output/output.mp4`.

## Examples

### Input Image
The repository includes sample images in the `data` folder that you can use for testing.

### Output
Processed files are saved to the `output` directory.

## How It Works
The application uses MediaPipe's face detection model to identify faces in the input. Once faces are detected, a Gaussian blur is applied to the region containing each face, effectively anonymizing the person while preserving the rest of the image.

## License
[Add your license information here]

## Acknowledgments
- [MediaPipe](https://mediapipe.dev/) for the face detection model
- [OpenCV](https://opencv.org/) for image and video processing capabilities
