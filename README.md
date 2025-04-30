# Crowd-Analytics-in-Surveillance-Video
This project processes a video file to analyze the crowd density at different frames using YOLOv8, a state-of-the-art object detection model. It tracks the number of people in each frame, categorizes the crowd as "Crowded" or "Calm," and visualizes the results in real-time.

# Requirements
To run this project, ensure you have the following Python libraries installed:
opencv-python
pandas
matplotlib
numpy
IPython
ultralytics (for YOLOv8)
# Parameters
MAX_DURATION_SEC: The maximum duration of the video to process (in seconds).
FRAME_SKIP: Number of frames to skip during processing (this speeds up analysis).
RESIZE_DIMS: Dimensions to resize the video frames for analysis.
PERSON_THRESHOLD: The threshold number of people for a frame to be labeled as "Crowded."
# Setup
Clone or download the project repository.
Ensure that you have a valid video file (In this project i have used video of the park) and update the video_path variable with the correct path if necessary.
Download the YOLOv8 model weights file (yolov8n.pt) from the official Ultralytics GitHub or use the provided one in the project directory.
# Usage
Running the Script: After setting up the environment and ensuring the correct video file path and YOLOv8 model are in place, simply run the Python script.
The script will:
Process the video frame by frame.
Detect people using YOLOv8.
Categorize the crowd as "Crowded" or "Calm."
Display the annotated video frames along with a real-time graph of crowd density.

# Output:
The analysis results are saved to a CSV file called crowd_status_results.csv containing the following columns:
frame: The frame number.
time_sec: The timestamp of the frame in seconds.
num_people: The number of people detected in the frame.
status: The status of the frame ("Crowded" or "Calm").
# Visualization
The script uses matplotlib to display the following:
Video Frames: Annotated frames showing the crowd status and number of people detected.
Crowd Density Graph: A real-time graph that shows the number of people over time, with a red dashed line indicating the threshold for "Crowded."
# License
This Project is under MIT License
