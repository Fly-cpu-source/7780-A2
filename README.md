# COMP7780 Assignment 2 – Cycle 3
**Group 3 · Vitality**

---

## Prerequisites

- Node.js installed
- MySQL 8.0 installed (login as `user99`, password `user99`)

---

## Setup Steps

### Step 1 — Run SQL files (in order)

```sql
source create_user.sql
source create_db.sql
source create_tables.sql
```

### Step 2 — Install dependencies

```bash
npm install
```

### Step 3 — Start the server

```bash
node index.js
```

Server runs at `http://localhost:3000`

---

## Test Cases

| # | Action | Expected Result |
|---|---|---|
| 1 | Open `http://localhost:3000` | Home page loads |
| 2 | Click **Order Now** button | Redirects to `/product` page |
| 3 | Select a customer (e.g. `cust1`) and click **Add to Cart** on any dish | Alert: "Added to cart" |
| 4 | Click **Checkout** | Redirects to PayPal payment page |
| 5 | After adding to cart, check DB: `SELECT * FROM cart;` | New row inserted with correct cust_username, prod_id, qty, price |

---

## Test Accounts

| Customer | Username |
|---|---|
| Customer 1 | cust1 |
| Customer 2 | cust2 |
| Customer 3 | cust3 |
| Customer 4 | cust4 |

---

## Products

| Dish | Price | prod_id |
|---|---|---|
| Hakka Braised Pork | $66 | 1 |
| Honey Glazed Char Siu | $56 | 2 |
| Wok-Fried Beef | $78 | 3 |
