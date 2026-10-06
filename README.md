#  ZENPAY

> **Pay Smart. Save Smarter.**

A UPI-first digital payments platform with a smart budgeting and transaction-protection layer designed to help users understand, control, and protect their everyday spending.

**🌐 Live Demo:** [ZenPay](https://zenpay-gamma.vercel.app/)
**👥 Team:** Hacksmith

---

## 🚩 The Problem

Digital payments have made transactions faster, but managing money responsibly is still difficult.

Users often face problems such as:

* **Cash Flow Blind Spot** — People don't know how much they can safely spend today without affecting the rest of the month.
* **The EMI That Ate the Salary** — Recurring payments can consume a large portion of monthly income without users noticing the long-term impact.
* **Split the Bill, Save the Friendship** — Group expenses such as trips, rent, and dinners create unnecessary calculation and settlement friction.
* **Fraudulent Refund Requests** — Refund and payment scams exploit the speed and trust associated with digital payments.
* **Credit Visibility Gap** — First-time earners and informal workers may have limited financial history.
* **Missed Financial Benefits** — Users often don't discover relevant financial assistance, benefits, or savings opportunities at the right time.

The common problem is simple:

> **People can make payments instantly, but they don't always have enough financial context before making them.**

---

# 🚀 Our Solution

**ZenPay** adds a smart financial decision layer around digital payments.

Instead of simply processing a transaction, ZenPay helps users understand its impact **before and after money moves**.

The platform combines:

* UPI payment flows
* Daily spending limits
* Real-time budget tracking
* Expense categorization
* Safe-to-Spend calculations
* Transaction risk checks
* Financial planning assistance

The goal is to move from:

**Pay → Track Later**

to:

**Understand → Decide → Pay → Track**

---

# ✨ Key Features

### 💳 UPI Payments

Send and receive money through a simulated/integrated UPI payment experience.

### 💰 Smart Budgeting

Categorize expenses and monitor where money is going in real time.

### 📊 Daily Spending Limits

Set a daily spending limit and track spending against the available amount.

### 🛡️ Money Protection Layer

Before a payment is confirmed, ZenPay checks the transaction against spending limits and behavioral signals.

Potentially risky transactions can trigger a clear warning instead of silently proceeding.

### 🧠 Safe-to-Spend

ZenPay calculates an estimated amount the user can safely spend based on their remaining budget and remaining days in the budgeting period.

### 🤖 AI Financial Planning

Provides personalized budgeting guidance based on user-provided financial information, helping users structure their spending and savings goals.

---

# 📸 Platform Showcase

## 1. 💓 The Heart — Smart Dashboard

The dashboard provides a single, easy-to-understand view of the user's financial position.

The **Daily Pulse** highlights the amount currently considered safe to spend while also displaying recent transactions and spending information.

<img width="975" height="473" alt="ZenPay Smart Dashboard" src="https://github.com/user-attachments/assets/0f269c83-983c-44df-bccd-8d4496778d35" />

---

## 2. 🛡️ The Guard — Protection Layer

The Protection Layer evaluates transactions before confirmation.

It can flag situations such as:

* Spending above the configured limit
* Unusually large transactions
* Sudden changes in spending behavior
* Suspicious refund/payment patterns

Instead of displaying a generic warning, ZenPay provides a simple explanation so the user can make an informed decision.

<img width="975" height="471" alt="ZenPay Protection Layer" src="https://github.com/user-attachments/assets/eb1e8787-7f3d-4fa7-8238-c2e592b6cbcd" />

---

## 3. 🤖 AI Architect — Financial Blueprint

The AI-powered planning experience generates a personalized financial structure based on the information provided by the user.

It can help organize income into areas such as:

* Needs
* Wants
* Savings
* Financial goals

<img width="975" height="471" alt="ZenPay AI Financial Planner" src="https://github.com/user-attachments/assets/973e84c7-758b-4132-bb83-18a40b129900" />

---

# 🔍 Transaction Risk Detection

ZenPay's protection system uses multiple signals to identify potentially risky transactions.

Examples include:

| Signal              | Purpose                                                                     |
| ------------------- | --------------------------------------------------------------------------- |
| Spending Limit      | Detects transactions exceeding the user's configured limit                  |
| Safe-to-Spend       | Checks whether the transaction could negatively affect the remaining budget |
| Spending Pattern    | Detects unusual increases compared with previous spending                   |
| Transaction Context | Evaluates suspicious payment or refund patterns                             |
| Payee Behavior      | Considers unusual or unexpected payment activity                            |

A transaction that triggers a risk condition can be paused and presented with a **plain-language warning** before confirmation.

<img width="901" height="819" alt="ZenPay Fraud Detection System" src="https://github.com/user-attachments/assets/ffd4fb75-edcf-48bc-ae72-15107a1d41ed" />

> **Note:** These checks are implemented as product-level risk signals and should not be interpreted as a replacement for production-grade banking or fraud-detection infrastructure.

---

# ⚙️ How It Works

## 1. Spend Guard Engine

ZenPay calculates the user's current safe spending amount using the remaining budget and remaining days in the budgeting period.

### Formula

```text
Safe-to-Spend Today =
Remaining Budget / Days Left in Period
```

The calculation is updated as transactions occur.

For example:

```text
Remaining Budget = ₹10,000
Days Remaining = 10

Safe-to-Spend Today = ₹10,000 / 10
                     = ₹1,000
```

If the user spends ₹500, the remaining budget changes and the calculation is updated accordingly.

---

## 2. Protection Layer

Every outgoing transaction can pass through multiple checks before confirmation.

### Risk Checks

```text
1. Does the transaction exceed the Safe-to-Spend amount?

2. Is the transaction significantly larger than the user's
   normal spending pattern?

3. Does the transaction resemble a suspicious
   payment/refund pattern?
```

If a transaction triggers a risk condition:

```text
Transaction
     ↓
Risk Evaluation
     ↓
 ┌───────────────┐
 │   Low Risk    │ → Continue Payment
 └───────────────┘

 ┌───────────────┐
 │ Potential Risk│ → Warning → User Decision
 └───────────────┘
```

This creates a **decision point before payment**, rather than simply showing users what happened after the money was already spent.

---

## 3. Adaptive Budgeting

The user's available spending amount changes dynamically as transactions occur.

```text
Payment
   ↓
Update Spending
   ↓
Recalculate Remaining Budget
   ↓
Recalculate Safe-to-Spend
   ↓
Update Dashboard
```

This allows the budgeting layer to respond to actual spending instead of relying on a fixed daily number.

---

# 🛠️ Tech Stack

### Frontend

* Next.js
* React
* TypeScript
* Tailwind CSS
* shadcn/ui

### Backend & Data

* Supabase
* PostgreSQL
* Firebase

### Deployment

* Vercel

---

# 🗂️ Project Architecture

```text
ZENPAY
│
├── Frontend
│   ├── Dashboard
│   ├── UPI Payment Flow
│   ├── Budget Management
│   ├── Transactions
│   └── AI Financial Planner
│
├── Smart Budget Engine
│   ├── Daily Limits
│   ├── Safe-to-Spend
│   └── Spending Analysis
│
├── Protection Layer
│   ├── Limit Checks
│   ├── Spending Pattern Checks
│   └── Transaction Risk Signals
│
└── Data Layer
    ├── User Data
    ├── Transactions
    └── Budget Information
```

---

# 🗺️ Accessing the Platform

### Live Application

**https://zenpay-gamma.vercel.app/**

The application opens directly into the ZenPay experience.

From the dashboard, users can:

1. View their **Safe-to-Spend** amount
2. Review recent transactions
3. Send money through the UPI flow
4. Configure their daily spending limit
5. Monitor their budget
6. Access financial planning features

There is no separate marketing page required before accessing the core product experience.

---

# 🧪 Recommended Product Demo

A simple way to demonstrate ZenPay's core value:

1. Open the dashboard.
2. Set a relatively low daily spending limit.
3. Initiate a payment above the available spending threshold.
4. Let the Protection Layer evaluate the transaction.
5. Show the plain-language warning.
6. Confirm the transaction to demonstrate that the system provides **decision support rather than silently blocking the user**.
7. Return to the dashboard and show the updated spending information.

This demonstrates the key product concept:

> **ZenPay isn't only tracking spending — it helps users make better decisions before spending.**

---

# 🚀 Local Setup

## Prerequisites

* Node.js 18+
* npm
* Git

## Clone the Repository

```bash
git clone [your-repository-url]
cd zenpay
```

## Install Dependencies

```bash
npm install
```

## Configure Environment Variables

Create a `.env.local` file in the project root.

```env
[ENV_VAR_NAME]=your_key_here
```

Add the required environment variables for the services used by the project.

## Run Development Server

```bash
npm run dev
```

Open:

```text
http://localhost:3000
```

---

# 👥 Team — Hacksmith

| Name                      | Profile                                                           |
| ------------------------- | ----------------------------------------------------------------- |
| **Pooja Santosh Sharma**  | [LinkedIn](https://linkedin.com)                                  |
| **Shreya Nitin Sankpal**  | [LinkedIn](https://www.linkedin.com/in/shreya-s-sh-ba8113411/)    |
| **Samarth Manish Shelar** | [LinkedIn](https://www.linkedin.com/in/samarth-shelar-180718439/) |

---

## 💡 Product Vision

ZenPay aims to make digital payments more financially aware.

Instead of treating every transaction as an isolated payment, the platform considers the user's **budget, spending behavior, and financial context** to help them make better decisions.

> **Pay Smart. Save Smarter.**
