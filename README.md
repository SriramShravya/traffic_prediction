#  AI-Powered Traffic Detection & Prediction System  

This project is a complete **traffic analysis pipeline** that:  
- Detects and tracks **persons, cars, bikes, and auto-rickshaws** in videos using **YOLOv8**.  
- Prevents double counting (persons on vehicles, auto overlaps between models).  
- Computes **vehicle speeds**, **traffic density**, and **conditions (Light / Moderate / Heavy)**.  
- Exports results to **CSV (frame-wise + summarized)**.  
- Uses **Random Forest ML model** to classify real-time traffic from detection statistics.  

# Project Features  

1. **YOLOv8 Training on Roboflow Dataset**
   - Custom-trained YOLOv8 model for auto-rickshaw detection.  
   - Integrated with Roboflow for dataset management.  

2. **Object Detection & Tracking**
   - Two models used:
     - **Custom YOLOv8 (autorickshaw detection)**
     - **Base YOLOv8s (general detection: persons, cars, bikes)**  
   - Avoids double counting with IoU-based filtering.  

3. **Traffic Analytics**
   - Frame-wise counts of persons, cars, bikes, autos.  
   - Vehicle speeds (rough estimates).  
   - Traffic condition classification: **Low / Moderate / High**.  

4. **ML Traffic Prediction**
   - Random Forest Classifier trained on labeled data.  
   - Predicts **Light / Moderate / Heavy traffic** from detected counts & average speed.  
   - Generates final summary of overall traffic condition.  

5. **Outputs**
   - Annotated traffic video.  
   - Frame-wise CSV (`combined_traffic_counts.csv`).  
   - 10-second summarized CSV (`summarized_traffic_every_10s.csv`).  
   - Final prediction CSV (`traffic_counts_with_predictions.csv`).  
