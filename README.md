# Translation and Chat App Using AI

## Overview

This project is a **Gradio-based web application** that provides language translation and conversational capabilities. It uses **Hugging Face Transformers** for natural language processing and the **gTTS library** for converting text to speech. The app supports multiple languages for translation and provides an interactive chat mode.

## Features
- **Translation**:
  - Translate text to English, Chinese, or Japanese.
- **Chat**:
  - Engage in a conversation with an AI assistant.
- **Text-to-Speech**:
  - Generate audio output for the translated or generated text.

## Technologies Used
- **Hugging Face Transformers**: For loading the **Qwen/Qwen2-1.5B-Instruct** model.
- **Gradio**: For building the user interface.
- **gTTS**: For converting text to speech.
- **PyTorch**: For efficient computation with GPU support.

---

## Installation

1. **Clone the Repository**:
   ```bash
   git clone <repository_url>
   cd <project_directory>
   ```

2. **Install Dependencies**:
   ```bash
   pip install accelerate gTTS gradio transformers torch
   ```

3. **Download the Model**:
   Ensure you have access to Hugging Face's **Qwen/Qwen2-1.5B-Instruct** model. If you don't, create a Hugging Face account and set up an access token:
   ```bash
   huggingface-cli login
   ```

---

## Running the Application

1. **Run the Script**:
   ```bash
   python app.py
   ```

2. **Access the Gradio Interface**:
   - The app will provide a **public shareable link** (e.g., `https://xxxxx.gradio.live`).
   - Open the link in your browser to access the app.

---

## How It Works

1. **Input Text**:
   - Enter the text you want to translate or use for chatting.

2. **Select Action**:
   - Choose one of the following:
     - **Translate to English**
     - **Translate to Chinese**
     - **Translate to Japanese**
     - **Chat**

3. **View Output**:
   - The app generates the output text based on your selected action.
   - It also creates an audio file (`output_audio.mp3`) using gTTS, which can be played or downloaded.

---

## File Structure
- **`app.py`**: Main application script.
- **Dependencies**:
  - **Hugging Face Transformers**: Handles model loading and tokenization.
  - **gTTS**: Converts text to audio.
  - **Gradio**: Provides the user interface.

---

## Customization

### Add More Languages
- Update the `process_input` function to include more translation options:
  ```python
  elif action == "Translate to Spanish":
      prompt = f"Please translate the following text into Spanish：{input_text}"
      lang = "es"
  ```

### Change the Language Model
- Replace the `language_model_name` with a different pre-trained model:
  ```python
  language_model_name = "new_model_name"
  ```

### Modify Gradio Interface
- Update the `action_options` list to include additional actions.

---

## Limitations
- **Model Size**: The **Qwen/Qwen2-1.5B-Instruct** model may require significant memory, especially on GPUs.
- **Language Support**: Limited to English, Chinese, and Japanese (can be extended).
- **Audio Quality**: Depends on the capabilities of gTTS.

---

## Future Enhancements
- Add support for more languages and actions.
- Integrate with a more advanced text-to-speech engine for improved audio quality.
- Deploy the app on a platform like Hugging Face Spaces for persistent hosting.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

## Acknowledgments
- Hugging Face for the **Qwen/Qwen2-1.5B-Instruct** model.
- The **Gradio** and **gTTS** communities for their excellent tools and libraries.

---
