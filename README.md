
# Parallel Image Filtering with OpenCV

## Overview
This project demonstrates how to apply parallel computing to perform image filtering tasks (blur and sharpen) on multiple images simultaneously. By leveraging CPU multithreading and GPU acceleration, the project compares and reduces processing time for filtering operations. The implementation uses Python, OpenCV, and PyTorch for efficient computation.

---

## Features
- **CPU-Based Parallel Processing:** Uses `ThreadPoolExecutor` for multithreading to process images in parallel on the CPU.
- **GPU-Based Acceleration:** Utilizes PyTorch to accelerate filtering operations on the GPU (if available).
- **Image Filters:** 
  - Gaussian Blur  
  - Sharpening Filter
- **Performance Comparison:** Measures and compares processing times for CPU and GPU implementations.

---

Setup Instructions
Prerequisites
- Python 3.x installed
- Required libraries:
  - `opencv-python`
  - `opencv-contrib-python`
  - `opencv-python-headless`
  - `torch`
  - `numpy`
  - `matplotlib`

 Install Dependencies
Run the following commands to install the required libraries:
```bash
pip install opencv-python-headless
pip install opencv-python
pip install opencv-contrib-python
pip install torch
pip install matplotlib

## How to Use
1. Upload Images:
   - Place your images in a directory (e.g., `images/`).
   - Upload images using the provided `files.upload()` function in the code.

2. Run the Code:
   - For CPU-based parallel filtering:
     - The script processes images in parallel using the `ThreadPoolExecutor`.
   - For GPU-based filtering:
     - The script leverages PyTorch to process images on the GPU.

3. Output:
   - Filtered images are saved in the `output_cpu/` directory for the CPU implementation.
   - Filtered images from the GPU implementation are displayed using `matplotlib`.

4. Performance Comparison:
   - The script outputs the processing time for both CPU and GPU implementations.

---


## Directory Structure
```
project/
├── images/               # Input image directory
├── output_cpu/           # Output directory for CPU-filtered images
├── README.md             # Project documentation
├── parallel_filtering.py # Main script for CPU and GPU filtering
```

---

## Performance Insights
- Parallel processing on the CPU significantly reduces the time taken compared to sequential processing.
- GPU acceleration (if available) provides an even faster alternative, especially for large datasets or high-resolution images.

---

## References
- OpenCV Documentation: https://docs.opencv.org  
- PyTorch Documentation: https://pytorch.org/docs  

