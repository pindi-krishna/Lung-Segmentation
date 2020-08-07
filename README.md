# Lung-Segmentation
1. Reimplementation of the proposed Architecture of paper [CE-Net: Context Encoder Network for 2D Medical Image Segmentation](https://arxiv.org/abs/1903.02740) and evaluating on Luna grand challenge dataset. 
2. Implementation is done using Pytorch deep learning framework.

## Dataset Descrioption 
1. The 2D images of data can be downloaded from [Kaggle](https://www.kaggle.com/kmader/finding-lungs-in-ct-data?select=2d_images.zip). 
2. Training data : 214 images 
3. Testing Data : 53 images

## Workflow : 
1. Resizing : (448, 448)
2. Data Augmentation Techniques : Color jittering in HSV color space, Random shifting , Random Scaling, Random Flipping, Random Rotating .
3. Generating a binary mask by setting the threshold = 0.5
4. Traning the Context Encoder Architecture on the above preprocessed data. 
5. Computing the metrics sensitivity and accuracy on test dataset. 

## Hyperparamters : 
1. Input size : (1,448, 448)
2. Batch_size = 8
3. Learning_rate = 0.0002
4. Epochs = 100
5. INITAL_EPOCH_LOSS = 10000
6. NUM_UPDATE_LR = 10  (Learning rate will be reduced by 2 if the no imprrovement in training accuracy for 10 epochs)
7. NUM_EARLY_STOP = 20 (If there is no imprrovement in training accuracy for 20 epochs, then training will be stopped).

## Results 
| Metrics | Reported Results | Reproduced Results | 
|-------- | ----------- | ---------- |
| Accuracy | 0.990 |  0.988 |
| Sensitivity | 0.980 | 0.977 |

# Thank you

