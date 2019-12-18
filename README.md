<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# Voice Gender Recognition using Machine Learning
*Alieldin Ramadan*

*Data Analytics, Barcelona, October 2019*

## Content
- [Project Description](#project-description)
- [Hypotheses / Questions](#hypotheses-questions)
- [Dataset](#dataset)
- [Cleaning](#cleaning)
- [Analysis](#analysis)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [Workflow](#workflow)
- [Organization](#organization)
- [Links](#links)

## Project Description
In this project the main objective was to train and test different machine learning models to be able to identify whether the speaker is a male or a female based on different features that were extracted from the voices, such as:
Mean_freq: Mean frequency (in kHz).
Mode_freq: Mode frequency (in kHz).
First_quartile: First quartile frequency (in kHz).
Kurtosis: kurtosis, a measure used to describe the distribution.
Centroid_freq: Centroid frequency (in kHz), a measure that indicates where the center of mass of the spectrum is located frequency.
Spectral_flatness_measure: Spectral flatness, provides a way to quantify how a sound is tone-like, as opposed to being noise-like.
Mean_fundamental_freq: Mean fundamental frequency (in kHz), the lowest frequency of a periodic waveform (Pitch of a voice).
Mean_MFCCs: Mean of Mel-frequency cepstral coefficients.
Std_MFCCs: Standerd deviation of Mel-frequency cepstral coefficients.
Max_MFCCs' : Maximum Mel-frequency cepstral coefficients.
Mean_Magnitude: Mean magnitude. 
Min_RMS: Minimum root mean square error.
Std_RMS: Standard deviation of the root mean square error.



## Hypotheses / Questions
* Can we identify gender based on acoustic properties/features of the speaker?
* What are the highly correlated acoustic properties/features to gender?
* What are the main indecators to determine whether a voice is a male's of a female's?

## Dataset
[voices.csv dataset - Kaggle.com](https://www.kaggle.com/primaryobjects/voicegender)

This was supposed to be the main dataset used to train and test the Machine learning models, but ended up not using it as I wasn't able to extract some of the features and the accuracy was low when testing it using other audio files. So I ended up creating a new dataset using the audio files downloaded from (Open Speech and Language Resources).

[Open Speech and Language Resources](http://www.openslr.org/45/)

## Cleaning
- For the voices.csv from Kaggle, the dataset was clean, just changed the gender column from categorical to numerical.
- For the other three datasets, they were created manually by extracting acoustic properties/features from Audio files, so it was clean as well.

## Analysis
* If you used Machine Learning in your final project, describe your feature selection process.

## Model Training and Evaluation
* Description is in the [Workflow](#workflow).

## Conclusion
* After using different machine learning models to identify gender, the best accuracy that was achieved using the neural network model with accuracy of 92% for the audio files from the same source and an accuracy of 81.8 % for the recorded audio files.

* The highly correlated acoustic properties/features to gender are:
1) Mean of Mel-frequency cepstral coefficients
2) First quartile frequency (in kHz)
3) Maximum Mel-frequency cepstral coefficients

## Future Work
- Including more Audio files from more people to increase the accuracy of the model.
- Records of children voices can be added and processed (Male, Female or child).
- Speaker recognition.

## Workflow
The first intention was to work on the kaggle dataset and build a model that can identify gender and then test the accuracy of the model on recorded audio files. After cleaning the data and taining and fitting the models, the next step was to extract the same features from the recorded Audio files and test the accuracy of the models. It was difficult to extract the same features and when testing the accuracy of the model on the recorded audios, the accuracy was low.

Downloaded a zipped file from *Open Speech and Language Resources* with 3843 audio files from 10 speakers, 5 females and 5 males. Separated 50 files out of the 3843 files, so I can use later for testing and used the other 3793 to create a new dataset with the features that I was successful in extracting.

Then the newly created dataset was used to train and fit different models for accuracy. After getting some models with high accuracy the next step was to test the other 50 voices from the same zipped file, the results were good and the accuracy was high.

To test the model further, I recorded the voices of 22 speakers, 11 females and 11 males (Friends and from TedX talks), processed the audio files and created a new dataframe with the extracted features, the highest accuracy that I got was 81% by using the Neural Network.
the model is saved in the (*saved_models* folder, with the name *voices_new_recorded.model*.

## Organization
Used Trello to keep track of the tasks done and those that were pending.

### Inside the repository there is a folder called 'Voice Gender Recognition using Machine Learning' in which there are three folders:
#### code:
- *Audio processing - New Voices.ipynb - This file has the code used to process and extract the features from the new Audio files downloaded from (Open Speech and Language Resources).*
- *Audio processing - Recorded voices.ipynb - This file has the code used to process and extract the features from the Audio files I recorded to test the accuracy of the models.*
- *Audio processing - To Test.ipynb - This file has the code used to process and extract the features from some audio files that I separated from the Audio files downloaded from (Open Speech and Language Resources), so I can test the accuracy of the model on these files as well.*
- *Voice Gender Recognition using Machine Learning - For the new voices Dataset.ipynb - This file has the code used to see the correlation between the features and the Gender and the training and testing of different models on the new voices datasets and at the end testing the accuracy of the models on the Audio files that were separated from the (Open Speech and Language Resources) Audio files.*
- *Voice Gender Recognition using Machine Learning - For the recorded voices.ipynb - This file has the code used to see the correlation between the features and the Gender and the training and testing of different models on the new voices datasets and at the end testing the accuracy of the models on the Audio files that I recorded*
- *Voice Gender Recognition using Machine Learning - Kaggle Voices Dataset.ipynb - This file has the code used to clean, analyze and creat, train and test models on the Voices dataset from Kaggle (These analysis were not helpful as the dataset was processed using R).*

#### datasets:
- *This folder contains four CSVs dataset:*
- - 1- voices.csv                   ---->  The dataset downloaded from Kaggle.com
- - 2- new_voices.csv               ---->  The dataset of the features extracted from the Audio files downloaded from (Open Speech and Language Resources)
- - 3- voices_to_test.csv           ---->  The dataset of the features extracted from the 50 audio files separated from (Open Speech and Language Resources) audiofiles.
- - 4- recorded_voices.csv          ---->  The dataset of the features extracted from the audio files I recorded.

#### saved_models:
- *This folder contains the deep learning models saved from the code.*

#### audio_to_test:
- *It was a folder that contained the audio files that I used for creating the new voices dataset and the audio files used to create the datasets to test the accuracy of the model whether the recorded or the separated. (The audio files were deleted due to the size, the link for the downloaded Audio files is [Open Speech and Language Resources](http://www.openslr.org/45/))*


## Links

[Repository](https://github.com/alieldinramadan/Project-Week-8-Final-Project)  
[Slides](https://docs.google.com/presentation/d/1FOXif4Rt3PdMC8ju35J6V7yDKksEyFi0MLDijOav8KE/edit?usp=sharing)  
[Trello](https://trello.com/b/A73tKFUM/project-5)  
