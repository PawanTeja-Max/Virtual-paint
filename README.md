# Virtual Paint 🎨

A real-time computer vision project built with Python and OpenCV. Virtual Paint uses a webcam to detect objects based on their color and can be extended to draw on the screen by tracking a colored object.

## Features

- **Live webcam feed** — captures video using OpenCV.
- **HSV color detection** — identifies objects based on their Hue, Saturation, and Value.
- **Interactive HSV trackbars** — adjust color thresholds in real time.
- **Binary masking** — isolates pixels that match the selected color range.
- **Contour detection** — locate detected objects for future drawing functionality.

## Tech Stack

- Python 3
- OpenCV (`opencv-python`)
- NumPy

## Installation

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd "virtual paint"
```

### 2. Create a virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```


### 4. Add values for ranges of Hue , Saturation and Value in myColors for your desired colors

### 5. Add values for Hue , Saturation and Values in myColorValues for contour colors

Any ideas for making this process easier and quicker would be highly appreciated

### 6. Run the project

```bash
python code.py
```

## How It Works

1. Capture frames from the webcam using `cv2.VideoCapture()`.
2. Convert each frame from BGR color space to HSV using `cv2.cvtColor()`.
3. Read the HSV threshold values from the trackbars.
4. Create a binary mask using `cv2.inRange()`.
5. Display the camera feed and the resulting color mask.
6. Use contour detection to identify the boundaries of detected objects.

## Controls

- Adjust the HSV trackbars to isolate the target color.
- Press **Q** to exit the application.

## Future Improvements

- Detect and track the largest colored object using contours.
- Draw on a virtual canvas using the object's position.
- Support multiple colors with separate drawing modes.
- Improve tracking stability with noise reduction.
- Maybe implementing a feature that can turn a fixed object into a mouse pointer

## Contributing

Contributions, suggestions, and improvements are welcome. Feel free to fork the repository and submit a pull request.
And any ideas related to future expansions will be highly appreciated
