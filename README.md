# Color Image Clustering using Self-Organizing Maps (SOM)

This project demonstrates the use of Self-Organizing Maps (SOM) for color image clustering and visualization. The implementation uses the MiniSom library to create a visual representation of how colors in an image are organized and related to each other in the color space.

## Overview

Self-Organizing Maps are a type of artificial neural network that create a low-dimensional (typically two-dimensional) representation of high-dimensional data. In this project, we use SOM to:
- Process RGB color images
- Create a organized map of colors present in the image
- Visualize how different colors relate to each other in the color space

## Requirements

- Python 3.x
- Required libraries:
  - numpy
  - matplotlib
  - minisom
  - PIL (Python Imaging Library)

Install dependencies using:
```bash
pip install numpy matplotlib minisom pillow
```

## Project Structure

```
├── README.md
├── color_image_clustring.ipynb   # Main Jupyter notebook with the implementation
├── 1.png                         # Sample input image
├── 2.png                         # Additional sample image
└── 3.png                         # Additional sample image
```

## How It Works

1. **Image Loading and Preprocessing**:
   - Loads an RGB image using PIL
   - Converts the image to a normalized numpy array
   - Reshapes the data to prepare it for SOM training

2. **SOM Configuration**:
   - Creates a 30x30 grid for the Self-Organizing Map
   - Uses 3 input features (R,G,B values)
   - Implements Gaussian neighborhood function
   - Uses optimized learning parameters

3. **Training**:
   - Initializes the SOM with random weights
   - Trains the network using 10,000 iterations
   - Organizes colors based on their relationships in the RGB color space

4. **Visualization**:
   - Displays the original image
   - Shows the corresponding SOM visualization
   - Demonstrates how colors are organized and related

## Usage

1. Open the Jupyter notebook `color_image_clustring.ipynb`
2. Replace '1.png' with your own image file if desired
3. Run all cells in sequence
4. The output will show your input image alongside its SOM color map

## Parameters

The SOM can be tuned using several parameters:
- `som_size`: Size of the grid (default: 30x30)
- `sigma`: Width of the neighborhood function (default: 2.0)
- `learning_rate`: Rate of convergence (default: 0.1)
- `num_iteration`: Number of training iterations (default: 10000)

## Results

The visualization provides:
- Left: Original input image
- Right: Self-organized color map showing the relationships between colors in the image

## Author

[Osama Seyam]

## Acknowledgments

- MiniSom library: https://github.com/JustGlowing/minisom
- Inspired by color clustering techniques in image processing
