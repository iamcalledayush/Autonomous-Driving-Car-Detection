### Summary of the Project
Implemented a car and object detection model using Deep Convolutional Neural Networks (CNNs) to detect cars and other objects in images.

#### Algorithms and Techniques Used:
- **Object Detection Model**: 
  - **YOLO (You Only Look Once)**: A real-time object detection algorithm that frames object detection as a single regression problem, directly predicting class probabilities and bounding box coordinates from images.
- **Method**:
  - Filter YOLO boxes by thresholding on object and class confidence.
  - Apply Non-Max Suppression (NMS) to eliminate redundant overlapping boxes using the Intersection Over Union (IoU) metric.
  - Convert YOLO box predictions to bounding box corners for accurate representation.
  - Convert the output of YOLO to predicted boxes along with their scores, coordinates, and classes.
  - Process an input image, applies the YOLO model, and visualizes the detection results.

#### Technical Components:
- **Libraries & Tools**: 
  - `TensorFlow` for model implementation.
  - `yad2k` for the YOLO model architecture.
  - `PIL` and `Matplotlib` for image processing and visualization.

#### Model Optimization:
- Utilized Non-Max Suppression (NMS) and Intersection Over Union (IoU) to reduce overlapping anchor boxes and select the best possible bounding box.
- Fine-tuned parameters like `max_boxes`, `iou_threshold`, and `score_threshold` to balance detection accuracy and speed.
