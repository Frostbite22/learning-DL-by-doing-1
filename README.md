# LEARNING DEEP LEARNING BY DOING - Project 1 
This is a self assigned deep learning project in which I make in practice.<br>
The dataset that I will be using is the [Sign Language MNIST](https://www.kaggle.com/datasets/datamunge/sign-language-mnist)  

## L2SVM as loss function 
According to this [paper :Deep Learning using Linear Support Vector Machines
](https://paperswithcode.com/paper/deep-learning-using-linear-support-vector) L2SVM might improve the overall accuracy over sigmoid activation functions so I will use L2SVM as loss function and compare it to crossEntropyLoss

## Ensemble of Networks 
Ensemble of network might improve the overall accuracy by combining multiple models such that each model might excel at a specific type of detection 

## K-fold cross validation 
Helps us avoid overfitting by changing the target data each data at validation

## MultiClassHingeLoss 
This loss function is based upon L2 hinge Loss which is squared hinge loss.<br>
It penelizes more the classifications within the margin boundary and it is differentiable thus we can apply the gradient descent to it, unlike the L1 hinge Loss which is not differentiable.

## Results 
CrossEntropyLoss and MultiClassHingeLoss yielded almost similar results :

| Model      | Loss Function | optimizer     | Train Accuracy | Test Accuracy  |
|   :----:    |    :----:   |   :----:  |  :----:   |   :----:    |
| ResNet18    | MultiClassHingeLoss       | SGD with Momentum   | 99%+ | 99%+ |
| ResNet18    | CrossEntropyLoss       | SGD with Momentum   | 99%+ | 99%+ |
| SimpleConv | MultiClassHingeLoss  | Adam | 99% | 97% | 
| SimpleConv | CrossEntropyLoss  | Adam | 99% | 96% | 
