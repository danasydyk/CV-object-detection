# CV Object Detection - XWOD Benchmark

Object detection on the [XWOD (Extreme Weather Object Detection)](https://www.kaggle.com/datasets/kuantinglai/exwod) benchmark using YOLOv8. The dataset contains 10,010 images across 7 extreme weather conditions (Rain, Snow, Fog, Haze, Flooding, Tornado, Wildfire) with 42,924 bounding box annotations across 6 classes: Car, Truck, Person, Bus, Motorcycle, Bike.

## Model

- **Architecture:** YOLOv8m (medium)
- **Pretrained on:** COCO
- **Input size:** 640×640
- **Augmentations:** Mosaic, Mixup, Copy-Paste, HSV shifts
- **Regularization:** Weight decay 0.001, frozen backbone (first 10 layers), early stopping

## Results

| Metric | Score |
|--------|-------|
| Precision | 0.700 |
| Recall | 0.499 |
| mAP@50 | 0.555 |
| mAP@50-95 | 0.311 |

## Demo

**Original video:**

https://github.com/danasydyk/CV-object-detection/blob/main/video.mp4

**Predicted video (YOLOv8m detections):**

https://github.com/danasydyk/CV-object-detection/blob/main/predicted.avi

## Files

- `kaggle.ipynb` — full training and evaluation notebook
- `video.mp4` — original test video
- `predicted.avi` — model predictions on test video
