+++
title = "Tracking Management System"
[extra]
labels = ["Internal Tools", "Data Product"]
image = "https://avatars.githubusercontent.com/u/583231"
summary = """Tracking Management System is a centralized platform to create, test and monitor traffic data for 65+ products.

I work with a data PM to redesign the platform as part of the Common Traffic Revamp project.
"""
+++

# Tracking Management System

*@Shopee, 2021*

### What is Tracking?

Tracker is a bunch of code integrated into Front End/BE. Once users triggered certain events (e.g. click something or view a new page), event handler methods are called, then we can collect the data to know users' behaviors with our products.

![image]()

### What is TMS?

**TMS** ( Tracking Management System) is a centralized platform for users to create, test, monitor, and control their tracking data.

![image]()

### What's Wrong with Our Tracking System?

The existing version was built by the development team several years ago without the designer's help. Over years we received many complains about this system, including:

1. Current scheme is hard to cover all position info as the App structure gets complex.
2. The creation and management flow is confusing and low in efficiency;
3. Tracking data is hard to understand, and cannot be used by others except the one who created it;
4. FE/BE: location and content info is scattered in the data field, makes it impossible to do full stock analysis in the user's life cycle 

## Redesign goals

* **for BI & Feature PM (user)**
  1. Simplify the creation and management flow to raise working efficiency;
  2. Clear guidance in tracking data structure;

* **for Data Team (owner)**
  1. Universal tracking data structure;
  2. Improve the usability of the system, so that the tracking data can serve a wider group of users.

## Step 1 Clarify goals & functional  hypothesis

In the first step, I talked with a data PM to get background and basic information, as well as a rough idea of what we are going to do. I got the following information from our first meeting:

* Target user and their tasks;
* Current user flow;
* Issues we solve and values we bring;
* Product abilities update;
* Expected results;

One core product ability update is that they are going to change the location data structure:​

|V1|V2|
|-|-|
| <ul><li>Page_Type</li><li>Page_Section</li><li>Target_Type</li></ul> | <ul><li>A_Site: Business domain units</li><li>B_Page: Product line pages</li><li>C_Block: Page sections up to 5 layers</li><li>D_Point: Atomic units</li></ul> |

e.g: Homepage Daily Discover Item

![image]()

**V1**

* Homepage
* null
* DD_tabs_2nd_item_2nd

**V2**

* A0001: shopee.sg
* B0001: Homepage
* C0001_c0002_2: Daily Discover- 2nd tab
* D0001_2: Atomic unit-2nd placement

The position ID of this item is:

* A0001.B0001.C0001_c0002_2.D0001

But data PMs are not 100% sure about this approach, so we need to verify its feasibility in user research, and they are open to better solutions.

We also aligned our responsibilities and cooperation method. My partner is a former engineer and new to PM position, she made it clear that she will focus on the data structure design, insuring dev resources, and communication with other stakeholders. So I was supposed to design the workflows as well as UI/UX.

## Step 2 Figure Out real User Needs Through Contextual Inquiry

To limit the length of this article, I'll just narrow down the narrative scope to Creation & Management flow, whose main users are FPM & BI & Data PM.

In this step, I intend to `clarify user intentions and task details` with target user groups. Also to find answers to my questions generated in Step 1:

I invited data PM and FE dev to join some of my observation sessions so I can cover more potential issues. We got a long [observation record](https://docs.google.com/spreadsheets/d/1szDVD3wMfF-gcHMUBiAo4EW2-J4p72SOqR61KNT2Mmg/edit?usp=sharing) and some key insights here:

1. Tasks for each roles are quite different:

  * FPMs are supposed to create position info because they are the business owner and know the content best;
  * BI & PA do most of the analysis work, they are supposed to design high-quality tracking events for SQL queries and are able to reuse across features; batch editing is important for them;
  * Data PM: Approve/reject new tracking requests; They are the only ones who define new operation;

2. Frequency of updates on each data point are also different:

  * Register new position is quite rare so usually we don't change the Page_level & Section_level info;
  * Most of the tracking updates happened at Target_level, eg: update data field;

3. Migration is a must for all business groups:

  * All teams have a large number of tracking in use and will continue to use them, but they also admit that there are too many aborted trackings in the system that are almost impossible to weed out.

I also got answers for my previous questions:

1. Why not define a standard position structure at least within product line?

  * Actually, some business lines did standardize their own position structure, although might not in the way defined by data team;
  * Current scheme can't cover all position info, so users have to figure out their own way;
  * We don't provide any guidance or reference in TMS;

2. How do they do cross-page traffic analysis?

  * PMs use the Pages function from TIDAL, but it's hard to find all tracking points, so basically just page traffic, for point level analysis they need to ask BI to write SQL query to get all data.

## Step 3 Map out user journey, reveal pain points and generate solutions

After getting all the necessary task details, we organize the behavior for each role step-by-step. We started from the creation flow :

![image]()

* Mark out pain points beside each step:
* Vote on the steps with poor user experience by a red dot;

After that, we look into stickers with read dot, discuss about :

* Are there any common underlying reasons for different pain points;
* If it's possible to address several pain points by the same solution;
* What's the minimum change we can adopt to solve the problem;
* What new features do we need to meet user goals;

![image]()
![image]()
![image]()

Through this discussion, the ideas of page structure and features for the new TMS gradually took shape.

We made some changes to the tracking data structure so that the concept becomes more straightforward for ordinary user, and based on that structure we can build a system where different roles are able to manage their tasks efficiently.

| V2 Scheme Position | V3 Scheme Position + Target |
|-|-|
| <ul><li>A_Site: Business domain units</li><li>B_Page: Product line pages</li><li>C_Block: Page sections up to 5 layers</li><li>D_Point: Atomic units</li></ul> | <ul><li>*A_Site: Business domain units*</li><li>B_Page: Product line pages</li><li>C_Block: Page sections up to 5 layers</li><li>D_Point: Atomic units</li><li>**Target: Tracking object**</li></ul> |

e.g: Homepage Daily Discover Item

![Image]()

V2 Scheme

* A0001: shopee.sg
* B0001: Homepage
* C0001_c0002_2: Daily Discover- 2nd tab
* D0001_2: Atomic unit-2nd placement

V3 Scheme

* B0001: Homepage
* C0001_c0002_2: Daily Discover- 2nd tab
* D0001_2: Atomic unit-2nd placement
* E0001: Item Card

We finalized product features, and also shared initial ideas about key UX (e.g: position table view) so that she can conduct feasibility study with devs at a very early stage.

## Step 4 Finalize Workflow

According to the adjusted product function and data format, we divide the whole tracking assets management module into four parts to meet the operation needs of different users at different frequencies.

* Position Library ( FPM; rarely use)

    B_page: the page info
    C_section: page section info. Can have no more than 3 layers
    D_point: The atomic unit that users interact with

* Target Library ( FPM & BI; frequently use)

    E_Target: the target that can be placed at any position, it can be a single object or a group of objects. e.g. item card, YMAL, banner, link.

* Operation Library ( Data PM; seldom use)

    Operation is a set of predefined user behaviour.e.g. impression, click, add to cart.

* Tracking Library ( All; frequently use)

    A combination of position, target and operation.

Finalised workflow:

![image]()

## Step 5 Low-to-High fidelity prototype

![image]()
![image]()
![image]()
![image]()
