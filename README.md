ud120-projects
==============

Starter project code for students taking Udacity ud120
### Machine Learning mini project - Naive Bayes

A couple of years ago, J.K. Rowling (of Harry Potter fame) tried something interesting. She wrote a book, “The Cuckoo’s Calling,” under the name Robert Galbraith. The book received some good reviews, but no one paid much attention to it--until an anonymous tipster on Twitter said it was J.K. Rowling. The London Sunday Times enlisted two experts to compare the linguistic patterns of “Cuckoo” to Rowling’s “The Casual Vacancy,” as well as to books by several other authors. After the results of their analysis pointed strongly toward Rowling as the author, the Times directly asked the publisher if they were the same person, and the publisher confirmed. The book exploded in popularity overnight.

We’ll do something very similar in this project. We have a set of emails, half of which were written by one person and the other half by another person at the same company . Our objective is to classify the emails as written by one person or the other based only on the text of the email. We will start with Naive Bayes in this mini-project, and then expand in later projects to other algorithms.

We will start by giving you a list of strings. Each string is the text of an email, which has undergone some basic preprocessing; we will then provide the code to split the dataset into training and testing sets. (In the next lessons you’ll learn how to do this preprocessing and splitting yourself, but for now we’ll give the code to you).

One particular feature of Naive Bayes is that it’s a good algorithm for working with text classification. When dealing with text, it’s very common to treat each unique word as a feature, and since the typical person’s vocabulary is many thousands of words, this makes for a large number of features. The relative simplicity of the algorithm and the independent features assumption of Naive Bayes make it a strong performer for classifying texts. In this mini-project, you will download and install sklearn on your computer and use Naive Bayes to classify emails by author.

#### Getting your codes set up
Check that you have a working python installation, preferably version 2.6 or 2.7 (that’s the version that we use--other versions may work, but we can’t guarantee it). If you're using Python 3, you may find some more extensive revision of code to get things working at this time, so you may want to set up a Python 2 environment to work through the course materials.

We will use pip to install some packages. First get and install pip from here. Using pip, install a bunch of python packages:

go to your terminal line (don’t open python, just the command prompt)
install sklearn: pip install scikit-learn
-- for your reference, here’s the sklearn installation instructions
install natural language toolkit: pip install nltk
Get the Intro to Machine Learning source code. You will need git to clone the repository: git clone https://github.com/udacity/ud120-projects.git
You only have to do this once, the code base contains the starter code for all the mini-projects. Go into the tools/ directory, and run startup.py. It will first check for the python modules, then download and unzip a large dataset that we will use heavily later. The download/unzipping can take a while, but you don’t have to wait for it to finish in order to get started on Part 1.

#### Timing your NB classifier
An important topic that we didn’t explicitly talk about is the time to train and test our algorithms. Put in two lines of code, above and below the line fitting your classifier, like this:

t0 = time()
< your clf.fit() line of code >
print "training time:", round(time()-t0, 3), "s"


Put similar lines of code around the clf.predict() line of code, so you can compare the time to train the classifier and to make predictions with it. What is faster, training or prediction?

We will compare the Naive Bayes timing to a couple other algorithms, so note down the speed and accuracy you get and we’ll revisit this in the next mini-project.
