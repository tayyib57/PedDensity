# Detection
## Pedestrian Flow Density Detection Based on Video

1. **detection.py**: Uses pre-trained Faster-RCNN parameters to identify and label pedestrians (the threshold for labeling pedestrians is 0.7, meaning the detection rate must reach 70%).<br>
2. **camshift2.py**: Uses mean-shift to track already labeled pedestrians, continuously updating their positions through iterations and marking them in real-time.<br>
3. **kalmon.py**: Utilizes the Kalman filter to predict pedestrian movement positions, improving tracking accuracy.<br>
4. **multi-object-tracking.py**: Uses a multi-object tracker to track multiple targets.<br>
5. **multi_camshift_detection.py**: Employs the camshift method for target tracking and uses the Kalman filter for prediction, achieving multi-target tracking (this method has larger target box movement).<br>
6. **multi_track_detection.py**: Finalized program for pedestrian target tracking and flow density detection based on video.

## Dependencies:
- **faster_rcnn_inception_v2_coco_2018_01_28** (Faster-RCNN network framework)
- **ssd_mobilenet_v1_coco_2018_01_28** (SSD-MobileNet network framework)
- **object_detection** (Object detection library, modified parameters to fit this program)

## Description:
This project focuses on pedestrian flow density detection based on video. The programming language used is Python (version 3.6.4), and the main tool library used is OpenCV 3.4.

## Main Methods:
1. Research on commonly used image preprocessing algorithms
2. Research on background modeling algorithms
3. Research on moving target detection algorithms
4. Research on target matching and tracking algorithms

## Updates:
Updated the pedestrian detection count in the marked area to determine if a point is inside a quadrilateral area. Main code can be found in the `isPosition(center_position)` function in `multi_track_detection.py`.

## Results:
![Result](https://github.com/librahfacebook/Detection/blob/master/result_images/result.jpg)

## Data Analysis Chart:
![Analysis](https://github.com/librahfacebook/Detection/blob/master/result_images/analysis.png)
