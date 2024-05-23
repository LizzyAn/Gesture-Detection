# Gesture-Detection
## Requirements
- opencv-python-headless
- numpy
- tensorflow

Install the required packages using:
```sh
pip install -r requirements.txt

Steps 
Upload Gesture Image/Video and Test Video
Process Gesture Image/Video to Extract Features
Process Test Video to Detect Gesture
Annotate Frames and Save Output Video

# Motion Detection in Video Sequences

## Objective
This project detects motion within a video sequence and annotates the frames where motion is detected with the text "DETECTED" in bright green.

## Setup Instructions

### Prerequisites
- Ensure you have Python 3.7 or above installed on your system.
- Google Colab environment.

### Installation
1. Create a virtual environment and install the required packages by running:
    ```sh
    python -m venv motion_env
    source motion_env/bin/activate  # On Windows use `motion_env\Scripts\activate`
    pip install -r requirements.txt
    ```

### Running the Code in Google Colab
1. Open [Google Colab](https://colab.research.google.com/) and create a new notebook.
2. Enable GPU by going to `Runtime` -> `Change runtime type` -> Set `Hardware accelerator` to `GPU`.
3. Upload the `test_video.mp4` file.
4. Copy and paste the provided Colab code into the notebook cells and run them step-by-step.

## Explanation of the Code
- **Data Processing**: The input test video is loaded and processed frame by frame.
- **Motion Detection**: Background subtraction using `cv2.createBackgroundSubtractorMOG2()` is applied to detect motion in each frame.
- **Annotation**: The text "DETECTED" is overlaid on frames where motion is detected.
- **Documentation**: This README provides setup and usage instructions, as well as an explanation of the approach.

## Challenges and Solutions
- **Varying Motion**: Motion detection may vary in sensitivity. The use of contour area filtering helps in handling some variability.
- **Performance**: Processing each frame can be computationally expensive. Optimizations include reducing the frame rate for processing or using GPU acceleration.

This approach provides a basic framework for motion detection, which can be further refined based on specific requirements and constraints.
