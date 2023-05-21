+++
title = "Chatbot UX Enhancement"
date = "2022-09-21"
[extra]
labels = ["App", "Data Driven"]
image = "chatbot.png"
summary = """Shopee Chatbot is an assistant bot in the Shopee e-commerce app, to answer users’ questions before they decide to access the live agent service.

In this project we reviewed the UX of a core task bot and raised **solution rate by 3.71%**.
"""
+++

# Chatbot Order Selection Revamp

<p class="time">@Shopee, 2022</p>

<span class="intro">
<span class="bg">

## About Chatbot & Order Selection

Shopee Chatbot serves 250k users per day in 8+ regions, answering all customer inquiries about orders, logistics, post-sale service, and so on. Chatbot saves an excellent amount of the cost for customer service.

In this project, we aimed to bring down the **drop rate, transfer to live agent rate** and raise the **resolution rate** and **CSAT** of Order Selection flow.

</span>
<span class="gif">
<img src="https://user-images.githubusercontent.com/52693877/239734548-dffdf14a-ac4d-4c71-81fd-e8af744cb58f.png">
</span>
</span>

## A bit Background

Over the past six months, the core metrics have been stagnant and remain at the industry average level. Chatbot team tried adjust the model, edited articles in Knowledge Base, but all seem not to be effective. 

## Choose a Research Method

Chatbot is characterised by large amount of data and small amount of information per piece of data. The product team has accumulated a lot of available data for research.

In contrast, the product team pays less attention to individual user experience or feedback than macro data fluctuation.

Given the above information, we decided to adopt a research method `based on data analysis` and `supplemented by usability test`.

<img src="https://user-images.githubusercontent.com/52693877/239734944-4c5707db-aa75-4c54-ad46-092d424a604e.svg" >


## Step 1 Mapping the User Journey and Find Out The Data We Need

Chatbot is a product with complex and interlaced flow, I mapped out the user journey to visualise the user flow and help us find out what data we need.

<img src="https://user-images.githubusercontent.com/52693877/239735221-206fa1dd-e344-4210-ac4d-669f37e82930.png" >


After mapping out the user journey, I asked BI team for the `traffic`,`drop rate`,`resolution rate`,and `CSAT`of each node based on different flow.

## Step 2 Form Hypothesis from Data and Journey Mapping

<div class="data">
  <div>High drop rate at Order Selection node.</div>
  <div>Drop rate at order selection node is higher for RR bots (11%) than Order bots (7%) for Click methods.</div>
  <div>Lower Customer satisfaction (CSAT) at Return/Refund bot than Order bot.</div>  
</div>


## Step 3 Verification

Pair each hypothesis with one or more ways to verify:


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
