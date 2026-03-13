Image Processing Lab – Case Studies (Python & OpenCV)
Overview

This lab demonstrates several image enhancement techniques using Python, OpenCV, NumPy, and Matplotlib in Google Colab.
The goal is to apply basic image intensity transformations to improve the visibility of important features in different types of images.

Each task simulates a real-world case study, such as surveillance enhancement, medical imaging improvement, and document processing.

Technologies Used

Python

OpenCV

NumPy

Matplotlib

Google Colab

Features / Image Processing Techniques
1. Image Negative Transformation

Purpose:
Enhance dark areas in images by inverting intensity values.

Formula:

s = 255 - r

Applications:

Night surveillance footage

Enhancing hidden details

Astronomical imaging

2. Contrast Stretching

Purpose:
Improve image contrast by expanding the range of intensity values.

Concept:

s = (r - r_min) / (r_max - r_min) * 255

Applications:

Medical X-ray images

Low contrast photographs

Satellite imagery

3. Log Transformation

Purpose:
Enhance darker regions while compressing bright areas.

Formula:

s = c * log(1 + r)

Applications:

Astronomical images

Images with large dynamic ranges

4. Power-Law (Gamma) Transformation

Purpose:
Adjust brightness and contrast using gamma correction.

Formula:

s = c * r^γ

Applications:

Display correction

Medical imaging

Photography enhancement

5. Thresholding

Purpose:
Convert grayscale images into binary images by separating foreground from background.

Example:

if pixel > threshold:
    pixel = 255
else:
    pixel = 0

Applications:

Document scanning

Object detection

Text extraction

Workflow

Upload an image using Google Colab.

Read the image using OpenCV.

Convert it to grayscale (if required).

Apply the required image processing technique.

Display results using Matplotlib.

Example Code Snippet
import cv2
import numpy as np
import matplotlib.pyplot as plt

img = cv2.imread("image.jpg", 0)

negative = 255 - img

plt.figure(figsize=(10,5))
plt.subplot(1,2,1)
plt.title("Original Image")
plt.imshow(img, cmap='gray')

plt.subplot(1,2,2)
plt.title("Negative Image")
plt.imshow(negative, cmap='gray')

plt.show()
Input

The program allows the user to upload images directly in Google Colab using:

from google.colab import files
uploaded = files.upload()
Output

The program displays:

Original Image

Processed Image

Enhanced visibility of important features

Learning Outcomes

After completing this lab, students will be able to:

Understand basic image enhancement techniques

Implement intensity transformations

Use OpenCV for image processing

Apply transformations to real-world scenarios

Author

Huzaifa Amir
