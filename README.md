# Parking-Spot-Detector-using-Computer-Vision

## Project Overview

The "Parking Spot Detection and Counter" project aims to utilize computer vision techniques to automate the detection and counting of available parking spots in a parking lot. The system processes a video feed, identifies parking spots, determines their occupancy status, and provides a real-time count of available spots.

## Objectives

1. **Detect Parking Spots:**
   The project identifies individual parking spots in a parking lot using a predefined mask image.

2. **Determine Occupancy Status:**
   The system analyzes video frames to determine whether each detected parking spot is empty or occupied.

3. **Real-time Count:**
   It provides a real-time count of available parking spots and visually represents this information on the video feed.

## Methodology

### Data Preparation

- **Mask Image:**
  A mask image (`mask_1920_1080.png`) is used to define the regions corresponding to parking spots in the video feed.

- **Video Feed:**
  The video feed (`parking_1920_1080_loop.mp4`) provides continuous frames of a parking lot, simulating real-world conditions.

### Processing Pipeline

1. **Connected Components Analysis:**
   Using the mask image, the system identifies connected components, each representing a parking spot.

2. **Feature Extraction:**
   For each detected parking spot, the system extracts relevant features from the video frames to determine occupancy status.

3. **Occupancy Determination:**
   A pre-trained machine learning model (`model.p`) classifies each parking spot as either empty or occupied based on the extracted features.

4. **Visualization:**
   The system draws bounding boxes around each parking spot in the video feed, color-coded to indicate occupancy status (green for available, red for occupied). Additionally, a counter displays the number of available spots.

## Results

The project successfully identifies and counts available parking spots in real-time. The following results were observed:

1. **Detection Accuracy:**
   The system accurately detects and delineates parking spots using the predefined mask.

2. **Occupancy Classification:**
   The pre-trained model effectively classifies the occupancy status of parking spots, achieving high accuracy.

3. **Real-time Performance:**
   The system processes video frames in real-time, providing continuous updates on the availability of parking spots.

### Visual Output

- **Bounding Boxes:**
  Each parking spot is outlined with a bounding box. Green boxes indicate available spots, while red boxes indicate occupied spots.

- **Availability Counter:**
  A counter displayed on the video feed shows the current number of available parking spots.

## Conclusion

The "Parking Spot Detection and Counter" project demonstrates the feasibility of using computer vision for real-time monitoring of parking lot occupancy. The system provides an automated, accurate, and efficient solution for detecting and counting available parking spots, which can be beneficial for smart parking systems and urban traffic management.

## Future Work

Potential improvements and future work could include:

1. **Enhanced Model Training:**
   Training the model on a larger and more diverse dataset to improve classification accuracy.

2. **Scalability:**
   Adapting the system to handle larger parking lots and different camera angles.

3. **Integration with IoT:**
   Integrating the system with IoT devices for better data collection and real-time reporting.
