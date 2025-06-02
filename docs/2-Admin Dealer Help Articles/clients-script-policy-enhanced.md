---
sidebar_label: 'Client Script Policy'
sidebar_position: 1
slug: /clients-script-policy
tags: [script, policy, trading, admin]
keywords: [client script policy, Ark Trader, script config, commission, stop offset]
description: Master your client trading parameters using the Client Script Policy system in Ark Trader.
---

# 📜 Client Script Policy

> 📅 *Posted by **Iyad Yasser** on 23 May 2022, 05:19 PM*

Welcome to the **Client Script Policy** interface in **Ark Trader** — a powerful admin-level tool to control script behavior, enforce constraints, and define trading boundaries for your clients.

![Policy Overview](/img/arkimgs/ClientsScriptPolicyList.png)

---

## 🧩 Overview

> A single policy applies to multiple accounts. If you need to customize for one account only:
- Duplicate the policy (rename & press **Add**)
- Customize the parameters
- Assign it via `Edit Account(s)`

---

## 📂 Grouping Policies

Group your policies for clarity:

- By product: *Comex*, *Stocks*, etc.
- By region: *USA*, *Europe*
- Or any structure matching your needs

---

## ⚙️ Policy Parameters

### 🔢 1. Commission Settings

```toggle
### Commission Types

- **Open Commission**
- **Close Commission**
- **Intraday Commission**

💡 *Intraday*: Applies when open & close occur on the same day.

🧮 Example Calculation:
- Lot Size: 2
- Open: 5, Close: 5, Intraday: 3

```text
Open = 2 × 5 = 10  
Close = 2 × 5 = 10  
Intraday = 2 × 3 = 6  
Total = 26
```

### Commission Methods

- **FIXED**: Value × Lot Size  
- **Point**: `Decimal Digits × Contract Size × Commission Points × Lots`  
- **Percentage**: `Contract Size × Lot Size × Price × (Percentage / 100)`

📌 Example (0.2% on 100,000 AUD, Lot Size 2, Price 0.71929):
`100,000 × 2 × 0.71929 × 0.002 = 287.716`
```

---

### 🛑 2. Limit/Stop Offset

```toggle
### Offset Rules

Control how far orders must be from market price.

- **Limit Offset**: Buy/Sell Limit, Take Profit
- **Stop Offset**: Buy/Sell Stop, Stop Loss

#### Offset Type: FIXED

- Entry/Exit not allowed if order price < Market Price - Offset
- Exit not allowed if order price > Market Price + Offset

#### Offset Type: High/Low

- Uses High/Low reference instead of Bid/Ask

#### DPR %

Limit order price range by % of previous close  
Example: Close = 1000, DPR = 10% ⇒ Range: 900–1100
```

---

### 💰 3. Deal Constraints

```toggle
### Trade Amount Rules

- **Minimum Amount Per Deal**
- **Maximum Amount Per Deal**
- **Max Quantity**
- **Amount Jump**

🧠 Amounts must be multiples of the jump value.

📌 Example:
- Jump: 0.5 ⇒ Allowed: 1.0, 1.5, 2.0...

💡 Max Quantity enforces net exposure control.
```

---

### 🧾 4. Required Margin

```toggle
### Margin Options

Type:
- **Percentage**: `Contract × Amount × Price × %`
- **Fixed**: Exact margin value locked

🧠 Margin = reserved capital per deal
```

---

### ⏱️ 5. Holding Margin

```toggle
Used to liquidate margin overuse by time or settings in the Space Station.

- Clients not meeting margin can still carry to next day.
- Controlled via:
  - Client Script Policy
  - Holding Liquidation (Generic Policy)
  - Holding Time (Space Station Settings)
```

---

### 📉 6. Spread Management

```toggle
### Spread Configuration

- **Source + Value**: Spread added from feed provider
- **Fixed**: Defined BID/ASK difference

#### Calculation Modes

- **From Bid**:
  - Ask = Bid + Spread
- **From Average**:
  - BID = (Bid + Ask)/2 - spread/2
  - ASK = (Bid + Ask)/2 + spread/2

### Spread Balance

Adjust BID/ASK with +/− pips
```

---

### 👁️ 7. Visibility

Set script visibility to **True** or **False** for this policy.

---

### 🛒 8. Can Buy / Can Sell

```toggle
Control trade types:
- Buy Only (e.g., Metal shops)
- Sell Disabled
- Both Disabled ⇒ Close-only mode
```

---

### 🚫 9. Block Trade

```toggle
Set block window (e.g., 5 sec) to prevent scalping or fast reverse trades.

- Prevents immediate Buy/Sell/Close
- Protects dealing room from pip-traders
```

---

### 📦 10–16. Management Utilities

```toggle
- **10. Policy**: Master list of all script values
- **11. Groups**: Drag & drop for structured views
- **12. Select All**: Mass edit values across scripts
- **13. Update**: Modify name/values for policies or scripts
- **14. Add**: Clone or create new policies
- **15. Delete**: Remove unused groups or unassigned policies
- **16. Close**: Exit policy screen
```

---

## 🧠 Pro Tips

- 💡 Always **duplicate** before editing shared policies
- 🔍 **Group wisely** for fast policy assignment
- 📋 **Audit trail**: Keep record of all changes

---

## 📚 Related Articles

- [Client Generic Policy](https://help.arktechltd.com/index.php?/Knowledgebase/Article/View/27)
- [Space Station Settings](https://help.arktechltd.com/index.php?/Knowledgebase/Article/View/39)
- [Script Manager Overview](https://help.arktechltd.com/index.php?/Knowledgebase/Article/View/45)

---

📩 For help, contact support or view the [original article](https://help.arktechltd.com/index.php?/Knowledgebase/Article/View/26/0/clients-script-policy)