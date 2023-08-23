# Pytorch-Custom-CNN-model
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

There are 4 Conv2d layers and 4 Linear Layer and use MaxPool in pooling layer
