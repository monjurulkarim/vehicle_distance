# Measuring the distance to the nearest vehicle
For developing advanced driving assistance systems (ADAS) it is required to detect the distance to the nearest vehicle from the user vehicle using the vehicle mounted camera. This repository contains the code for estimating the distance to the nearest vehicle using the principle of similar triangles. For detecting objects Yolo v3 has been used.

![ezgif com-gif-maker (3)](https://user-images.githubusercontent.com/40798690/87365452-e42b3280-c53b-11ea-85ed-0bf9615ac5b3.gif)

For object detection Yolo v3 has been used. The code for Yolo V3 has been taken from https://github.com/qqwweee/keras-yolo3. Then detection file has been modified to get the nearest vehicle and to get the perspective distance to that vehicle using the principle of similar triangles. The algorithm for distance estimation can be found in section 2.3 of this <a href="https://arxiv.org/abs/2106.10319"> paper</a>.


## Getting Started
* Install the required dependencies: (for reference see https://github.com/qqwweee/keras-yolo3 )
* download the pre-trained weight from: [download](https://drive.google.com/file/d/1BEfbOIdso_rVsQH8Tq_V-b1Kbt1bNK3S/view?usp=sharing) and put it inside `model_data` directory.
* [yolo.py](https://github.com/monjurulkarim/vehicle_distance/blob/master/yolo.py) : this file is for the detecting objects. Function `detect_image` has been modified to calculate the distance to the nearest car.
* [yolo_video.py](https://github.com/monjurulkarim/vehicle_distance/blob/master/yolo_video.py): call this code to run the inference

## How to run the detection code
On your terminal at the same directory type the following:
~~~~
python yolo_video.py --image
~~~~

## Citation
If you use this repository, please cite the following paper:

~~~~
@article{karim2021system,
  title={A system of vision sensor based deep neural networks for complex driving scene analysis in support of crash risk assessment and prevention},
  author={Karim, Muhammad Monjurul and Li, Yu and Qin, Ruwen and Yin, Zhaozheng},
  journal={arXiv preprint arXiv:2106.10319},
  year={2021}
}
~~~~
