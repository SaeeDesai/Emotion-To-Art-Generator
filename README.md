# Emotion-To-Art-Generator

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
git clone git@github.com:SaeeDesai/Emotion-To-Art-Generator.git
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

## Important Note

We were unable to upload the required files directly to GitHub due to size limitations. Therefore, we have shared the necessary folders via Google Drive.

**Please access the following links using your UMD account.**

---

### `archive(7)`

🔗 [https://drive.google.com/drive/folders/1s5yN9mEyubx7QHvPsMD7jYFUgIMJUak5?usp=sharing](https://drive.google.com/drive/folders/1s5yN9mEyubx7QHvPsMD7jYFUgIMJUak5?usp=sharing)

This folder contains the **raw GoEmotions dataset** as originally released, split across multiple CSV files. It serves as the foundational data source for training the multi-label emotion classification model.

### `official_data`

🔗 [[https://drive.google.com/drive/folders/1HBaqGL4yG9gmletsZG8X67l7rLscfCIY?usp=sharing](https://drive.google.com/drive/folders/1HBaqGL4yG9gmletsZG8X67l7rLscfCIY?usp=sharing)

This folder stores **cleaned and standardized datasets**, particularly the processed ArtEmis captions and labels. It functions as the **alignment layer** that enables consistent mapping between textual emotions and artistic emotion categories.

### `out_goemo_1`

🔗 [https://drive.google.com/drive/folders/1xhXEx0jfQfWEyUj7QxNdSs_L9jcqOPNv?usp=sharing](https://drive.google.com/drive/folders/1xhXEx0jfQfWEyUj7QxNdSs_L9jcqOPNv?usp=sharing)

This directory contains the **trained GoEmotions text classifier** along with its tokenizer and label metadata. It represents the core **emotion understanding module** that converts text into a 27-dimensional emotion probability representation.

### `emotion_sd_lora`

🔗 [https://drive.google.com/drive/folders/180vx9SoPs6mnNXf5niqaW59e624lqhdx?usp=sharing](https://drive.google.com/drive/folders/180vx9SoPs6mnNXf5niqaW59e624lqhdx?usp=sharing)

This folder includes the **LoRA-adapted Stable Diffusion components and generated artworks**. It corresponds to the final **emotion-to-art generation stage**, where detected emotions are translated into visually expressive images.

### `Reproducing the Results (Using Pretrained Models)`

To reproduce the project results **without retraining the models**, run the code blocks mentioned in the `code_sequence.ipynb` notebook in our main `project.ipynb` file.  
This notebook uses the **pretrained classifiers, mapping matrices, and LoRA parameters** provided, allowing you to directly generate emotion-driven artwork.

## Live Gradio Demo

To directly interact with the model and visualize the results through a user interface, use the Gradio link below:

**Gradio App:** https://015d5fcdb1edac31b1.gradio.live  
**Note:** This link is active until **December 19**.
