---
layout: post
title: AI in Finance
subtitle: Introduction to some concept and uses cases of AI in Finance
tags: [DataScience,Finance]
comments: true
---

{: .box-note}
**Note:** This is an article I wrote for my company to illustrate some use cases of machine learning in finance. 

## Artificial Intelligence in Finance

Artificial Intelligence and more specifically machine learning is transforming several industries. Without going into too much detail, Machine Learning is a subset of data science. They are algorithms that observe, manipulate and transform data in order to make predictions. Unlike traditional programming, there is no need to precisely define all the steps between incoming and outgoing data. We implement a learning model that adjusts by iterating on a large number of cases.
In many cases, the quality of the result will depend on the amount of data available to drive the model.

Now let's review some examples of applications in the financial world (banking, insurance and investment):

### Automation

It's possible to extract essential data from documents or to have a program that can interact in natural language with a client via the combination of a language model and a natural language processing algorithm. A language model is a model that predicts the next word in a sentence based on the previous words. It's often trained on a very large number of documents, for example OpenAI (https://openai.com/blog/better-language-models/) trained their model with 8 million web pages. Afterwards, you can teach the model the specific features of a certain type of document (legal documents, for example) using a technique called Transfer Learning.

Examples:
- Automate time-consuming tasks for a human such as:
    - Categorize documents according to their content
    - Summarize a document automatically to read it more quickly
    - Find specific information (financial or other data)

- Answer simple customer questions more quickly using conversational agent (ChatBot):
    - Helps guide clients to the desired information through a natural language conversation
    - Enables the customer to make transactions on the account without having to contact a call center

### Security/Compliance

The multitude of information accessible by banking institutions makes it quite simple to implement a machine learning algorithm to detect if a transaction is fraudulent. The model is trained with a data set that includes many parameters (information on transactions, connection habits, customer path on a website, etc...) and is given the answer for each case (fraudulent transaction or normal transaction). The model will eventually find relationships between all available parameters and a fraudulent transaction. Then, we can apply this model to real-time transactions and it will predict if a transaction is fraudulent (in order to block it) or if it is normal. This is called Supervised Learning because we train the model with labelled data (in this case the label is fraudulent or normal).

Examples:
- Detect fraud in real time
    - Fraudulent transactions
    - Fraudulent connections
- Anti-money laundering
    - Identify suspicious behaviours using transaction history

### Insurance/Credit

Such algorithms can also be used to model credit risk.  By using data from a company (financial reports and other documents) as parameters, we can predict a default probability that can help risk analysts to produce their ratings.

Examples :
- Support investment rating for private markets
- Suggest credit ratings and pricing in a more sophisticated and complex way than traditional tools based on a number of predefined rules
- Allows you to make a decision on whether or not to grant a loan in a few seconds

### Trading/Risk/Valuation

Different approaches can be used to predict market movements. These algorithms are capable of continuous improvement with what is called Reinforcement Learning. This implies that unlike a traditional statistical model, if the market changes, the model will adapt itself and the predictions will remain relevant.

Examples:
- Predict stock prices through different types of analysis
    - Fundamental Analysis (based on the study of financial statements)
    - Quantitative Analysis (based on probabilistic models)
    - Technical Analysis (based on price history)
    - Analysis based on external data (based on twitter, news, etc...)
- Markovian Decision-Making Process (MDP) for the Evaluation of Options

### Conclusion

There are many use cases in various sectors of finance. Artificial intelligence can be an asset in supporting growth, reducing operational risks and building on the mountains of data historized by financial institutions. 
The important thing is to identify the problems you want to solve and make sure that the required data are available.
