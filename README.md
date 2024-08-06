# License-Plate-Detection_ONNX

![Downloads](https://img.shields.io/github/downloads/Mrkomiljon/License-Plate-Detection_ONNX/total) [![GitHub Repository](https://img.shields.io/badge/GitHub-Repository-blue?logo=github)](https://github.com/Mrkomiljon/License-Plate-Detection_ONNX)

<video controls autoplay loop src="https://github.com/user-attachments/assets/14280f75-b719-46c3-a5bf-a83d8330645e" muted="false" width="100%"></video>



<video controls autoplay loop src="https://github.com/user-attachments/assets/cc641c10-164a-47be-acff-c461f0c386c3" muted="false" width="100%"></video>



Link: https://www.pexels.com/video/motor-vehicles-traveling-on-a-highway-5473757/

This repository contains code and instructions for performing object detection using YOLOv5 inference with ONNX Runtime.

## Features

- Inference using ONNX Runtime with GPU (tested on Windows).
- Easy-to-use Python scripts for inference.
- Supports multiple input formats: image, video, or webcam.

## Installation

#### Clone the Repository

```bash
git clone https://github.com/Mrkomiljon/License-Plate-Detection_ONNX.git
cd License-Plate-Detection_ONNX
```

#### Install Required Packages

```bash
pip install -r requirements.txt
```

## Usage

Before running inference, you need to download weights of the YOLOv5 model [weights](https://drive.google.com/drive/folders/1UvONZS20f_za1XJjgHBnUO5XtoUJISPd?usp=sharing) in ONNX format.


#### Inference

```bash
python main.py --weights weights/yolov5s.onnx --source assets/vid_input.mp4 # video
                                              --source 0 --view-img # webcam and display
                                              --source assets/img_input.jpg # image
```

- To save results add the `--save-img` argument and results will be saved under the `runs` folder
- To display video add the `--view-img` argument

**Command Line Arguments**

```
usage: main.py [-h] [--weights WEIGHTS] [--source SOURCE] [--img-size IMG_SIZE [IMG_SIZE ...]] [--conf-thres CONF_THRES] [--iou-thres IOU_THRES]
               [--max-det MAX_DET] [--save-img] [--view-img] [--project PROJECT] [--name NAME]

options:
  -h, --help            show this help message and exit
  --weights WEIGHTS     model path
  --source SOURCE       Path to video/image/webcam
  --img-size IMG_SIZE [IMG_SIZE ...]
                        inference size h,w
  --conf-thres CONF_THRES
                        confidence threshold
  --iou-thres IOU_THRES
                        NMS IoU threshold
  --max-det MAX_DET     maximum detections per image
  --save-img            Save detected images
  --view-img            View inferenced images
  --project PROJECT     save results to project/name
  --name NAME           save results to project/name
```

## Reference

1. https://github.com/ultralytics/yolov5


