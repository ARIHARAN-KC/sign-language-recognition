
# Sign Language to Text and Speech Conversion

This project converts sign language gestures into text and speech in real-time using computer vision and machine learning. It captures hand gestures via a webcam, processes them using a pre-trained CNN model, and displays the predicted characters and sentences on a GUI. The system also provides word suggestions and text-to-speech functionality.

---

## 📸 Demo Screenshot

![Sign Language to Text and Speech Conversion](https://github.com/user-attachments/assets/9efe854a-114b-4437-a381-4645c75e321e)

---

## 🚀 Features

* **Real-Time Sign Language Detection:** Captures hand gestures using a webcam and displays a green hand skeleton for visualization.
* **Text Conversion:** Converts detected gestures into text, displaying individual characters and forming sentences.
* **Speech Output:** Converts the generated text into speech using text-to-speech functionality.
* **Word Suggestions:** Provides up to four word suggestions for the last detected word using an English dictionary.
* **Reference Image:** Displays a sign language reference image alongside the hand skeleton for user guidance.
* **Interactive GUI:** Built with Tkinter, featuring webcam feed, hand skeleton, predicted text, suggestions, and control buttons (Speak, Clear).

---

## 🖥️ Requirements

### Hardware

* A webcam for capturing hand gestures.
* A CUDA-enabled GPU (optional, recommended for faster inference).

### Software

* Python 3.8 or higher

### Python Libraries

* `opencv-python`
* `numpy`
* `keras`
* `cvzone`
* `pyttsx3`
* `pyenchant`
* `pillow`
* `tkinter` (included with Python by default)

### Files

Ensure the following files are present in the project directory:

* `final_pred.py` (Main script)
* `cnn8grps_rad1_model.h5` (Pre-trained model)
* `white.jpg` (Background image)
* `sign-language.png` (Reference image)

---

## ⚙️ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/ARIHARAN-KC/sign-language-recognition.git
cd Sign-Language-To-Text-and-Speech-Conversion-master/Sign-Language-To-Text-and-Speech-Conversion-master
```

### 2️⃣ (Optional but recommended) Create Virtual Environment

```bash
python -m venv env
# Activate on Windows
.\env\Scripts\activate
# Activate on Linux/Mac
source env/bin/activate
```

### 3️⃣ Install Dependencies

```bash
pip install opencv-python numpy keras cvzone pyttsx3 pyenchant pillow
```

> **Note:**
>
> * `tkinter` comes pre-installed with Python.
> * If `pyenchant` installation fails on Windows, download a compatible wheel from [Unofficial Windows Binaries for Python](https://www.lfd.uci.edu/~gohlke/pythonlibs/) and install it using:
>
> ```bash
> pip install path/to/pyenchant‑xxx.whl
> ```

---

## 🎯 Usage

To run the application:

```bash
python final_pred.py
```

You will see:

* Live webcam feed (left side).
* Hand skeleton (center-right).
* Sign language reference image.
* Character prediction & sentence formation.
* Word suggestions.
* Speak and Clear buttons.

### 🖐 Interacting with the Application:

* Show your hand gestures in front of the webcam.
* The model will detect and convert gestures into text.
* Use suggestion buttons to correct words.
* Click **Speak** to hear the text.
* Click **Clear** to reset.

---

## 🗂 Project Structure

```bash
.
├── final_pred.py
├── cnn8grps_rad1_model.h5
├── white.jpg
├── sign-language.png
└── README.md
```

---

## 🔧 How It Works

* **Hand Detection:** Uses `cvzone` for detecting hand landmarks.
* **Skeleton Drawing:** Creates a green hand skeleton for model input.
* **Prediction:** Feeds processed image into a pre-trained CNN model (`cnn8grps_rad1_model.h5`).
* **Text Formation:** Builds sentences from continuous character predictions.
* **Suggestions:** Uses `pyenchant` for spelling corrections.
* **Speech Output:** Converts text to speech using `pyttsx3`.

---

## 💡 Troubleshooting

* **Webcam Issues:** Check if your camera index is correct in `cv2.VideoCapture(0)`.
* **Missing Files:** Ensure all required model and image files are present.
* **Library Errors:** Verify all dependencies are installed in the virtual environment.
* **GUI Display Issues:** Default resolution is `1600x900`. Modify as needed based on your screen.

---

## 📈 Future Improvements

* Add support for numbers and special characters.
* Improve accuracy with larger dataset.
* Dynamic reference image updates.
* Multi-language speech output support.

---

## 🤝 Contributors

* [ARIHARAN-KC](https://github.com/ARIHARAN-KC) *(Original Author)*

---

## 🙏 Acknowledgements

* [`cvzone`](https://github.com/cvzone/cvzone) - Hand Tracking
* [`pyttsx3`](https://pypi.org/project/pyttsx3/) - Text-to-Speech
* [`pyenchant`](https://pypi.org/project/pyenchant/) - Word Suggestions

---

⭐ **If you like this project, please consider giving it a star on GitHub. It really helps!** ⭐

---

---
