# 🚦 Real-Time Traffic Monitoring & Intelligent Control System

An **AI-powered smart traffic management system** that leverages **YOLOv8** for real-time vehicle detection and **LSTM neural networks** for traffic flow prediction. The system dynamically controls traffic signals, prioritizes emergency vehicles, and provides a live visualization dashboard.

---

## 📸 Demo

![System Demo](https://i.postimg.cc/Zn2ZpLh8/Chat-GPT-Image-Apr-20-2025-02-37-11-PM.png)

🎥 **[Watch the Demo Video](https://drive.google.com/file/d/1aijR05oew3JxfjD6C62UK2TpRercrF2t/view?usp=sharing)**

---

## 🧠 Key Features

- 🔍 Real-time vehicle detection using **YOLOv8**
- 🚨 Emergency vehicle recognition and priority control
- 📈 Traffic congestion prediction using **LSTM neural networks**
- 🟢 Adaptive traffic signal control
  - Dynamic green light extension
  - Idle time reduction
  - Emergency override logic
- 📊 Live dashboard visualization
  - Vehicle counts
  - Traffic decisions
  - Real-time updates
- 🎥 Supports video files and live camera feeds

---

## 🧰 Technology Stack

| Layer               | Tools / Libraries |
|--------------------|------------------|
| Object Detection   | YOLOv8 (Ultralytics) |
| Video Processing  | OpenCV |
| Prediction Model  | TensorFlow / Keras (LSTM) |
| Dashboard UI      | Plotly Dash |
| Backend Logic     | Python (Multithreading) |

---

## 🚀 System Workflow

1. **Video Input**  
   Captures real-time video from a camera or video file using OpenCV

2. **Vehicle Detection**  
   YOLOv8 detects cars, buses, bikes, and emergency vehicles

3. **Traffic Prediction**  
   LSTM model predicts congestion levels based on vehicle density

4. **Decision Engine**  
   Adjusts traffic signal timing dynamically and prioritizes emergency vehicles

5. **Live Dashboard**  
   Displays vehicle count and traffic decisions with periodic updates

---

## 🖥️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/pratik1416
cd traffic-manage
```

### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 3️⃣ Prepare Input
- Add a sample video named `traffic_video.mp4`  
**OR**
- Connect a live camera feed

> YOLOv8 model weights are automatically downloaded via Ultralytics.

### 4️⃣ Run the Application
```bash
python app.py
```

---

## 📁 Project Structure

```
📂 traffic-monitoring-system/
│
├── evaluation_results/     # Generated evaluation plots
├── traffic_video.mp4       # Sample traffic footage
├── traffic_lstm.h5         # Pre-trained LSTM model
├── yolov8n.pt              # YOLOv8 nano weights
├── app.py                  # Main application script
├── evaluate.py             # Evaluation pipeline script
├── requirements.txt        # Dependencies
└── README.md               # Project documentation
```

---

## 📊 Public Traffic Datasets & Evaluation

To benchmark the detection and prediction models, we use standardized public datasets.

### Supported Datasets
1. **[UA-DETRAC](https://detrac-db.rit.albany.edu/)**: A challenging real-world multi-object detection and multi-object tracking benchmark.
2. **[BDD100K](https://bdd-data.berkeley.edu/)**: A diverse driving dataset for heterogeneous multitask learning.
3. **[METR-LA / PEMS-BAY](https://github.com/liyaguang/DCRNN)**: Traffic forecasting datasets containing traffic speed readings.

### Running the Evaluation Pipeline
We provide an evaluation script to calculate Accuracy, Precision, Recall, Specificity, F1-score, Confusion Matrix, Correlation Matrix, and FPS.

```bash
python evaluate.py --dataset path/to/dataset
```
*Note: If no dataset is provided, the script will run a demonstration using synthetic data and the sample video to generate the required plots in the `evaluation_results/` directory.*

---

## 🔮 Future Enhancements

- 📡 Integration of multiple camera feeds
- 🗄️ Storage of historical traffic data
- 📢 Real-time alerts to traffic authorities
- ☁️ Cloud deployment for large-scale use
- 🧠 Reinforcement learning for smarter signal optimization

---

## 🧑‍💻 Author

**Pratik Verma**  
📧 Email: vermapratik2213@gmail.com 
🔗 [LinkedIn] www.linkedin.com/in/pratikverma1414

---

⭐ If you find this project useful, consider giving it a star!
