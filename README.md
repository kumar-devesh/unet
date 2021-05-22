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

```python

100% 100/100 [01:09<00:00,  1.43it/s]
{'bg': ([0], [0]), 'face': ([1], [1]), 'lb': ([2], [2]), 'rb': ([3], [3]), 'le': ([4], [4]), 're': ([5], [5]), 
'nose': ([6], [6]), 'ulip': ([7], [7]), 'imouth': ([8], [8]), 'llip': ([9], [9]), 'hair': ([10], [10]), 
'eyes': ([4, 5], [4, 5]), 'brows': ([2, 3], [2, 3]), 'mouth': ([7, 8, 9], [7, 8, 9]), 
'overall': ([4, 5, 2, 3, 6, 7, 8, 9], [4, 5, 2, 3, 6, 7, 8, 9])}
f1_bg=0.9379874802503227
f1_face=0.8975739275489326
f1_lb=0.7412928929443516
f1_rb=0.761212647106676
f1_le=0.8356334041047417
f1_re=0.8646787965487952
f1_nose=0.8890915506337703
f1_ulip=0.7408777201730343
f1_imouth=0.7816763526742705
f1_llip=0.8074722443257171
f1_hair=0.6783965714892594
f1_eyes=0.8500789292304956
f1_brows=0.7517517121254107
f1_mouth=0.8676697731729751
f1_overall=0.8555103672626286
```


## How to use

Upload the unet directory to drive and set

```python
dir_path= 'path/to/unet/directory' 
```

To get class wise f1 scores run the cell specifying paths

```python
!python3   path/to/f1_score/    path/to/test/labels    path/to/test/preds  path/to/labels_names.txt
```
