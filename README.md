# Super Resolution using ESRGAN

This project implements super-resolution using the Enhanced Super-Resolution Generative Adversarial Network (ESRGAN) model. It can upscale low-resolution images to high-resolution equivalents using deep learning techniques.

## Table of Contents
- [Introduction](#introduction)
- [How It Works](#how-it-works)
- [Setup](#setup)
- [Usage](#usage)
- [Results](#results)

## Introduction

ESRGAN (Enhanced Super-Resolution Generative Adversarial Network) is a powerful model for increasing the resolution of images. This project uses a pre-trained ESRGAN model to upscale images by a factor of 4 approximately.

## How It Works

ESRGAN is built on the GAN (Generative Adversarial Network) architecture:

1. **Generator**: Creates high-resolution images from low-resolution inputs.
2. **Discriminator**: Tries to distinguish between real high-resolution images and those generated by the Generator.

During training, the Generator is rewarded for producing images that fool the Discriminator, while the Discriminator is rewarded for correctly identifying fake images.

## Setup

1. Clone this repository:
   ```
   git clone https://github.com/your-username/Super_Resolution_using_ESRGAN.git
   cd Super_Resolution_using_ESRGAN
   ```

2. Create and activate a virtual environment:
   ```
   python -m venv env
   .\env\Scripts\activate  # On Windows
   source env/bin/activate  # On Unix or MacOS
   ```

3. Install the required libraries:
   ```
   pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu124
   pip install opencv-python glob2
   ```

4. Download the pre-trained model:
   - Get the model from [this Google Drive link](https://drive.google.com/drive/u/0/folders/17VYV_SoZZesU6mbxz2dMAIccSSlqLecY)
   - Place the downloaded model in the `models/` directory

## Usage

1. Place your low-resolution images in the `LR/` directory [this Kaggle link](https://www.kaggle.com/datasets/adityachandrasekhar/image-super-resolution). [Present as LR_1, LR_2, LR_3]

2. Run the super-resolution process:
   ```
   python test.py
   ```

3. Find the upscaled images in the `results/` directory. [this Google Drive link](https://drive.google.com/file/d/1YZqgis-6zGV-2Tz_1M0uADBw8m7HiHLi/view?usp=drive_link)
4. The images in the `results/` directory can be compared with the images in the `high_res` directory and the comparison can be done. [Present as high_res_1, high_res_2, high_res_3, high_res_4]

## Results

The ESRGAN model increases the image size by a factor of 4. For example, if your input image is 100x100 pixels, the output will be approximately 400x400 pixels.

---

Note: All the credit for the project structure and code goes to the [ESRGAN repository](https://github.com/xinntao/ESRGAN). I just used this open source project to run it on a dataset and check for the recent developments in enhanching resolution of images.
