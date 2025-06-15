# Sign Language to Text and Speech Conversion

This project converts sign language gestures into text and speech in real-time using computer vision and machine learning. It captures hand gestures via a webcam, processes them using a pre-trained CNN model, and displays the predicted characters and sentences on a GUI. The system also provides word suggestions and text-to-speech functionality.

---

## 📸 Demo Screenshot

!Sign Language to Text and Speech Conversion![Screenshot (53)](https://github.com/user-attachments/assets/9efe854a-114b-4437-a381-4645c75e321e)

---

## 🚀 Features

- **Real-Time Sign Language Detection**: Captures hand gestures using a webcam and displays a green hand skeleton for visualization.
- **Text Conversion**: Converts detected gestures into text, displaying individual characters and forming sentences.
- **Speech Output**: Converts the generated text into speech using text-to-speech functionality.
- **Word Suggestions**: Provides up to four word suggestions for the last detected word using an English dictionary.
- **Reference Image**: Displays a sign language reference image alongside the hand skeleton for user guidance.
- **Interactive GUI**: Built with Tkinter, featuring webcam feed, hand skeleton, predicted text, suggestions, and control buttons (Speak, Clear).

---

## 🖥️ Requirements

### Hardware

- A webcam for capturing hand gestures.
- A CUDA-enabled GPU (optional, recommended for faster inference).

### Software

- Python 3.8 or higher

### Python Libraries

- `opencv-python`
- `numpy`
- `keras`
- `cvzone`
- `pyttsx3`
- `pyenchant`
- `pillow`
- `tkinter` (included with Python)

### Files

Ensure the following files are present in the project directory:

- `final_pred.py`
- `cnn8grps_rad1_model.h5` (pre-trained model)
- `white.jpg` (background image)
- `sign-language.png` (reference image)

---

## ⚙️ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/ARIHARAN-KC/sign-language-recognition.git
cd Sign-Language-To-Text-and-Speech-Conversion-master/Sign-Language-To-Text-and-Speech-Conversion-master

🤝 Contributors
ARIHARAN-KC (Original Author)

🙏 Acknowledgements
cvzone - Hand Tracking

pyttsx3 - Text-to-Speech

pyenchant - Word Suggestions

⭐ If you like this project, please consider giving it a star on GitHub. It really helps! ⭐
