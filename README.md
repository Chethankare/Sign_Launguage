# Sign Language Recognition System

This project is a comprehensive **Sign Language Recognition System** that converts **American Sign Language (ASL)** gestures into **text** and **speech** in real-time. The system uses computer vision and deep learning to detect hand gestures from a webcam feed and translates them into meaningful sentences.

---

## Key Features

- **Real-time ASL Recognition**: Captures hand movements via webcam and interprets ASL gestures.  
- **Text Conversion**: Translates gestures into readable text.  
- **Speech Output**: Converts recognized text to spoken words using TTS.  
- **Spell Check**: Dictionary-based suggestions for correcting words.  
- **Interactive GUI**: User-friendly interface with live video and real-time results.

---

## Technical Components

### Data Collection

- `data_collection_binary.py`: Captures binary thresholded hand images.  
- `data_collection_final.py`: Collects grayscale images with skeletal overlays.

### Prediction Engine

- `final_pred.py`: Main application for real-time gesture prediction.

---

## System Requirements

- Python 3.7 or higher  
- OpenCV 4.0 or higher  
- TensorFlow or Keras  
- cvzone  
- pyttsx3  
- pyenchant  
- Tkinter

---

## Installation

Open your terminal or command prompt and run:

```bash
pip install opencv-python cvzone keras tensorflow pyttsx3 pyenchant
```

---

## Usage

### Run the Main Application

```bash
python final_pred.py
```

### Instructions

- Place your hand in the camera view.  
- The system detects and displays recognized gestures as characters.  
- Formed sentences appear in the Sentence section.  
- After a short pause, the system converts text to speech.

---

## Key Controls

- **Natural Gestures**: Automatically translate to characters.  
- **Space Gesture**: Adds a space between words.  
- **B Gesture**: Clears the current sentence.  
- **Next Gesture**: Confirms character input.

---

## Technical Approach

- **Hand Detection**: Uses MediaPipe hand tracking.  
- **Gesture Classification**: CNN model trained on ASL alphabet.  
- **Context Handling**:  
  - Character disambiguation (for example, distinguishing between D and 1)  
  - Space detection  
  - Backspace support  
  - Word suggestion using spell checker

---

## Directory Structure

```
Sign_Language/
├── AtoZ/                    Dataset folder containing labeled images for ASL alphabets A to Z
├── data_collection_binary.py
├── data_collection_final.py
├── final_pred.py
├── model.h5                Pretrained CNN model for gesture recognition
├── white.jpg               Background image used in GUI display
```

---

## Future Improvements

- Support for phrase-level recognition  
- Expanded vocabulary beyond alphabet  
- Multi-hand gesture recognition  
- Mobile application version

---

## About

This project was developed as part of academic research in computer vision and human-computer interaction. Contributions and feedback are welcome.
