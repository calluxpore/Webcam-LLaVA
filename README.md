# Webcam-LLaVA

This project captures images from your webcam at regular intervals, sends them to the LLaVA model running on Ollama, and receives textual descriptions of the images. The results are written to a text file for easy reference. This tool leverages **OpenCV** for webcam handling and **requests** for interacting with the locally running LLaVA model.

## Features:
- Captures images from your webcam.
- Sends images to the LLaVA multimodal model.
- Receives text descriptions of what the LLaVA model detects in the image.
- Logs descriptions in a text file (`llava_output.txt`).

---

## Installation

### 1. Clone the repository:

```bash
git clone https://github.com/yourusername/webcam-llava.git
cd webcam-llava
```

### 2. Install Python dependencies:
```bash
pip install opencv-python
pip install requests
```

### 3. Set Up Ollama and LLaVA Model:
Ensure that the **Ollama** server is running and the **LLaVA** model is installed.

```bash
ollama serve
ollama pull llava
```

---

## Running the Script

To start the script, run the following command in your terminal:

```bash
python webcam_llava.py
```

The script will:
1. Capture an image from the webcam every 20 seconds.
2. Send the captured image to the LLaVA model for analysis.
3. Log the description of what the model detects in `llava_output.txt`.

---

## Requirements

- Python 3.x
- **Python Libraries**:
  - `opencv-python`
  - `requests`
  
Install them with:

```bash
pip install opencv-python requests
```

---

## Usage Instructions

1. **Start Ollama**: Make sure Ollama is running locally with the LLaVA model.
   ```bash
   ollama serve
   ```

2. **Run the Python Script**:
   ```bash
   python webcam_llava.py
   ```

3. **Stop the Script**:
   Press **Ctrl + C** in the terminal to stop the script.

---

## Troubleshooting

- **Black Screen from Webcam**: Ensure you are using the correct backend for Windows (`cv2.CAP_DSHOW`) and check your camera settings.
- **Invalid JSON Response**: Ensure that Ollama is running the LLaVA model properly and that requests are not sent in parallel, as the model doesn't support simultaneous processing.

---

## Acknowledgements
- **OpenCV** for webcam handling.
- **Ollama** and **LLaVA** for multimodal AI processing.
