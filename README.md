## BLIP: Bootstrapping Language-Image Pre-training 
additional Finetuning NLLB for ThaiCaptioning (EN/TH)

This project is a web application that generates descriptive captions for any uploaded image. It uses the **Salesforce BLIP** model for high-quality captioning and the **Facebook NLLB** model to provide instant, high-accuracy translations from English to Thai.
and this project is to defined the finetuned NLLB model by using LoRA adapter to improve performance of Thai's captioning.
## Live Demo & Screenshot

**You can try the app live here:** https://huggingface.co/spaces/Nutthakrit/BLIP-Project

<img width="1588" height="552" alt="image" src="https://github.com/user-attachments/assets/f8d6780d-73e7-4220-b0cf-9d240c15d403" />


## Features

* **Image Upload:** Upload any JPG or PNG image.
* **Multi-Style Captions:** Generates three different types of captions:
    * **Main:** A balanced, high-quality caption.
    * **Short:** A concise, brief description.
    * **Detailed:** A longer, more descriptive caption.
* **Plausibility Score:** Displays a confidence score (e.g., `12.34%`) for each caption, showing how "sure" the AI is about its generation.
* **Bilingual (EN/TH):** Provides both the original English (🇬🇧) caption and a translated Thai (🇹🇭) and compare the captioning's for NLLP base model with finetuned model

## Tech Stack

* **Backend:** [Python](https://www.python.org/)
* **Web Framework:** [Flask](https://flask.palletsprojects.com/)
* **AI Models:** [Hugging Face Transformers](https://huggingface.co/docs/transformers/index)
* **Deep Learning:** [PyTorch](https://pytorch.org/)
* **Frontend:** HTML, CSS, JavaScript
* **Deployment:** [Hugging Face Spaces](https://huggingface.co/spaces)

##  Models Used

1.  **Image Captioning:** [Salesforce/blip-image-captioning-large](https://huggingface.co/Salesforce/blip-image-captioning-large)
2.  **Translation (EN-TH):** [facebook/nllb-200-distilled-600M](https://huggingface.co/facebook/nllb-200-distilled-600M)

##  How to Run Locally

If you want to run this project on your own computer:

1.  **Clone this repository:**
    ```bash
    git clone [MY-REPO]
    cd [YOUR-PROJECT-FOLDER]
    ```

2.  **Create a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate
    # On Windows: venv\Scripts\activate
    ```

3.  **Install all dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the Flask app:**
    ```bash
    python app.py
    ```
    *(Wait for the models to download for the first time)*

5.  **Open the app in your browser:**
    Go to `http://127.0.0.1:5000`
