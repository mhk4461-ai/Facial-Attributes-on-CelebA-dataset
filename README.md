# Facial-Attributes-on-CelebA-dataset
ResNet/MobileNetV2 CNN Hybrid model to analyze Attributes in CelebA Dataset
Quick summary:

I have chosen the CelebA dataset from Kaggle (more details in code below). The objective of the model I am making is to accurately predict image attributes for a given image in the dataset. The attributes I have chosen are "Smiling", "Sunglasses", "Blond Hair", "Young", and "Male".

The Model I have chosen is inspired by ResNet and is similar to a MobileNetV2 CNN. It is similar to these two because it uses inverted bottlenecks and residucal connections. The main distinction between my model and these two is that mine utilizes Grouped Convolutions, instead of depthwise separable (like in MobileNetV2) and standard (as in ResNet).

To train this model, I used BCELogitsLoss as my loss function. This is similar to Cross Entropy, but is used for multi-label classification. Cross Entropy cannot be used for multi-label classifications. Then, I used an SGD optimizer, as we have a larger dataset. This model takes a while to train. When running training and logging loss per epoch, this section of code will take about 25-30 minutes.
