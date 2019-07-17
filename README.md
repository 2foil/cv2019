# CV & AI Project 2019


![](https://img.shields.io/badge/python-3.7-brightgreen.svg)
![](https://img.shields.io/pypi/l/numpy.svg)
![](https://img.shields.io/github/languages/code-size/2foil/cv2019.svg)
![](https://img.shields.io/pypi/format/torch.svg)
![](https://img.shields.io/badge/pytorch-1.1.0-brightgreen.svg)

## Files
- `src/` the source code of our project
- `results.ipynb` show the face detection results
- `training.ipynb` train the MTCNN
- `data.dat` the face detection result(face box data).

The jupyter files demonstrate the usage of our program.

## Dependency

To run our code for face detection, you should have `pytorch` installed.
If not, use `pip intsall torch` to install pytorch.

## Usage

It's quite easy to use our program for face detection.

Suppose you have a test image, on which you want to detect faces and its path is `path/to/image`.

First, import the functions and modules we need.

```python
from src import detect_faces, show_bboxes
from PIL import Image
```

Then, follow the steps below:

```python
img = Image.open('path/to/image')           # open the test image.
bb, _ = detect_faces(Image.open(img))       # using the MTCNN to detect the human face
new_img = show_boxes(img, bb, 'yellow', 3)  # get the new image with the human face labeled
new_img.save('path/to/new_img.jpg')        # save the result image for review

```

There you are! :)

Just open the `new_img.jpg` saved and you'll find all the faces are detected on that image.

## Face Detection Demo
![demo](./new_8.JPG)