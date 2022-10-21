# Face Mask Detection

The project is about the development of an algorithm that could help in controlling the use of masks in public places by the analysis of video footage, photos, etc.

## Acknowledgements

The code constitutes an implementation of the approach proposed by [Joshi et al.](https://ieeexplore.ieee.org/abstract/document/9242625)

## Framework

### Face Detection

The goal is to detect person faces from images taken in a wild environment. For this purpose [<b>MTCNN</b>](https://github.com/ipazc/mtcnn) was used: a Convolutional Neural Network that exploits multi-task learning to integrate face detection and face alignment.
MTCNN was evaluated on [<i>Face Mask Dataset</i>](https://www.kaggle.com/datasets/aditya276/face-mask-dataset-yolo-format) that contains 924 images of people with and without mask (```FaceMaskDetection_main.ipynb```).

| Recall | Precision | F1 |
| ------ | --------- | -- |
| 74.4%  |    82.8%  |78.4%|
