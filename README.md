<!-- hide -->
# NLP Project Tutorial
<!-- endhide -->

- In our last exploring NLP notebook we built an email spam detector using Natural Language Processing techniques and the Support Vector Machine (SVM) algorithm for classification.

- In this project, we will again build a spam detector but this time using URLs instead of emails. 

## 🌱  How to start this project

You will not be forking this time, please take some time to read this instructions:

1. Create a new repository based on [machine learning project](https://github.com/4GeeksAcademy/machine-learning-python-template/generate) by [clicking here](https://github.com/4GeeksAcademy/machine-learning-python-template).
2. Open the recently created repostiroy on Gitpod by using the [Gitpod button extension](https://www.gitpod.io/docs/browser-extension/).
3. Once Gitpod VSCode has finished opening you start your project following the Instructions below.

## 🚛 How to deliver this project

Once you are finished creating your URL spam detector, make sure to commit your changes, push to your repository and go to 4Geeks.com to upload the repository link.


## 📝 Instructions

**URL Spam detector**

We will use a URL dataset which you can find in the following link https://raw.githubusercontent.com/4GeeksAcademy/NLP-project-tutorial/main/url_spam.csv

**Step 1:**

 Load your dataset and do the necessary transformations on your target variable.

**Step 2:**

Do the necessary NLP cleaning process. Exclude the stop words, you may add words like 'com', 'http', etc to your list.
Here is another idea on how to exclude some words by creating new columns:

```py
df['len_url'] = df['url'].apply(lambda x : len(x))
df['contains_subscribe'] = df['url'].apply(lambda x : 1 if "subscribe" in x else 0)
df['contains_hash'] = df['url'].apply(lambda x : 1 if "#" in x else 0)
df['num_digits'] = df['url'].apply(lambda x : len("".join(_ for _ in x if _.isdigit())) )
df['non_https'] = df['url'].apply(lambda x : 1 if "https" in x else 0)
df['num_words'] = df['url'].apply(lambda x : len(x.split("/")))

target = 'is_spam'
features = [f for f in df.columns if f not in ["url", target]]
X_train, X_test, y_train, y_test = train_test_split(df[features], df[target], test_size=0.2, random_state=0)
```

**Step 3:**

Use Support Vector machine to build a url spam classifier.

**Step 4:**

As always, use your notebook to experiment and make sure you are getting the results you want. 

Use you app.py file to save your defined steps, pipelines or functions in order. 

In your README file write a brief summary.

Solution guide: 

https://github.com/4GeeksAcademy/NLP-project-tutorial/blob/main/solution_guide.ipynb
