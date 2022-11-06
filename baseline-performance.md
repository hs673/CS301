According to the Training and Validation Loss graph, after around 30 Epochs, the validation loss becomes significantly greater than the training loss. Validation loss indicates how well the model fits new data, and a high validation loss means that the model is not predicting the satellite test image well. Training loss indicates how well the model is fitting training data, a high training loss meaning that the model does not predict the training data well. The higher validation loss than training loss means that the model is underfitting and was not trained enough to accurately predict the new test images.

In the Training and Validation IoU graph, the validation IoU has a low value hovering around .2 also indicating that the model does not accurately predict the new test images.


# picture
# ![validationset1](validationset1.png?raw=true "segmentedimages") 
# ![validationset2](validationset2.png?raw=true "segmentedimages") 
# ![validationset3](validationset3.png?raw=true "segmentedimages") 
# ![validationset4](validationset4.png?raw=true "segmentedimages") 
# ![tvloss](tvloss.png?raw=true "trainingvalidationloss") 
# ![tvIoU](tvIoU.png?raw=true "trainingvalidationIoU") 