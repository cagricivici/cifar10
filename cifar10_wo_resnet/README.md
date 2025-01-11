# Purpose:
To see the results what if i dont use ResNet advantages. Without having well-run weights and biases that comes from pretrained model of Resnet, i would expect that the model takes time in training. Also results must be slighly lower than the resnet's. But in order to enhance the model, i apply data augmentation to dataset so that it would give more sensible information even though it is very limitted by comparing the dataset that was used in training ResNet.

# Results:
Here it is for wo data augmentation:

- Takeaways: 
* accuracies are always increasing trend which is good.
* losses are decreasing constantly until 30th of epochs. After that, they are aparting from each other. Until the early stop, val_loss suffers to increasing more. The result would be that the dataset in validation and train are not various. So it makes the model defenseless for validation data or test data. Here we can see that the line in val_loss are not constanly decreasing.
* But scores are quite good when we consider that only cnn model is applied, nothing else is done here. By the time and effort point of view, it could be quite acceptable.
![image](https://github.com/user-attachments/assets/a01d4dcb-d130-4d31-bd4d-08e868cbabe5)



#Keynotes:
- 
