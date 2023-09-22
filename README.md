<!-- hide -->
# SVM - Step by step guide
<!-- endhide -->

- Understanding a new dataset.
- Model the data using an SVM.
- Analyze the results and optimize the model.

## 🌱  How to start this project

Follow the instructions below:

1. Create a new repository based on [machine learning project](https://github.com/4GeeksAcademy/machine-learning-python-template/generate) by [clicking here](https://github.com/4GeeksAcademy/machine-learning-python-template).
2. Open the newly created repository in Codespace using the [Codespace button extension](https://docs.github.com/en/codespaces/developing-in-codespaces/creating-a-codespace-for-a-repository#creating-a-codespace-for-a-repository).
3. Once the Codespace VSCode has finished opening, start your project by following the instructions below.

## 🚛 How to deliver this project

Once you have finished solving the exercises, be sure to commit your changes, push to your repository and go to 4Geeks.com to upload the repository link.

## 📝 Instructions

### Spam link detection system

We want to implement a system that is able to automatically detect whether a web page contains spam or not based on its URL.

#### Step 1: Loading the dataset

The dataset can be found in this project folder under the name `url_spam.csv`. You can load it into the code directly from the link (`https://raw.githubusercontent.com/4GeeksAcademy/NLP-project-tutorial/main/url_spam.csv`) or download it and add it by hand in your repository.

#### Step 2: Preprocess the links

Use what we have seen in this module to transform the data to make it compatible with the model we want to train. Segment the URLs into parts according to their punctuation marks, remove stopwords, lemmatize, and so on.

Make sure to conveniently split the dataset into `train` and `test` as we have seen in previous lessons.

#### Step 3: Build an SVM

Start solving the problem by implementing an SVM with the default parameters. Train it and analyze its results.

#### Step 4: Optimize the previous model

After training the SVM, optimize its hyperparameters using a grid search or a random search.

#### Step 5: Save the model

Store the model in the corresponding folder.

> NOTE: Solution: https://github.com/4GeeksAcademy/NLP-project-tutorial/blob/main/solution.ipynb