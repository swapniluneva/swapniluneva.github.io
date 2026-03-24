---
layout: default
title: User Guide
---

# User Guide

**Who this is for:** Everyone who uses Application day-to-day — from supervisors placing orders to facility operators running the till. No technical knowledge required.

---

## What is Application?

Application is a system for managing stock and sales across multiple shop locations.

It tracks the full journey of every product — from the moment it is ordered from a supplier, through the warehouse, out to each shop, and finally sold to a customer. Every person in the business has their own role and sees only what they need to do their job.

---

## The Big Picture

Think of the business as having three layers:

```
SUPPLIER  →  WAREHOUSE  →  SHOP (Facility)  →  CUSTOMER
```

1. A **Supervisor** orders goods from a supplier using a Purchase Order.
2. The goods arrive at the **Warehouse**. A Warehouse Manager records them and then sends them to the right shop.
3. The shop (**Facility**) receives the stock. A Facility Operator sells it to customers at the till.
4. An **Accountant** records payments to suppliers and keeps the finances in order.
5. An **Admin** manages users, settings, and the overall system.

Each step is tracked, so you always know exactly where stock is and what has been paid.

---

## Who Does What

### Supervisor
The Supervisor manages the product catalogue and purchasing.

**Typical tasks:**
- Add new products to the system (name, price, unit)
- Create Purchase Orders to buy stock from suppliers
- Review and approve orders before they are sent for fulfilment
- Monitor stock levels and facility performance from the overview dashboard
- Manage vendors (suppliers), warehouses, and facilities

---

### Warehouse Manager
The Warehouse Manager is responsible for stock once it arrives at the warehouse.

**Typical tasks:**
- Mark a Purchase Order as received when the goods arrive — this adds the stock to the warehouse
- Send stock to a shop by creating a Dispatch
- Mark a dispatch as "In Transit" once it leaves the warehouse
- View current stock levels at the warehouse

---

### Facility Operator
The Facility Operator runs the day-to-day operation of a shop.

**Typical tasks:**
- Confirm receipt of stock when a dispatch arrives from the warehouse
- Sell products to customers using the Point of Sale (POS) screen
- Process returns from customers
- View the day's sales summary at the end of each day

---

### Accountant
The Accountant handles all financial transactions.

**Typical tasks:**
- Record payments made to suppliers (against a Purchase Order)
- Settle outstanding supplier balances
- View the purchase daybook (a chronological log of all purchases and payments)

---

### Admin
The Admin has full access to everything.

**Typical tasks:**
- Create and manage user accounts
- Configure system settings (e.g. which vendor to use for direct stock transfers)
- Toggle features on or off (e.g. enabling direct stock adjustments at facilities)

---

## Key Concepts in Plain English

### Product
A product is any item sold in your shops. Products are defined once in a central catalogue and can be stocked at any number of shops. The selling price is set on the product and cannot be changed at the till — this ensures price consistency across all locations.

### Vendor
A vendor is a supplier — the company or person you buy stock from. Each Purchase Order is linked to a vendor, so you always know who supplied which goods.

### Warehouse
The warehouse is where stock is held before it is sent to shops. Stock sits in the warehouse until a Warehouse Manager dispatches it.

### Facility (Shop)
A facility is an individual shop or outlet. Each facility has its own stock — stock at one shop cannot be used to sell at another.

### Purchase Order (PO)
A Purchase Order is a formal request to buy stock from a vendor. It goes through an approval process before the goods are received:

```
Draft  →  Submitted  →  Approved  →  Received
```

Stock does not enter the warehouse until the PO reaches **Received** status.

### Dispatch
A dispatch is the movement of stock from the warehouse to a shop. Once a dispatch is created, stock immediately leaves the warehouse. The shop operator then confirms the exact quantity received.

```
Pending  →  In Transit  →  Confirmed
```

### Stock at a Shop
Stock only becomes available for sale at a shop after a dispatch has been **confirmed** by the facility operator. Even if the warehouse has plenty of stock, the shop cannot sell it until it has been formally received.

### Sale (POS)
A sale is recorded at the till when a customer buys something. The system automatically deducts the sold quantity from the shop's stock. The selling price is always pulled from the product catalogue — the operator cannot change it at the till.

### Return
If a customer returns an item, the Facility Operator records a return. The stock is added back to the shop's inventory automatically.

### Payment (to a Supplier)
After receiving goods from a vendor, the Accountant records payments against the Purchase Order to track what has been paid and what is still outstanding.

---

## Common Workflows

### How stock gets from a supplier to the till

1. **Supervisor** creates a product in the catalogue (if it doesn't exist yet).
2. **Supervisor** raises a Purchase Order — selects the vendor, warehouse, and products with quantities.
3. **Supervisor** submits and approves the PO.
4. **Warehouse Manager** marks the PO as **Received** when the goods arrive — the stock now sits in the warehouse.
5. **Warehouse Manager** creates a **Dispatch** to send stock to the target shop, then marks it **In Transit**.
6. **Facility Operator** confirms receipt when the goods arrive at the shop — the stock is now available at the till.
7. Customers can now be served at the **POS**.

---

### How a sale works at the till

1. Facility Operator opens the **POS** screen.
2. Adds products to the cart — only products with stock available are shown.
3. Enters customer details (optional) and selects the payment method (Cash, Card, UPI, or Bank Transfer).
4. Completes the sale. The stock is deducted automatically.

---

### How a return is processed

1. Facility Operator goes to **Sale Returns**.
2. Looks up the original sale (optional — returns can also be recorded without a linked sale).
3. Records the product, quantity, and reason.
4. The stock is added back to the shop automatically.

---

### How a supplier is paid

1. Accountant opens **Payments** or **Vendor Settlement**.
2. Selects the vendor and the Purchase Order being paid against.
3. Enters the amount and payment method.
4. The vendor's outstanding balance is updated.

---

### What happens at the end of the day

The Facility Operator opens the **Day Summary** for their shop. This shows:
- Total sales for the day
- Breakdown by payment method
- Number of transactions
- Any returns processed

This summary helps reconcile the till at closing.

---

## Things to Know

### Stock is tracked per shop
Each shop has its own independent stock. If Shop A has 100 units and Shop B has 0, you cannot sell from Shop A's stock at Shop B. Stock must be dispatched to each shop individually.

### Prices are controlled centrally
The selling price of every product is set by the Supervisor in the product catalogue. Facility Operators cannot change prices at the till. Any price change is recorded automatically with the date and the old value, so there is always a full history.

### Stock leaves the warehouse on dispatch, not on arrival
The moment a Warehouse Manager creates a dispatch, that stock is removed from the warehouse count. It has not yet arrived at the shop — but it is no longer available to dispatch again. This prevents double-dispatching the same stock.

### Partial deliveries are supported
If a dispatch of 50 units arrives at a shop but only 40 are in good condition, the Facility Operator can confirm receipt of just 40. The dispatch will be marked as **Partially Received**. The remaining 10 units are not automatically returned to the warehouse — they must be handled manually.

### Every action is recorded
TradeCore keeps a complete audit trail. Every stock movement, sale, return, and payment is logged with who did it and when. Nothing can be silently changed.

---

## Frequently Asked Questions

**Why can't I see a product at the POS?**
The product either has no stock at your shop, or stock has not yet been received from a dispatch. Check with your Warehouse Manager whether a dispatch is in transit.

**Why can't I change the price at the till?**
Prices are set centrally by the Supervisor to ensure consistency. Contact your Supervisor to update the price in the product catalogue.

**A dispatch arrived but I can't see it to confirm it — why?**
The Warehouse Manager needs to mark the dispatch as **In Transit** before it appears for confirmation at the facility. Follow up with the warehouse.

**I made a sale with the wrong quantity — can I fix it?**
Sales cannot be edited once completed. Process a return for the difference and record a new sale with the correct quantity.

**What is the "Direct Transfer (System)" vendor I see in Purchase Orders?**
This is an internal system vendor used automatically when a Warehouse Manager records stock directly (outside of a formal Purchase Order). You do not need to interact with it directly.
