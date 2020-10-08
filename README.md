# EDA_for_hate_speech
Using textual data augmentation in NLP, to explore deep learning model performance on an imbalanced hate speech dataset. Tools used Python, Keras, Scikit-learn &amp; Tensorflow. 











### Please note:
HS = Hate speech, SR = Synonym Replacement, RS = Random Swap, RD = Random Deletion, RI = Random Insertion, DA = Data

#### ///////////////////////////////////////////////////////////////////////////////

# Running the code.

To run the code make sure you have the following :

Install NLTK :

Download Wordnet

After which proceed to 
### Download the .ipynb file titled  000_DA_HS 
Download the .ipynb file titled 000_DA_HS.ipynb


### Download the dataset folder
Download the dataset folder which contains the test, val, train, and train augmeneted files


### Open the 000_DA_HS.ipynb 
Open 000_DA_HS.ipynb proceed to the second block of code to change the address for the test, validation and (train data - choose smaple of choice) 
The source test, validation and train data are titled:

#### Test = test_data_hs

#### Train = train_data_hs

#### Validation = val_data_hs

### Run the 000_DA_HS.ipynb code file
Click run till you reach the code block for training and observe the results. To run a differnt dataset all you do id change the address for the train data on the second line in the code



# Running code with Augmented datasets?
There are 15 concatenated combinations made on on the four EDA techniques, with these techniques, as such we have 15 augmented training dataset. They are grouped by number of augmentations performed each seperated with a comma(,). They are listed as follows

### Single Augmentation
SR, RS, RD, RI

### Double Augmentation
SR_RS, SR_RD, SR_RI, RS_RD, RS_RI, RD_RI

### Three or more Augmentation
SR_RS_RD, SR_RS_RI, SR_RI_RD, RI_RS_RD, SR_RS_RD_RI


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

### Please note each augmented train data has the term "train_hs" before its corresponding name

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
