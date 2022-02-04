## YOLOX Trained Models

Have you ever wanted a **fast**/**accurate** object detection model, but didn't have **time**/**resources** to train it?

### Intro

This repo aims to provide a variety **trained models**, which you can use directly
with [YOLOX](https://github.com/Megvii-BaseDetection/YOLOX) framework.

We also train models on different datasets with bigger/lower **object area** to **exploit performance**. For example, if you
need a face detector that will be used on mobile front cameras, there is no need to detect faces that have very
**small area**. We can take advantage of this and use a lower input resolution, so inference is very **fast**.

### Request Model

Models are mainly trained with Open [Images Dataset V6](https://storage.googleapis.com/openimages/web/index.html), which
has 600 classes. If you would like to see a model here, which is not present, feel free to open an issue 
[here](https://github.com/ankandrew/yolox-models/issues/new?assignees=&labels=train+model&template=request-new-model.md&title=%5BTRAIN%5D+-+).

### Models

#### Face

| Model | Activation | Input Resolution | mAP<sup>test<br>0.5:0.95</sup> | Area | Weights |
|-------|------------|------------------|--------------------------------|------|---------|
| nano  | silu       | 128x128          | ...                            | 10%  | link    |
| nano  | leaky relu | 128x128          | ...                            | 10%  | link    |

### TODO

- [ ] Make script to reproduce datasets
- [ ] Create issue template for new requested models

## Reference

```latex
 @article{yolox2021,
  title={YOLOX: Exceeding YOLO Series in 2021},
  author={Ge, Zheng and Liu, Songtao and Wang, Feng and Li, Zeming and Sun, Jian},
  journal={arXiv preprint arXiv:2107.08430},
  year={2021}
}
```