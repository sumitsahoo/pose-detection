# 🏃🏻 YOLO Pose Detection Project

This project uses the YOLO (You Only Look Once) real-time object detection system, specifically the Ultralytics implementation, to perform pose detection.

## 📦 Dependencies

This project requires the Ultralytics YOLO library. You can install it with poetry:

```bash
poetry add ultralytics
```

Run the app with poetry:

```bash
poetry run python main.py
```


## 👨🏻‍💻 Usage
The main script for this project is main.py. It loads a YOLO model trained for pose detection and uses it to perform pose detection on webcam input.

```python
from ultralytics import YOLO

model = YOLO("yolov8m-pose.pt")  # Load model

results = model(source=0, show=True, conf=0.3, save=True)  # Webcam
```
In this script, source=0 tells the model to use the webcam as the input source. show=True will display the webcam feed with the pose detection overlay. conf=0.3 sets the confidence threshold for detections, and save=True will save the output frames.

## 📜 License

MIT License

Copyright (c) 2024 Sumit Sahoo

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.