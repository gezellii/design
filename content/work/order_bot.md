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

Given the above information, we decided to adopt a research method **based on data analysis** and **supplemented by usability test**.

<img src="https://user-images.githubusercontent.com/52693877/239734944-4c5707db-aa75-4c54-ad46-092d424a604e.svg" >


### Step 1 Mapping the User Journey and Find Out The Data We Need

Chatbot is a product with complex and interlaced flow, I mapped out the user journey to visualise the user flow and help us find out what data we need.

<img src="https://user-images.githubusercontent.com/52693877/239735221-206fa1dd-e344-4210-ac4d-669f37e82930.png" >


After mapping out the user journey, I asked BI team for the **traffic**,**drop rate**,**resolution rate**,and **CSAT**of each node based on different flow.

### Step 2 Form Hypothesis from Data and Journey Mapping

<div class="arrow">
  <div class="key">
    <div class="inline-title">Data Anomalies</div>
    <br/><br/><br/><br/>
    <div>High drop rate at Order Selection node.</div>
    <br/><br/><br/><br/><br/><br/><br/>
    <div>Drop rate at order selection node is higher for RR bots (11%) than Order bots (7%) for Click methods.</div>
    <br/><br/><br/><br/>
    <div>Lower Customer satisfaction (CSAT) at Return/Refund bot than Order bot.</div>  
  </div>
  <div class="symbol">
    <br/><br/><br/><br/><br/><br/><br/><br/><div>---></div><br/><br/><br/><br/>
    <br/><br/><br/><div>---></div><br/><br/><br/><br/><br/><br/>
    <div>---></div>
  </div>
  <div class="value">
    <div class="inline-title">Possible Reasons</div>
    <div class="group-p">

1. the order card information confused user and result in hesitation;
2. the user don’t know how to find other order;
3. the user can’t find the wanted order because we don’t have it at all(hard to believe but possible)

    </div>
    <div class="group-p"><ol start="4">

4. the user might not want to inquire about a specific order;
5. our copywriting make the user believe that clicking on an order card means raise RR for that order.

    </ol></div>
    <div class="group-p"><ol start="6">

6. we send nonsense messages;
7. the nature of that topic;

    </ol></div>
  </div>
</div>


### Step 3 Verification

Pair each hypothesis with one or more ways to verify:

<img src="https://user-images.githubusercontent.com/52693877/240283369-fde503ac-ddf3-4574-bdac-b74f82359a2e.png" >

At this step, we conducted several user testing, checked agent-customer chat history exported from live agent admin, communicated with BI team for more detailed data, and conducted fast A/B testing on UX writing. 
Full verification data <link>[here](https://docs.google.com/spreadsheets/d/1U6D6JAdLe83aEqkONwu0Fh34PJGa0EcLX161wne69-c/edit#gid=0)</link>.

### Step 4 Actions

Along with the movement of our research, solutions came quite naturally for each pain point. 

<img src="https://user-images.githubusercontent.com/52693877/240284485-44652a07-2131-4444-b682-c05a4cc6050a.png" >

## Craft Design Solutions

### 1. Change information to help users recognise their order

<div class="pic">
<div><img src="https://user-images.githubusercontent.com/52693877/240286571-9a204b76-fdff-48f9-ba5d-c095be37c6d6.png" ></div>
<div><img src="https://user-images.githubusercontent.com/52693877/240286588-76efbace-fe2b-41ba-8715-7159e350939a.png" ></div>
</div>

### 2. Explore UI options to enhance affordance

<div class="pic">
<div><img src="https://user-images.githubusercontent.com/52693877/240286602-cbfcb29c-990e-4a4d-9d9c-a04cbed33d75.png" ></div>
<div><img src="https://user-images.githubusercontent.com/52693877/240286610-25c23ceb-ea3d-448c-a029-a055cdc4b56c.png" ></div>
</div>

### 3. Alternative flow to  allow users back to any possible enquiries  

<div class="pic">
<div><img src="https://user-images.githubusercontent.com/52693877/240286627-5d36d83b-ed35-474f-9d7f-425d1edc1ca5.png" ></div>
<div><img src="https://user-images.githubusercontent.com/52693877/240286631-66c01b3f-2cd2-4761-935b-2628f8321d25.png" ></div>
</div>

### 4. Advice on UX writing

<div class="pic">
<div><img src="https://user-images.githubusercontent.com/52693877/240286636-d3701d9c-af46-47de-9b13-70d0c857f7f2.png" ></div>
<div><img src="https://user-images.githubusercontent.com/52693877/240286642-b1e23dd7-80b8-49cb-8874-4d5ac2194011.png" ></div>
</div>

With all A/B test results, the final design we get has the highest performance of **+3.71% in resolution rate**, **- 6.82% in drop rate**, **-2.73% in transfer to live agent rate**. [Link](https://docs.google.com/spreadsheets/d/1d4jLm2_o1jYWMGqTmbin11taxrZAmwDhVp9AEtZ5iZA/edit?usp=sharing)

Based on the traffic of the order bot in the last three months, the labor cost saved by bringing down the transfer to live agent rate is around 1 million USD/ year( based on ID salary). 

We also did further analysis to understand why the final design outperforms other options. [Link](https://docs.google.com/spreadsheets/d/1tf_NF1O4DfNZGtwqaw7cVimGoKrvABNALraCJcx3naM/edit?usp=sharing)



## What's More?

If you are interested in Chatbot , we can talk about some other related products such as:

* [Task Flow Editor](https://www.figma.com/file/mUepWRHQ9tlug2wKUM5zfu/Chatflow-Editor-(Latest)?type=design&node-id=12%3A24&t=kjMq6i1wk9hx8bsT-1):  An Integrated operation management platform for customer servers to create & manage all chatbot flows;
* [Annotation Portal](https://www.figma.com/file/kCkkutGnQ5IeAzUKoz6lDS/Data-Annotation?type=design&node-id=5873%3A76560&t=3FYl9aMma3CruBNC-1): A place for customer servers QA team to review and correct chatbot answer;
* [Data Insights](https://www.figma.com/file/SE0o4qIS19JAcIRChtILEm/Insights-Data-Portal---Past?type=design&node-id=1822%3A11838&t=w5trwwxOoqSMIFiH-1): A data dashboard for Chatbot product team to check chatbot performance;


