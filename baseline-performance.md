Contributors: Guilherme Vilatoro Taglianeti, Hwa-Lyang Sugihara 

In this project, we are using Unet to train our model to predict accurate segmented images of satellite photos. 

There are six classes with which each satellite photo can be annotated that includes Buildings, Land, Road, Vegetation, Water, and Unlabeled. Each class has their own visual representaton on the photo with a unique color overlay. Each image in the training and validation sets is cropped to reformat them into patches of 256x256x3.  This model is fed 72 pictures from the training set that are already populated with the color overlay. After using Unet to generate the model, we tested the model against the validation set. 

Validation loss indicates how well the model fits new data while training loss indicates how well the model fits the training data. 

In our first attempt at the model, the satellite image, the training label, and the model-generated segmented image did not match up to each other as a result of incorrect file sorting. In our training and validation loss graph, the validation loss became significantly greater than the training loss indicating that our model was underfitting the images. In our training and validation IoU graph, the validation IoU had a low value hovering around .21 also indicating that the model does not accurately predict the new test images. We fixed the path of the images using images.sort after listing all the images in the subdirectory and were able to get more accurate results in our last attempt.

Our last attempt is shown in the images and graphs below. The 10 sample predicted segmented images produced by the model are very similar to the training label associated with it.

In our training and validation loss graph, the decreasing trend demonstrated by the graph shows that the model for both the training and validation set is producing less errors as it processes more epochs. The validation loss is slightly greater than the training loss after around 20 epochs and stays stagnant. A greater validation loss than training loss indicates that the model is underfitting the images. This is may be due to the lack of new training data from the repetition of the training set images in the epochs. In the training and validation IoU graph, both the training and validation IoU increase indicating that the model prediction for both the training set and the validation set is becoming more accurate at predicting the classes that are supposed to overlay the image to look like the training label.

In the following precision recall graph, the precision and recall values are in an inverse relationship. Precision is measured by how many class predictions are good out of all the classes put over the prediction image. Recall is measured by whether the class was correctly identified when it was supposed to be over the prediction image.

# ![validationset1](val1.png?raw=true "segmentedimages") 
# ![validationset2](val2.png?raw=true "segmentedimages") 
# ![validationset3](val3.png?raw=true "segmentedimages") 
# ![validationset4](val4.png?raw=true "segmentedimages") 
# ![tvgraphs](tvgraphs.png?raw=true "trainingvalidationgraphs") 
# ![precisionrecall](pr.png?raw=true "precisionrecall") 
