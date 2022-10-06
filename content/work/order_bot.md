+++
title = "Shopee Order Bot"
[extra]
labels = ["Data Driven", "UX Writing"]
image = "https://avatars.githubusercontent.com/u/583231"
summary = """Shopee Chatbot is an assistant bot in the Shopee e-commerce app, to answer users’ questions before they decide to access the live agent service.

In this project we reviewed the UX of a core task bot and raised solution rate by 3.71%.
"""
+++

# Chatbot Order Selection Revamp

<p class="time">@Shopee, 2022</p>

<span class="intro">
  <span>

  ## Background

  Shopee Chatbot serves 250k users per day in 8+ regions, answering all customer inquiries about orders, logistics, post-sale service, and so on. Chatbot saves an excellent amount of the cost for customer service.

  In this project, we aimed to bring down the **drop rate, transfer to live agent rate** and raise the **resolution rate** and **CSAT** of Order Selection flow.</td>
  </span>
  <span>

  ## My Role

  Research:

  * Journey mapping, Data analysis, User testing

  Design:

  * UI/UX design, UX writing</td>
  </span>
</span>




## Choose a Research Method

Chatbot is characterised by a large amount of data and small amount of information per piece of data. It’s a product team that pays more attention to macro data fluctuation rather than individual user feedback, and the development team has accumulated a large amount of available data.

Given the above information, we decided to adopt a research method `based on data analysis` and `supplemented by usability test`.

## Step 1 Mapping the User Journey and Find Out The Data We Need

![image]()

After mapping out the user journey I found that I would like to have the traffic, drop rate, resolution rate, and CSAT of each node based on different flows.

## Step 2 Hypothesis from Data and Test Them

### Anomalies

Checking the data we found several anomalies :

1. Order Selection drop rate is considered to be high in general;
2. Drop rate at the order selection node is higher for Return/Refund bots (11%) than Order bots (7%) for Click methods
3. CSAT at Return/Refund bot is obviously lower than Order bot;

### Hypothesis

With the issues from the data I conducted a UX audit for our current flow, and formed some hypotheses to explain the anomalies:

1. Order Selection drop rate is high because：
  * The `order card information` confused users and result in hesitation;
  * Users don’t know `how to find other orders`;
  * Users can’t find the wanted order because `we don’t have the order` at all(hard to believe but possible)
2. Drop rate at order selection node is higher for RR bots (11%) than Order bots (7%) for Click methods because：
  * Users might want to inquire something `not about a specific order`;
  * Our copywriting makes the user believe that `clicking on an order card equals raising a return/refund` for that order.
3. Return/Refund bot CSAT is lower than Order bot because：
  * We send nonsense messages;
  * We force them to choose an order when they don't want to do so;
  * Of the nature of the business;

### Verification

Pair each hypothesis with one or more ways to verify:

![image]()

## Step 3 Verify the Hypothesis and Propose Design Solutions

Get validation result:

![image]()

## Step 4 Craft Design Solutions

![image]()
![image]()
![image]()
![image]()
![image]()

## Step 5 A/B Test Design Options to Get the Final Design

With all A/B test results, the final design we get has the highest performance of + 3.71% in resolution rate, - 6.82% in drop rate, -2.73% in transfer to live agent rate. [Link](https://docs.google.com/spreadsheets/d/1d4jLm2_o1jYWMGqTmbin11taxrZAmwDhVp9AEtZ5iZA/edit?usp=sharing)

Based on the traffic of the order bot in the last three months, the labor cost saved by bringing down the transfer to live agent rate is around 1 million SGD/ year( based on ID salary). We didn’t count the user retention or order contribution related to the increase in resolution rate and CSAT.

We also did further analysis to understand why the final design outperforms other options. [Link](https://docs.google.com/spreadsheets/d/1tf_NF1O4DfNZGtwqaw7cVimGoKrvABNALraCJcx3naM/edit?usp=sharing)

## What's More?

During this project, we also found some other UX issues that were not directly related to this feature, which derived into some other projects later, including:

* Answer article browsing experience enhancement;
* Chat Flow Editor portal configuration structure change;

I can't list them one by one because of the limitations of space. If you are interested in any part of it, I will be happy to share it with you when we meet.
