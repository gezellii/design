+++
title = "Tracking Management System"
date = "2021-07-21"
[extra]
labels = ["Web", "Internal Portal"]
image = "tracking.png"
summary = """Tracking Management System is a centralized platform to create, test and monitor traffic data for 65+ products.

I work with a data PM to redesign the platform as part of the Common Traffic Revamp project.
"""
+++

# Tracking Management System
<p class="time">@Shopee, 2021</p>

### What is Tracking?

Tracker is a bunch of code integrated into Front End/BE. Once users triggered certain events (e.g. click something or view a new page), event handler methods are called, then we can collect the data to know users' behaviors with our products.

<img src="https://user-images.githubusercontent.com/52693877/240526205-2c3ef334-4177-4a6d-9aa6-f98213095878.png" width="75%" >

### What is TMS?

**TMS** ( Tracking Management System) is a centralized platform for users to create, test, monitor, and control their tracking data.

<img src="https://user-images.githubusercontent.com/52693877/240598542-dba244f3-6c9e-43e3-bfe1-50fa3bc1c2c1.png" width="100%" >

### What's Wrong with Our Tracking System?

The existing version was built by the development team several years ago without the designer's help. Over years we received many complains about this system, including:

1. Current scheme is **hard to cover all position** info as the App structure gets complex.
2. The creation and management flow is confusing and **low in efficiency**;
3. Tracking data is **hard to understand**, and cannot be used by others except the one who created it;
4. FE/BE: location and content info is **scattered** in the data field, makes it impossible to do full stock analysis in the user's life cycle 

## Redesign goals
<div class="pic">
<div>

#### For BI & Feature PM (user)

  1. Simplify the creation and management flow to raise working efficiency;
  2. Clear guidance in tracking data structure;
</div>
<div>

#### For Data Team (owner)

  1. Universal tracking data structure;
  2. Improve the usability of the system, so that the tracking data can serve a wider group of users.
</div>
</div>




### Step 1: Clarify goals & functional  hypothesis

In the first step, I talked with a data PM to get background and basic information, as well as a rough idea of what we are going to do. Usually for all my design projects, I would like to get the following information from our first meeting with PMs:

* Target user and their tasks;
* Current user flow;
* Issues we solve and values we bring;
* Product abilities update;
* Expected results;

One core product ability update for TMS is that they are going to change the location data structure:​

<div class="mapping">
  <div></div>
  <div>
    <div class="orange-title">V1</div>

* Page_Type
* Page_Section
* Target_Type

    </div>
  <div>
    <div class="green-title">V2</div>
    <ul>

* A_Site: Business domain units
* B_Page: Product line pages
* C_Block: Page sections up to 5 layers
* D_Point: Atomic units
  
    </ul>
  </div>
  <div></div>
</div>

<br>

<img src="https://user-images.githubusercontent.com/52693877/240936098-3879da7d-891e-4dc6-b8f8-62ba4f6dbfdb.png" width="100%" >



But data PMs are not 100% sure about this approach, so we need to verify its feasibility in user research, and they are open to better solutions.

We also aligned our responsibilities and cooperation method. My partner is a former engineer and new to PM position, she made it clear that she will focus on the **data structure design**, insuring **dev resources**, and communication with other stakeholders. So I was supposed to design the **workflows** as well as **UI/UX**.

### Step 2: Figure Out real User Needs Through Contextual Inquiry

To limit the length of this article, I'll just narrow down the narrative scope to **Creation & Management** flow, whose main users are FPM & BI & Data PM.

In this step, I intend to **clarify user intentions and task details** with target user groups. Also to find answers to my questions generated in Step 1:

I invited data PM and FE dev to join some of my observation sessions so I can cover more potential issues. We got a long [observation record](https://docs.google.com/spreadsheets/d/1szDVD3wMfF-gcHMUBiAo4EW2-J4p72SOqR61KNT2Mmg/edit?usp=sharing) and some key insights here:

#### 1. Tasks for each roles are quite different:

  * FPMs are supposed to create position info because they are the business owner and know the content best;
  * BI & PA do most of the analysis work, they are supposed to design high-quality tracking events for SQL queries and are able to reuse across features; batch editing is important for them;
  * Data PM: Approve/reject new tracking requests; They are the only ones who define new operation;

#### 2. Frequency of updates on each data point are also different:

  * Register new position is quite rare so usually we don't change the Page_level & Section_level info;
  * Most of the tracking updates happened at **Target_level**, eg: update data field;

#### 3. Migration is a must for all business groups:

  * All teams have a large number of tracking in use and will continue to use them, but they also admit that there are too many aborted trackings in the system that are almost impossible to weed out.

I also got answers for my previous questions:

#### 1. Why not define a standard position structure at least within product line?

  * Actually, some business lines did standardize their own position structure, although might not in the way defined by data team;
  * Current scheme can't cover all position info, so users have to figure out their own way;
  * **We don't provide any guidance** or reference in TMS;

#### 2. How do they do cross-page traffic analysis?

  * PMs use the Pages function from TIDAL, but it's hard to find all tracking points, so basically just page traffic, for point level analysis they need to ask BI to write SQL query to get all data.

### Step 3: Map out user journey, reveal pain points and generate solutions

After getting all the necessary task details, we organized the behavior for each role step-by-step, talked about the pain points and the underline reasons behind them, and what we can do to help with :

<div class="tracking">
<div>
<img src="https://user-images.githubusercontent.com/52693877/240938529-e3b18a23-c53b-424e-b3eb-0244e2f01f49.png" width="100%" >
</div>
<div>
<img src="https://user-images.githubusercontent.com/52693877/240940298-39c49d93-ce49-4b3f-bf48-3454abd820d4.png" width="100%" >
</div>
</div>
<br>
<div class="tracking">
<div>
<img src="https://user-images.githubusercontent.com/52693877/240938563-cd2f3187-5a1b-4a0c-9ad1-50b38720f00c.png" width="100%" >
</div>
<div>
<img src="https://user-images.githubusercontent.com/52693877/240938571-5cc4fe39-592f-438b-a8a3-d3d21a01715c.png" width="100%" >
</div>
<div>
<img src="https://user-images.githubusercontent.com/52693877/240938587-bf2486bc-1c78-4117-a3bb-01f0d6fe8947.png" width="100%" >
</div>
</div>


Through this discussion, the ideas of page structure and features for the new TMS gradually took shape.

We made some changes to the tracking data structure so that the concept becomes more straightforward for ordinary user, and based on that structure we can build a system where different roles are able to manage their tasks efficiently.

<div class="mapping">
  <div></div>
  <div>
    <div class="orange-title"> V2 Scheme: Position </div>

* A_Site: Business domain units
* B_Page: Product line pages
* C_Block: Page sections up to 5 layers
* D_Point: Atomic units

    </div>
  <div>
    <div class="green-title">V3 Scheme: Position + Target</div>
    <ul>

 *  <div class=disable ><div>/ A_Site: Business domain units</div></div>
 * B_Page: Product line pages
 * C_Block: Page sections up to 5 layers
 * D_Point: Atomic units
 * **Target: Tracking object**
    </ul>
  </div>
  <div></div>
</div>

<br>

<img src="https://user-images.githubusercontent.com/52693877/240951294-f71cb011-1d2d-4cf7-a84e-d4097bed64f9.png" width="100%" >

We **finalized product features**, and also shared initial ideas about key UX (e.g: position table view) so that she can conduct feasibility study with devs at a very early stage.

### Step 4 Finalize Workflow

According to the adjusted product function and data format, we divide the whole tracking assets management module into four parts to **meet the operation needs of different users with different tasks and frequencies**.

#### 1. Position Library ( FPM; rarely use) 
- B_page: the page info
- C_section: page section info. Can have no more than 3 layers
- D_point: The atomic unit that users interact with

#### 2. Target Library ( FPM & BI; frequently use)

- E_Target: the target that can be placed at any position, it can be a single object or a group of objects. e.g. item card, YMAL, banner, link.

#### 3. Operation Library ( Data PM; seldom use)

- Operation is a set of predefined user behaviour.e.g. impression, click, add to cart.

#### 4. Tracking Library ( All; frequently use)

- A combination of position, target and operation.

Finalised workflow:

<img src="https://user-images.githubusercontent.com/52693877/240955824-a9cd71e8-5b33-43ea-b6be-827492aa96dc.png" width="100%" >

### Step 5 Low-to-High fidelity prototype

<img src="https://user-images.githubusercontent.com/52693877/240955814-911e70de-eb6f-4130-9178-4d3049d76f53.png" width="100%" >
<br>
<img src="https://user-images.githubusercontent.com/52693877/240955801-a1c02e12-a424-44f8-9ed5-ded994ebcaff.png" width="100%" >
<br>
<img src="https://user-images.githubusercontent.com/52693877/240955782-c3c6b1c8-8d6b-4c5c-b32e-8187bbaf5092.png" width="100%" >
<br>
<img src="https://user-images.githubusercontent.com/52693877/240955760-eaf11543-c11e-4464-9657-efae7992db7f.png" width="100%" >
<br>

Full Prototype in Figma: [link](https://www.figma.com/proto/8hA6lqRIbL7IvgKqtDlEjY/TMS-Tracking-Revamp?page-id=24101%3A102438&node-id=24101-102439&viewport=643%2C481%2C0.64&scaling=min-zoom&starting-point-node-id=24101%3A102439&show-proto-sidebar=1)
