# Object Detection with YOLO V8

[![Watch the video](https://drive.google.com/file/d/1UUEnnnhtwJu528QqwIuSndUCx0grbXQg/view?usp=drive_link)](https://drive.google.com/file/d/1METIKP6e4p6RFO6_fGChYjEUp0n_CfYh/view?usp=drive_link)
___
## Dataset

dataset is in roboflow:

```python
!pip install roboflow

from roboflow import Roboflow
rf = Roboflow(api_key="7N79litXnSci7JtMDYwZ")
project = rf.workspace("own-ns5nt").project("hard-hat-sample-f9qdp")
dataset = project.version(3).download("yolov8")
```
___
### Attention

after running jupyter file you will see an error. it is just for relative and absolute paths!

to fix this you shoud modify `data.yaml` file like this:

```
test: /content/datasets/Hard-Hat-Sample-3/test/images
train: /content/datasets/Hard-Hat-Sample-3/train/images
val: /content/datasets/Hard-Hat-Sample-3/valid/images
```
* *absolute path instead of relative path*
___