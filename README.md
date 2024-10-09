### Summary of the Project
Implemented a car and object detection model using Deep Convolutional Neural Networks (CNNs) to detect cars and other objects in images.

#### Algorithms and Techniques Used:
- **Object Detection Model**: 
  - **YOLO (You Only Look Once)**: A real-time object detection algorithm that frames object detection as a single regression problem, directly predicting class probabilities and bounding box coordinates from images.
- **Key Functions and Methods**:
  - `yolo_filter_boxes`: Filters YOLO boxes by thresholding on object and class confidence.
  - `yolo_non_max_suppression`: Applies Non-Max Suppression (NMS) to eliminate redundant overlapping boxes using the Intersection Over Union (IoU) metric.
  - `iou`: Calculates the Intersection Over Union between two bounding boxes to evaluate overlap.
  - `yolo_boxes_to_corners`: Converts YOLO box predictions to bounding box corners for accurate representation.
  - `yolo_eval`: Converts the output of YOLO to predicted boxes along with their scores, coordinates, and classes.
  - `predict`: Processes an input image, applies the YOLO model, and visualizes the detection results.

#### Technical Components:
- **Libraries & Tools**: 
  - `TensorFlow` for model implementation.
  - `yad2k` for the YOLO model architecture.
  - `PIL` and `Matplotlib` for image processing and visualization.

#### Model Optimization:
- Utilized Non-Max Suppression (NMS) and Intersection Over Union (IoU) to reduce overlapping anchor boxes and select the best possible bounding box.
- Fine-tuned parameters like `max_boxes`, `iou_threshold`, and `score_threshold` to balance detection accuracy and speed.

The project showcases the integration of YOLO for detecting cars and other objects with real-time processing capabilities, making it suitable for applications in autonomous driving and intelligent transportation systems.
