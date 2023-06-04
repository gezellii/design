+++
title = "Tracking Management System"
date = "2022-07-21"
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

<br>

<img src="https://user-images.githubusercontent.com/52693877/243146520-273ffe4e-4384-49bb-ad3e-85ca88216b84.png" width="75%" >

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

In this project, we are focusing on updating one core product ability for TMS: the **location data structure**. While the approach to changing the data structure is not yet fully confirmed by the data PMs, we aim to verify its feasibility through user research and remain open to alternative solutions.

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

To ensure smooth collaboration, we have defined our **responsibilities** and **cooperation methods**. My partner, a former engineer transitioning to a PM role, will primarily handle the data structure design, resource allocation, and communication with other stakeholders. Meanwhile, I'm going to designing the workflows and ensuring usibility.

### Step 2: Figure Out real User Needs Through Contextual Inquiry

To limit the length of this article, I'll just narrow down the narrative scope to Creation & Management flow, whose main users are FPM & BI & Data PM.

In this step, my focus was on gaining clarity regarding **user intentions and task details** by engaging with the target user groups. Additionally, I aimed to find answers to the questions that arose in Step 1.

 I invited the data PM and FE dev to participate in several observation sessions. This allowed us to address a broader range of potential issues.  We got a long [observation record](https://docs.google.com/spreadsheets/d/1szDVD3wMfF-gcHMUBiAo4EW2-J4p72SOqR61KNT2Mmg/edit?usp=sharing) and some key insights here:

#### 1.Varied Tasks for Different Roles:

  * **FPMs**: as the business owners with a deep understanding of the content, are primarily responsible for creating position information.
  * **BI & PA**: handle extensive analysis work and are responsible for designing high-quality tracking events for SQL queries that can be reused across features. Batch editing is particularly important for them.
  * **Data PM**: Approve/reject new tracking requests; and they are the sole role in defining new operations.

#### 2. Different Frequencies of Data Point Updates:

  * Registering new positions is relatively **rare**. People don't Usually change the Page_level & Section_level info;
  * Most of the tracking updates occur at the Target_level, involving **frequent** modifications to specific data fields.

#### 3. Necessity of Migration for All Business Groups:

  * All teams rely heavily on existing tracking data and will continue to do so.

  * However, there is a consensus among teams that there are numerous abandoned or **outdated trackings** within the system that are challenging to identify and remove.

I also got answers for my previous questions:

#### 1. Why not define a standard position structure at least within product line?

  * Actually, some business lines did standardize their own position structure, although might not in the way defined by data team;
  * Current scheme can't cover all position info, so users have to figure out their own way;
  * **We don't provide any guidance** or reference in TMS;

#### 2. How do they do cross-page traffic analysis?

  * PMs use the Pages function from TIDAL, but it's hard to find all tracking points, so basically just page traffic. For point level analysis they always need to ask BI to write SQL query to get all data.

### Step 3: Map out user journey, reveal pain points and generate solutions

After obtaining the necessary task details, we proceeded to organize the behavior for each role in a step-by-step manner. During this process, we identified the pain points experienced by users and delved into the underlying reasons behind them, brainstormed potential solutions to address these pain points:

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

During our discussions, the ideas surrounding the page structure and features for the new TMS began to take shape. 

We made some changes to the **tracking data structure** so that the concept becomes more straightforward for ordinary user. This new structure allows for the efficient management of tasks by different roles within the system. 

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

We **finalized product features**, and also shared initial prototype for key UX (e.g: position table view) so that she can conduct feasibility study with devs at a very early stage.

### Step 4 Finalize Workflow

According to the adjusted product function and data format, we divide the whole tracking assets management module into **four parts**.

This division allows us to cater to the specific operational needs of different users who have varying tasks and frequencies. By tailoring each part to accommodate the unique requirements of different user groups, we aim to optimize the overall user experience and improve efficiency in managing tracking assets.

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


<img src="https://user-images.githubusercontent.com/52693877/240955824-a9cd71e8-5b33-43ea-b6be-827492aa96dc.png" width="100%" >

### Step 5 Low-to-High fidelity prototype

In the final step, I transitioned low-fidelity sketch to high-fidelity design files that are ready for development by utilizing Shopee enterprise design system.

<img src="https://user-images.githubusercontent.com/52693877/240955814-911e70de-eb6f-4130-9178-4d3049d76f53.png" width="100%" >
<br>

For the newly introduced UX( Map View for example), I took the responsibility of building the component from scratch, ensuring it aligned with our design principles and met the needs of our users. After polishing the component, we integrated it into our existing design system. 

<img src="https://user-images.githubusercontent.com/52693877/240955801-a1c02e12-a424-44f8-9ed5-ded994ebcaff.png" width="100%" >
<br>
<img src="https://user-images.githubusercontent.com/52693877/240955782-c3c6b1c8-8d6b-4c5c-b32e-8187bbaf5092.png" width="100%" >
<br>
<img src="https://user-images.githubusercontent.com/52693877/240955760-eaf11543-c11e-4464-9657-efae7992db7f.png" width="100%" >
<br>

Full Prototype in [Figma](https://www.figma.com/proto/8hA6lqRIbL7IvgKqtDlEjY/TMS-Tracking-Revamp?page-id=24101%3A102438&node-id=24101-102439&viewport=643%2C481%2C0.64&scaling=min-zoom&starting-point-node-id=24101%3A102439&show-proto-sidebar=1).

<br>

If you are interested in other features of TMS, we can talk about:
* [Debug View](https://www.figma.com/file/Ysfvfjx0vRuqIL6pGipTU5/TMS-Debug-View?type=design&node-id=1%3A74&t=WbQTRES4d0c6IJzE-1): A real-time simulation tool for developers to debug newly built tracker.
* [Live View](https://www.figma.com/file/nFBBiyYTjEYbPQ9fAEEgng/TMS-Live-View?type=design&node-id=540%3A14048&t=PxyYOloN7roROYUX-1): A library that accesses users' real-time operational data for analysis.
* [TMS Monitor](https://www.figma.com/file/Mtk6VlE890YOSwV2rg0LFZ/Monitoring-Alert-and-Insight?type=design&node-id=157%3A9117&t=ULo77bcMlHqIIrwK-1): A data dashboard helps tracking owners to monitor alert and generate insight.