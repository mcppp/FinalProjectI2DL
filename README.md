#FinalProjectI2DL

This repository includes two projects with the same goal: sentiment analysis. The project based on AUDIO uses the dataset RAVDESS and the project based on IMAGE uses the dataset FER-2013. Both datasets are available to download from Kaggle.

FER-2013 https://www.kaggle.com/msambare/fer2013
RAVDESS emotional speech audio https://www.kaggle.com/uwrfkaggler/ravdess-emotional-speech-audio


AUDIO PROJECT (done in Google Colab)


A) Feature extraction:

- RAVDESS dataset of emotional speech is available to download from Kaggle
- The notebook Extract_features.npy extracts the audio features from the speech samples from RAVDESS (if you use it, make sure the paths are adapted to your environment)
- The features are already extracted and are available in the respository. You can load them directly and use them as a dataset: feature_matrix.npy contains features, labels.npy contains the labels.


B) Running the model:The notebook is adapted to be used in Google colab. Comment the lines regarding Google colab out if you don't want to use it. Either way, make sure all the paths are correct. 


Recommended
   1. Download AUDIO_simple.npy , feature_matrix.npy and labels.npy. 
      (Alternatively you can download the RAVDESS dataset from Kaggle and use Extract_features.npy to create your own feature_matrix.npy and labels.npy. Make sure the downloaded dataset contains only 24 folders for the 24 actors, please delete any extra folders)
  
   2. Run AUDIO_simple.npy : it loads the feature_matrix.npy and labels.npy, trains the model and reports performance by showing accuracy and confussion matrix based on the    unseen test set. Training is fast. 



Alternative
- The model has already been trained. You can download the audio_best.pth file from the following link and load it for classification: https://drive.google.com/file/d/1oRFs0qc0-0ocn6fOxNGwFde0KBja43KV/view?usp=sharing. Run AUDIO_simple.npy but comment cell #14 out to deactivate training, and uncomment cell #16 to load the trained weights. Make sure the paths are correct. 

***************************************************************************************************************************************************************************


IMAGE PROJECT 

This project has been done using the Google Cloud, since Google Colab is too slow. The training has been done in the Google Cloud and the live testing has been done locally in order to use the laptop camera.



A) Running the model

    Recommended (without training)
    - Download FER-2013 dataset. Make sure the paths in the notebook IMAGE_project.npy are correct before you run. 
    - Training is time-consuming. 
      I recommend loading the saved face_11.pth and running the model to see confussion matrix and accuracy results based on the test set. 
      You can download the .pth file in : https://drive.google.com/file/d/1-p0U14Yj0q3GMCdrkw7O5gYDDctLUajw/view?usp=sharing
      Make sure the path in cell #18 is correct -> now you can run the notebook


    Alternative (training it yourself)
      - If you want to train the model yourself, uncomment cell #17 and comment cell #18 out . Now you can run the notebook. 
        You can stop the training after any validation round. 
        If you stop it between train and validation rounds, the code that prints validation vs. training accuracy curve will not work.



B) Live testing
- For live testing, run locally LIVEtesting.npy on your computer (to provide access to the laptop's camera). Make sure the path to load the face_11.pth file is correct. You can download the .pth file same way as above in: https://drive.google.com/file/d/1-p0U14Yj0q3GMCdrkw7O5gYDDctLUajw/view?usp=sharing



