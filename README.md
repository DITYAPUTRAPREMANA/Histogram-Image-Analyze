# Histogram Image Analyzer

This program is a simple graphical user interface (GUI) tool built using Python that allows users to upload an image, analyze its histogram, and display various statistical data (mean, variance, and standard deviation) for the image's grayscale and color histograms. It provides an easy way to visualize the distribution of pixel intensity levels within an image.

## Features

* **Grayscale Histogram Analysis**: For grayscale images or the grayscale channel of color images, the program will calculate and display the histogram, along with statistics (mean, variance, and standard deviation).
* **Color Histogram Analysis**: For color images, the program will calculate and display the histograms of the Red, Green, and Blue (RGB) channels, as well as statistics (mean, variance, and standard deviation) for each channel.
* **Histogram Visualization**: The histograms are visualized as bar charts using `matplotlib`.
* **User-friendly GUI**: The program uses `Tkinter` for the GUI to allow users to easily upload an image file and perform analysis.

## Requirements

Before running the program, ensure you have the following libraries installed:

* **OpenCV**: `opencv-python` for image processing.
* **NumPy**: `numpy` for numerical operations.
* **Matplotlib**: `matplotlib` for visualizing the histograms.
* **Tkinter**: Tkinter for the GUI (typically pre-installed with Python).

You can install the required libraries using `pip`:

```bash
pip install opencv-python numpy matplotlib
```

## How to Use

1. **Run the program**: Execute the `Histogram Image Analyzer` Python script.
2. **Upload an Image**: Click the **"Upload dan Analisis Gambar"** button in the GUI to choose an image from your computer.
3. **View Results**: Once the image is uploaded, the program will analyze the histogram of the image and show statistical data (mean, variance, and standard deviation) for both grayscale and color histograms (if applicable).
4. **Histogram Visualization**: The histograms of the image will be displayed as bar charts.

## Example Output

* For a **grayscale image**, the output will display the histogram of the image in black and provide the mean, variance, and standard deviation.
* For a **color image**, the program will display three histograms (one for each RGB channel) and the associated statistical data for each channel.

## Code Explanation

### Key Functions:

1. **`calc_histogram()`**: This function computes the histogram of an image (or a specific channel). It can handle both grayscale and color images.

2. **`normalize_histogram()`**: This function normalizes the histogram by dividing each value by the total number of pixels in the image.

3. **`stats_histogram()`**: This function calculates statistical values such as the mean, variance, and standard deviation for a normalized histogram.

4. **`analyze_image_histogram()`**: This function is responsible for reading the image, determining whether it is grayscale or color, and calling the necessary functions to compute the histogram and display statistics and graphs.

5. **`open_and_analyze()`**: This function allows the user to upload an image via the Tkinter file dialog, then it passes the file path to the `analyze_image_histogram()` function for analysis.

### GUI Elements:

* A **label** provides instructions to the user.
* A **button** allows the user to upload an image and trigger the analysis.
* A **file dialog** enables the user to select an image file from their system.
