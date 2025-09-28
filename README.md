🚘 Car Parking Detection

This project uses YOLOv8 object detection to monitor and analyze the occupancy of parking slots in real-time. With the help of a user-friendly Streamlit interface, it provides a powerful tool for car parking management using both predefined and custom videos.
🧠 Features

🎯 High-accuracy vehicle detection using YOLOv8.
📊 Real-time vacant and occupied parking slot statistics.
📹 Works with built-in videos or custom uploaded videos.
✍️ Interactive tool to draw, modify, and save parking slots.
💾 Automatically saves slots for each video.
🧱 Modular code using OpenCV and NumPy.
📁 Project Structure

.
├── app.py              # Streamlit app for real-time detection and dashboard
├── mark_slots.py       # OpenCV tool to define and save parking slots manually
├── parking_slots/      # Directory to store saved slot definitions
├── videos/             # Predefined video files (easy1.mp4, easy2.mp4, etc.)
└── yolov8m.pt          # YOLOv8 model weights (auto-downloaded if available)

⚙️ Requirements

Python 3.8+
YOLOv8
OpenCV
Streamlit
NumPy
Install dependencies:
pip install streamlit opencv-python-headless ultralytics numpy
🚀 Getting Started

Step 1: Mark Parking Slots

Run the following script to draw parking slot polygons on a video frame:
python mark_slots.py
Use left-click to draw or drag points.
Right-click to delete the last slot.
Press s to save, q to quit without saving.
Press c to copy the last drawn slot.
Saved slot coordinates will be stored in parking_slots/ as .npy files.
Step 2: Start the Streamlit App

streamlit run app.py
Choose a predefined video or upload your own.
The app will use the corresponding saved slots or ask you to draw them if not found.
Live status of total, vacant, and occupied slots will be displayed side-by-side with the video.
📦 Model Weights

Ensure the YOLOv8 weights file (yolov8m.pt) is in the working directory. It should automatically download when the model is loaded, but if there’s a connection issue, you can manually download it from: https://github.com/ultralytics/assets/releases/
📷 Sample Videos(make sure all videos are in 1 folder )

Make sure sample videos (easy1.mp4, easy2.mp4, etc.) are placed in the videos/ directory. You can add more videos and draw slot files for each.
🧑‍💻 Author

Kunal Sharma
[Teerthanker Mahaveer University]
Project submitted to Cogent Infotech
