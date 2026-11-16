# ⚽ Football Analysis System

A computer vision-based football match analysis system built with **Python, PyTorch, OpenCV, and YOLOv5**. The project automates player and ball detection, multi-object tracking, team classification, camera movement estimation, and player speed and distance analytics.

It also includes a **Next.js web application** for video uploads, backed by cloud infrastructure using **AWS EC2 and Amazon SQS** to orchestrate video-processing jobs.

---

## 🚀 Key Features

### Computer Vision & Deep Learning
- **Player and Ball Detection:** Detects players and the football using YOLOv5.
- **Object Tracking:** Tracks players across video frames.
- **Ball Assignment:** Associates the detected ball with nearby players.
- **Team Classification:** Classifies players into teams based on visual features.
- **Camera Movement Estimation:** Estimates camera motion to improve tracking consistency.
- **Speed & Distance Analytics:** Calculates player movement speed and distance covered.
- **Perspective Transformation:** Uses perspective mapping to estimate real-world player positions.

### Web Application & Cloud Infrastructure
- **Video Upload Interface:** Upload football match videos through a Next.js frontend.
- **Cloud Processing:** Runs video-analysis workloads on AWS EC2.
- **Job Orchestration:** Uses Amazon SQS to manage and coordinate processing tasks.
- **Deployment:** Frontend hosted on Vercel.

---

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Computer Vision | OpenCV |
| Deep Learning | PyTorch |
| Object Detection | YOLOv5 |
| Data Processing | NumPy, Pandas |
| Frontend | Next.js |
| Cloud Infrastructure | AWS EC2 |
| Message Queue | Amazon SQS |
| Frontend Deployment | Vercel |

---

## 📂 Project Structure

```text
Football-Analysis/
│
├── main.py
├── requirements.txt
│
├── input_videos/                 # Input match videos
├── output_videos/                # Processed output videos
│
├── models/                       # Trained model weights
│
├── camera_movement_estimator/    # Camera motion estimation
├── player_ball_assigner/         # Ball-to-player assignment
├── speed_distance_estimator/     # Speed and distance analytics
├── team_assigner/                # Team classification
├── trackers/                     # Object tracking
├── utils/                        # Video and bounding-box utilities
├── view_transformer/             # Perspective transformation
│
└── training/
    └── football_training_yolo_v5.ipynb
```

---

## ⚙️ Getting Started

### 1. Clone the Repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd Football-Analysis
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it:

**Windows**
```bash
venv\Scripts\activate
```

**Linux / macOS**
```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Add Model Weights

Place your trained YOLOv5 model weights inside the `models/` directory.

Example:

```text
models/
└── best.pt
```

### 5. Add Input Video

Place your football match video inside:

```text
input_videos/
```

### 6. Run the Analysis Pipeline

```bash
python main.py
```

Processed videos and analysis outputs are saved in the configured output directories, including `output_videos/` and `runs/`.

---

## 🧠 Model Training

The project includes a YOLOv5 training notebook:

```text
training/football_training_yolo_v5.ipynb
```

To train or fine-tune the detection model:

1. Open the training notebook.
2. Configure the dataset and training parameters.
3. Train the YOLOv5 model.
4. Export the trained weights.
5. Place the resulting weights in the `models/` directory.

---

## ☁️ Cloud Architecture & Deployment

The project extends beyond local video processing with a cloud-based video-analysis workflow.

**Architecture overview:**

```text
          User
           |
           v
    Next.js Frontend
           |
           v
      Video Upload
           |
           v
    Backend Services
           |
           v
      Amazon SQS
           |
           v
       AWS EC2
           |
           v
   Python CV Pipeline
           |
           v
   Analysis & Results
```

### Infrastructure Components

| Component | Responsibility |
|---|---|
| Next.js | Video upload and frontend interface |
| Vercel | Frontend hosting and deployment |
| AWS EC2 | Backend processing infrastructure |
| Amazon SQS | Processing-job orchestration |
| Python Pipeline | Computer vision and football analytics |

---

## 🌐 Live Demo

Explore the web application:

**[Football Analysis Web App](https://football-analysis-front.vercel.app/)**

---

## 📊 Analysis Capabilities

| Module | Functionality |
|---|---|
| Object Detection | Player and ball detection |
| Tracking | Player tracking across frames |
| Ball Assignment | Player-ball association |
| Team Assignment | Team classification |
| Camera Estimation | Camera movement estimation |
| Speed Analytics | Player speed estimation |
| Distance Analytics | Distance covered estimation |
| View Transformation | Perspective-based coordinate mapping |

---

## 🔮 Future Improvements

- Improve detection accuracy under challenging lighting and occlusion.
- Extend tracking robustness during player interactions.
- Add advanced match statistics and player performance metrics.
- Introduce real-time analytics and interactive visualizations.
- Optimize cloud processing for larger video workloads.

---

## 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Open a pull request.

---

**Built with Python, Computer Vision, Deep Learning, and Cloud Technologies.** ⚽
