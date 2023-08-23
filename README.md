# Pytorch-Custom-CNN-model

Dataset- <br>
It is a medical images directory structure branched into 3 subfolders (COVID, NORMAL, PNEUMONIA) which contains the Chest X-ray (CXR) Images.<br>
COVID: 1626 images<br>
NORMAL: 1802 images<br>
PNEUMONIA: 1800 images<br>
Original Dataset Link- https://www.kaggle.com/datasets/sachinkumar413/covid-pneumonia-normal-chest-xray-images <br>
In the Dataset folder contains customized dataset which is splitting the whole dataset into three parts- <br>

1- Training (70%) <br>
2- Validation (15%) <br>
3- Testing (15%) <br>

Model Architecture: <br>

CNN(<br>
  (conv_layers): Sequential(<br>
    (0): Conv2d(3, 16, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1))<br>
    (1): ReLU()<br>
    (2): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)<br>
    (3): Conv2d(16, 32, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1))<br>
    (4): ReLU()<br>
    (5): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)<br>
    (6): Conv2d(32, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1))<br>
    (7): ReLU()<br>
    (8): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)<br>
    (9): Conv2d(64, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1))<br>
    (10): ReLU()<br>
    (11): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)<br>
  )<br>
  (fc_layers): Sequential(<br>
    (0): Linear(in_features=25088, out_features=512, bias=True)<br>
    (1): ReLU()<br>
    (2): Dropout(p=0.2, inplace=False)<br>
    (3): Linear(in_features=512, out_features=256, bias=True)<br>
    (4): ReLU()<br>
    (5): Dropout(p=0.2, inplace=False)<br>
    (6): Linear(in_features=256, out_features=128, bias=True)<br>
    (7): ReLU()<br>
    (8): Dropout(p=0.2, inplace=False)<br>
    (9): Linear(in_features=128, out_features=3, bias=True)<br>
  )<br>
)<br>

There are 4 Conv2d layers and 4 Linear Layer and use MaxPool in the pooling layer <br>

# Model Summary: <br>

| Layer (type) | Output Shape | Param #      |
|--------------|--------------|--------------|
| Conv2d-1     | [-1, 16, 224, 224] | 448      |
| ReLU-2       | [-1, 16, 224, 224] | 0        |
| MaxPool2d-3  | [-1, 16, 112, 112] | 0        |
| Conv2d-4     | [-1, 32, 112, 112] | 4,640    |
| ReLU-5       | [-1, 32, 112, 112] | 0        |
| MaxPool2d-6  | [-1, 32, 56, 56]   | 0        |
| Conv2d-7     | [-1, 64, 56, 56]   | 18,496   |
| ReLU-8       | [-1, 64, 56, 56]   | 0        |
| MaxPool2d-9  | [-1, 64, 28, 28]   | 0        |
| Conv2d-10    | [-1, 128, 28, 28]  | 73,856   |
| ReLU-11      | [-1, 128, 28, 28]  | 0        |
| MaxPool2d-12 | [-1, 128, 14, 14]  | 0        |
| Linear-13    | [-1, 512]          | 12,845,568|
| ReLU-14      | [-1, 512]          | 0        |
| Dropout-15   | [-1, 512]          | 0        |
| Linear-16    | [-1, 256]          | 131,328  |
| ReLU-17      | [-1, 256]          | 0        |
| Dropout-18   | [-1, 256]          | 0        |
| Linear-19    | [-1, 128]          | 32,896   |
| ReLU-20      | [-1, 128]          | 0        |
| Dropout-21   | [-1, 128]          | 0        |
| Linear-22    | [-1, 3]            | 387      |
| **Total params** |               | **13,107,619**|
| **Trainable params** |           | **13,107,619**|
| **Non-trainable params** |       | **0**       |
| **Input size (MB)** |           | **0.57**    |
| **Forward/backward pass size (MB)** | | **25.86**|
| **Params size (MB)** |            | **50.00**   |
| **Estimated Total Size (MB)** |   | **76.44**   |

