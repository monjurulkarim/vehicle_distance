# Measuring the distance to the nearest vehicle
For developing advanced driving assistance systems (ADAS) it is required to detect the distance to the nearest vehicle from the user vehicle using the vehicle mounted camera. This repository contains the code for estimating the distance to the nearest vehicle using the the principle of similar triangles. For detecting objects Yolo v3 has been used.

![ezgif com-gif-maker (3)](https://user-images.githubusercontent.com/40798690/87365452-e42b3280-c53b-11ea-85ed-0bf9615ac5b3.gif)

For object detection Yolo v3 has been used. The code for Yolo V3 has been taken from https://github.com/qqwweee/keras-yolo3. Then detection file has been modified to get the nearest vehicle and to get the perspective distance to that vehicle using the principle of similar triangles.


## Getting Started
* Install the required dependencies: (for reference see https://github.com/qqwweee/keras-yolo3 )
* download the pre-trained weight from: 
* [custom.py](https://github.com/monjurulkarim/Tracking_manufacturing/blob/master/custom.py) : this code is used for loading data and training the model
* [Training.ipynb](https://github.com/monjurulkarim/Tracking_manufacturing/blob/master/Training.ipynb): loading the weight and calling the training function
* [result_calculation.ipynb](https://github.com/monjurulkarim/Tracking_manufacturing/blob/master/result_calculation.ipynb): this code is used for detecting objects with or without temporal coherence. This also calculates precision, recall and f1-score of the model.
* [mrcnn/visualize_frame_relation_4f.py](https://github.com/monjurulkarim/Tracking_manufacturing/blob/master/mrcnn/visualize_frame_relation_4f.py) : this code is used for visualizing the detected objects with mask.
