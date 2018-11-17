# pneumonia_detection
Code used in Kaggle Pneumonia Detection competition

The notebooks here contain code I used for the Kaggle Pneumonia Detection challenge. I used segmentation to detect the locations within
the chest x-rays that contained features which looked like pneumonia. 

The deep learning model used here is the Hourglass model, which I'd previously used for pose estimation. I created a mask for the pneumonia
detections and another mask for the negative labels and used a simple squared error between the masks and the network output to 
train the network.

For inference, I used the connected components algorithm from opencv library and pixel thresholds to get the bounding box parameters. I also
used an ensemble method to combine the output of two models to get the best results. The method to generate the models is written in the
pneumonia_detection_v3 notebook. The ensemble method is mentioned in the pneumonia_infer_v3 notebook.

Code written in: Tensorflow
Train and test data from: https://www.kaggle.com/c/rsna-pneumonia-detection-challenge

