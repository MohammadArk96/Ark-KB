---
id: order-screen
title: 📋 Order Screen
sidebar_label: 'Order Screen'
slug: /order-screen
sidebar_position: 3
tags: [orders, trading, pending orders, SL, TP]
keywords: [pending orders, buy limit, sell stop, stop loss, take profit, trader tools]
description: A full guide for monitoring and managing pending trading orders including stop loss, take profit, and execution behavior.
--------------------------------------------------------------------------------------------------------------------------------------

# 📋 Order Screen Overview

Welcome to the **Order Screen** — your central hub for tracking and managing all six types of pending orders in detail.

![Order Screen](https://arktechltd.com/Knowledgebase/OrderScreen.png)

\:::info What does the Order Screen do?
This screen displays and manages the following pending order types:

* **Buy Limit**
* **Sell Limit**
* **Buy Stop**
* **Sell Stop**
* **Stop Loss (SL)**
* **Take Profit (TP)**
  \:::

## 🧾 Key Data Fields

### 📌 Script Name

The name of the instrument for which the order is placed.

### 🔢 Order Number

A unique, non-duplicate identifier for each pending order.

### 🕒 Date/Time

The timestamp (in milliseconds) indicating when the order was created.

### 💰 Amount

The amount the trader specifies to open or close the order with.

### 🎯 Pending Price

The target price at which the order is intended to be triggered.

### 📉 Current Price

* For **Buy orders** (Buy Limit / Buy Stop): shows the **Ask** price.
* For **Sell orders** (Sell Limit / Sell Stop): shows the **Bid** price.
* **SL/TP** depends on the type of deal.

### 🛑 Stop Loss (SL)

If the order is:

* **Buy** → SL must be *lower* than the market price.
* **Sell** → SL must be *higher* than the market price.

💡 *Double-click the SL cell to set or update the Stop Loss value.*

### 🎯 Take Profit (TP)

If the order is:

* **Buy** → TP must be *higher* than the market price.
* **Sell** → TP must be *lower* than the market price.

💡 *Double-click the TP cell to set or update the Take Profit value.*

### 💬 Comment

Notes from the trader, added from desktop or mobile for future reference. Useful for logging reasons like news or gold price moves.

---

## ⚠️ Order Execution Notes

\:::warning Important
Even if the last price touches the pending price, the order might not trigger:

* If the **Last Price** is not broadcast as a **Bid** or **Ask**, the order won’t hit.
* Some brokers only allow triggering based on **Bid/Ask**.
* Others also include **High/Low** — depends on your **Dealing Room Configuration**.
  \:::

If SL is hit with the full amount, the open deal is closed completely and any TP on the same deal is automatically canceled.

---

## 🧰 Menu Options

### 🔄 Update Order

Opens the [Quotes Screen](https://help.arktechltd.com/index.php?/Knowledgebase/Article/View/2/1/quotes-screen) to modify SL or TP.

![Update Order](https://arktechltd.com/Knowledgebase/UpdateOrder.png)

### ❌ Cancel Checked Orders

Cancel one or multiple selected orders with a single action.

### 📈 Go To Market

Converts the pending order into a market order instantly based on current market price.

### 🔤 Font Settings

Customize font type, size, and appearance.

![Font Settings](https://arktechltd.com/Knowledgebase/FontSettings.png)

### 📊 Column Chooser

Use drag-and-drop to hide columns. To restore, double-click the column name in the popup.

![Column Chooser](https://arktechltd.com/Knowledgebase/ColumnChooser.png)

### 📤 Export / Auto Arrange

More features available in the [Export & Arrange article](https://help.arktechltd.com/index.php?/Knowledgebase/Article/View/43).

---

Need help? Visit the [Order Screen Help Page](https://help.arktechltd.com/index.php?/Knowledgebase/Article/View/4/5/order-screen).
