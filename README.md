# EDA_for_hate_speech
Abstract - Using textual data augmentation in NLP, to improve deep learning model performance on an imbalanced hate speech dataset. Tools used Python, Keras, Scikit-learn &amp; Tensorflow. 

Quick links
* [*Running the code*](https://github.com/ethanbakare/EDA_for_hate_speech#running-the-code)

* [Dataset Used](https://github.com/ethanbakare/EDA_for_hate_speech#dataset-used)

* [*Data Augmentation Method Used*](https://github.com/ethanbakare/EDA_for_hate_speech#data-augmentation-method-used)

* [*Running the code*](https://github.com/ethanbakare/EDA_for_hate_speech#running-the-code)

* [*Running the code*](https://github.com/ethanbakare/EDA_for_hate_speech#running-the-code)


#### Key Terms
Data imbalance:
> When classes in a dataset are highly unequally represented with one class being greater than other or others by a wide margin.

Data Augmentation:
> Entails using available data to create additional synthetic data samples.


#### Problem
With an imbalanced dataset involving a classification task, where the minority class is essential to the problem being tackled. Abstractions learnt by the classification algorithm are skewed towards the majority class, so performance is poorer in the underrepresented class. As consequence the key performance metric is poor(the minority class)
#### //////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
## Dataset Used:
The dataset chosen for this task is the hatebase dataset [Davidson et al. 2017](https://arxiv.org/abs/1703.04009) this imbalanced dataset was annotated by crowd flower from a random sample 25,000 tweets. It consists of three classes

* **Hate - 0**
* **Offensive - 1**
* **Neither - 2**

<img src="https://github.com/ethanbakare/EDA_for_hate_speech/blob/master/images/data%20set.png" width = "300"/>



## Data Augmentation Method Used:
Easy Data Augmentation are a group of 4 *simple data augmentation* techniques that are easy to implement created by [Jason Wei](https://arxiv.org/pdf/1901.11196.pdf). Listed as follows:

**Synonym Replacement (SR):** Goes through each sentence, selects a number of words “n”  (not stop words) at random Replaces each selected word with one of its own random synonyms.

**Random Swap (RS):** It iterates through each sentence selecting two words randomly and swapping their positions, this is done “n” times.

**Random Deletion (RD):** It goes through each sentence in the corpus, with a probability “p” each word in the sentence is removed or not based based on “p”.

**Random Insertion (RI):** Goes through each sentence, selecting a number of words “n” (not stop words) at random and adding a synonym of each selected word at random positions in the sentence.


<img src="https://github.com/ethanbakare/EDA_for_hate_speech/blob/master/images/EDA_tech.png" height="400"/>


## Model Pipeline:
The LSTM model architecture consist of 6 layers: 
1 embedding layer, 1 spatial drop out layer, a 128 neuron LSTM layer with input dropout and recurrent drop out, and 1 dense layer with relu activation function, 1 dropout layer and an output dense layer with a soft max function.

<img src="https://github.com/ethanbakare/EDA_for_hate_speech/blob/master/images/model_pipeline.png" width height="420"/>



#### //////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

# Running the code.

To run the code make sure you have the following :

Install NLTK

Download Wordnet

**Please note:** SR = Synonym Replacement, RS = Random Swap, RD = Random Deletion, RI = Random Insertion

After which proceed to 
### Download the .ipynb file titled  '000_DA_HS' & dataset folder
Download the .ipynb file titled 000_DA_HS.ipynb as well as the dataset folder which contains the test, val, train, and train augmented files


### Open the 000_DA_HS.ipynb 
Open 000_DA_HS.ipynb proceed to the second block of code to change the address for the test, validation and (train data - choose sample of choice) 

The source test, validation and train data are titled:

 Test = **test_data_hs**    |   Train = **train_data_hs**   |    Validation = **val_data_hs**

### Run the 000_DA_HS.ipynb code file
Click run till you reach the code block for training and observe the results. To run a different dataset all you do is change the address for the train data on the second line in the code



# Running code with Augmented datasets?
There are 15 concatenated combinations made on on the four EDA techniques, with these techniques, as such we have 15 augmented training dataset. They are grouped by number of augmentations performed each seperated with a comma(,). They are listed as follows

<img src="https://github.com/ethanbakare/EDA_for_hate_speech/blob/master/images/data_creation.png" width height="300"/>

### Single Augmentation
SR, RS, RD, RI

### Double Augmentation
SR_RS, SR_RD, SR_RI, RS_RD, RS_RI, RD_RI

### Three or more Augmentation
SR_RS_RD, SR_RS_RI, SR_RI_RD, RI_RS_RD, SR_RS_RD_RI

//////////////////////////////////////////////////////

**Please note:** each augmented train data has the term "train_hs" before its corresponding name

//////////////////////////////////////////////////////



## Results Obtained:
Comparing the results obtained using the baseline and augmented datasets using a variety of performance metrics


<img src="https://github.com/ethanbakare/EDA_for_hate_speech/blob/master/images/we23.png" height="700">


Figure 1: F1 Score Single Augmentation 
<img src="https://github.com/ethanbakare/EDA_for_hate_speech/blob/master/images/1STY.png" width="400">
Figure 2: F1 Score Double Augmentation 
<img src="https://github.com/ethanbakare/EDA_for_hate_speech/blob/master/images/2STY.png" width="400">
Figure 3: F1 Score Third or more Augmentation 
<img src="https://github.com/ethanbakare/EDA_for_hate_speech/blob/master/images/3STY.png" width="400">





