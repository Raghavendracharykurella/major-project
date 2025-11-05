# Gesture Controlled Presentation System

## Overview
An innovative presentation control system that uses hand gestures detected via webcam to control PowerPoint presentations. This system leverages computer vision and machine learning to provide a touchless, intuitive way to navigate through slides.

## Features
- **Hand Gesture Recognition**: Real-time detection and recognition of hand gestures using MediaPipe
- **Touchless Control**: Navigate presentations without physical contact with any device
- **Multiple Gesture Commands**:
  - ✋ Open palm (5 fingers) - Next slide
  - ✌️ Peace sign (2 fingers) - Previous slide
  - 👍 Thumbs up - Start/Resume presentation
  - 👎 Thumbs down - End presentation
- **Visual Feedback**: On-screen display of detected gestures and hand landmarks
- **Real-time Processing**: Low-latency gesture detection for smooth presentation control
- **Cross-platform Compatibility**: Works on Windows, macOS, and Linux

## Tech Stack
- **Python 3.7+**: Core programming language
- **OpenCV (cv2)**: Computer vision and webcam interface
- **MediaPipe**: Hand tracking and landmark detection
- **python-pptx**: PowerPoint file handling
- **pyautogui**: Keyboard automation for presentation control

## Prerequisites
- Python 3.7 or higher
- Webcam
- PowerPoint or compatible presentation software
- Windows/macOS/Linux operating system

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/Raghavendracharykurella/major-project.git
cd major-project
```

### 2. Install Required Libraries
```bash
pip install opencv-python
pip install mediapipe
pip install python-pptx
pip install pyautogui
```

Or use the requirements file (if provided):
```bash
pip install -r requirements.txt
```

## Usage

### Running the Application
1. Open your PowerPoint presentation in presentation mode
2. Run the gesture control script:
```bash
python gesture_control.py
```
3. Position yourself in front of the webcam
4. Use the following gestures:
   - Show 5 fingers (open palm) to go to the next slide
   - Show 2 fingers (peace sign) to go to the previous slide
   - Thumbs up to start/resume
   - Thumbs down to end

### Tips for Best Performance
- Ensure good lighting conditions
- Position your hand clearly in the webcam frame
- Keep your hand steady when making gestures
- Maintain a distance of 1-2 feet from the camera
- Avoid cluttered backgrounds

## How It Works

### System Architecture
1. **Webcam Capture**: The system captures video frames from the webcam using OpenCV
2. **Hand Detection**: MediaPipe's hand tracking solution detects and tracks hand landmarks in each frame
3. **Gesture Recognition**: Custom algorithm analyzes hand landmarks to identify specific gestures
4. **Command Execution**: Recognized gestures trigger corresponding keyboard commands via PyAutoGUI
5. **Visual Feedback**: Detected gestures and hand landmarks are displayed on screen in real-time

### Gesture Detection Algorithm
- **Finger Counting**: Analyzes the positions of fingertip landmarks relative to finger base landmarks
- **Orientation Detection**: Determines hand orientation to distinguish between different gestures
- **Temporal Filtering**: Implements gesture stabilization to avoid false positives
- **Confidence Thresholding**: Only triggers commands when gesture confidence exceeds threshold

### Code Flow
```python
1. Initialize webcam and MediaPipe hand detector
2. While application is running:
   a. Capture frame from webcam
   b. Process frame with MediaPipe
   c. Extract hand landmarks
   d. Analyze landmarks to identify gesture
   e. Execute corresponding presentation command
   f. Display visual feedback
   g. Check for exit condition
3. Release resources and close application
```

## Project Structure
```
major-project/
│
├── gesture_control.py      # Main application script
├── README.md              # Project documentation
├── index.html             # GitHub Pages showcase
├── requirements.txt       # Python dependencies
└── assets/               # Additional resources
    ├── images/          # Screenshots and diagrams
    └── docs/            # Additional documentation
```

## Configuration
You can customize the following parameters in the code:
- **Gesture confidence threshold**: Adjust sensitivity of gesture detection
- **Hand detection confidence**: Set minimum confidence for hand detection
- **Camera resolution**: Configure webcam resolution for optimal performance
- **Gesture cooldown**: Set delay between consecutive gesture recognitions

## Troubleshooting

### Common Issues
1. **Hand not detected**: Improve lighting or adjust camera position
2. **Incorrect gesture recognition**: Calibrate finger counting thresholds
3. **Lag in response**: Reduce camera resolution or improve processing power
4. **Commands not executing**: Ensure presentation software is in focus

## Future Enhancements
- [ ] Add more gesture commands (pointer mode, annotation)
- [ ] Implement machine learning for improved gesture recognition
- [ ] Add gesture customization interface
- [ ] Support for multiple hand tracking
- [ ] Mobile app integration
- [ ] Gesture recording and playback
- [ ] Voice command integration

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License
This project is open source and available under the MIT License.

## Acknowledgments
- MediaPipe team for the excellent hand tracking solution
- OpenCV community for computer vision tools
- All contributors and users of this project

## Contact
- GitHub: [@Raghavendracharykurella](https://github.com/Raghavendracharykurella)
- Project Link: [https://github.com/Raghavendracharykurella/major-project](https://github.com/Raghavendracharykurella/major-project)

## Demo
For a live demonstration and more information, visit our [GitHub Pages](https://raghavendracharykurella.github.io/major-project/)

---

**Note**: This system is designed for educational and demonstration purposes. For production use, additional testing and optimization may be required.
