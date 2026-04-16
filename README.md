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

## Paths to Replace

Before running the commands below, replace these two paths with your own:

| Placeholder | Replace with |
|---|---|
| `C:\Program Files\MySQL\MySQL Server 8.0\bin\mysql.exe` | Your MySQL install path |
| `C:\Users\26764\Desktop\7780\Assignments-20260410\Assignment 2\assignment2 project\cycle3\code` | The folder where you saved this project |

---

## Step 1 — Open CMD

1. Press **Win + R** on your keyboard
2. Type `cmd` and press **Enter**
3. A black window (Command Prompt) will open

---

## Step 2 — Set Up the Database

Run these 3 commands **one by one** in CMD:

```
"C:\Program Files\MySQL\MySQL Server 8.0\bin\mysql.exe" -u user99 -puser99 < "C:\Users\26764\Desktop\7780\Assignments-20260410\Assignment 2\assignment2 project\cycle3\code\SQL\create_user.sql"
```
```
"C:\Program Files\MySQL\MySQL Server 8.0\bin\mysql.exe" -u user99 -puser99 < "C:\Users\26764\Desktop\7780\Assignments-20260410\Assignment 2\assignment2 project\cycle3\code\SQL\create_db.sql"
```
```
"C:\Program Files\MySQL\MySQL Server 8.0\bin\mysql.exe" -u user99 -puser99 < "C:\Users\26764\Desktop\7780\Assignments-20260410\Assignment 2\assignment2 project\cycle3\code\SQL\create_tables.sql"
```

No error message = success.

---

## Step 3 — Go to the Project Folder

```
cd "C:\Users\26764\Desktop\7780\Assignments-20260410\Assignment 2\assignment2 project\cycle3\code"
```

---

## Step 4 — Install Dependencies

```
npm install
```

Wait until it finishes.

---

## Step 5 — Start the Website

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

Open Chrome or Edge and go to:
```
http://localhost:3000
```

---

## Testing Checklist

- [ ] Home page loads at `http://localhost:3000`
- [ ] Clicking **Order Now** goes to the product page
- [ ] Product page shows 3 dishes with prices
- [ ] Select a customer from the dropdown (e.g. `cust1`)
- [ ] Click **Add to Cart** on any dish — a popup says "Added to cart"
- [ ] Click **Checkout** — PayPal payment page appears
- [ ] Open a new CMD window and run to verify order was saved in DB:
  ```
  "C:\Program Files\MySQL\MySQL Server 8.0\bin\mysql.exe" -u user99 -puser99 -e "USE comp7780; SELECT * FROM cart;"
  ```

---

## Test Accounts

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
| MySQL command not recognized | Check that the mysql.exe path is correct on your machine |
| `npm install` gives error | Make sure Node.js installed successfully, then reopen CMD |
| `node index.js` gives error | Run `npm install` first, then try again |
| Page won't open | Make sure CMD is still open and showing "running on port 3000" |
| Database error | Run the 3 SQL files again in the correct order |
