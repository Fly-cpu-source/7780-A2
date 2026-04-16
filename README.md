# COMP7780 Assignment 2 – Cycle 3 · Group 3 Vitality
## Tester Setup Guide

---

## Before You Start

Make sure these are installed on your computer:
- [Node.js](https://nodejs.org) — download and install the LTS version
- MySQL 8.0 — should already be installed for this course

---

## Step 1 — Set Up the Database

1. Open **MySQL Workbench** (or MySQL command line)
2. Log in with:
   - Username: `user99`
   - Password: `user99`
3. Run these 3 SQL files **one by one, in this order**:
   - Open `SQL/create_user.sql` → click Run
   - Open `SQL/create_db.sql` → click Run
   - Open `SQL/create_tables.sql` → click Run

---

## Step 2 — Install Project Dependencies

1. Open the **project folder** in File Explorer
2. Click the address bar at the top, type `cmd`, press Enter
   - This opens a black command window
3. Type the following and press Enter:
   ```
   npm install
   ```
4. Wait until it finishes (you'll see a blinking cursor again)

---

## Step 3 — Start the Website

In the same command window, type:
```
node index.js
```

You should see:
```
Server is running on port 3000
```

**Leave this window open** — closing it will stop the website.

---

## Step 4 — Open the Website

Open your browser (Chrome / Edge) and go to:
```
http://localhost:3000
```

---

## Testing Checklist

Go through each item below and tick if it works:

- [ ] **Home page loads** at `http://localhost:3000`
- [ ] Clicking **Order Now** goes to the product page
- [ ] Product page shows 3 dishes with prices
- [ ] Select a customer from the dropdown (e.g. `cust1`)
- [ ] Click **Add to Cart** on any dish — a popup says "Added to cart"
- [ ] Click **Checkout** — PayPal page appears
- [ ] In MySQL Workbench, run `SELECT * FROM cart;` — new rows appear with the correct order info

---

## Test Accounts

Use any of these customer names in the dropdown:

| Customer | Username |
|---|---|
| Customer 1 | `cust1` |
| Customer 2 | `cust2` |
| Customer 3 | `cust3` |
| Customer 4 | `cust4` |

---

## Something Went Wrong?

| Problem | Fix |
|---|---|
| `npm install` gives error | Make sure Node.js is installed. Re-download from nodejs.org |
| `node index.js` gives error | Run `npm install` first, then try again |
| Page won't open | Make sure the command window is still open and showing "running on port 3000" |
| Database error | Make sure all 3 SQL files were run in the correct order |
