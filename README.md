# Image Upsampling for Pixelated Images

This repository contains Python code to detect and upsample pixelated regions in images using OpenCV . It includes functions to evaluate the quality of upsampled images using PSNR and SSIM metrics.

## Features

- **Pixelated Region Detection**: Identifies pixelated regions in images.
- **Image Upsampling**: Uses bicubic interpolation to upscale pixelated regions.
- **Quality Evaluation**: Measures image quality using PSNR and SSIM metrics.

## Requirements

Ensure you have the following dependencies installed:
- Python 3.x
- OpenCV (`cv2`)
- NumPy
- Matplotlib
- scikit-image (`skimage`)

You can install Python dependencies using pip:
```bash
pip install  opencv-python numpy matplotlib scikit-image
```

## Usage

### 1. Clone the Repository

Clone this repository to your local machine:
```bash
git clone https://github.com/your_username/image-upsampling.git
cd image-upsampling
```

### 2. Run the Code

Modify and run the `evaluate_image` function in `upsample.py` with your image path and desired parameters:
```python
import cv2
from upsample import evaluate_image

# Load your image
image_path = "path/to/your/image.png"
image = cv2.imread(image_path)

# Check if image loaded successfully
if image is None:
    raise ValueError("Error loading image. Please check the file path and format.")

# Experiment with different parameters
upsample_factor = 16  # Experiment with values like 2, 4, 8, 16
block_size = 2        # Experiment with values like 2, 4, 8, 16
threshold = 0.6       # Experiment with values like 0.2, 0.4, 0.6, 0.8

# Evaluate the image
evaluate_image(image, upsample_factor, block_size, threshold)
```

### 3. Interpret Results

- The script will display:
  - The original pixelated image.
  - The upsampled image with the specified upsample factor.
  - The PSNR (Peak Signal-to-Noise Ratio) value, indicating image quality.
  - Optionally, the SSIM (Structural Similarity Index), a measure of image similarity.

### 4. Experiment and Customize

Feel free to experiment with different values for `upsample_factor`, `block_size`, and `threshold` to see how they affect the upsampled image quality.



- This project utilizes OpenCV  for image processing.
- PSNR and SSIM metrics are calculated using scikit-image.

