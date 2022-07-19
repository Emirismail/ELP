# ELP

This repository is designed to provide an open-source dataset for license plate detection and recognition:

## Download
#### It can be downloaded from:
* [GDrive](https://drive.google.com/drive/folders/1thG3MtalX2FfkQX1KUhFzWZ0FOmmvEUU?usp=sharing)


## Annotation

*  The bounding box of the license plate in the image;
*  The bounding box of the characters in the current license plate;
*  The sequence label of the current license plate;

## Dataset Annotations

Annotations are embedded in txt files.


- **Bounding box coordinates**: The coordinates are the center (x,y), width and height.


- **License plate number**: Most images in ELP have only one LP. Each LP number is comprised of letters and numbers.

```
Alphabets = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'J', 'K', 'L', 'M', 'N', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']

Digits = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']

```



### Metrics
We consider precision, recall, F1-score, mAP and LPRR.

- Detection. For each image, the detector outputs LP bounding box. The bounding box is considered to be correct if and only if its IoU with the ground truth bounding box is more than 50% (IoU > 0.5). Also, we compute mAP on the test set. 

- Recognition. A LP recognition is correct if and only if all characters in the LP number are correctly detected.


## Label Toolkit
* [labelImg](https://github.com/tzutalin/labelImg)
  
## Acknowledgement


## Limitation of Liability
It is worth noting that ELP can only be used for academic research, not for commercial use.