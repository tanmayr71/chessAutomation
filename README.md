# Automated Chess Board Recognition and Interaction Using a Top-View Setup

## Project Overview

This project aims to develop a system that identifies and classifies chess pieces from a top-down view of the chessboard. The approach simplifies visual complexity, making it well-suited for image processing techniques.

<img width="458" alt="image" src="https://github.com/tanmayr71/chessAutomation/assets/55703966/05435eb7-5727-4208-8263-de18f047e809">

## Demo

Watch the demo video on [YouTube](https://youtu.be/cFyKQfR4T-Q).

<img width="1072" alt="image" src="https://github.com/tanmayr71/chessAutomation/assets/55703966/efb3fdf7-9416-48da-b71b-9657da6440d1">



## Features

- **Cost-Effective**: Minimal hardware requirements, no need for expensive setups.
- **Efficiency**: Processes frames quickly, enabling near real-time tracking (~0.5 to 1 second).
- **Simplicity and Robustness**: Less prone to errors in varied lighting and different chessboard or piece appearances.
- **Scalability**: Easily adaptable to different environments without extensive reconfiguration.

  <img width="1470" alt="image" src="https://github.com/tanmayr71/chessAutomation/assets/55703966/166ca2b2-03ac-4032-bf09-7509a514efa5">


## Methodology

### Image Preprocessing

1. **Edge Detection**: Utilizes Sobel operators to compute gradients and detect edges.
2. **Saddle Point Detection**: Identifies potential chess square corners.
3. **Hough Transform**: Used for line detection as an alternative to saddle points.
4. **Contour Identification**: Uses Canny edge detection to outline sharp changes and simplifies contours with the Douglas-Peucker algorithm.
5. **Perspective Transformation**: Corrects perspective distortions to achieve a top-down view of the chessboard.

### Change Detection

1. **Image Subtraction**: Identifies areas of change between two aligned chessboard images.
2. **Thresholding and Cleaning**: Isolates significant movements and reduces noise using morphological operations.

### Move Detection

1. **Analyzing Detected Changes**: Converts detected image changes into specific chess moves.
2. **Chess Notation Conversion**: Translates grid indices into standard chess notation.

## Results

- **Processing Time**: Shows quick response times, enabling near real-time tracking.
- **Accuracy**: Efficiently detects and tracks chess piece movements in real-time.

## Contributions

- **Tanmay Rathi**: Implemented the algorithm logic, conducted experiments, and prepared the presentation.
- **Simardeep Singh Mehta**: Designed and implemented the UI and backend, integrated the algorithm with the web application, and contributed to documentation and presentation.
- **Avadhoot Kulkarni**: Assisted in algorithm implementation, wrote the report, and contributed to testing and integration.

## Future Work

- **Advanced Detection Algorithms**: Incorporating CNNs or template matching for improved accuracy.
- **Multi-Angle Support**: Enhancing the system's adaptability to various viewpoints.
- **User Interface Improvements**: Improving the UI for better user experience.

## Getting Started

1. **Clone the repository**: `git clone https://github.com/tanmayr71/chessAutomation.git`
2. **Navigate to the project directory**: `cd chessAutomation`
3. **Install dependencies**: `pip install -r requirements.txt`
4. **Run the application**: `python app.py`

## Contact

For any questions or feedback, please reach out to:

- Tanmay Rathi: tr2452@nyu.edu
- Simardeep Singh Mehta: sm11377@nyu.edu
- Avadhoot Kulkarni: ak10576@nyu.edu
