# 🎨 Emotion-To-Art-Generator

**Emotion-To-Art-Generator** is a multimodal deep learning project that converts **textual emotions into AI-generated artwork**.  
The system first detects the emotion expressed in a given text using a **fine-tuned Transformer-based emotion classifier**, and then generates an **art image aligned with that emotion** using a **fine-tuned Stable Diffusion v1.5 model**.

## What is This Project?

This project bridges **Natural Language Processing (NLP)** and **Generative Computer Vision** by mapping emotions inferred from text directly into visual art.

## Pipeline Overview

### Text Input
- User provides a sentence or paragraph.

### Emotion Classification
- A **fine-tuned Transformer model** predicts the emotion from the text.
- Trained using emotion-labeled datasets.
- Model performance evaluated using **F1-score**.

### Emotion-to-Art Generation
- The predicted emotion is transformed into a text prompt.
- A **fine-tuned Stable Diffusion v1.5 model** generates an artistic image corresponding to that emotion.

### Interactive Interface
- A **Gradio-based UI** allows users to input text and visualize generated art in real time.

## Models Used

### Emotion Classification Model
- Transformer-based architecture (Hugging Face `transformers`)
- Fine-tuned for emotion classification
- Outputs:
  - Emotion probabilities
  - Final predicted emotion label

### Image Generation Model
- **Stable Diffusion v1.5** (via `diffusers`)
- Fine-tuned to emphasize emotional tone in generated artwork
- Uses **CLIP text encoders** for prompt conditioning

---

## Installation

### Clone the Repository

```bash
git clone https://github.com/your-username/Emotion-To-Art-Generator.git
cd Emotion-To-Art-Generator
```

### Create a Virtual Environment (Recommended)
```bash
python -m venv venv
source venv/bin/activate     # macOS / Linux
venv\Scripts\activate        # Windows
```

### Install Dependencies
```bash
pip install -r requirements.txt
```
