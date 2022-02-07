## YOLOX Trained Models

Have you ever wanted a **fast**/**accurate** object detection model, but didn't have **time**/**resources** to train it?

### Intro

This repo aims to provide a variety **trained models** on **different objects**, which you can use directly
with [YOLOX](https://github.com/Megvii-BaseDetection/YOLOX) framework.

We also train models on different views of the datasets that have bigger/lower **object area**. For example, if you need
a face detector that will be used on mobile front cameras, there may be no need to detect faces that have very
**small area** (very far objects). We can take advantage of this and use a lower input resolution, so inference is
very **fast**.

### Contents

- [Request Model](#request-model)
- [Models](#models)
    * [Face](#face)

### Request Model

Models are mainly trained with Open [Images Dataset V6](https://storage.googleapis.com/openimages/web/index.html), which
has 600 classes. If you would like to see a model here, which is not present, feel free to open an issue
[here](https://github.com/ankandrew/yolox-models/issues/new?assignees=&labels=train+model&template=request-new-model.md&title=%5BTRAIN%5D+-+).

### Models

#### Face

| Model | Activation | Input Resolution | mAP<sup>test<br>0.5:0.95</sup> | Area  | Weights                                                                                                        | Experiment                                                                                     |
|-------|------------|------------------|--------------------------------|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| nano  | silu       | 128x128          | 74.20                          | > 10% | [github](https://github.com/ankandrew/yolox-models/releases/download/v1.0.0/faces_10p_area_nano_128_silu.pth)  | [github](https://github.com/ankandrew/yolox-models/releases/download/v1.0.0/nano_128_silu.py)  |
| nano  | leaky relu | 128x128          | 73.68                          | > 10% | [github](https://github.com/ankandrew/yolox-models/releases/download/v1.0.0/faces_10p_area_nano_128_lrelu.pth) | [github](https://github.com/ankandrew/yolox-models/releases/download/v1.0.0/nano_128_lrelu.py) |
| nano  | silu       | 160x160          | 72.72                          | > 5%  | [github](https://github.com/ankandrew/yolox-models/releases/download/v1.0.0/faces_5p_area_nano_160_silu.pth)   | [github](https://github.com/ankandrew/yolox-models/releases/download/v1.0.0/nano_160_silu.py)  |
| nano  | leaky relu | 160x160          | 71.90                          | > 5%  | [github](https://github.com/ankandrew/yolox-models/releases/download/v1.0.0/faces_5p_area_nano_160_lrelu.pth)  | [github](https://github.com/ankandrew/yolox-models/releases/download/v1.0.0/nano_160_lrelu.py) |
| nano  | silu       | 192x192          | 66.97                          | > 1%  | [github](https://github.com/ankandrew/yolox-models/releases/download/v1.0.0/faces_1p_area_nano_192_silu.pth)   | [github](https://github.com/ankandrew/yolox-models/releases/download/v1.0.0/nano_192_silu.py)  |
| nano  | leaky relu | 192x192          | 66.21                          | > 1%  | [github](https://github.com/ankandrew/yolox-models/releases/download/v1.0.0/faces_1p_area_nano_192_lrelu.pth)  | [github](https://github.com/ankandrew/yolox-models/releases/download/v1.0.0/nano_192_lrelu.py) |

_Note: You can try using any model with slightly higher/lower input resolution and will also work fine._

### TODO

- [x] Create issue template for new requested models
- [ ] Make script to reproduce datasets

### Reference

```latex
 @article{yolox2021,
  title={YOLOX: Exceeding YOLO Series in 2021},
  author={Ge, Zheng and Liu, Songtao and Wang, Feng and Li, Zeming and Sun, Jian},
  journal={arXiv preprint arXiv:2107.08430},
  year={2021}
}
```