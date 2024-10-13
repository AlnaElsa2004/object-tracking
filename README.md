# Object Tracking in Computer Vision

## Project Overview
This project implements object tracking using two popular techniques: **KCF (Kernelized Correlation Filters)** and **CSRT (Channel and Spatial Reliability Tracking)**. The primary goal is to compare the performance of these algorithms in tracking objects across video frames and to conclude which tracker performs better in terms of accuracy and efficiency.

During the development, it was observed that **CSRT** outperformed **KCF** in tracking accuracy, especially in challenging scenarios where objects undergo rapid changes in appearance or movement. However, **KCF** proved to be faster, making it suitable for applications requiring real-time tracking with less computational overhead.

## Tools and Technologies
- **Language:** Python
- **IDE:** Visual Studio Code
- **Libraries:**
  - OpenCV
  - Numpy

## Trackers Used:
1. **KCF (Kernelized Correlation Filter):**
   - Suitable for real-time object tracking.
   - Faster but less accurate in scenarios with occlusions or object deformation.

2. **CSRT (Channel and Spatial Reliability Tracking):**
   - More accurate than KCF, especially when handling object appearance changes.
   - Slightly slower but better for applications where accuracy is crucial.

## Prerequisites
Ensure the following are installed before running the project:

1. Python 3.x
2. Install necessary libraries using pip:

    ```bash
    pip install opencv-python opencv-contrib-python numpy
    ```

## Project Setup
1. Clone or download this repository to your local machine.
2. Open the project folder in **Visual Studio Code**.
3. Make sure you have a video file for testing, and place it in the project directory. Update the file path in the code if necessary.

## How to Run
1. Open the terminal in Visual Studio Code.
2. Run the Python script using the following command:

    ```bash
    python object_tracking.py
    ```

3. You will be prompted to select the object to track in the video by drawing a bounding box. Press **SPACE** or **ENTER** to confirm the selection, or **C** to cancel.
4. The program will then track the object using the selected tracker (either KCF or CSRT) until the end of the video.

## Key Insights
- **KCF**: Provides faster tracking but struggles with objects that deform or become occluded.
- **CSRT**: Offers better tracking accuracy and is more robust to changes in object appearance, though at the cost of some speed.

## Conclusion
In this project, we experimented with both KCF and CSRT tracking algorithms. After extensive testing, **CSRT** was found to be more efficient in terms of accuracy and reliability. However, if real-time performance is a priority, **KCF** could be a better choice due to its faster processing time.

## Future Work
- Implementing additional tracking algorithms like **MOSSE**, **MedianFlow**, or **TLD** for further comparison.
- Optimizing the project for real-time object tracking applications using hardware acceleration.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
