# Real-time Video Edge Detection

## Student Information
* **Name:** Lê Hoàng Bách Đạt
* **Student ID:** 22127061
* **University:** VNUHCM - University of Science

## Live Demo
👉 **[Click here to view the project on Web](https://mahesvara7061.github.io/canvas_api_video_edge_detection_demo/)**

## Project Description
This project demonstrates real-time edge detection on a video stream. It plays a video and simultaneously processes each frame to detect and highlight the edges of objects in real-time, displaying the result on an adjacent canvas.

## Technologies Used
* **HTML5:** Used for the semantic structure of the web page, specifically utilizing the `<video>` element to play the source media.
* **Canvas 2D API:** Used for rendering the video frames and performing pixel-level manipulation on the CPU. The `getImageData()` and `putImageData()` methods are utilized to read, process, and write pixel arrays in real-time.

## The Sobel Algorithm
To detect edges, this project implements the **Sobel operator**. The step-by-step process involves:
1. **Grayscale Conversion:** Each frame is first converted from RGB to grayscale to simplify intensity calculations.
2. **Convolution:** A 3x3 matrix (kernel) slides over every pixel of the frame. It calculates the gradient of image intensity in both the horizontal (X) and vertical (Y) directions.
3. **Magnitude Calculation:** The horizontal and vertical gradients are combined using the Pythagorean theorem ($G = \sqrt{G_x^2 + G_y^2}$) to determine the overall edge strength at that specific pixel.
4. **Thresholding:** Pixels with a magnitude above a certain threshold (e.g., 60) are highlighted, while others are suppressed. This filters out noise and results in a clear edge map.

## How to Run Locally
If you prefer to run the project locally instead of using the web version:
1. Clone this repository to your local machine.
2. Ensure you have the source video file (e.g., `seal.mp4`) in the same directory as the `index.html` file to avoid CORS (Cross-Origin Resource Sharing) security issues from the browser.
3. Open `index.html` in any modern web browser.
4. Click play on the original video to see the edge detection process in action on the canvas.