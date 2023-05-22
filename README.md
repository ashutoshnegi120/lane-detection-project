# Lane Detection Using Python and OpenCV

## Introduction
This project aims to develop a lane detection system using Python and OpenCV. The system analyzes images or video streams and detects lane boundaries on roads. Lane detection is a fundamental task in autonomous driving, advanced driver-assistance systems (ADAS), and computer vision applications.

## Prerequisites
To run this project, you need the following prerequisites:
- Python 3.x installed on your system
- OpenCV library (version 3.4 or higher) installed
- NumPy library installed
- Matplotlib library installed

## Setup and Usage
1. Clone the project repository to your local machine.
2. Make sure you have the required libraries installed by running the following commands:
   ```
   pip install opencv-python
   pip install numpy
   pip install matplotlib
   ```
3. Open the project in your preferred Python IDE or editor.
4. Modify the input source path (image file or video file) in the main script as required.
5. Run the main script, `lanes.py`.

## Approach
The lane detection algorithm implemented in this project follows a common computer vision approach. The key steps involved are as follows:

1. **Input Preprocessing**: The input image or video frame is read and preprocessed to enhance relevant features. Common preprocessing techniques include resizing, grayscaling, blurring, and edge detection.

2. **Region of Interest Selection**: A region of interest (ROI) is defined to focus only on the relevant part of the image where lane lines are expected. This step helps reduce noise and processing time.

3. **Edge Detection**: The Canny edge detection algorithm is applied to identify the edges in the ROI. The Canny algorithm detects significant changes in pixel intensity, highlighting the edges.

4. **Hough Transform**: The Hough transform is applied to the edge-detected image to identify lines in the image space. The Hough transform represents lines as points in a parameter space.

5. **Line Filtering**: The detected lines are filtered based on slope and position within the ROI. Only lines with slopes falling within a specific range are considered.

6. **Line Averaging and Extrapolation**: The remaining lines are averaged and extrapolated to obtain two lane lines. The averaging helps reduce noise and provides a smoother representation of the lanes.

7. **Visualization**: The detected lane lines are overlaid on the original image or video frame to provide visual feedback.

## Project Files
- `lanes.py`: The main script that performs lane detection on an image or video source.
- `test_image.jpg`: sample images for testing the lane detection algorithm.
- `test2.mp4/`:sample videos for testing the lane detection algorithm.

## Acknowledgments
The lane detection algorithm implemented in this project is inspired by various open-source projects and tutorials available online. Special thanks to the authors and contributors of these resources.

## License
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT). Feel free to modify and distribute the code as per the terms of the license.

## Conclusion
Lane detection is a crucial component of autonomous vehicles and ADAS systems. This project provides a basic implementation of a lane detection system using Python and OpenCV. You can further enhance the algorithm by incorporating advanced techniques such as deep learning-based approaches or lane tracking algorithms. Happy lane detection!
