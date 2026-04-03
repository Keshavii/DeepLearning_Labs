# Dataset Description

## Overview

The dataset used in this project consists of images containing multiple object classes along with corresponding annotations in Pascal VOC format. It is used for training, validation, and evaluation of object detection models across different architectures including R-CNN, Faster R-CNN, and YOLO.

---

## Dataset Structure

LINK of dataset: https://www.kaggle.com/datasets/mbkinaci/fruit-images-for-object-detection/data

The dataset is organized in a format compatible with YOLO training as well as traditional pipelines:

dataset/
│
├── images/
│   ├── train/
│   ├── val/
│
├── labels/
│   ├── train/
│   ├── val/

- **images/** contains input images in `.jpg` format  
- **labels/** contains corresponding annotation files in YOLO format (`.txt`)  
- Each image has a corresponding label file with the same filename  

---

## Annotation Format

### Pascal VOC (Original)

Annotations were initially provided in XML format:
# Dataset Description

## Overview

The dataset used in this project consists of images containing multiple object classes along with corresponding annotations in Pascal VOC format. It is used for training, validation, and evaluation of object detection models across different architectures including R-CNN, Faster R-CNN, and YOLO.

---

## Dataset Structure

The dataset is organized in a format compatible with YOLO training as well as traditional pipelines:

dataset/
│
├── images/
│   ├── train/
│   ├── val/
│
├── labels/
│   ├── train/
│   ├── val/

- **images/** contains input images in `.jpg` format  
- **labels/** contains corresponding annotation files in YOLO format (`.txt`)  
- Each image has a corresponding label file with the same filename  

---

## Annotation Format

### Pascal VOC (Original)

Annotations were initially provided in XML format:
# Dataset Description

## Overview

The dataset used in this project consists of images containing multiple object classes along with corresponding annotations in Pascal VOC format. It is used for training, validation, and evaluation of object detection models across different architectures including R-CNN, Faster R-CNN, and YOLO.

---

## Dataset Structure

The dataset is organized in a format compatible with YOLO training as well as traditional pipelines:

dataset/
│
├── images/
│   ├── train/
│   ├── val/
│
├── labels/
│   ├── train/
│   ├── val/

- **images/** contains input images in `.jpg` format  
- **labels/** contains corresponding annotation files in YOLO format (`.txt`)  
- Each image has a corresponding label file with the same filename  

---

## Annotation Format

### Pascal VOC (Original)

Annotations were initially provided in XML format:
# Dataset Description

## Overview

The dataset used in this project consists of images containing multiple object classes along with corresponding annotations in Pascal VOC format. It is used for training, validation, and evaluation of object detection models across different architectures including R-CNN, Faster R-CNN, and YOLO.

---

## Dataset Structure

The dataset is organized in a format compatible with YOLO training as well as traditional pipelines:

dataset/
│
├── images/
│   ├── train/
│   ├── val/
│
├── labels/
│   ├── train/
│   ├── val/

- **images/** contains input images in `.jpg` format  
- **labels/** contains corresponding annotation files in YOLO format (`.txt`)  
- Each image has a corresponding label file with the same filename  

---

## Annotation Format

### Pascal VOC (Original)

Annotations were initially provided in XML format:
<object> <name>apple</name> <bndbox> <xmin>...</xmin> <ymin>...</ymin> <xmax>...</xmax> <ymax>...</ymax> </bndbox> </object> ```
YOLO Format (Converted)

For training YOLO, annotations were converted into:
<class_id> <x_center> <y_center> <width> <height>
