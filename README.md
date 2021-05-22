# unet
unet semantic segmentation on helen* dataset

## UNET Architecture

![alt text](https://github.com/kumar-devesh/unet/blob/29f8da74d5bb9349aad348d2705db14516587d67/images/unet_architecture.png)

## Dataset

Helen* dataset consists 2000 train images, masks and 100 test images, masks with 11 classes. 
The dataset has been resized to 256,256 for both images and segmentation masks.

![alt text](https://github.com/kumar-devesh/unet/blob/main/images/image_7.png)
![alt text](https://github.com/kumar-devesh/unet/blob/main/images/label_7.PNG)

![alt text](https://github.com/kumar-devesh/unet/blob/main/images/image_45.png)
![alt text](https://github.com/kumar-devesh/unet/blob/main/images/label_45.PNG)

## Model predictions on test set

![alt text](https://github.com/kumar-devesh/unet/blob/main/images/label.png)
![alt text](https://github.com/kumar-devesh/unet/blob/main/images/pred.png)


## Model class wise f1 scores

![alt text](https://github.com/kumar-devesh/unet/blob/main/images/f1score.PNG)


## How to use

Upload the unet directory to drive and set

```python
dir_path= 'path/to/unet/directory' 
```

To get class wise f1 scores run the cell specifying paths

```python
!python3   path/to/f1_score/    path/to/test/labels    path/to/test/preds  path/to/labels_names.txt
```
