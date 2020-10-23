# Deepfake-Detection
This code is an ensembled model of ResNext and Exception Net, submitted to Deepfake Detection Challenge in Kaggle conducted by Facebook

# Methods
1. Blaze Face was applied for face detection.
2. Simple Binary Classifier is used for the Classification of Real and Fake Videos.
3. DFDC datset was used for training the model.
4. RESNEXT and Exception Net were used for classification.

# Parameters
I've tried various learning rates lr (0.001, 0.0015, 0.002, 0.004), epochs (10, 12, 20, 42), patience (2, 5, 7) and factor (0.1, 0.2, 0.5, 0.7). The result from these is the score of 0.50480 for the Xception single model, and 0.43846 for the Resnext + Xception esemble. Further tweeking of these parameters do help increase the public LB score by a bit. Also, yet interestingly, as the score of the single model Xception decreases, the higher scoring esembles have equal weights, i.e. 0.5 for Resnext and 0.5 for Xception. Feel free to tweek these parameters further. Since it may take a long time to train depending on your hardware, plan to tweak parameters properly based on the insights gathered from past trainings.

# Results
Results are cross entropy loss for Real and Fake:

1. Resnext single model public score: 0.46441
2. Xception single model public score: 0.50480
3. Inference Model Score: 0.4306
