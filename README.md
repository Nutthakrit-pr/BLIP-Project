## BLIP: Bootstrapping Language-Image Pre-training 
additional Finetuning NLLB for ThaiCaptioning (EN/TH)

This project is a web application that generates descriptive captions for any uploaded image. It uses the **Salesforce BLIP** model for high-quality captioning and the **Facebook NLLB** model to provide instant, high-accuracy translations from English to Thai.
and this project is to defined the finetuned NLLB model by using LoRA adapter to improve performance of Thai's captioning.
## Live Demo & Screenshot

**You can try the app live here:** https://huggingface.co/spaces/Nutthakrit/BLIP-Project

<img width="809" height="378" alt="image" src="https://github.com/user-attachments/assets/ffee76a1-dc94-435f-b1a0-a0cb742dbff5" />



## Features

* **Image Upload:** Upload any JPG or PNG image.
* **Multi-Style Captions:** Generates three different types of captions:
    * **Main:** A balanced, high-quality caption.
    * **Short:** A concise, brief description.
    * **Detailed:** A longer, more descriptive caption.
* **Plausibility Score:** Displays a confidence score (e.g., `12.34%`) for each caption, showing how "sure" the AI is about its generation.
* **Bilingual (EN/TH):** Provides both the original English (🇬🇧) caption and a translated Thai (🇹🇭) and compare the captioning's for NLLP base model with finetuned model


##  Models Used

1.  **Image Captioning:** [Salesforce/blip-image-captioning-large](https://huggingface.co/Salesforce/blip-image-captioning-large)
2.  **Translation (EN-TH):** [facebook/nllb-200-distilled-600M](https://huggingface.co/facebook/nllb-200-distilled-600M)

## How to Download and Run This Project
[In Cleaned_data_for_BLIP.ipynb : In that file, I've already downloaded and cleaned data from kaggle. you can use the cleaned data in the Release section]
### 1. Download
1. Look for the **"Releases"** section on the right side of this page.
2. Click on the latest version (e.g., `v1.0`).
3. Scroll down to the **"Assets"** section at the bottom of that page.
4. Click on the file named **`[NLLB-Project.zip]`** to download it.

### 2. Install / Run
1. Find the downloaded file on your computer (usually in your `Downloads` folder).
2. **Right-click** the zip file and select **"Extract All..."** (Windows) or double-click it (Mac).
3. Open the new extracted folder.
4. Double-click the file named **`[finetune.py]`** to run it.
   
    ```bash

    python finetune.py

    ```
    it will take 2-6 hours depends on CPU
5. Zip file **Final_Adapter** which you will have it when you have already done the finetuning  
   
### 3. Test in Complete_BLIP_project.ipynb
1. Run all in ipynb file
2. Upload the **Final_Adapter.zip**
3. Upload some image
4. Put the Thai reference sentence to describe that image
5. It will Show the evaluation of this project
   
### ⚠️ Troubleshooting Security Warnings
Because this software is new, your computer might try to block it. Here is how to bypass those warnings safely:

**On Windows (SmartScreen):**
* If you see a blue window saying *"Windows protected your PC"*:
* Click **More info**.
* Click the **Run anyway** button.

**On Mac:**
* If you see a warning that the app *"cannot be opened"*:
* **Right-click** (or Control-click) the app icon.
* Select **Open** from the menu.
* Click **Open** again in the pop-up window.
