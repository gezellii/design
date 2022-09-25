+++
title = "Joybuy Web/App Revamp"
[extra]
labels = ["E-commerce", "Three Markets"]
image = "https://avatars.githubusercontent.com/u/583231"
summary = """Joybuy is an overseas e-commerce platform under JD.COM.

This is a full revamp that covers the core shopping flow, I will elaborate two parts:
    * Homepage
    * Payment
"""
+++

# JOYBUY Revamp

*@JD International, 2016-2017*

### Background

Joybuy is JD.com's international site, which was launched in 2015. When the initial version operated until the end of 2016, with the sharp rise in the number of users, we noticed that the site performance dropping and the overall user experience was not good, so we launched a revamp to improve the overall user experience.

### My Role

Research:

Site audit, Sitemap, Data analysis

Design:

Prototyping, UX design, Branding

## Site Audit

As it was an overall improvement to the whole flow, in order to determine and prioritise what we were going to solve, we did a site audit on a typical user journey first:

![image]()

Site Audit

As it was an overall improvement to the whole flow, in order to determine and prioritise what we were going to solve, we did a site audit on a typical user journey first:

From this sitemap we already found some problems such as:

* Insufficient diversion channels on the Homepage.
* Missing Infos on the Product detail page.
* Redundant steps of the Checkout process.
* Missing functions in the Account system.
* etc.

To verify our hypothesis, we listed down associated user behaviours, converted them into measurable metrics, then turned to the BI team and customer service team for all we need to prove our thoughts:

![image]()

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

| EN | RU | ES |
|:-  |:-  |:-  |
| ![image]() | ![image]() | ![image]() |
| **ISABELLA, 27** | **IVANOVICH, 35** | **CAMILA, 23** |
| Location: London, UK | Location: Moscow, Russia | Location: Madrid, Spain |
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

![image]()

### Final Design

With our target audiences' persona we settled down the visual style of our websites:

![image]()
![image]()
![image]()
![image]()
![image]()
![image]()

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

![image]()

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

![image]()

### Final Design

Checkout main page

![image]()

Checkout with third party payment

![image]()

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

I can't list them one by one of the limitations of space. If you are interested in any part of it, I will be happy to share with you when we meet.
