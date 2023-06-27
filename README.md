# Fish Image Dataset
This is a dataset of fish images used to train the ResNet model. The dataset contains images with `HaveFish` and `NoFish` underwater image.

## Structure of Dataset

In this structure, the dataset is organized as follows:

- `global-detection-dataset/`: The root folder of the image data.
    - `train/`: Contains the training images.
        - `hasFish/`: Contains the images include fish.
            - hasFish1.jpg
            - hasFish2.jpg
            - ...
        - `notHasFish/`: Contains the images does not include fish.
            - notHasFish1.jpg
            - notHasFish2.jpg
            - ...
    - `test/`: Contains the testing images.
        - `hasFish/`: Contains the images include fish.
            - hasFish1.jpg
            - hasFish2.jpg
            - ...
        - `notHasFish/`: Contains the images does not include fish.
            - notHasFish1.jpg
            - notHasFish2.jpg
            - ...

## Usage
This dataset can be directly loaded by using `ImageFolder` and `DataLoader` in PyTorch.
```python
train_set = ImageFolder(root='../global-detection-dataset/train', transform=transform)
test_set = ImageFolder(root='../global-detection-dataset/test', transform=transform)
train_loader = DataLoader(train_set, batch_size=batch_size, shuffle=True)
test_loader = DataLoader(test_set, batch_size=batch_size, shuffle=True)
```
