# classification-of-cognitive-states-using-eeg-data

## Dataset
https://physionet.org/content/eegmat/1.0.0/

## Result
![image](https://github.com/praveen-019/classification-of-cognitive-states-using-eeg-data/assets/72589374/26610554-ba02-496b-930b-707766497c39)

## Approach-1: classification using logistic regression
### Brief Description (in-depth explination is included with code in jupyter notebook)
step-1: downloaded and loaded the data using glob

step-2: extracted the data using mne and created labels

step-3: extracted 12 statistical features from the data

step-4: based on concatenated features logistic regression is applied and 62.6% accuracy is achieved

## Approach-2: classification using custom CNN
### Brief Description (in-depth explination is included with code in jupyter notebook)
step-1: downloaded and loaded the data using glob

step-2: extracted the data and features using mne and created labels

step-3: reshaped the data that would fit cnn and scaled the data before applying k folds cross validation for more accuracy

step-4: constructed the custom cnn with 5 convolution layers and with sigmoid activation function for last layer

step-5: after trainning the CNN model 70.8% accuracy is achieved

## Approach-3: classification using chrononet (CNN + GRU)
### Brief Description (in-depth explination is included with code in jupyter notebook)
step-1: downloaded and loaded the data using glob

step-2: extracted the data and features using mne and created labels

step-3: reshaped the data that would fit cnn and scaled the data before training

step-4: constructed the custom model using keras, tensorflow as shown in the following image

![image](https://github.com/praveen-019/classification-of-cognitive-states-using-eeg-data/assets/72589374/4eca5c80-ea63-42e8-9595-6bd002965713)

which was proposed in a paper named: ChronoNet: A Deep Recurrent Neural Network for Abnormal EEG Identification in 2018.

Link: https://arxiv.org/pdf/1802.00308

step-5: trained the model and applied k fold cross validation and achieved 89.6% accuracy

## Approach-4: classification using EEGNET
### Brief Description (in-depth explination is included with code in jupyter notebook)
step-1: downloaded and loaded the data using glob extracted the data using mne 

step-2: extracted the features using psd analysis of frequency bands (delta, theta, alpha, beta, gamma) using welch

step-3: reshaped the data that would fit eegnet and scaled the data before training

step-4: constructed the EEGNET model using keras, tensorflow and with sigmoid activation function for last layer

step-5: after trainning the CNN model 60.8% accuracy is achieved
