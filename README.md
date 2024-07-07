# Panorama Generation

This project shows the process of generating a panoramic image from multiple overlapping photos using computer vision techniques. The project uses feature detection, matching, homography estimation, and image stitching to create a panorama.


## Project Structure
`1.jpg, 2.jpg, ..., 8.jpg`: Input images for creating the panorama.
`panaroma.ipynb`: The main script containing the code for generating the panorama.

## Prerequisites

Ensure the following libraries are installed:
`pip install opencv-python numpy matplotlib`

## Algorithm

### Feature Detection and Matching:

- Detect features in each image using the SIFT algorithm.
- Match features between successive images using Brute Force and FLANN based matchers.

### Homography Estimation and RANSAC:

- Compute the homography matrix to align overlapping images.
- Utilize RANSAC (Random Sample Consensus) to robustly estimate the homography matrix, reducing the influence of outliers.

### Image Warping and Stitching:

- Warp images using the homography matrix.
- Stitch images together to form a panorama.

### Cropping and Blending:

- Crop and blend the stitched image to remove black borders and create a smooth panorama.

## Output Image:

<img width="753" alt="image" src="https://github.com/sanya21561/panaroma/assets/108148388/70a6cfcd-4fb3-41b9-ad5d-600d0ac4fd88">
