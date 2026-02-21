# Pre-trained Image Classifier for Dogs

## Overview
This project is a Python-based image classifier that detects dogs, non-dog animals, and objects, and identifies dog breeds using pre-trained CNN models: **ResNet**, **AlexNet**, and **VGG**. The project allows testing on both default images (`pet_images/`) and custom uploaded images (`uploaded_images/`).

Open-source under the **Udacity License**.

---

## Objectives
1. Correctly distinguish dog images from non-dog images.
2. Accurately classify the breed of dogs in dog images.
3. Compare performance of three CNN models: **ResNet**, **AlexNet**, and **VGG**, and identify which model performs best for the uploaded images.

---

## Model Comparison on Uploaded Images

| Model   | Total Images | Dog Images | Not-a-Dog Images | Correct Dogs (%) | Correct Not-Dogs (%) | Correct Breed (%) | Notes on Misclassifications |
|---------|-------------|------------|-----------------|-----------------|---------------------|-----------------|----------------------------|
| ResNet  | 4           | 2          | 2               | 100             | 100                 | 0               | Misclassified breeds for Dog_01 and Dog_02 |
| VGG     | 4           | 2          | 2               | 100             | 100                 | 0               | Misclassified breeds for Dog_01 and Dog_02 |
| AlexNet | 4           | 2          | 2               | 50              | 100                 | 0               | Misclassified Dog_02 as non-dog, Dog_01 breed wrong |

**Observation:**  
Based on uploaded images, **VGG** performed the best overall for classifying dogs and non-dogs, even though breed classification was still imperfect. AlexNet misclassified one dog image as a non-dog, making it less reliable.

---

## Technologies
- Python 3  
- PyTorch & torchvision  
- ImageNet pre-trained models (ResNet, AlexNet, VGG)

---

## Setup
1. Install Python 3 and required libraries (`torch`, `torchvision`, `PIL`).  
2. Clone/download the workspace.  
3. Ensure the folders `pet_images/` and `uploaded_images/` exist.

Upload your images to uploaded_images/ and run:

sh run_models_batch_uploaded.sh

Results are saved as .txt files for each CNN model.

---

## Usage

### Default Pet Images
To classify the default pet images in `pet_images/`, run:

```bash
sh run_models_batch.sh
Uploaded Images

To classify your own uploaded images in uploaded_images/, follow these guidelines:

Images must be JPEG (.jpg) and RGB (3 channels).

Images should be roughly square.

Naming convention:

Dog images: Dog_01.jpg, Dog_02.jpg

Other animals: Animal_Name_01.jpg

Objects: Object_Name_01.jpg

Run the classification script for uploaded images:

sh run_models_batch_uploaded.sh

Results will be saved as .txt files for each CNN model.






