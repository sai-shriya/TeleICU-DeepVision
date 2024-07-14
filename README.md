<h1 align="center">TeleICU-DeepVision</h1>

<p align="center">This repository is for a project aimed at enhancing TeleICU systems. The solution uses deep learning and video processing to recognize different people in the ICU room and detect patient movements. This helps remote healthcare professionals monitor more patients simultaneously.</p><br>

## 💡Synopsis

The system utilizes YOLOv5, an open-source deep learning model, to detect and classify persons (including patients) in real-time video streams. It then applies optical flow analysis to detect movement within the patient's area of interest. Optionally, the system can calculate accuracy metrics against ground truth annotations to evaluate detection performance.

<br>

## Demo
https://github.com/user-attachments/assets/c0c10c23-5477-4497-b8e9-94d4448626ea

<br>

## 🔥 Highlights
***Automated Identification***: &nbsp;Uses deep learning to detect and classify individuals in the ICU, including nurses, doctors, family members, and patients.
  
***Patient Activity Monitoring***: &nbsp;Analyzes and identifies various activities of patients, especially when they are alone, to ensure their safety.
  
***Movement Detection***: &nbsp;Utilizes optical flow to detect and track patient movements, alerting healthcare professionals to any unusual or significant activity.
  
***Performance Metrics***: &nbsp;Calculates and displays the average prediction time and accuracy of detections to ensure system reliability and effectiveness.
  
***Remote Accessibility***: &nbsp;Allows healthcare professionals to monitor patients from any location, including from home, reducing the need for on-site presence.

<br>

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/sai-shriya/TeleICU-DeepVision.git
   cd TeleICU-DeepVision
   ```
   
2. Run the code:
   - Replace the path with your current path.
   - Uncomment and provide ground truth values if you have tested manually.

   **Note:** Run the code on Jupyter Notebook or Google Colab for optimal performance.

<br>

## Usage
To process a video and detect patient movements using the provided input and output video paths, execute the following command in your terminal:

 ```python
   # Example code snippet
   input_video_path = "replace_with_your_current_path/input_video.mp4"
   output_video_path = "replace_with_your_current_path/output_video.mp4"
   process_video(input_video_path, output_video_path, ground_truths)
```

<br>

## 🚀 Process Flow
1. ***Video Capture***: &nbsp;Continuous video feed from the ICU is captured and fed into the system.
   
2. ***Preprocessing***: &nbsp;Video frames are preprocessed for noise reduction and enhanced clarity.
   
3. ***Object Detection***: &nbsp;The YOLOv5 model detects and classifies individuals in the ICU.
   
4. ***Movement Analysis***: &nbsp;Optical flow algorithms analyze the movement of identified patients.
   
5. ***Performance Metrics Calculation***:
   - **Prediction Time**: &nbsp;Calculate the average prediction time per frame
   - **Accuracy**: &nbsp;Calculate the accuracy of detections

<br>

## 🤖 Tech Layout
<div align="center">
  <img src="https://github.com/user-attachments/assets/0f729b86-662d-485a-91db-007288c0a71c" height="400px" width="auto" alt="architecture">
</div>

<br>

## 🔧 Tools and Algos
- **Deep Learning Framework**: `PyTorch` for building and training the deep learning models.
  
- **Object Detection Model**: `YOLOv5` for detecting and classifying individuals in the ICU.
	+ The YOLO algorithm divides the input image into a grid of cells, and for each cell, it predicts the probability of the presence of an object and the bounding box coordinates of the object.

	+ **Why YOLOv5?**
	YOLOv5 can be used to detect and track objects more accurately in real-time video streams, enhancing the effectiveness of identifying moving objects in the ICU room for the "TeleICU-DeepVision" project. It provides precise bounding boxes and class labels, aiding in better analysis and monitoring.

<br>
<div align="center">
<img src="https://github.com/user-attachments/assets/5c9e82ee-2b76-460f-b312-5f61df07559b" height="200px" width="auto" alt="yolo">
</div>
<br>
  
- **Video Processing**: `OpenCV` for capturing, preprocessing, and analyzing video frames.
	+OpenCV, short for Open Source Computer Vision Library, is an open-source computer vision and machine learning software library used for real-time operation. Originally developed by Intel.

	+ **Why OpenCV?**
	OpenCV is used for its efficient implementation of image processing algorithms, such as optical flow, which is essential for tracking movement and changes in video streams in the "TeleICU-DeepVision" project. It provides real-time performance and a wide range of tools for computer vision tasks.
  
- **Movement Analysis**: &nbsp;Object movement based on `Optical flow algorithms` for detecting and tracking patient movements.
	+Optical flow is one of the efficient approaches to track the movement of objects. Optical flow studies the relative motion of objects across different frame sequences based on the velocity of movement of objects and illumination changes.

	+ **Why Optical flow?**
	Object movement based on optical flow is used to detect and track subtle patient movements and interactions in the ICU room, which is crucial for continuous monitoring and early intervention. It provides detailed motion analysis, enhancing the accuracy of patient activity recognition in the "TeleICU-DeepVision" project.

<br>
<div align="center">
<img src="https://github.com/user-attachments/assets/fa8e61b9-dcb8-428f-b471-9ee6779dbd4c" height="300px" width="auto" alt="opticalflow">
</div>
<br>
  
- **Data Analysis**: `Numpy` for numerical computations and `Scikit-learn` for clustering and other analytical tasks.
  
- **Performance Metrics**: &nbsp;Custom code for calculating average prediction time and accuracy of the system's detections.

<br>

## Conclusion
Our TeleICU monitoring system addresses the challenge of limited remote patient monitoring capacity by leveraging deep learning and video processing technologies. Using YOLOv5 for robust object detection and optical flow for movement analysis, the system allows one healthcare professional to monitor multiple ICU patients efficiently. By automating identification of personnel and patient activities, it enhances monitoring accuracy and reduces operational strain. This scalable solution, powered by PyTorch and OpenCV, supports remote monitoring from any location, exemplifying a transformative approach to ICU patient care in modern healthcare settings.
