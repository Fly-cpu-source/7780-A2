# COMP7780 Assignment 2 – Cycle 3 · Group 3 Vitality
## Tester Setup Guide

---

## Before You Start

Make sure these are installed on your computer:
- **Node.js** — open CMD and run:
  ```
  winget install OpenJS.NodeJS.LTS
  ```
  Wait for it to finish, then **close and reopen CMD**.
- **MySQL 8.0** — should already be installed for this course

---

## Step 1 — Open CMD

1. Press **Win + R** on your keyboard
2. Type `cmd` and press **Enter**
3. A black window (Command Prompt) will open

---

## Step 2 — Set Up the Database

In the CMD window, type these commands **one by one** and press Enter each time:

```
mysql -u user99 -puser99 < "C:\Users\26764\Desktop\7780\Assignments-20260410\Assignment 2\assignment2 project\cycle3\code\SQL\create_user.sql"
mysql -u user99 -puser99 < "C:\Users\26764\Desktop\7780\Assignments-20260410\Assignment 2\assignment2 project\cycle3\code\SQL\create_db.sql"
mysql -u user99 -puser99 < "C:\Users\26764\Desktop\7780\Assignments-20260410\Assignment 2\assignment2 project\cycle3\code\SQL\create_tables.sql"
```

> **Note:** Replace the path above with the actual folder path where you saved this project.

No error message = success. You can continue.

---

## Step 3 — Go to the Project Folder

In CMD, navigate to the project folder:

```
cd "C:\Users\26764\Desktop\7780\Assignments-20260410\Assignment 2\assignment2 project\cycle3\code"
```

> Replace the path above with your own folder path.

---

## Step 4 — Install Dependencies

In CMD, type:

```
npm install
```

Wait until it finishes. You'll see a blinking cursor again when it's done.

---

## Step 5 — Start the Website

In the same CMD window, type:

```
node index.js
```

You should see:
```
Server is running on port 3000
```

**Leave this CMD window open** — closing it will stop the website.

---

## Step 6 — Open the Website

Open your browser (Chrome / Edge) and go to:
```
http://localhost:3000
```

---

## Testing Checklist

Go through each item and check if it works:

- [ ] Home page loads at `http://localhost:3000`
- [ ] Clicking **Order Now** goes to the product page
- [ ] Product page shows 3 dishes with prices
- [ ] Select a customer from the dropdown (e.g. `cust1`)
- [ ] Click **Add to Cart** on any dish — a popup says "Added to cart"
- [ ] Click **Checkout** — PayPal payment page appears
- [ ] Open a **new CMD window** and run the command below to verify the order was saved:
  ```
  mysql -u user99 -puser99 -e "USE comp7780; SELECT * FROM cart;"
  ```
  You should see your order in the results.

---

## Test Accounts

Use any of these in the customer dropdown:

| Username |
|---|
| `cust1` |
| `cust2` |
| `cust3` |
| `cust4` |

---

## Something Went Wrong?

| Problem | Fix |
|---|---|
| `mysql` is not recognized | Add MySQL to PATH, or use full path: `"C:\Program Files\MySQL\MySQL Server 8.0\bin\mysql.exe"` |
| `npm install` gives error | Make sure Node.js is installed. Download from nodejs.org |
| `node index.js` gives error | Run `npm install` first, then try again |
| Page won't open | Make sure CMD is still open and showing "running on port 3000" |
| Database error on SQL files | Run the 3 SQL files again in the correct order |
