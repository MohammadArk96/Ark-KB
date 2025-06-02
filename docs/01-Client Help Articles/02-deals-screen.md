---
id: deals-screen
title: 📊 Deals Screen
sidebar_position: 2
description: Monitor and manage all your active trading deals in real-time.
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import Admonition from '@theme/Admonition';

# 📊 Deals Screen Overview

Welcome to the **Deals Screen** — your central dashboard for monitoring **live trading activity** with precision. This screen gives you deep insight into all open trades including their values, margins, profits, and actions.

![Deals Screen UI](https://arktechltd.com/Knowledgebase/Client'sdealsscreen.png)

<Admonition type="tip" title="Live Trading Control Center">
Track, adjust, and manage every trade you open. From SL/TP to custom notes — it's all here.
</Admonition>

---

## 🧾 Deal Information at a Glance

Each row represents an open deal with detailed attributes:

| Field | Description |
|-------|-------------|
| **Script Name** | The asset involved in the deal |
| **Ticket ID** | Unique ID for the trade |
| **Date / Time** | Timestamp of trade request (milliseconds) |
| **Buy / Sell** | Trade direction |
| **Amount** | Volume of the trade |
| **Open Price** | Entry price for the deal |
| **Current Price** | Real-time price (Bid for Buy, Ask for Sell) |
| **Open Commission** | Broker fee applied at opening |
| **Used Margin** | Funds locked as collateral |
| **PnL** | Profit & Loss calculated live |
| **Value** | Cost: `Amount × Contract × Open Price` |
| **Comment** | Trader remarks (e.g., "News-based", "OneClick") |

---

## 🎯 SL / TP Configuration

<Tabs>
<TabItem value="stop-loss" label="🛑 Stop Loss (SL)" default>

**Stop Loss** allows automatic closing at a set loss threshold.

- **Buy Deal** ➜ SL must be **below** market price.
- **Sell Deal** ➜ SL must be **above** market price.

💡 *Double-click the SL cell to apply.*

</TabItem>
<TabItem value="take-profit" label="💰 Take Profit (TP)">

**Take Profit** allows automatic closing when reaching a set profit.

- **Buy Deal** ➜ TP must be **above** market price.
- **Sell Deal** ➜ TP must be **below** market price.

💡 *Double-click the TP cell to apply.*

</TabItem>
</Tabs>

---

## ⚙️ Actions Menu

### 📌 Right-Click Options

You can right-click on any deal to access:

#### 📍 Place SL/TP Order

![Place SLTP Order](https://arktechltd.com/Knowledgebase/PlaceAnSLTPOrder.png)

```txt
✔ Validate price rules based on direction.
✔ Submit partial or full amount.
✔ Add optional comments (shown in History screen).
```

#### ✅ One-Click Features

Provided (if broker allows):

- **Close Checked**: End multiple trades instantly.
- **Duplicate Checked**: Copy selected trades in same direction.
- **Hedge Checked**: Create opposite direction trades.

### 🧠 Smart Selection

You can filter open trades and apply actions:
- All Deals
- Profitable Only
- Unprofitable Only

![Filter & Select](https://arktechltd.com/Knowledgebase/Client'sdealsscreenselectmenu.png)

---

## 🎨 Personalize Your Interface

### ✏️ Font Settings

![Font Settings](https://arktechltd.com/Knowledgebase/FontSettings.png)  
Customize font type, size, and display — just for this screen.

### 🧩 Column Chooser

![Column Chooser](https://arktechltd.com/Knowledgebase/ColumnChooser.png)

Drag and drop columns to hide or re-show them. A minimalist layout is one click away.

---

## 📤 Export & Layout Tools

- **Export To** – Export table data to different formats  
- **Auto Arrange [A]** – Neatly auto-align all columns

[Learn more ➜](https://help.arktechltd.com/index.php?/Knowledgebase/Article/View/43)

---

<Admonition type="info" title="Need Help?">
If any options are not available, contact your broker to enable advanced actions or permissions.
</Admonition>