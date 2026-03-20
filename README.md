<div align="center">

# 🛡️ GigShield 
### *An Adaptive Insurance for the Gig Economy*

---

### 🚀 Guidewire DEVTrails 2026  
**Problem Statement:** AI-Powered Insurance for India’s Gig Economy  

</div>

---

## 👥 Team Details

### 🧑‍💻 Team Name  
**God Mode**

### 👨‍👩‍👧‍👦 Team Members

1. Nischal V Pattedar  
2. Jugunta Prakash  
3. Penumarthi Hima Varshini  

---

## 1. 🚀 Problem Statement, Objective & Vision

---

### 1.1 🚨 Problem Statement

<div align="center">
  <img src="https://github.com/user-attachments/assets/da24a0f8-dbdc-429d-92aa-eaf368974bcf" width="25%" />
  <img src="https://github.com/user-attachments/assets/697ebfd8-93fc-4e62-b3a1-96f4b5a787c7" width="30%" />
  <img src="https://github.com/user-attachments/assets/e90374ad-9fb3-40fc-99a8-ed7502efa5ec" width="30%" />
</div>

The rapid growth of the gig economy has enabled millions of delivery partners to earn through platforms like:

- 🍔 **Food Delivery** (Zomato, Swiggy)  
- 🛒 **Quick Commerce** (Zepto, Blinkit, Instamart)  
- 📦 **E-commerce** (Amazon, Flipkart)  

However, all delivery partners share a critical vulnerability:

> ⚠️ **Their income is directly tied to continuous delivery operations.**

Any disruption — environmental or operational — leads to **immediate income loss with zero protection**.

---

### ❗ Core Problem Dimensions

#### 1. Environmental Exposure

Delivery partners operate in uncontrolled outdoor environments, making them highly vulnerable to:

- Heavy Rainfall (≥10 mm/hr)  
- Flooding / Waterlogging (>30 cm)  
- Extreme Heat (≥35–42°C depending on category)  
- Severe Air Pollution (AQI >300)  

📉 **Result:**

- Unsafe working conditions  
- Reduced orders or complete shutdown  
- Total loss of earnings  

---

#### 2. Operational Dependency

Each delivery ecosystem has a **single point of failure**:

| Category | Dependency        | Failure Impact              |
|----------|-----------------|----------------------------|
| 🍔 Food Delivery | Restaurants       | Instant order collapse     |
| 🛒 Quick Commerce | Dark Stores       | No order assignment        |
| 📦 E-commerce     | Sortation Hubs    | Full slot income loss      |

---

#### 3. Income Instability

- No base salary  
- No guaranteed income  
- Earnings fluctuate hourly  

📊 **Example:**

| Scenario        | Earnings      |
|---------------|--------------|
| Normal Peak   | ₹300–₹400     |
| Disruption    | ₹0            |

---

#### 4. Insurance Gap

Existing insurance solutions:

- ✔ Cover accidents / health  
- ❌ **Do NOT cover income loss**  

---

### 1.2 📖 Real-World Persona Scenarios

### 1.2.1 👤Persona 1 — Food Delivery (Zomato / Swiggy)

**Worker Profile:** Two-wheeler rider, 3–7 km delivery radius, 4–6 orders/hour peak, ₹25–35/order.

**Income Structure:**
- Lunch Peak (12–3 PM): ~₹240 (33% of daily income)
- Dinner Peak (6–11 PM): ~₹360 (50% of daily income)
- Off-peak (3–6 PM): ~₹120

**Critical Risk:** Heavy rain at 6:30 PM wipes out the entire dinner rush — 50% of daily income lost in one event.

**Trigger Condition:** Rain >10 mm/hr OR Environmental Risk Score >2.3 during peak window.

**Application Workflow:**

```
[Rider Goes Online on App]
        ↓
[GPS Zone Verified + Policy Active Check]
        ↓
[Real-Time Environmental Monitor]
  → Rain API (IMD/OpenWeatherMap)
  → AQI API (CPCB)
  → Heat Index
  → Traffic API (Google Maps)
        ↓
[Risk Score Computed Every 15 Min]
  Environmental Score = 0.40(Rain) + 0.30(Heat) + 0.20(AQI) + 0.10(Traffic)
        ↓
[Score > 2.3 OR Rain > 10mm/hr?]
  YES → Check: Is this a Peak Hour?
         YES → Trigger Claim Automatically
         NO  → Standard Claim (lower payout rate)
  NO  → Continue Monitoring
        ↓
[Fraud Engine Validates]
  → GPS not spoofed
  → Orders dropped to <30% baseline
  → Rider was online during disruption
        ↓
[Payout Calculated]
  Peak Loss = Hours Lost × ₹40/hr
  Off-Peak Loss = Hours Lost × ₹25/hr
        ↓
[UPI Payout Initiated < 5 Minutes]
```

**Example — Ravi, Koramangala:**
📉 Heavy rain at 7 PM (dinner peak), lasts 3 hours → 3 × ₹40 = **₹120 auto-paid to UPI**

---

### 1.2.2 👤 Persona 2 — Quick Commerce (Zepto / Blinkit / Swiggy Instamart)

**Worker Profile:** Two-wheeler, 2–5 km radius, 3–6 orders/hour, ₹25–35/order. Income depends on dark store availability + weather.

**Critical Unique Risk:** If the dark store (micro-warehouse) is closed or order assignment rate drops >20%, the rider has zero alternative source of pickups — unlike food riders who can wait at multiple restaurants.

**Trigger Conditions:**
- Rain >10 mm/hr, OR
- Flood depth >30 cm, OR
- AQI >300, OR
- Dark store order assignment rate drops to <60% of baseline

**Application Workflow:**

```
[Rider Logs In → Zone Assigned (Low/Medium/High Risk)]
        ↓
[Multi-Signal Monitor: Every 10 Min]
  → Weather (Rain, Flood, Heat, AQI)
  → Dark Store Order Rate (Platform API / Mock)
  → Zone Traffic Congestion
        ↓
[Composite Disruption Score Calculated]
        ↓
[Threshold Breached?]
  → YES: Was rider active in affected zone?
     → YES: Was disruption ≥ 60 min continuous?
        → YES: Compute Income Loss
               Loss = Hours × Avg Hourly Rate (zone-adjusted)
        ↓
[Fraud Engine: 4-Layer Check]
  Layer 1: Disruption vs Order Rate Consistency
  Layer 2: GPS Zone Match
  Layer 3: Zone-Switch Pattern Analysis (anti-exploitation)
  Layer 4: Reputation Score Gate
        ↓
[Auto-Payout to UPI]
```

**Example — Rahul, Zepto, Bengaluru:**
📉 Heavy rain at 6 PM stops deliveries for 3 hours → 3 × ₹120/hr = **₹360 paid automatically**

---

### 1.2.3 👤 Persona 3 — E-Commerce Last-Mile (Amazon Flex / Flipkart Ekart)

**Worker Profile:** Two-wheeler/mini-van, 15–40 km city-wide route, 15–25 packages per slot, 2 slots/day (9 AM–1 PM, 4 PM–8 PM), ₹20–35/package.

**Critical Unique Risk:** Slot-based income cliff — entire batch of 20 packages assigned at hub. If the hub is inaccessible or heat forces route abandonment at package #10, income is lost proportionally. One hub outage affects 200–500 riders simultaneously.

**Trigger Conditions:**
- Hub inaccessibility (flood, curfew, shutdown)
- Temperature >38°C during slot (sustained outdoor exposure stricter than other personas)
- Rain >10 mm/hr mid-route
- Arterial road blockage (verified via traffic API)

**Application Workflow:**

```
[Rider Reports to Hub → Slot Assignment Confirmed]
        ↓
[Slot-Level Monitor Activated]
  → Hub status API
  → Route weather (temperature, rain)
  → Arterial road status (traffic API)
        ↓
[Disruption During Active Slot?]
  → Hub Inaccessible: Full slot payout
  → Mid-Route Disruption: Proportional payout
    = (Undelivered Packages / Total Assigned) × Slot Earning
        ↓
[Fraud Validation]
  → Manifest Cross-Check: Claimed undelivered = Platform manifest?
  → GPS Route Trace: Did rider leave hub area during claimed disruption?
  → Cluster Analysis: Is this a genuine hub-wide event or single-rider anomaly?
        ↓
[Payout Computed and Sent via UPI]
```

**Example — Arjun, Amazon Flex, Whitefield:**
📉 Heat hits 42°C mid-morning, forces route abandonment after 10 of 20 packages delivered → (10/20) × ₹600 = **₹300 auto-paid**
 
---

🔥 **Key Insight**

> A single disruption event can wipe out **30–80% of daily income** within minutes to hours.

---

### 1.3 🎯 Objective of the Solution

The goal is to build a **unified, scalable insurance system** that protects delivery partners from real-time income shocks.

---

#### 🎯 Core Objectives

1. **Universal Coverage**
   - Food Delivery  
   - Quick Commerce  
   - E-commerce  

2. **Zero-Touch Claim System**
   - No manual claims  
   - No paperwork  
   - Fully automated payouts  

3. **Real-Time Risk Detection**
   - Weather APIs  
   - AQI systems  
   - Traffic data  
   - Platform delivery logs  

4. **Fair & Adaptive Premiums**
   - Location risk  
   - Behavior  
   - Historical patterns  
   - Forecasted disruptions  

5. **Scalable Unified Framework**
   - ✅ One platform → Multiple delivery modules  

---

### 1.4 💡 Proposed Solution: Shield

**GigShield** is a **parametric insurance system** that uses **real-time data + predefined triggers** to automatically compensate delivery partners.

---

#### ⚙️ System Workflow

```
[ External Data Sources ]
        ↓
Weather API | AQI API | Traffic API | Platform Logs
        ↓
[ Risk Engine ]
        ↓
Environmental Risk + Operational Risk
        ↓
[ Trigger Detection ]
        ↓
If Risk ≥ Threshold → Trigger Activated
        ↓
[ Income Loss Engine ]
        ↓
Loss Calculation (Category-specific)
        ↓
[ Instant Payout System ]
        ↓
UPI Transfer (within minutes)
```


---

### 1.5 🧠 Technical Foundation (Parametric Model)

The system follows a **parametric insurance approach**, where payouts depend on **data-driven triggers** instead of manual claims.

#### 🔑 Core Trigger Logic


If (Environmental Risk ≥ High) OR (Operational Risk ≥ High)
AND Rider Active
→ Payout Triggered


#### 📥 Key Inputs

- Rainfall intensity  
- Temperature  
- AQI  
- Order rates  
- Hub/store availability  
- Traffic congestion  

---

### 1.6 🚀 Why Parametric Insurance?

| Feature            | Traditional Insurance | GigShield |
|-------------------|---------------------|----------|
| Claim Process     | Manual              | Automatic |
| Processing Time   | Days                | Minutes  |
| Transparency      | Low                 | High     |
| Fraud Risk        | High                | Low      |
| Scalability       | Limited             | High     |

---

### 1.7 🌍 Impact & Value Proposition

#### 👤 For Delivery Partners
- Income stability  
- Financial protection  
- Reduced uncertainty  

#### 🏢 For Platforms
- Better rider retention  
- Improved reliability  
- Operational stability  

#### 🌐 For Ecosystem
- First real-time gig worker insurance system  
- Scalable across cities and countries  

---

## 2. Unified Persona Analysis & Delivery Workflow

---

### 2.1 👥 Unified Delivery Ecosystem Overview

<div align="center">
  <img src="https://github.com/user-attachments/assets/7b70c990-9f2a-4b9a-b936-676ad410e933" width="50%" />
</div>

GigShield is designed to support three distinct but overlapping delivery ecosystems:

- 🍔 **Food Delivery**
- 🛒 **Quick Commerce**
- 📦 **E-commerce**

Although all involve last-mile delivery, their **operational behavior, risk patterns, and income models differ significantly**.

🔍 **Unified Insight**

> All delivery partners earn only when deliveries are successfully completed,  
> but the **point of failure differs across categories**.

---

### 2.2 📊 Persona Comparison (Unified View)

| Attribute            | 🍔 Food Delivery     | 🛒 Quick Commerce     | 📦 E-commerce        |
|---------------------|--------------------|----------------------|---------------------|
| Platforms           | Zomato, Swiggy     | Zepto, Blinkit       | Amazon, Flipkart    |
| Delivery Type       | Meals              | Groceries            | Packages            |
| Radius              | 8–35 km            | 2–5 km               | 15–40 km            |
| Time per Delivery   | 20–40 min          | 5–10 min            | Slot-based (4 hrs)  |
| Income Model        | Per order          | Per order            | Per package / slot  |
| Peak Dependency     | Very High (70–80%) | Moderate             | Fixed slots         |
| Critical Dependency | Restaurants        | Dark Stores          | Hubs                |
| Failure Impact      | Instant            | Gradual → Full       | Bulk loss           |

---

### 2.3 🍔 Food Delivery Workflow (Zomato / Swiggy)

#### 🔄 Workflow

1. Customer places order  
2. Restaurant prepares food (15–20 min)  
3. Rider assigned  
4. Rider picks up order  
5. Delivery to customer (20–30 min)  
6. Repeat cycle  

#### ⚠️ Critical Risk Point

Entire system depends on:

- Restaurant availability  
- Peak-hour demand  

#### 🚨 Failure Scenario

Heavy Rain at 6:30 PM  
→ Orders drop to near zero  
→ Rider idle  
→ **Income = ₹0**

#### 💡 Key Insight

> Food delivery income is highly concentrated in **peak windows**, making it extremely fragile.

---

### 2.4 🛒 Quick Commerce Workflow (Zepto / Blinkit)

<div align="center">
  <img src="https://github.com/user-attachments/assets/e63ab625-1b1b-42a2-8957-3d2441a0a5a5" width="40%" />
  <img src="https://github.com/user-attachments/assets/44ac1bc8-6526-4ee1-9f7d-4632cf1d130a" width="45%" />
</div>

#### 🔄 Workflow

1. Customer places order  
2. Order routed to nearest dark store  
3. Items packed (2–5 min)  
4. Rider assigned  
5. Pickup from store  
6. Delivery (5–10 min)  
7. Repeat  

#### ⚠️ Critical Risk Point

Entire system depends on:

- Dark store operations  
- Inventory + packing  

#### 🚨 Failure Scenario

Flooding in zone  
→ Dark store shuts down  
→ No orders assigned  
→ Rider idle  
→ **Income = ₹0**

#### 💡 Key Insight

> Quick commerce failures are **zone-based**, and once a zone fails,  
> riders cannot easily switch areas.

---

### 2.5 📦 E-commerce Workflow (Amazon / Flipkart)

#### 🔄 Workflow

1. Rider reports to hub  
2. Packages assigned (15–25)  
3. Route optimized  
4. Deliver across multiple locations  
5. Confirm deliveries  
6. Return undelivered packages  

#### ⚠️ Critical Risk Point

Entire system depends on:

- Hub accessibility  
- Route continuity  

#### 🚨 Failure Scenario

Extreme Heat (42°C) OR Hub Closed  
→ Rider cannot complete route  
→ Packages undelivered  
→ **Income loss (partial/full slot)**  

#### 💡 Key Insight

> E-commerce losses occur in **bulk (slot-based)** rather than gradually.

---

### 2.6 🔁 Unified Workflow (GigShield Perspective)

#### ⚙️ System-Level Workflow

```
[User Delivery Activity]
          ↓
  [Platform Systems] (Food / Quick / E-commerce)
          ↓
[External Data Sources] Weather | AQI | Traffic | Zone Data
          ↓
      [GigShield Risk Engine]
          ↓
Environmental Risk + Operational Risk
          ↓
       [Trigger Engine]
          ↓
      If Threshold Crossed
          ↓
      [Income Loss Engine]
          ↓
Category-Specific Calculation
          ↓
    [Instant Payout System]
          ↓
        UPI Transfer
```
---

### 2.7 ⚖️ Failure Point Comparison

| Category     | Failure Trigger    | Speed of Impact     | Recovery            |
|--------------|------------------|---------------------|---------------------|
| Food         | Peak disruption   | ⚡ Instant           | Slow                |
| Quick        | Store failure     | ⏳ Gradual → Full    | Medium              |
| E-commerce   | Slot failure      | 💥 Bulk             | None (slot lost)    |

---
## 3. Risk Factors Across Delivery Categories

---

### 3.1 🌍 Overview of Risk Modeling

Delivery partner income is affected by two major classes of risks:

- 🔹 **Environmental Risks**  
  External natural conditions affecting delivery capability  

- 🔹 **Operational Risks**  
  Platform/system-level disruptions affecting order flow  

🧠 **Core Design Principle**

> All risks are quantified using **standardized APIs and global benchmarks**, not arbitrary thresholds.

---

### 3.2 🌧 Environmental Risk Factors

All environmental risks are derived using:

- IMD (Indian Meteorological Department)  
- WMO (World Meteorological Organization)  
- CPCB AQI Standards  
- OSHA Heat Guidelines  

---

#### 3.2.1 🌧 Rainfall Risk Classification

<div align="center">
  <img src="https://github.com/user-attachments/assets/997d8982-dbed-467d-bda2-3f19e03598eb" width="30%" />
</div>

📊 **Standard (IMD / WMO)**

| Rain Type | Rainfall (mm/hr) | Risk Label | Impact            |
|----------|------------------|-----------|-------------------|
| Light    | < 2.           | Low       | Normal            |
| Moderate | 2.– 10         | Medium    | Slow deliveries   |
| Heavy    | 10 – 50          | High      | Order collapse    |
| Extreme  | > 50             | High      | Full shutdown     |

⚠️ **Category Impact**

- 🍔 Food → Dinner peak destroyed instantly  
- 🛒 Quick → Delivery slowdown → stop  
- 📦 E-commerce → Route unsafe  

---

#### 3.2.2 🌊 Flooding / Waterlogging

<div align="center">
  <img src="https://github.com/user-attachments/assets/55974720-77c6-4640-869f-1be51dc831d1" width="30%" />
</div>

| Flood Depth | Risk   | Impact            |
|------------|--------|-------------------|
| < 10 cm    | Low    | Minor delay       |
| 10 – 30 cm | Medium | Route deviation   |
| > 30 cm    | High   | No movement       |

⚠️ **Category Impact**

- 🍔 Food → Restaurant access blocked  
- 🛒 Quick → Dark store shutdown  
- 📦 E-commerce → Route failure  

---

#### 3.2.3 🌡 Temperature Risk (OSHA-Based)

<div align="center">
  <img src="https://github.com/user-attachments/assets/a68393cb-42ed-4cd3-98d6-3b983c9210ec" width="40%" />
</div>

| Risk   | Temperature | Impact        |
|--------|-------------|--------------|
| Low    | 10–28°C     | Normal       |
| Medium | 28–35°C     | Fatigue      |
| High   | ≥ 35°C      | Unsafe       |

🔥 **E-commerce Special Case**

| Risk    | Temperature |
|---------|------------|
| High    | ≥ 38°C     |
| Extreme | > 42°C     |

⚠️ **Impact**

- Reduced delivery speed  
- Worker fatigue  
- Route abandonment  

---

#### 3.2.4 🌫 Air Quality Index (CPCB)

<div align="center">
  <img src="https://github.com/user-attachments/assets/90c22666-441d-4bd7-98d6-b8476bf9f375" width="80%" />
</div>

| AQI  | Category        | Risk   | Impact        |
|------|----------------|--------|--------------|
| ≤150 | Good–Moderate  | Low    | Normal       |
| 151–300 | Poor        | Medium | Slower       |
| >300 | Severe         | High   | Shutdown     |

⚠️ **Impact**

- Restaurant closures  
- Outdoor restrictions  
- Health hazards  

---

### 3.3 ⚙️ Operational Risk Factors

---

#### 3.3.1 🍔 Food Delivery Risks

**Peak Hour Order Collapse**

| Orders/hr          | Risk   | Impact          |
|--------------------|--------|-----------------|
| ≥ 80% normal       | Low    | Normal          |
| 50–80%             | Medium | Partial loss    |
| < 50% OR <1.5/hr   | High   | Peak collapse   |

**Restaurant Failure Rate**

| Closure % | Risk   |
|-----------|--------|
| < 20%     | Low    |
| 20–50%    | Medium |
| > 50%     | High   |

**Customer Cancellation Cascade**

> Rain → cancellations → zero assignments  

---

#### 3.3.2 🛒 Quick Commerce Risks

**Dark Store Availability**

| Assignment Rate | Risk   |
|-----------------|--------|
| ≥ 80%           | Low    |
| 50–80%          | Medium |
| < 50%           | High   |

**Traffic Congestion**

| Map Color | Risk   |
|-----------|--------|
| Green     | Low    |
| Yellow    | Medium |
| Red       | High   |

---

#### 3.3.3 📦 E-commerce Risks

**Hub Operational Status**

| Status      | Risk   | Impact         |
|-------------|--------|---------------|
| Operational | Low    | Normal        |
| Partial     | Medium | Reduced load  |
| Closed      | High   | Slot lost     |

**Route Blockage (Traffic Index)**

| Blockage % | Risk   |
|------------|--------|
| < 20%      | Low    |
| 20–60%     | Medium |
| > 60%      | High   |

**Social Disruptions**

- Curfews  
- Strikes  
- Road blockades  

---

### 3.4 📊 Risk Score Mapping

| Risk Label | Score |
|------------|------|
| Low        | 1    |
| Medium     | 2    |
| High       | 3    |

---

### 3.5 🧮 Risk Aggregation Models

#### 3.5.1 Environmental Risk Formula


Environmental Risk =
0.3× Heat +
0.30 × Rain +
0.20 × Flood +
0.1× AQI


---

#### 3.5.2 Operational Risk (Category-Based)

**🍔 Food Delivery**

0.60 × Orders + 0.25 × Restaurant + 0.15 × Traffic


**🛒 Quick Commerce**

0.60 × DarkStore + 0.40 × Traffic


**📦 E-commerce**

0.65 × Hub + 0.35 × Route Blockage


---

### 3.6 🚨 Overriding Conditions (Critical Design)

Even without full calculation, some conditions automatically trigger **HIGH risk**:

- Rain ≥ 10 mm/hr  
- Flood > 30 cm  
- Orders < 1.5/hr  
- Dark store shutdown  
- Hub closed  

---

## 4. Eligibility Criteria (Unified Across All Delivery Categories)

---

### 4.1 🎯 Overview

<div align="center">
  <img src="https://github.com/user-attachments/assets/0bb54851-6678-46a7-9bcd-92d179d6ee5d" width="30%" />
</div>

The **Eligibility Criteria** define the conditions under which a delivery partner qualifies for:

- ✅ Coverage activation  
- ✅ Trigger-based payout eligibility  

🧠 **Core Principle**

> A payout is valid **ONLY IF** a verified disruption directly affects an **actively working delivery partner** within an authorized operational context.

---

### 4.2 👤 Platform Registration Requirement

The delivery partner must be officially registered with a supported platform:

#### 🍔 Food Delivery
- Zomato  
- Swiggy  

#### 🛒 Quick Commerce
- Zepto  
- Blinkit  
- Swiggy Instamart  
- Dunzo  

#### 📦 E-commerce
- Amazon (Flex / DSP)  
- Flipkart (Ekart Logistics)  

✅ **Verification Mechanism**

- Partner ID linked during onboarding  
- API-based validation of active status  

---

### 4.3 🟢 Active Delivery Status (Critical Condition)

🔑 **Rule**

> The policy is active **ONLY during periods when the rider is actively working.**

#### ✅ Required Conditions

- Rider is online on platform  
- Rider is accepting/assigned deliveries or slots  
- GPS tracking enabled  
- Activity verified via platform logs  

---

#### 📊 Category-Specific Conditions

##### 🍔 Food Delivery

- ≥ 5 orders in last 7 days  
- Active during peak hours:
  - Lunch: 12–3 PM  
  - Dinner: 6–11 PM  
- Minimum 2 peak sessions/week  

##### 🛒 Quick Commerce

- Active order acceptance  
- Continuous delivery activity  
- Valid GPS + zone presence  

##### 📦 E-commerce

- Must have assigned delivery slot  
- Active delivery manifest required  
- At least 1 delivery completed in past 7 days  

---

#### ❌ Ineligible Cases

- Rider offline during disruption  
- GPS disabled  
- No active orders/slot  

---

### 4.4 🗺 Valid Working Zone / Route Constraint

🧠 **Core Rule**

> Coverage is valid **ONLY within platform-assigned zones or routes.**

---

#### 🍔 Food Delivery Zones

- Restaurant clusters  
- Platform-assigned zones  
- Dynamic peak-hour assignments  

✔ Allowed:
- Primary zone  
- Temporary reassignment (< 5 km)  

---

#### 🛒 Quick Commerce Zones

- Dark store–linked zones  
- Hyperlocal (2–5 km radius)  

✔ Allowed:
- Platform-assigned zones  
- Demand-based reassignment  

---

#### 📦 E-commerce Routes

- Hub-based delivery routes  
- Assigned delivery manifest  

✔ Allowed:
- Assigned route zones  
- Platform-approved route changes  

---

#### ❌ Invalid Cases

- Deliveries outside assigned zones  
- Personal/off-platform deliveries  
- Self-initiated zone switching  

---

### 4.5 🌍 Geographic Limitation

🔒 **Rule**

> Coverage is restricted to the **registered city/region**.

**Example:**

- Bengaluru-registered rider → ✅ Covered within Bengaluru  
- Delhi activity → ❌ NOT covered  

📌 **Reason**

- Risk models are city-specific  
- API validation tied to geography  

---

### 4.6 💳 Policy Activation Requirement

#### ✅ Mandatory Conditions

- Weekly premium paid  
- Auto-debit successful  
- Policy status = **ACTIVE**  
- UPI/bank linked  

#### ⏱ Activation Timing

- Policy starts: **Monday 00:01**  
- Validity: **7 days**  

#### ❌ Ineligible

- Payment failed  
- Policy expired  
- Paused subscription  

---

### 4.7 ⏰ Time-Based Eligibility (Critical for Food & E-commerce)

#### 🍔 Food Delivery (Peak-Based Eligibility)

Must be active during:

- Lunch Peak → 12:00–15:00  
- Dinner Peak → 18:00–23:00  

---

#### 📦 E-commerce (Slot-Based Eligibility)

Must have assigned slot:

- Morning: 9 AM–1 PM  
- Evening: 4 PM–8 PM  

---

#### 🛒 Quick Commerce

- No strict peak window  
- Based on active working hours  

---

### 4.8 🧾 New vs Existing Partner Rules

#### 🆕 New Delivery Partners

- Minimum **2–4 weeks observation period**  
- Baseline earnings established  
- Activity tracking required  

---

#### 🔁 Existing Partners

Must meet:

- Activity thresholds  
- GPS validation  
- Platform engagement  

---

### 4.9 🚨 Ineligibility & Fraud Conditions

#### ❌ Automatic Disqualification Cases

- Rider offline during disruption  
- Fake GPS / location spoofing  
- No platform activity  
- Operating outside assigned zone  
- Claiming outside registered city  
- Voluntary inactivity  

---

#### 🚫 Special Fraud Cases

- Claim during non-peak hours (food)  
- Claim without assigned slot (e-commerce)  
- Claim without order assignment (quick commerce)  

---

### 4.10 📊 Eligibility Decision Flow


START
↓
Is rider registered on platform?
↓ YES
Is policy active?
↓ YES
Is rider online with GPS?
↓ YES
Is rider in valid zone/route?
↓ YES
Is rider active during disruption window?
↓ YES
→ ELIGIBLE FOR PAYOUT

ANY "NO" → NOT ELIGIBLE
----

## 5. Coverage Definition (Unified Policy Coverage)

---

### 5.1 🎯 Overview

The **GigShield policy** provides financial compensation for **income loss** caused by external disruptions that prevent delivery partners from completing their work.

🧠 **Core Principle**

- ✅ **ONLY income loss is covered**  
- ❌ No physical damage, health, or accident coverage  

---

### 5.2 ✅ Covered Events

Coverage is triggered when **external, verifiable conditions** disrupt delivery operations.

---

#### 🌍 5.2.1 Environmental Events

Applicable across all categories:

- 🌧 Heavy Rainfall (≥10 mm/hr)  
- 🌊 Flooding / Waterlogging (>30 cm)  
- 🌡 Extreme Temperature (≥35°C or category-specific thresholds)  
- 🌫 Severe Air Pollution (AQI >300)  

---

#### ⚙️ 5.2.2 Operational Events (Category-Specific)

##### 🍔 Food Delivery

- Restaurant closures (>50% in 2 km radius)  
- Peak-hour order collapse (<1.5 orders/hour)  
- Customer cancellation cascade  
- Traffic congestion affecting pickup  

---

##### 🛒 Quick Commerce

- Dark store shutdown / unavailability  
- Order assignment drop (<50% baseline)  
- Traffic congestion delays  
- Zone-level operational disruption  

---

##### 📦 E-commerce

- Hub closure / inaccessibility  
- Route blockage (traffic or flooding)  
- Partial route abandonment  
- Platform suspension during extreme conditions  

---

#### 🚧 5.2.3 Social & External Events

- Curfews  
- Strikes / protests  
- VIP movement restrictions  
- Sudden zone lockdowns  

---

### 5.3 📊 What is Covered

The policy compensates **loss of earnings**, calculated based on delivery activity.

---

#### 💰 Covered Components

| Component                 | Description                    |
|--------------------------|--------------------------------|
| Loss of working hours    | Rider unable to work           |
| Loss of orders           | Reduced assignments            |
| Loss of delivery slots   | (E-commerce)                   |
| Partial delivery failure | Undelivered packages           |

---

#### 📌 Category-Wise Coverage Logic

##### 🍔 Food Delivery

✔ Covered:

- Peak-hour income loss  
- Order collapse during lunch/dinner  
- Restaurant inaccessibility  

❗ **Example:**


4 hours dinner rain
→ 4 × ₹45/hour = ₹180 payout


---

##### 🛒 Quick Commerce

✔ Covered:

- Loss of delivery hours  
- Dark store shutdown  
- Reduced order assignment  

❗ **Example:**


3 hours disruption
→ 3 × ₹120/hour = ₹360 payout


---

##### 📦 E-commerce

✔ Covered:

- Full slot loss  
- Partial slot loss  
- Undelivered packages  

❗ **Example:**


12 undelivered packages × ₹28
= ₹336 payout


---

### 5.4 ❌ What is NOT Covered

This is strictly enforced to avoid ambiguity and fraud.

---

#### 🚫 Exclusions Table

| Exclusion                     | Reason                     |
|------------------------------|----------------------------|
| Vehicle damage               | Not income-related         |
| Personal injury              | Health insurance scope     |
| Accidents                    | Separate insurance domain  |
| Voluntary inactivity         | No disruption              |
| Late deliveries (completed)  | Income still earned        |
| Restaurant internal delays   | Not external               |
| Off-peak slowdown            | Only critical windows covered |
| Personal deliveries          | Outside platform           |

---

### 5.5 ⚖️ Category-Specific Rules

##### 🍔 Food Delivery

✔ Covered:

- Lunch (12–3 PM)  
- Dinner (6–11 PM)  

❌ Not Covered:

- Off-peak periods  
- Minor delays  

---

##### 🛒 Quick Commerce

✔ Covered:

- Any active working hour disruption  

---

##### 📦 E-commerce

✔ Covered:

- Assigned slot disruption  

❌ Not Covered:

- No slot assigned  
- Voluntary cancellation  

---

### 5.6 📐 Coverage Logic (System View)

```
Disruption Occurs
↓
Is it Environmental OR Operational?
↓ YES
Is it within defined thresholds?
↓ YES
Is rider eligible (Section 4)?
↓ YES
→ Income Loss Calculated
→ Payout Triggered

Else → Not Covered
```
---

### 5.7 🧠 Golden Rule of Coverage

> 💡 If income is **not lost**, the policy **does not pay**.

---

## 6. Disruption Triggers (Parametric Risk Engine)

---

### 6.1 🎯 Overview

The **Disruption Trigger Engine** is the core decision-making system of **GigShield**.

It determines:

- ⚡ **WHEN** a disruption has occurred  
- ⚡ **WHETHER** a payout should be triggered  

🧠 **Core Principle**

> A payout is triggered when **quantified risk exceeds predefined thresholds** based on real-world data.

---

### 6.2 📊 Risk Score Mapping

All risk factors are standardized into numeric values:

| Risk Label | Score |
|------------|------|
| Low        | 1    |
| Medium     | 2    |
| High       | 3    |

---

### 6.3 🌍 Environmental Risk Model

#### 📐 Formula


Environmental Risk =
0.35 × Heat +
0.30 × Rain +
0.20 × Flood +
0.15 × AQI


---

#### 📊 Weight Justification

| Factor | Weight | Reason                                      |
|--------|--------|---------------------------------------------|
| 🌡 Heat | 35%   | Continuous exposure risk (esp. e-commerce)  |
| 🌧 Rain | 30%   | Immediate disruption of deliveries          |
| 🌊 Flood| 20%   | Route blockage                             |
| 🌫 AQI  | 15%   | Gradual slowdown / shutdown                |

---

#### 📈 Risk Classification

| Score Range | Label              |
|-------------|--------------------|
| 1.0 – 1.5   | Low                |
| 1.5 – 2.3   | Medium             |
| > 2.3       | High (Trigger Level)|

---

### 6.4 ⚙️ Operational Risk Models

---

#### 🍔 6.4.1 Food Delivery


Operational Risk =
0.60 × Order Collapse +
0.25 × Restaurant Failure +
0.15 × Traffic


🔍 **Key Drivers**

- Orders < 1.5/hr → critical  
- Restaurants closed > 50%  
- Peak-hour congestion  

---

#### 🛒 6.4.2 Quick Commerce


Operational Risk =
0.60 × Dark Store +
0.40 × Traffic


🔍 **Key Drivers**

- Store shutdown = zero orders  
- Traffic affects delivery speed  

---

#### 📦 6.4.3 E-commerce


Operational Risk =
0.65 × Hub Status +
0.35 × Route Blockage


🔍 **Key Drivers**

- Hub closure = full slot loss  
- Route blockage = partial loss  

---

### 6.5 🚨 Overriding Conditions (Instant Trigger)

Some conditions are so severe that they **skip calculations**:

#### 🔴 Automatic HIGH Risk

- Rain ≥ 10 mm/hr  
- Flood depth > 30 cm  
- Orders < 1.5/hr (food)  
- Dark store shutdown  
- Hub closed  
- Extreme heat (> 42°C)  

🧠 **Reason**

> These events cause **immediate and total income disruption**.

---

### 6.6 🔗 Combined Trigger Logic

#### 📐 Final Condition


IF (Environmental Risk > 2.3)
OR (Operational Risk > 2.3)
AND Rider Eligible (Section 4)
→ TRIGGER PAYOUT


⚠️ **Important Notes**

- Environmental **OR** Operational is sufficient  
- Must satisfy eligibility conditions  

---

### 6.7 🧪 Real-World Example (Food Delivery)

**Scenario: Dinner Peak Rain**

- Rain = 15 mm/hr → High (3)  
- Flood = Medium (2)  
- Temp = Medium (2)  
- AQI = Medium (2)  

#### Environmental Score:


= (3×0.30) + (2×0.20) + (2×0.35) + (2×0.15)
= 2.4 → HIGH


- Orders/hr = 1 → HIGH  

✅ **Result**

- → TRIGGER ACTIVATED  
- → Payout initiated  

---

### 6.8 🧪 Real-World Example (E-commerce)

**Scenario: Hub Closure**

- Hub Status = Closed → High (3)  
- Route = Medium (2)  

#### Operational Score:


= (3×0.65) + (2×0.35)
= 2.65 → HIGH


✅ **Result**

- → TRIGGER ACTIVATED  
- → Slot payout  

---

### 6.9 🔄 Trigger Workflow

```
[Data Input]
↓
Weather + AQI + Traffic + Platform Logs
↓
[Risk Classification]
↓
Assign Scores (1,2,3)
↓
[Risk Aggregation]
↓
Environmental + Operational Scores
↓
[Threshold Check]
↓
If HIGH → Trigger
↓
[Send to Loss Engine]
↓
[Instant Payout]
```

---

## 7. Dynamic Premium Model (AI-Driven Pricing Engine)

---

### 7.1 🎯 Overview

The **Dynamic Premium Model** determines the **weekly insurance premium** for each delivery partner based on:

- 📊 Risk Exposure  
- 🤖 AI Predictions  
- 👤 Behavioral Reliability  

🧠 **Core Principle**

> Riders pay **only for the risk they are exposed to**, not a fixed universal price.

---

### 7.2 ⚙️ End-to-End Premium Workflow

```
[Data Collection]
↓
Weather + AQI + Traffic + Platform Data
↓
[Risk Classification]
↓
Environmental + Operational Risk
↓
[Risk Exposure Model]
↓
Zone / Route Risk Calculation
↓
[AI Prediction Layer]
↓
7-Day Disruption Forecast
↓
[Reputation Engine]
↓
Behavior Score (0–100)
↓
[Premium Engine]
↓
Final Weekly Premium
↓
[Policy Update]
(Monday 00:01)
```
---

### 7.3 💰 Base Premium Structure

Base premiums vary across categories due to different income risk profiles.

#### 📊 Category-Wise Base Premium

| Category            | Low Risk | Medium Risk | High Risk |
|--------------------|----------|-------------|-----------|
| 🍔 Food            | ₹35      | ₹50         | ₹65       |
| 🛒 Quick Commerce  | ₹25      | ₹35         | ₹45       |
| 📦 E-commerce      | ₹30      | ₹42         | ₹55       |

🧠 **Insight**

- 🍔 Food → Higher volatility (peak collapse)  
- 🛒 Quick → Lower per-hour income  
- 📦 E-commerce → Higher per-event loss (slot-based)  

---

### 7.4 📍 Risk Exposure Models

---

#### 🍔 7.4.1 Food Delivery (Zone-Based)


Effective Risk =
Σ (Zone Work % × Zone Risk Value)


📊 **Example**

| Zone         | Work % | Risk |
|--------------|--------|------|
| Koramangala  | 50%    | 3    |
| Indiranagar  | 30%    | 2    |
| Whitefield   | 20%    | 1    |

👉 **Score = 2.4 → High Risk**

---

#### 🛒 7.4.2 Quick Commerce (Multi-Zone)


Effective Risk =
Σ (Zone % × Risk Value)


✔ Same logic as food  
✔ Based on dark store zones  

---

#### 📦 7.4.3 E-commerce (Route-Based)


Effective Route Risk =
Σ (Route Zone % × Risk Value)


📊 **Example**

| Zone Type | %   | Risk |
|-----------|-----|------|
| Low       | 35% | 1    |
| Medium    | 40% | 2    |
| High      | 25% | 3    |

👉 **Score = 1.9 → Medium Risk**

---

### 7.5 🤖 AI-Based Risk Prediction

#### 🧠 Models Used

- XGBoost → Primary (high accuracy)  
- LSTM → Time-series forecasting  
- Random Forest → Pattern detection  
- Logistic Regression → Baseline  

---

#### 📥 Inputs

- Weather forecast (rain, temperature, AQI)  
- Historical disruption patterns  
- Traffic trends  
- Platform activity (orders, hubs, stores)  

---

#### 📤 Output


"Thursday 6 PM → 82% disruption probability"
→ Premium increased by +20%


🎯 **Purpose**

- Predict future risk  
- Adjust pricing proactively  

---

### 7.6 👤 Delivery Partner Reputation Score

#### 📐 Formula


Reputation =
0.4 × Performance +
0.3 × Claims +
0.2 × Activity +
0.1 × Stability


---

#### 📊 Factors

| Factor            | Weight | Description                  |
|------------------|--------|------------------------------|
| Performance      | 40%    | Orders/slots completed       |
| Claims Behavior  | 30%    | Valid vs suspicious claims   |
| Activity         | 20%    | Weekly engagement            |
| Stability        | 10%    | Zone/route consistency       |

---

#### 📈 Score Classification

| Score   | Level  |
|---------|--------|
| 80–100  | High   |
| 50–80   | Medium |
| <50     | Low    |

---

### 7.7 ⚖️ Reputation-Based Adjustment

| Level  | Adjustment         |
|--------|--------------------|
| High   | −10% (discount)    |
| Medium | No change          |
| Low    | +15% (penalty)     |

🧠 **Insight**

- Encourages honest behavior  
- Discourages fraud  

---

### 7.8 ⚖️ Risk-Adjusted Coverage (Fairness Model)

Higher-risk riders:

- Pay higher premium  
- Receive higher payouts  

📊 **Example**

| Zone Risk  | Premium | Payout/hour |
|------------|--------|-------------|
| High Risk  | ₹101   | ₹45         |
| Low Risk   | ₹74    | ₹35         |

---

### 7.9 🧮 Final Premium Formula


Final Premium =
Base × Risk Exposure × AI Factor × Reputation Adjustment


---

#### 📊 Worked Example (Food Rider)

- Base = ₹50  
- Zone Risk = 1.8  
- AI Factor = 1.25  
- Reputation = 0.90  


Final = ₹50 × 1.8 × 1.25 × 0.90
= ₹101/week


---

### 7.10 🔄 Weekly Pricing Model

#### ⏱ Update Cycle

- Every **Monday 00:01**

---

#### 🔁 Process

- Previous week data analyzed  
- New risk calculated  
- AI prediction applied  
- Premium updated  

---

#### 📉 Example

| Week   | Condition      | Premium |
|--------|---------------|---------|
| Week 1 | Monsoon       | ₹101    |
| Week 2 | Clear weather | ₹81     |
| Week 3 | Heatwave      | ₹95     |

---

## 8. Income Loss Calculation (Payout Engine)

---

### 8.1 🎯 Overview

The **Income Loss Calculation Engine** determines the exact compensation amount payable to a delivery partner when a disruption trigger is activated.

🧠 **Core Principle**

> 💡 **Payout = Actual earnings lost due to verified disruption**

---

### 8.2 ⚙️ Activation Conditions

Income loss is calculated **ONLY when all conditions are met**:

#### ✅ Required Conditions

- Disruption trigger activated (**Section 6**)  
- Rider eligible (**Section 4**)  
- Covered event (**Section 5**)  
- Minimum disruption duration satisfied  

---

#### ⏱ Minimum Duration Rules

| Category            | Minimum Duration        |
|--------------------|------------------------|
| 🍔 Food            | ≥ 30 minutes           |
| 🛒 Quick Commerce  | ≥ 30 minutes           |
| 📦 E-commerce      | ≥ 45–60 minutes (slot-based) |

---

### 8.3 📊 Earnings Estimation Model

🧠 **Key Idea**

Each rider has a **personalized earning baseline**, calculated from historical platform data.

---

#### 🍔🛒 8.3.1 Food & Quick Commerce

##### 📐 Formulas
Average Peak Earnings =
Total Peak Earnings ÷ Peak Hours Worked

Average Non-Peak Earnings =
Total Non-Peak Earnings ÷ Non-Peak Hours Worked


---

##### 📊 Example

- Peak earnings = ₹900 over 20 hours → ₹45/hour  
- Non-peak = ₹500 over 20 hours → ₹25/hour  

---

#### 📦 8.3.2 E-commerce

##### 📐 Formula
Average Earnings per Package =
Total Earnings ÷ Total Packages Delivered


---

##### 📊 Example

- ₹560 earned from 20 packages → ₹28/package  

---

### 8.4 📉 Disruption Duration Calculation

🧠 **Definition**

Time during which delivery operations are **significantly affected**.

#### 📌 Conditions

- Must meet trigger criteria  
- Must exceed minimum duration  
- Continuous or aggregated disruption  

---

### 8.5 💰 Final Income Loss Formulas

---

#### 🍔 Food Delivery
Income Loss =
PeakHoursLost × PeakRate +
NonPeakHoursLost × NonPeakRate


---

#### 🛒 Quick Commerce
Income Loss =
TotalHoursLost × AvgHourlyIncome


---

#### 📦 E-commerce

**Full Slot Loss**
Assigned Packages × Avg Earning per Package


**Partial Loss**
Undelivered Packages × Avg Earning per Package


---

### 8.6 📊 Real-World Examples

---

#### 🍔 Food Delivery (Dinner Peak Rain)

- Peak Rate = ₹45/hour  
- Disruption = 4 hours  
Loss = 4 × 45 = ₹180


---

#### 🛒 Quick Commerce (Store Shutdown)

- Avg Income = ₹120/hour  
- Disruption = 3 hours  
Loss = 3 × 120 = ₹360


---

#### 📦 E-commerce (Partial Slot Loss)

- Packages assigned = 20  
- Delivered = 8  
- Undelivered = 12  
- Avg earning = ₹28  
Loss = 12 × 28 = ₹336


---

### 8.7 ⚖️ Proportional Loss Handling

🧠 **Rule**

> Partial disruption → **Partial payout**

**Example**

- 2 hours disrupted out of 5-hour peak  
→ Only **2 hours compensated**

---

### 8.8 🚀 Instant Payout System

#### ⚡ Workflow
```
Trigger Detected
↓
Loss Calculated
↓
Amount Validated
↓
Payout Initiated
↓
UPI Transfer (< 5 minutes)
```

---

### 8.9 🔍 Validation Before Payout

To ensure accuracy:

- Platform data (orders/packages)  
- GPS activity  
- API validation (weather, AQI, traffic)  

---

## 9. Fraud Detection & Claim Validation (Multi-Layer Security Engine)

---

### 9.1 🎯 Overview

The **Fraud Detection & Claim Validation Engine** ensures that:

- ✅ Only **genuine income loss claims** are paid  
- ❌ All **fraudulent or manipulated claims** are automatically rejected  

🧠 **Core Principle**

> A claim is valid **ONLY IF** a verified disruption directly causes **measurable income loss** for an active delivery partner.

---

### 9.2 ⚖️ Claim Validation Conditions

A payout is triggered **ONLY when ALL conditions are satisfied**:

#### ✅ Mandatory Conditions

- **Verified Disruption**  
  - Must meet parametric trigger thresholds (**Section 6**)  

- **Active Rider**  
  - Rider online during disruption  
  - GPS active  

- **Valid Operational Context**  
  - Assigned zone / route  
  - Active order / slot  

- **Actual Income Loss**  
  - Orders/packages reduced or stopped  

❌ **If ANY condition fails → Claim Rejected**

---

### 9.3 🔐 Multi-Layer Fraud Detection System

---

#### 🧱 Layer 1: Contextual Validation

🎯 **Purpose**  
Ensure disruption matches expected real-world impact  

✅ **Checks**

- Rain during dinner peak (food)  
- Dark store failure (quick commerce)  
- Hub closure (e-commerce)  

❌ **Fraud Example**

- Claiming rain disruption at 3 AM (non-peak food)  
→ ❌ Rejected  

---

#### 📍 Layer 2: GPS & Location Validation

🎯 **Purpose**  
Ensure rider is physically present in affected zone  

✅ **Checks**

- Rider GPS within disruption zone  
- Movement patterns consistent  
- No teleporting anomalies  

❌ **Fraud Detection**

- GPS spoofing  
- Sudden location jumps  
- Inactive location during claim  

---

#### 📊 Layer 3: Platform Data Validation

🎯 **Purpose**  
Verify actual work disruption via platform logs  

✅ **Data Sources**

- Order assignment rate  
- Package delivery logs  
- Slot completion status  
- Store/hub status  

❌ **Fraud Example**

- Rider claims no orders  
- Platform shows normal assignment  
→ ❌ Rejected  

---

#### ⏱ Layer 4: Time & Activity Validation

🎯 **Purpose**  
Ensure rider was actively working during disruption  

✅ **Checks**

- Online status  
- Order acceptance  
- Slot activity  

❌ **Fraud Example**

- Rider offline before disruption  
→ ❌ No payout  

---

#### 🤖 Layer 5: Behavioral Analysis (AI Layer)

🎯 **Purpose**  
Detect suspicious claim patterns over time  

📊 **Signals**

- High claim frequency  
- Repeated claims in same pattern  
- Claims without corresponding disruption  

🚨 **Actions**

- Reduce reputation score  
- Increase premium  
- Flag for manual review  

---

### 9.4 🚫 Fraud Scenarios & Handling

---

#### 🔴 Scenario 1: Peak Hour Gaming (Food)

- Rider logs in only during rain  
- No prior activity  

→ ❌ Flagged as suspicious  
→ Reduced payout / rejection  

---

#### 🔴 Scenario 2: Fake Zone Claim

- Rider claims flood in Koramangala  
- GPS shows Whitefield  

→ ❌ Rejected  

---

#### 🔴 Scenario 3: Ghost Orders (Quick Commerce)

- Claims store shutdown  
- Platform shows active assignments  

→ ❌ Rejected  

---

#### 🔴 Scenario 4: Slot Manipulation (E-commerce)

- Rider skips slot intentionally  

→ ❌ No payout  

---

### 9.5 📐 Claim Validation Flow

```
Trigger Activated
↓
Check Eligibility (Section 4)
↓
Validate GPS Location
↓
Check Platform Data
↓
Validate Activity Status
↓
Run Behavioral Analysis
↓
IF ALL PASS
→ APPROVED → PAYOUT

ELSE
→ REJECTED

```
---

### 9.6 ⚖️ Claim Confidence Score (Advanced Layer)

🧠 **Concept**

Each claim is assigned a **confidence score (0–100):**


Confidence Score =
0.30 × GPS Accuracy +
0.30 × Platform Data Match +
0.20 × Activity +
0.20 × Behavior


---

#### 📊 Decision Logic

| Score   | Action        |
|---------|--------------|
| ≥ 80    | Auto-approve |
| 50–80   | Review       |
| < 50    | Reject       |

---

### 9.7 🔁 Feedback Loop to Premium Model

Fraud detection directly impacts pricing:

- Frequent claims → **Higher premium**  
- Clean history → **Discounts**  

---

## 10. Policy Limits & Renewal (Policy Lifecycle Management)

---

### 10.1 🎯 Overview

This section defines:

- 📊 How long the policy lasts  
- 🔄 How it renews  
- 💰 Limits on payouts  
- ⚖️ Financial sustainability of the system  

🧠 **Core Principle**

> The policy operates as a **dynamic weekly subscription model** with controlled payout exposure.

---

### 10.2 📅 Policy Duration

#### ⏱ Standard Duration

- Each policy is valid for **7 days (1 week)**  

---

#### 🕒 Timeline

| Event        | Time           |
|--------------|----------------|
| Policy Start | Monday 00:01   |
| Policy End   | Sunday 23:59   |

---

🧠 **Why Weekly?**

- Matches dynamic risk changes (weather, demand)  
- Enables frequent premium updates  
- Keeps the system responsive and fair  

---

### 10.3 🔄 Policy Renewal Mechanism

#### ⚙️ Automatic Renewal

- Policies are **auto-renewed every week**  
- Premium recalculated dynamically (**Section 7**)  

---

#### 💳 Payment Method

- Auto-debit (UPI / Bank)  

---

#### 📌 Renewal Flow

```
End of Week
↓
Recalculate Risk (AI + Data)
↓
Generate New Premium
↓
Notify Rider
↓
Auto-Debit
↓
Policy Renewed

```
---

#### ❌ Renewal Failure Cases

- Insufficient balance  
- Payment failure  
- User disables auto-renew  

→ Policy becomes **INACTIVE**

---

### 10.4 ⏸ Policy Pause Option

#### ✅ Allowed

- Rider can pause policy for the **next cycle**

---

#### 📌 Conditions

- Must pause before renewal time  
- No coverage during paused period  

---

🧠 **Use Case**

- Rider on leave  
- Temporary inactivity  

---

### 10.5 💰 Payout Limits (Financial Control)

🎯 **Purpose**

- Prevent system abuse  
- Ensure long-term sustainability  

---

#### 📊 10.5.1 Weekly Payout Cap

Each rider has a **maximum payout limit per week**:

| Category            | Weekly Cap     |
|--------------------|---------------|
| 🍔 Food            | ₹800–₹1200    |
| 🛒 Quick Commerce  | ₹700–₹1000    |
| 📦 E-commerce      | ₹1000–₹1500   |

🧠 **Basis**

- Based on average weekly earnings  
- Prevents over-compensation  

---

#### 📊 10.5.2 Per-Event Cap

Limits payout for a **single disruption event**:

| Category | Cap          |
|----------|-------------|
| Food     | ₹200–₹300   |
| Quick    | ₹300–₹400   |
| E-commerce | ₹400–₹600 |

🧠 **Reason**

- Avoid extreme payouts  
- Maintain fairness  

---

### 10.6 ⚖️ Fair Usage Policy

🚨 **Rules**

- Multiple small claims allowed  
- Repeated high claims flagged  
- Suspicious patterns → reviewed  

---

#### 📌 Example

- 5 claims in a day → flagged  
- Same pattern repeated → premium increased  

---

### 10.7 🔁 Renewal-Based Adjustments

📈 **Premium Changes Based On:**

- Risk exposure  
- Claim frequency  
- Behavior score  

---

#### 📉 Example

| Scenario        | Premium Impact |
|----------------|----------------|
| High claims    | +15%           |
| Clean history  | −10%           |
| Low risk week  | Reduced        |

---

### 10.8 🔐 Policy Status States

#### 📊 States

| Status    | Meaning                    |
|-----------|----------------------------|
| ACTIVE    | Eligible for coverage      |
| INACTIVE  | No coverage                |
| PAUSED    | Temporarily disabled       |
| EXPIRED   | Renewal failed             |

---

### 10.9 🧠 System-Level Lifecycle


New → Active → (Paused / Expired) → Renewed → Active
---

## 11. Tech Stack & Architecture

### 11.1 Platform Decision: Web (Progressive Web App)

**Rationale:**
- Delivery riders use Android phones with limited storage; native app installation friction is high
- PWA installs like an app but serves via browser — no Play Store dependency
- Web platform allows instant updates without version fragmentation
- Admin dashboard (insurer view) is naturally web-first

**Two Interfaces:**
1. **Rider PWA** — Mobile-first, Kannada/Hindi/English, simple 3-screen flow
2. **Admin Web Dashboard** — Full analytics, fraud review queue, risk monitoring

### 11.2 Full Tech Stack

**Frontend:**
```
Rider PWA:         React + Vite + TailwindCSS + PWA manifest
Admin Dashboard:   React + Vite + TailwindCSS + Recharts / Nivo
State Management:  Zustand
API Layer:         Axios + React Query (caching + background refetch)
```

**Backend:**
```
Runtime:           Node.js (Express) — Phase 1-2
                   FastAPI (Python) — ML microservice
API Style:         REST (primary) + WebSocket (real-time disruption push)
Auth:              JWT + Refresh Token rotation
```

**Database:**
```
Primary DB:        PostgreSQL (riders, policies, claims, payouts)
Cache:             Redis (real-time risk scores, session tokens, API response cache)
Time-Series:       TimescaleDB (extension on Postgres) — weather event logs, order rate history
```

**AI/ML:**
```
Premium Model:     XGBoost (scikit-learn) — retrained weekly via cron
Fraud Detection:   Isolation Forest (scikit-learn) — runs on every claim event
Serving:           FastAPI microservice, called synchronously during claim processing
Experiment Track:  MLflow (Phase 2)
```

**External APIs:**
```
Weather:           OpenWeatherMap API (current + 7-day forecast)
                   IMD Open Data Portal (backup / cross-validation)
AQI:               CPCB AQI API (aqicn.org for mock in Phase 1)
Traffic:           Google Maps Platform — Routes API + Traffic Layer
Payments:          Razorpay (test mode Phase 1-2, production Phase 3)
Platform Data:     Simulated mock API (Phase 1-2); real integration plan in Phase 3
```

**Infrastructure:**
```
Hosting:           AWS (EC2 + RDS + ElastiCache) or Render.com (Phase 1 demo)
CI/CD:             GitHub Actions
Containers:        Docker + Docker Compose (local dev)
Monitoring:        Sentry (errors) + Datadog (metrics) — Phase 2
```

### 11.3 High-Level Architecture Diagram

```
┌─────────────────────────────────────────────────────────────────┐
│                         CLIENT LAYER                            │
│   Rider PWA (React)              Admin Dashboard (React)        │
└─────────────┬───────────────────────────┬───────────────────────┘
              │ HTTPS / WSS               │ HTTPS
┌─────────────▼───────────────────────────▼───────────────────────┐
│                      API GATEWAY (Express)                       │
│  /auth  /policy  /claims  /payouts  /dashboard  /admin          │
└─────┬──────────┬──────────────┬──────────────┬──────────────────┘
      │          │              │              │
┌─────▼──┐  ┌───▼────┐  ┌──────▼──────┐  ┌───▼───────────────┐
│ Auth   │  │ Policy │  │   Claims    │  │  Disruption       │
│Service │  │Service │  │   Service   │  │  Monitor Service  │
└─────┬──┘  └───┬────┘  └──────┬──────┘  └───┬───────────────┘
      │          │              │              │
      └──────────┴──────────────┴──────────────┘
                                │
              ┌─────────────────▼──────────────────┐
              │           PostgreSQL + Redis        │
              └─────────────────┬──────────────────┘
                                │
              ┌─────────────────▼──────────────────┐
              │         ML Microservice (FastAPI)   │
              │  - Premium Calculation (XGBoost)   │
              │  - Fraud Scoring (Isolation Forest) │
              └─────────────────┬──────────────────┘
                                │
              ┌─────────────────▼──────────────────┐
              │           External APIs             │
              │  OpenWeatherMap | CPCB | Google Maps│
              │  Razorpay | Platform Mocks          │
              └────────────────────────────────────┘
```

## 12. Development Plan & Milestones

### Phase 1 (March 4–20): Ideation & Foundation ✅ IN PROGRESS
- [x] All 3 persona policy documents complete
- [x] Technical architecture defined
- [x] DB schema designed
- [x] API contracts defined
- [x] Adversarial defense strategy documented
- [ ] GitHub repo setup with this README
- [ ] 2-minute strategy video recorded

### Phase 2 (March 21 – April 4): Automation & Protection
**Week 3:**
- Rider onboarding flow (PWA)
- Policy creation + Razorpay test mode payment
- Weather API integration (OpenWeatherMap)
- Basic disruption monitor (cron job, every 15 min)

**Week 4:**
- Dynamic premium calculation (XGBoost model — trained on synthetic data)
- Auto-claim trigger on disruption threshold breach
- Fraud scoring (Isolation Forest — Phase 1 version)
- UPI mock payout flow
- Claims management UI

### Phase 3 (April 5–17): Scale & Optimise
**Week 5:**
- Advanced GPS spoofing detection (accelerometer + cell tower mismatch)
- ZDCI (Zone Disruption Confirmation Index) implementation
- Claim Burst Index for coordinated ring detection
- Admin fraud review dashboard
- Simulated Razorpay payout with real test mode transactions

**Week 6 (Final):**
- Full admin analytics dashboard (loss ratios, zone risk heat map, weekly forecast)
- Worker dashboard (earnings protected, coverage status)
- 5-minute demo video with simulated rainstorm trigger
- Final pitch deck (PDF)
- End-to-end E2E test suite

---
## 13. 📲 Platform Justification (Web vs Mobile)

### ✅ Final Decision: **Mobile App First Approach**

---

### 13.1 🎯 Overview

GigShield is designed for **delivery partners who operate entirely on the move**.  
Their interaction with any system must be:

- ⚡ Instant  
- 📍 Location-aware  
- 📱 Always accessible  

Given this context, a **mobile-first platform** is not just preferred — it is **essential**.

---

### 13.2 🧠 Core Rationale

> 💡 Delivery partners live on their phones, not desktops.

A mobile app aligns directly with how riders:

- Accept orders  
- Navigate routes  
- Track earnings  
- Communicate with platforms  

---

### 13.3 📊 Web vs Mobile Comparison

| Factor                     | 🌐 Web Platform              | 📲 Mobile App (Chosen)        |
|--------------------------|-----------------------------|-------------------------------|
| Accessibility            | Requires browser            | Always available              |
| Real-time interaction    | Limited                     | Instant & seamless            |
| GPS integration          | Weak                        | Strong (native support)       |
| Push notifications       | Limited                     | Real-time alerts              |
| Offline capability       | Minimal                     | Supported                     |
| Ease of use (on road)    | Poor                        | Optimized for riders          |
| Background processing    | Not reliable                | Fully supported               |
| Sensor integration       | Limited                     | Full (GPS, motion, etc.)      |

---

### 13.4 🚴 Rider-Centric Requirements

Delivery partners require:

- 📍 **Live GPS tracking** for validation  
- 🔔 **Instant notifications** for payouts and disruptions  
- ⚡ **Quick access** without login friction  
- 🔄 **Background activity tracking** during deliveries  

👉 These are **natively supported only on mobile platforms**.

---

### 13.5 ⚙️ System-Level Advantages of Mobile

#### 📍 1. Real-Time GPS Validation

- Continuous location tracking  
- Accurate zone validation  
- Fraud prevention (no spoofing anomalies)

---

#### 🔔 2. Instant Trigger Notifications

- Disruption alerts  
- Payout confirmations  
- Policy updates  

---

#### ⚡ 3. Background Execution

- Risk monitoring runs silently  
- No need for user interaction  
- Ensures zero-touch experience  

---

#### 📡 4. Seamless API Integration

- Weather, AQI, traffic APIs  
- Platform data sync  
- Real-time decision making  

---

#### 💳 5. Integrated Payments

- UPI-based instant payouts  
- Auto-debit for premiums  
- Secure and fast transactions  

---

### 13.6 🧩 User Experience Advantages

- One-tap policy activation  
- Real-time earnings visibility  
- Clear payout breakdown  
- Minimal cognitive load while working  

🧠 Designed for **speed, clarity, and zero distraction**

---

### 13.7 🔐 Security & Fraud Prevention Benefits

Mobile enables stronger validation through:

- GPS verification  
- Device-level authentication  
- Continuous activity tracking  

👉 Significantly reduces fraud compared to web-based systems

---

### 13.8 🚀 Scalability & Future Scope

Mobile-first architecture enables:

- Integration with delivery apps (SDK/API)  
- Real-time analytics dashboards  
- AI-driven notifications  
- Wearable integration (future)  

---

### 13.9 ⚖️ Why Not Web?

❌ Web platforms fail in:

- Real-time tracking  
- Background execution  
- Seamless notifications  
- On-the-move usability  

👉 A web-only solution would **break the core value proposition of GigShield**


---
## 14. 🛡️ Adversarial Defense & Anti-Spoofing Strategy
---

### 14.1 🚨 Crisis Overview: Market Exploit Scenario

A critical vulnerability was identified in parametric insurance systems:

> ⚠️ **Mass GPS Spoofing Attack by Coordinated Delivery Workers**

#### 📉 What Happened

- A group of **500 delivery workers** formed coordinated Telegram groups  
- Used **GPS spoofing applications** to fake location data  
- Simulated presence in:
  - 🌧 Heavy rain zones  
  - 🔴 High-risk disruption areas  

#### 💣 Attack Outcome

System falsely detected:
- Severe environmental conditions  
- Active riders in affected zones  

➡️ **Trigger engine activated → Mass false payouts issued**

#### 🚨 Impact

- 💰 Instant liquidity drain  
- 📉 System exploitation at scale  
- ❌ Traditional GPS validation failed completely  

---

### 14.2 🧠 Core Problem

> ❗ **GPS-based verification alone is no longer reliable**

#### ❌ Why Traditional Systems Fail

GPS spoofing apps can:
- Fake coordinates  
- Simulate movement  
- Bypass basic validation checks  

#### 🔥 New Threat Model

| Threat              | Description                         |
|--------------------|-------------------------------------|
| Location Spoofing  | Fake GPS coordinates                |
| Coordinated Fraud  | Multiple users attacking together   |
| Idle Exploit       | Claiming while sitting at home      |
| Data Manipulation  | Faking environmental presence       |

---

### 14.3 🎯 Solution Overview

GigShield introduces a **multi-dimensional AI-driven anti-spoofing system**:

> 🔐 Location is validated using **behavioral, environmental, and system-level signals** — not just GPS

---

### 14.4 🧱 Multi-Layer Anti-Spoofing Architecture

```
    Input Layer
    ↓
    GPS + Accelerometer + Network + Platform Logs
    ↓
    Validation Layer
    ↓
    Movement + Behavior + Context Analysis
    ↓
    AI Detection Layer
    ↓
    Anomaly Detection Models
    ↓
    Decision Engine
    ↓
    Approve / Flag / Reject
```

### 14.5 🧩  Differentiation Strategy (AI-Based Detection)

### 🧠 Objective

Differentiate between:

✅ Genuine stranded delivery partner

❌ Coordinated spoofing attacker

### 🔍 Key Idea

- Real riders → natural movement + behavioral consistency

- Fake riders → synthetic/static patterns

### 🤖 AI Models Used

- Isolation Forest → anomaly detection

- LSTM → movement pattern validation

- Graph-based clustering → detect coordinated fraud

### 🚨 Detection Signals
- Signal	Genuine Rider	Spoofed Rider
- Movement	Continuous	Static / artificial
- Speed Variation	Natural	Constant / unrealistic
- Order Activity	Present	Absent
- Behavior Pattern	Random	Repetitive

### 14.6 📊  Advanced Data Signals (Beyond GPS)
📡 Multi-Sensor Data Fusion

GigShield uses multiple data sources simultaneously:

### 📍 Location Layer

- GPS coordinates

- Network triangulation

- WiFi signals

### 📱 Device Sensors

- Accelerometer (movement detection)

- Gyroscope (direction changes)

### 📶 Network Signals

- Network latency

- Signal strength variation

- Tower switching

### 📊 Platform Data

- Order acceptance

- Delivery completion

- Route consistency

### 🧠 Insight

❗ Fake GPS ≠ Fake movement, network, and behavior simultaneously

### 14.7 🤝 Coordinated Fraud Detection (Graph Intelligence)
### 🧠 Problem

Fraud is not individual — it is group-based

### 🔍 Solution

Build interaction graphs of riders

Detect:

- Same location clusters

- Same claim timing

- Identical behavior

### 🚨 Example
500 riders
→ Same zone
→ Same time
→ No movement

→ FLAGGED AS FRAUD CLUSTER

### 14.8 ⚖️  UX Balance Strategy (Fairness Layer)
### 🎯 Challenge

Avoid penalizing genuine riders during real disruptions

### ✅ Solution
- Scenario	Action
- High confidence fraud	Reject
- Medium confidence	Flag + delay payout
- Low confidence	Approve
  
### 🧠 Smart Handling

- Soft flags instead of immediate rejection

- Partial payouts allowed

- Appeal/review mechanism

### 14.9 📐 Anti-Spoofing Decision Logic

IF (GPS valid)
AND (Movement valid)
AND (Platform activity valid)
AND (Behavior normal)
→ APPROVE

ELSE IF suspicious
→ FLAG

ELSE
→ REJECT

---
