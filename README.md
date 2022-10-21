# Face Mask Detection

The project is about the development of an algorithm that could help in controlling the use of masks in public places by the analysis of video footage, photos, etc.

## Acknowledgements

The code constitutes an implementation of the approach proposed by [Joshi et al.](https://ieeexplore.ieee.org/abstract/document/9242625)

## Python dependencies

<ul>
  <li>OpenCV</li>
  <li>Numpy</li>
  <li>Tensorflow</li>
</ul>

## Face Detection

Detect person faces from images taken in a wild environment with [<b>MTCNN</b>](https://github.com/ipazc/mtcnn), a CNN that exploits multi-task learning to integrate face detection and face alignment.

![Unknown](https://user-images.githubusercontent.com/34343511/197197731-2c1942a7-062e-447f-807e-9d8f881029b4.png)

In ```FaceMaskDetection_main.ipynb```, MTCNN was evaluated on [<i>Face Mask Dataset</i>](https://www.kaggle.com/datasets/aditya276/face-mask-dataset-yolo-format) that contains 924 images of people with and without mask.

| Precision | Recall |  F1  |
| --------- | ------ | ---- |
|   82.8%   | 74.4%  | 78.4%|

### Mask Prediction

Predict the presence of masks with [<b>MobileNetV2</b>](https://arxiv.org/abs/1801.04381), a network architecture that performs feature extraction for object detection and segmentation.

![Unknown-1](https://user-images.githubusercontent.com/34343511/197201968-f4dbb74e-90f1-4253-b45f-2c8b8ca56b36.png)

In ```MaskDetection_training.ipynb``` the cited network was trained on [<i>Face Mask Detection ~12K Images Dataset</i>](https://www.kaggle.com/datasets/ashishjangra27/face-mask-12k-images-dataset) that contains only faces of people with and without masks.

In ```FaceMaskDetection_main.ipynb```, the trained MobileNetV2 model was used to be evaluated on <i>Face Mask Dataset</i>.

|              | Precision | Recall | F1  |
| ------------ | --------- | ------ | --- |
| WithMask     | 75%       | 93%    | 83% |
| WithoutMask  | 91%       | 69%    | 78% |
