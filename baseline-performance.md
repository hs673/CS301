In this project, we are using Unet to train our model to predict an accurate segmented image of a satellite photo. There are six classes with which each satellite photo can be annotated that includes Buildings, Land, Road, Vegetation, Water, and Unlabeled. Each class has their own visual representaton on the photo with a unique color overlay. This model is fed 72 pictures from the training set that are already populated with the color overlay.After using Unet to generate the model, we tested the model against the validation set. 

Validation loss indicates how well the model fits new data while training loss indicates how well the model is fitting the training data. 

According to the Training and Validation Loss graph, after around 30 Epochs, the validation loss becomes significantly greater than the training loss. A high validation loss means that the model is not predicting the satellite test image well. The decreasing training loss values are a result of the model's recall because it is seeing the same 72 images again. The higher validation loss than training loss means that the model is underfitting the data and was not trained with enough data to accurately predict the new test images.

In the Training and Validation IoU graph, the validation IoU has a low value hovering around .21 also indicating that the model does not accurately predict the new test images. The model is seeing the same images again in the training set which is the reason why the training IoU increases as the model goes through the epochs. 

# ![validationset1](validationset1.png?raw=true "segmentedimages") 
# ![validationset2](validationset2.png?raw=true "segmentedimages") 
# ![validationset3](validationset3.png?raw=true "segmentedimages") 
# ![validationset4](validationset4.png?raw=true "segmentedimages") 
# ![tvloss](tvloss.png?raw=true "trainingvalidationloss") 
# ![tvIoU](tvIoU.png?raw=true "trainingvalidationIoU") 
