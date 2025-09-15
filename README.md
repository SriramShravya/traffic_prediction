# Traffic Prediction and Object Detection using YOLOv8 and Roboflow

This project performs **traffic object detection and tracking** on video data using YOLOv8 models trained on a custom Roboflow dataset. The system detects and tracks persons, cars, motorcycles, and autorickshaws in video frames, counts unique objects, and outputs annotated videos along with detailed CSV traffic summaries.

## Features

- Train YOLOv8 model on Roboflow traffic dataset
- Run object detection & tracking on input videos
- Differentiate between walking persons and persons on vehicles
- Track unique IDs for persons, cars, motorcycles, and autorickshaws
- Annotate video frames with bounding boxes and IDs
- Generate full-frame and summarized CSV reports with traffic counts over time
