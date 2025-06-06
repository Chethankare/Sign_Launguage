# Sign Language Recognition System
This project is a comprehensive Sign Language Recognition system that converts American Sign Language (ASL) gestures into text and speech in real-time. The system uses computer vision and deep learning to detect hand gestures from a webcam feed and translates them into meaningful sentences.

Key Features:
Real-time ASL Recognition: Captures hand movements through webcam and interprets ASL gestures

Text Conversion: Translates gestures into readable text

Speech Output: Converts recognized text to spoken words

Spell Check: Integrates dictionary suggestions for word correction

Interactive GUI: User-friendly interface displaying live camera feed and recognition results

Technical Components:
Data Collection:

data_collection_binary.py: Captures binary thresholded hand images

data_collection_final.py: Collects grayscale images with skeletal overlays

Prediction Engine:

final_pred.py: Main application for real-time gesture recognition

System Requirements:
Python 3.7+

OpenCV 4.0+

Keras/TensorFlow

cvzone

Pyttsx3

Enchant (for spell checking)

Tkinter (for GUI)

Installation:
bash
pip install opencv-python cvzone keras tensorflow pyttsx3 pyenchant
Usage:
Run the main application:

bash
python final_pred.py
Use the GUI interface:

Position your hand in the camera view

The system will detect gestures and display recognized characters

Formed sentences appear in the "Sentence" section

Automatic speech conversion occurs after pauses

Key Controls in Application:
Natural hand movements translate to characters

Space gesture: Add space between words

'B' gesture: Clear current sentence

'Next' gesture: Confirm character input

Technical Approach:
Hand Detection: Uses MediaPipe hand tracking

Gesture Classification: CNN model trained on ASL alphabet

Context Handling: Special algorithms for:

Character disambiguation (e.g., differentiating 'D' vs '1')

Space detection

Backspace functionality

Word suggestion

Directory Structure:
