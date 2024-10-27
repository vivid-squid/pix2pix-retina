# Synthetic Retinal Image Generation with Pix2Pix GAN

This project leverages a Pix2Pix Generative Adversarial Network (GAN) to generate synthetic high-resolution retinal images, addressing the shortage of such images for medical research and diagnostics. By transforming vessel structure masks into realistic retina images, this approach creates data that can be used to enhance training datasets, improve diagnostic tools, and facilitate medical research in ophthalmology.

## Project Overview

The scarcity of high-resolution retinal images presents challenges in fields like medical diagnostics, AI model training, and ophthalmological research. This project utilizes the Pix2Pix GAN framework, implementing a U-Net generator and PatchGAN discriminator to capture the fine-grained details required for realistic retinal images.

## Key Components

- **Dataset**: The model was trained using the Kaggle Retina Blood Vessel Segmentation dataset, with preprocessing steps to resize, normalize, and augment the images.
- **GAN Architecture**:
  - **Generator**: A U-Net structured generator captures the intricate structures in retinal images, facilitating realistic synthesis.
  - **Discriminator**: A PatchGAN discriminator assesses the realism of local image patches, improving the generation of high-fidelity images.
- **Evaluation Metrics**:
  - Mean Squared Error (MSE)
  - Structural Similarity Index (SSIM)
  - Peak Signal-to-Noise Ratio (PSNR)

## Results

The `final_result` folder contains the output for 70 generated images, each compared to the original images. For example, in the provided image, the "Source" column represents the input vessel structure mask, the "Generated" column displays the synthetic retina image, and the "Expected" column shows the real retina image used for comparison.

- **Performance Metrics**:
  - **MSE**: 0.0378
  - **SSIM**: 0.7295
  - **PSNR**: 21.13

These metrics demonstrate the model’s effectiveness in generating retinal images that closely resemble the original structure and quality of real images.

## Folder Structure

- `final_result/`: Contains generated images and comparison with original images (total of 70 images).
- `test_result_0.png`: Sample comparison showing "Source", "Generated", and "Expected" images side-by-side.

## Usage

To use the Pix2Pix GAN for generating synthetic retinal images, follow these steps:

1. **Install Dependencies**: Install the necessary Python libraries using:
   ```bash
   pip install numpy pandas matplotlib tensorflow tqdm

2. **Run Model**: Use the provided scripts to train the Pix2Pix model on your dataset. Adjust hyperparameters as needed for improved results.

3. **Visualize Results**: Generated images can be found in the final_result folder, with each image accompanied by its source and expected counterparts for comparison.