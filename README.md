Sign Language to Text and Speech Conversion
This project converts sign language gestures into text and speech in real-time using computer vision and machine learning. It captures hand gestures via a webcam, processes them using a pre-trained CNN model, and displays the predicted characters and sentences on a GUI. The system also provides word suggestions and text-to-speech functionality.
Features

Real-Time Sign Language Detection: Captures hand gestures using a webcam and displays a green hand skeleton for visualization.
Text Conversion: Converts detected gestures into text, displaying individual characters and forming sentences.
Speech Output: Converts the generated text into speech using text-to-speech functionality.
Word Suggestions: Provides up to four word suggestions for the last detected word using an English dictionary.
Reference Image: Displays a sign language reference image alongside the hand skeleton for user guidance.
Interactive GUI: Built with Tkinter, featuring webcam feed, hand skeleton, predicted text, suggestions, and control buttons (Speak, Clear).

Requirements

Hardware:
A webcam for capturing hand gestures.
A CUDA-enabled GPU (recommended for faster model inference).


Software:
Python 3.8 or higher
Libraries: opencv-python, numpy, keras, cvzone, pyttsx3, pyenchant, pillow, tkinter
Pre-trained model: cnn8grps_rad1_model.h5 (included in the repository)
White background image: white.jpg (included in the repository)
Reference image: sign-language.png (included in the repository)



Installation

Clone the Repository:
git clone https://github.com/<your-username>/Sign-Language-To-Text-and-Speech-Conversion.git
cd Sign-Language-To-Text-and-Speech-Conversion-master/Sign-Language-To-Text-and-Speech-Conversion-master


Set Up a Virtual Environment (optional but recommended):
python -m venv env
.\env\Scripts\activate  # On Windows
# source env/bin/activate  # On Linux/Mac


Install Dependencies:
pip install opencv-python numpy keras cvzone pyttsx3 pyenchant pillow


Note: tkinter is included with Python by default.
If pyenchant installation fails on Windows, download a pre-built wheel from Unofficial Windows Binaries for Python and install it with:pip install <path-to-downloaded-wheel>




Verify Required Files:Ensure the following files are present in the project directory:

final_pred.py
cnn8grps_rad1_model.h5
white.jpg
sign-language.png



Usage

Run the Application:
python final_pred.py

This will launch a Tkinter window with the following components:

Webcam feed (left side)
Green hand skeleton (center-right)
Sign language reference image (right of the hand skeleton)
Current character and sentence display (bottom left)
Word suggestion buttons (bottom center)
Speak and Clear buttons (bottom right)


Interact with the Application:

Show your hand gestures in front of the webcam to detect sign language characters.
The detected character will appear under "Character", and the sentence will form under "Sentence".
Use the suggestion buttons to correct the last word in the sentence.
Click "Speak" to hear the sentence aloud.
Click "Clear" to reset the sentence and suggestions.


Close the Application:

Click the window's close button to exit. The webcam and all windows will be released properly.



Project Structure

final_pred.py: Main script containing the application logic, GUI, and prediction pipeline.
cnn8grps_rad1_model.h5: Pre-trained CNN model for gesture recognition.
white.jpg: Background image used for drawing the hand skeleton.
sign-language.png: Reference image showing sign language gestures.
README.md: Project documentation (this file).

How It Works

Hand Detection: Uses the cvzone library to detect hands in the webcam feed.
Skeleton Drawing: Draws a green hand skeleton on a white background for visualization.
Gesture Prediction: Feeds the skeleton image into a pre-trained CNN model (cnn8grps_rad1_model.h5) to predict the corresponding sign language character (A-Z, space, backspace, next).
Text Formation: Builds a sentence from predicted characters, handling spaces and backspaces.
Word Suggestions: Uses pyenchant to suggest corrections for the last word in the sentence.
Speech Output: Converts the sentence to speech using pyttsx3.

Troubleshooting

Webcam Not Working:
Ensure your webcam is connected and accessible.
Check if cv2.VideoCapture(0) is using the correct camera index (try 1 or 2 if 0 fails).


Model Prediction Errors:
Verify that cnn8grps_rad1_model.h5 is in the project directory.
Ensure your system supports CUDA if using GPU acceleration.


Reference Image Not Loading:
Confirm that sign-language.png exists in the project directory.
Check the file path in final_pred.py matches your system.


GUI Elements Misaligned:
The window size is set to 1600x900. Adjust your screen resolution or modify the window size in final_pred.py if needed.



Future Improvements

Add support for more sign language gestures (e.g., numbers, special characters).
Improve model accuracy with a larger dataset and retraining.
Implement dynamic reference image updates to show only the current predicted letter.
Add support for multiple languages in text and speech output.

Contributing
Contributions are welcome! Please fork the repository, make your changes, and submit a pull request. For major changes, open an issue first to discuss your ideas.
License
This project is licensed under the MIT License. See the LICENSE file for details.
Acknowledgments

Built using cvzone for hand tracking.
Uses pyttsx3 for text-to-speech.
Word suggestions powered by pyenchant.

