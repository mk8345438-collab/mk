```bash
cd ~/Desktop/virtual-wall

python3 << 'PYEOF'
import os

with open(".gitignore", "w") as f:
    f.write("venv/\n__pycache__/\n*.pyc\ncalibration.json\nmodels/\n.DS_Store\n")

with open("requirements.txt", "w") as f:
    f.write("mediapipe>=1.0.0\npyautogui\nnumpy\nopencv-python\n")

readme_content = """# 🖱️ Air Mouse with Computer Vision & Auto-Zoom

A Python-based virtual mouse system that tracks your hand gestures and maps them to your screen, featuring **Auto-Zoom** for far-distance detection! Built with OpenCV and MediaPipe, optimized for Arch Linux.

---

## 🏗️ System Architecture

```text
+-------------------+       +---------------------+       +-------------------+
| 1. Camera Feed    | ----> | 2. MediaPipe Hands  | ----> | 3. Gesture Logic  |
| (1080p/720p)      |       | (Landmark Tracking) |       | (Tap Detection)   |
+-------------------+       +---------------------+       +---------+---------+
                                                                      |
                                      +-------------------------------+-------------------------------+
                                      |                                                               |
                                      v                                                               v
                        +-------------------------+                                       +-------------------------+
                        | 4. Perspective Transform|                                       | 5. PyAutoGUI Control    |
                        | (Maps camera to screen) |                                       | (Move, Left/Right Click)|
                        +-------------------------+                                       +-------------------------+
```

---

## ✨ Features

- 🎯 **4-Point Calibration**: Easily map any screen (Monitor or TV) to your camera view.
- 🔍 **Auto-Zoom**: Automatically zooms in on your hand when you move further away, ensuring accurate tracking from 2-3 meters!
- 👆 **Tap-to-Click**: 
  - ☝️ **1 Finger Tap**: Left Click
  - ☝️🖖 **2 Fingers Tap**: Right Click
- ⚡ **Optimized Performance**: Smooth cursor movement with adjustable smoothing.

---

## 🐧 Installation (Arch Linux)

### 1. Clone the repository
```bash
git clone https://github.com/mk8345438-collab/air-mouse.git
cd air-mouse
```

### 2. Create and activate virtual environment
```bash
python -m venv venv
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

```bash
python air_mouse_far.py
```

### Controls:
| Gesture | Action |
|---------|--------|
| ☝️ Index finger UP | Move Mouse |
| ☝️ UP → DOWN → UP | Left Click |
| ☝️🖖 UP → DOWN → UP | Right Click |
| ✊ Fist / Hand Down | Pause |
| `R` | Recalibrate |
| `ESC` | Exit |

---

## 👤 Author

**Mohammad**  
*13-year-old AI & Python Developer*  

---
*Made with ❤️ and Computer Vision*
"""

with open("README.md", "w", encoding="utf-8") as f:
    f.write(readme_content)

print("✅ فایل‌های پروژه با موفقیت ساخته شدند!")
PYEOF

git init
git add .
git commit -m "Initial commit: Air Mouse with Auto-Zoom and Tap-to-Click"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/air-mouse.git
git push -u origin main
```
