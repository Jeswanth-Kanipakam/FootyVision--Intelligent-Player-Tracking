# FootyVision — Intelligent Player Tracking

FootyVision is a comprehensive computer vision project that combines object detection, tracking, clustering, and geometric transformations to analyze football matches. The project leverages both state-of-the-art and custom-trained AI models to detect players, referees, and footballs, then track them across video frames while calculating speed and distance covered by individual players.

---

## 🔍 Project Overview

This project utilizes **YOLO** (You Only Look Once), a state-of-the-art object detection model, to identify:
  - Players  
  - Referees  
  - Footballs

To enhance the results, we also **train a custom object detector** on a football-specific dataset.

### Key Functionalities:
  - **Tracking:** Track all detected objects across video frames.
  - **Team Assignment:** Identify team affiliation based on t-shirt color using **KMeans clustering**.
  - **Camera Movement Compensation:** Use **optical flow** to measure and adjust for camera movement.
  - **Scene Calibration:** Apply **perspective transformation** to measure movement in real-world units (meters).
  - **Player Stats:** Calculate each player's **speed** and **distance covered**.

---

## 📦 Modules Used

The following modules and algorithms are implemented in this project:

| Module                               | Purpose                                                     |
|--------------------------------------|-------------------------------------------------------------|
| **YOLO**                             | Object detection (players, referees, balls)                 |
| **KMeans**                           | Pixel segmentation and clustering for team identification   |
| **Optical Flow**                     | Compensate for camera motion across frames                  |
| **Perspective Transformation**       | Calibrate field perspective to measure distance in meters |
| **Speed & Distance Calculation**     | Compute player performance metrics from tracking data     |

---

## 📁 Dataset & Input Video

  - **Dataset:** [Football Players Detection Dataset](https://universe.roboflow.com/stageodilon/detection-football-players/dataset/1) from Roboflow
  - **Input Video:** Must be uploaded manually — download from **Kaggle** and place it in the root or a specified folder.

---

## 🚀 How to Use

1. **Upload Input Video:**
   - Download a football match video from Kaggle or other sources.
   - Place the video file in the project directory or a user-specified path.

2. **Create Required Folders:**
   Make sure these folders exist before running the code:
   
   output_videos/
   
   stubs/
   
   These folders are used for storing:
      - `output_videos/`: Annotated output videos with tracking and labels
      - `stubs/`: Intermediate or debug information

4. **Update Code with Paths:**
   Modify your code to include correct paths to:
    - Input video
    - Output video folder
    - Stub/debug folder

---

## 🧠 Future Improvements

  - Real-time inference support
  - Integration with live match feeds
  - Deep learning-based team classification
  - Player re-identification across cameras

---

## 🤝 Contribution

Feel free to fork, contribute, or suggest improvements via issues or pull requests.

---

## 🙌 Acknowledgements

- [YOLO by Ultralytics](https://github.com/ultralytics/yolov5)
- [Roboflow Dataset](https://universe.roboflow.com)
- [Kaggle Datasets and Videos](https://www.kaggle.com)

---

Contact

Jeswanth Kanipakam: LinkedIn - https://www.linkedin.com/in/jeswanth-kanipakam

Email: jeswanthkanipakam@gmail.com

