# COMP7780 Assignment 2 – Cycle 3
**Group 3 · Vitality**

---

## Submitted Files

| File / Folder | Description |
|---|---|
| `comp7780_home.html` | Company information page |
| `comp7780_product.html` | Product listing and online order page |
| `public/` | Images and video assets |

> `index.js`, `connect.js`, `package.json`, and SQL files are provided by the instructor.

---

## How to Run

### 1. Set up the database

Run the following SQL files **in order** as `user99`:

```
create_user.sql
create_db.sql
create_tables.sql
```

### 2. Place submitted files

Copy `comp7780_home.html`, `comp7780_product.html`, and `public/` into the `cycle3` project folder (alongside `index.js` and `connect.js`).

### 3. Install dependencies

```bash
npm install
```

### 4. Start the server

```bash
node index.js
```

### 5. Open in browser

```
http://localhost:3000
```

---

## Test the Application

1. Visit `http://localhost:3000` — home page loads
2. Click **Order Now** — redirects to product page
3. Select a customer and add items to cart
4. Click **Checkout** — PayPal payment page appears
