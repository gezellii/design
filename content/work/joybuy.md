+++
title = "Joybuy Whole Revamp"
date = "2016-11-21"
[extra]
labels = ["App", "Web", "0 to 1"]
image = "joybuy.png"
summary = """Joybuy is an overseas e-commerce platform under JD.COM.
This is a full revamp that covers the core shopping flow, I will elaborate two parts:

- Homepage
- Payment
"""
+++

# JOYBUY Revamp

<p class="time">@JD International, 2016-2017</p>

<span class="intro">
<span class="bg">

## Background

Joybuy is JD.com's international site, which was launched in 2015. When the initial version operated until the end of 2016, with the sharp rise in the number of users, we noticed that the site performance dropping and the overall user experience was not good, so we launched a revamp to improve the overall user experience.

</span>
<span class="role">

## My Role

Research:

Site audit, Sitemap, Data analysis

Design:

Prototyping, UX design, Branding
  
</span>
</span>

## Site Audit

As it was an overall improvement to the whole flow, in order to determine and prioritise what we were going to solve, we did a site audit on a typical user journey first:

<img src="https://user-images.githubusercontent.com/52693877/241350271-9b3119bb-12e8-4f88-a990-61a445c40108.png">


From this sitemap we already found some problems such as:

* Insufficient diversion channels on the Homepage.
* Missing Infos on the Product detail page.
* Redundant steps of the Checkout process.
* Missing functions in the Account system.
* etc.

To verify our hypothesis, we listed down associated user behaviours, converted them into measurable metrics, then turned to the BI team and customer service team for all we need to prove our thoughts:

<img src="https://user-images.githubusercontent.com/52693877/241350269-f816cb34-b640-4bc9-beb1-9c7c1c6bf39b.png">

The data turned out to support most of our hypothesis:

* Bounce rates and exit rates are normally high throughout all time.
* Traffic keeps raising over the past three months.
* Checkout page has the highest bounce rate, especially in filling address and payment step.
* Product page has higher bounce rates but convert better than the homepage.
* Account page has high bounce rate in Account setting, but amazingly it didn't get too much user complains.

At the same time, we also observed some UI issues during the audit, which we decided to solve by setting personas for different regions and rebranding. So we also asked for user data to create user portraits:

* English site buyers are more equal between men and women, and the best-selling items are home decorations, men's and women's clothing.
* Russian site buyers are mainly men. Best-selling items are mobile phones, small electronic devices, cars and motorcycle supplies. There are a number of small wholesaler users who purchase goods in bulk.
* Spanish site buyers are mainly young women, and the best-selling categories are wigs, makeup, and clothing.

3 personas were outlined to represent the core audiences:

| EN                                                                                                  | RU                                                                                               | ES                                                                                  |
| :-------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------- |
| <img src="https://user-images.githubusercontent.com/52693877/241350268-d5053cde-95c5-42bf-9918-ad438f81dcdc.png" style=" width:280px">                                                                                         | <img src="https://user-images.githubusercontent.com/52693877/241350267-8f65e412-d7c6-4938-9011-dfad2ed408f2.png" style="width:280px">                                                                                        | <img src="https://user-images.githubusercontent.com/52693877/241350265-384e5d40-60b3-4c8d-9118-e97a65ae2865.png" style="width:280px">                                                                         |
| **ISABELLA, 27**                                                                                    | **IVANOVICH, 35**                                                                                | **CAMILA, 23**                                                                      |
| Location: London, UK                                                                                | Location: Moscow, Russia                                                                         | Location: Madrid, Spain                                                             |
| Enjoy adding pops of colours to her home. Appreciates quality products, but at an affordable price. | Keen to buy some cheap accessories online for his motorcycle. Interested in electronic products. | A young worker with a passion for life. Like colourful trinkets and trendy clothes. |

**Conclusion**: Based on all findings, we feel that the top priorities are the *Homepage & Category*, and the *Checkout & Registration*, Account & Order system should follow as phase 2.

---

## Homepage & Category

### Goal

* Bring down drop rate from homepage, and diverse traffic to other pages as desired.
* Raise order conversion rate.

### Objective

* Provide a clear and consistent category system;
* Enrich the first two screens to meet the browsing needs of all users (new user/bargain hunter/ return buyer)
* Display promotion information effectively.
* Enable shopping from the homepage.

### Solution

* Optimise the interaction of category navigation.
* Add shortcut entrances to: campaign page / permanent hot-selling category / brands page.
* Increase the priority of the Flash deal channel.
* Prioritise high-level information to the top 50% of the page.
* Always display the price of items.

We also decide to keep those principles in mind when designing as well as reviewing our solutions:

* Move users a step closer to their goal with every click.
* Users should be aware of where they are going before jumping.
* Provide a universal way to come back to the homepage.
* We should test site performance after the change.

### Prototype

<img src="https://user-images.githubusercontent.com/52693877/241350262-e68fce25-a271-4b68-a9b8-88da36572349.png">

### Final Design

With our target audiences' persona we settled down the visual style of our websites:

<img src="https://user-images.githubusercontent.com/52693877/241350242-019e634c-4ced-4923-9610-5b242aef3ba9.png">

<div class="image-joy">
    <div>
        <img src="https://user-images.githubusercontent.com/52693877/241350240-4241fabd-75b8-441b-9b85-b21e990cf691.png" />
    </div>
    <div>
        <img src="https://user-images.githubusercontent.com/52693877/241350237-63d237bf-8913-43e9-b728-2df57c6487a0.png">
        <img src="https://user-images.githubusercontent.com/52693877/241350239-71c29d36-5b89-4cac-9953-d4c76c24b03f.png">
    </div>
    <div>
        <img src="https://user-images.githubusercontent.com/52693877/241350233-b55728d7-e0e6-44be-bf75-a48eeabca90c.png">
        <img src="https://user-images.githubusercontent.com/52693877/241350228-a121a178-722a-48c8-a271-9c4cb9963ea8.png">
    </div>
</div>
<br>

---

## Checkout & Payment

### Goal

* To bring down bounce rate in the checkout flow.
* Raise the payment complete rate.

### Objective

* Provide an all-in-one checkout  process;
* Reduce redundant steps to lighten mental burden while user filling checkout information;
* Provide trustworthy payment experience;

### Solution

* Combine Shipping & Billing address;
* Keep total coast within sight all the time;
* Explain how the third-party flow works within their particular checkout process;
* Offer guest checkout ( Declined by tech limitation); Allow social sign-in;
* Show user guarantee policy;  Connect users to customer support;

<img src="https://user-images.githubusercontent.com/52693877/241350195-7e9f6d84-c36c-4eb9-bbe5-c507ac087ba8.png">

From a quantitative study of reasons for checkout abandonments done by @Baymard, we got double-confirm of our analysis : 

* **Facilitating users’ preferences.** Users may prefer certain payment methods over others for any number of reasons, ranging from privacy concerns to simplicity and speed, to how secure they believe an option to be.
* **Declined payments.** Potential abandonments due to credit card declines — resulting from issues such as accounts having insufficient funds, technical issues with providers, or expired cards — can be avoided by providing fallback options.
* **System redundancy.** The more payment methods you accept, the more redundancy there will be in your payment system should one of them break down temporarily or have to be taken down for maintenance.
* **Trust issue.** Users want the website to give them enough information to make them believe that the payment is guaranteed.

We decide to keep those principles in mind when designing the UX:

* As simple as possible.
* Users should be in full control at all times.
* Users should be aware of what will happen for each action.

### Prototype

<img src="https://user-images.githubusercontent.com/52693877/241350184-bfb22a16-e992-4a4e-9585-9c2af91a6a9e.png">

### Final Design

Checkout main page

<img src="https://user-images.githubusercontent.com/52693877/241350190-0cf90046-90a6-400d-b5e6-ae5fa7d5c77b.png">

Checkout with third party payment

<img src="https://user-images.githubusercontent.com/52693877/241350193-d0c43586-dd08-4692-8633-8f8897ee7f02.png">

---

## Other Modules

In this year-long project, we had almost taken care of every corner of JOYBUY, including

* Product detail page;
* Flash Deal channel;
* Category channel;
* Shopping cart;
* My Account;
* Order history;
* Help center;
* ...

It was the very first comperhensive project that built my foundamental understanding of an ecommerce product.
So even so many years have passed and it now seems that it has a lot to fall short of - especially idealistic - I still have this project here as a memorial to my first job, and it was a happy experience.