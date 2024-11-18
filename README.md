# Meesho_Data_Challenge

To install the required dependencies, use the following command:

pip install numpy==1.26.4 pandas==2.2.3 tensorflow==2.16.1 tqdm==4.66.4 matplotlib==3.7.5 scikit-learn==1.2.2

How to run training code :
1. There are three model training files : EfficientNetV2S, Xception, InceptionResnetV2.
2. You need to define image directory and train.csv paths, at the start of the code indicated by the comment.
3. Run the codes, and download the models and encoders files it creates, it is suggested to train 1 category at a time by commenting out the other categories in the CATEGORY_ATTRIBUTES.
   
For directly using the prediction part of code :
1. You need to define test image directory and test.csv paths, at the start of the code indicated by the comment.
2. The models are saved at "https://drive.google.com/drive/folders/1Ns17cJCJGXbyW_7zIFmN-7-AtUJzSZOG?usp=drive_link"
3. The folder contains model files for each of the 5 category (Men Tshirts, Sarees, Kurtis, Women Tshirts, Women Tops & Tunics) in the 3 model (EfficientNetV2S, Xception, InceptionResnetV2) files.
4. Specify the paths correctly in the Prediction_ensemble code for each model and encoder for each category after downloading the model files.
5. Run the code, and it should generate a Submission.csv file.

Note: Single model prediction can also be tested, eg : Use Prediction_EfficientNet code file and update the paths with the model paths for it and run it to get the submission file only based on the EfficientNetV2S model.
