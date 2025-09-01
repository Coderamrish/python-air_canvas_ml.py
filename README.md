# ✨ Air Canvas ML Model

> **Author:** *Amrish Kumar*

---
## 🚀 Project Overview

Ever wished to capture your imagination by simply waving your finger in the air? **Air Canvas ML** brings your drawings to life, using real-time computer vision and machine learning to let you sketch in mid-air. No touch—just gestures!

---
## 🛠️ Technology Choices & Justification

- **Python**: Fast prototyping, huge ecosystem for CV/ML.
- **OpenCV**: Robust, industry-standard for real-time image/video processing and UI overlays.
- **MediaPipe**: Google's advanced hand tracking framework, efficient and easy for gesture recognition.
- **NumPy**: High-performance numerical operations for image arrays.
- **collections.deque**: Fast and memory-efficient storage for stroke points.

*Combining these, we deliver a smooth, interactive experience for air drawing!*

---
## 🎨 Features & UI Highlights

- **Modern Dark Mode Canvas**  
  Enhanced visibility and style for your sketches.

- **Sleek, Rounded Color Buttons with Live Highlight**  
  Intuitive color selection with animated borders, emoji icons, and easy visual feedback.

- **Clear Button with Animated Trash Icon**  
  Instantly erase your canvas with a single gesture.

- **Real-Time Hand Tracking Overlay**  
  See your detected hand landmarks live as a semi-transparent guide.

- **Dynamic Gesture Hints & Instructions**  
  Always know how to interact—helpful overlays guide you.

- **Undo/Redo (optional)**  
  Go back and forth between recent strokes.

---

## ✋ Gesture Recognition Logic

**Air Canvas ML** uses intelligent hand landmark tracking (via MediaPipe) to identify four main gestures:

| Gesture         | How it Works                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------|
| **Draw**        | Track the tip of the index finger (`landmark 8`). If away from thumb, record movement.      |
| **Pause (Lift)**| Thumb (`landmark 4`) close to index tip vertically (<30px): stops drawing, starts new stroke|
| **Select Color**| Move fingertip into any top-bar zone: <br> - Blue: `160-255`px <br> - Green: `275-370`px <br> - Red: `390-485`px <br> - Yellow: `505-600`px                                       |
| **Clear**       | Move fingertip into "Clear" button zone (`40-140`px): all strokes reset, canvas erased      |

---

## 🖼️ User Interface Preview

![UI Preview](https://user-images.githubusercontent.com/821285086/demo-ui-preview.png) <!-- Optional: Add a real screenshot or mockup! -->

| Button | Action       | Emoji/Icon |
|--------|--------------|------------|
| Blue   | Draw Blue    | 🟦         |
| Green  | Draw Green   | 🟩         |
| Red    | Draw Red     | 🟥         |
| Yellow | Draw Yellow  | 🟨         |
| Clear  | Erase Canvas | 🗑️         |

Current color is highlighted with a bright border!

---

## 📝 Getting Started

### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

### 2. Run the App
```bash
python air canvas ml.py
```
Press **Q** to exit.

---

## 📋 Requirements

See [`requirements.txt`](./requirements.txt) for full details:
```text
opencv-python
mediapipe
numpy
```

---

## 📖 License

MIT

---

## 💬 Contact

Questions, feedback, or want to collaborate?  
Find me on GitHub: [Coderamrish](https://github.com/Coderamrish)

---

*Bring your imagination to life—draw without boundaries!*
