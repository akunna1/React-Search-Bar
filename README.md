# 🔍 React-Search-Bar

A simple React.js project focused on **making a search bar** for a webpage.

---

## Purpose

Build an interactive search bar in React that fetches and filters data as a user types—great for dynamic web pages or apps with lots of content.

---

## 🌐 Data Source

Uses [JSONPlaceholder](https://jsonplaceholder.typicode.com/) to simulate API calls and return example data like users or posts.

---

## 🛠 Optional Backend Setup with Node.js

If you'd rather use your own API:

### Backend (Node.js + Express)

* Create an Express server with a `/search` route
* Filter data based on user input
* Return the filtered results

```js
app.get('/search', (req, res) => {
  const query = req.query.q.toLowerCase();
  const results = data.filter(item =>
    item.name.toLowerCase().includes(query)
  );
  res.json(results);
});
```

### Frontend (React)

Update your `fetchData()` function to call your backend:

```js
fetch(`http://localhost:5000/search?q=${searchTerm}`)
```

### Enable CORS

In your server file:

```js
const cors = require('cors');
app.use(cors());
```
