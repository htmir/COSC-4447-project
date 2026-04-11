# COSC-4447-project
COSC Group 23 semester project

To run the code:

First open up the .pynb in Google Colab and connect to a GPU runtime for faster processing.
Next we must download the dataset into Colab first by uploading a Kaggle API key as a .json.
Generate a legacy key on Kaggle website under accounts.

Then run:

#Download and unzip dataset from kaggle into Colab's SSD

!pip install -q kaggle

!kaggle datasets download -d paultimothymooney/kermany2018 -p /content

!unzip -oq /content/kermany2018.zip -d /content

Run the block to verify all samples are present, should total to 84484.

Run all blocks in subsequent order except for the training loop, a set of optimized parameters is provided in the repo.

Then upload the paramter file, eyenet_optim_parameters, and load the model onto GPU.

Evaluate the CNN classfier on the test and validation sets.

Then, collect flattened feature vectors of train, test, and validation samples using the feature extraction function from the EyeNet class.

Finally put the model in eval mode and classify test samples using SVM and KNN.
