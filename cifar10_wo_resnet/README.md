# Purpose:
To see the results what if i dont use ResNet advantages. Without having well-run weights and biases that comes from pretrained model of Resnet, i would expect that the model takes time in training. Also results must be slighly lower than the resnet's. But in order to enhance the model, i apply data augmentation to dataset so that it would give more sensible information even though it is very limitted by comparing the dataset that was used in training ResNet.

# Results:
## No Data Augmentation

 Takeaways: <br />
* accuracies are always increasing trend which is good.
* losses are decreasing constantly until 30th of epochs. After that, they are aparting from each other. Until the early stop, val_loss suffers to increasing more. The result would be that the dataset in validation and train are not various. So it makes the model defenseless for validation data or test data. Here we can see that the line in val_loss are not constanly decreasing.
* But scores are quite good when we consider that only cnn model is applied, nothing else is done here. By the time and effort point of view, it could be quite acceptable.
  
![image](https://github.com/user-attachments/assets/a01d4dcb-d130-4d31-bd4d-08e868cbabe5)

## Data Augmentation

 Takeaways: <br />
* I noticed that if I directly use the model that works for no data augmentation, it seems to be weak. That's why, I want the gradient to be less vanished by having small dropouts.
* I cut out the 64 dense neurons from the FC layer. The reason why is that i want the model not to memorise the input that leads the model overfitting. I am thinking that less deep in FC gives the model the change not to be overfitted easily.
* I did not change the depth of CONV layer because it is where the image are being introduced by capturing features from each image.

* ![image](https://github.com/user-attachments/assets/d6095496-9e14-4b17-953b-143dfa86b7ff)

## Summary:
When i augment the input data with small changes in model, i got much more better results which is even more close to resnet model's results. 
